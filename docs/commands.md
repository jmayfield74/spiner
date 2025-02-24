# LexiQL (LQL) Commands

LexiQL (LQL) commands let you craft and query dynamic contexts—data buckets blending explicit inputs, pre-trained knowledge, and live web searches. Here’s every command, its intent, docs, and a simple spin to get you rolling.

## General Pattern

LQL’s magic lies in its flow—commands build contexts, queries fetch data seamlessly from three sources:
- **Explicit Data**: You define it—e.g., `INSERT INTO [context: foo] (name) VALUES ('Alice')`—stored in session state, always there.
- **Pre-Trained Data**: Pulled from my baked-in knowledge (up to early 2025)—e.g., "world myths" grabs Thor, Loki—fetched live at query time unless persisted.
- **Web Data**: Live searches (simulated here)—e.g., "songs about myths" pulls "Thunder Road"—grabbed at query time, not pre-stored.

**Inference**: Undefined stuff—like functions (e.g., `reverse(name)` without a CTE)—gets smart guesses from context. Say "recent" in `WHERE date ~ 'recent'`, and I’ll assume "last year or so"—it’s fluid, not fussy.

**Seamless Blend**: Query `[context: myths]`, and explicit "Loki", pre-trained "Thor", and web-sourced "Zeus" mix naturally—relationships (e.g., Thor to thunder songs) pop out without you splitting hairs. No pre-loading—data’s live unless you `PERSIST`.

## Commands

### `CREATE CONTEXT <context_name> FROM <description>`
#### Intent
Kickstarts a context—your data sandbox—ready to hold explicit entries and pull dynamic data when queried. It’s the "here’s what I’m about" step—flexible, no rigid setup.

#### Docs
- `<context_name>`: Tags it (e.g., `[context: foo]`).  
- `<description>`: Backticks (e.g., `"tech news"`)—hints at pre-trained/web data to fetch live at query time.

#### Sample
`CREATE CONTEXT [context: myths] FROM "world mythologies"`  
- **Result**: "Context [context: myths] created." (Empty bucket, ready for explicit data or live queries.)

### `INSERT INTO <context> [(<fields>) VALUES (<values>) | FROM <description>]`
#### Intent
Fills your context—either with hard data you set or cues for more live info. It’s how you seed or expand—explicit for control, dynamic for breadth.

#### Docs
- `<context>`: Must exist—your target bucket.  
- `<fields>`/`<values>`: Explicit entries (e.g., `'name', 'Loki'`).  
- `FROM <description>`: Adds a live data hint (e.g., `"Greek gods"`)—fetched at query time.

#### Sample
`INSERT INTO [context: myths] (name, role) VALUES ('Loki', 'trickster')`  
- **Result**: "Data inserted into [context: myths]." (Loki’s in the bucket.)  
`INSERT INTO [context: myths] FROM "Norse legends"`  
- **Result**: "Data inserted into [context: myths]." (Cue for Norse data later.)

### `SELECT <fields> FROM <context> [WHERE <conditions>] [AS <format>] [WITH <definitions>]`
#### Intent
Grabs data—explicit and live—letting you filter and shape it. It’s your "get me this" command—precise yet open to creative tweaks with CTEs.

#### Docs
- `<fields>`: What to fetch (e.g., `name`)—can infer undefined (e.g., `speed` guesses from context).  
- `<context>`: Source bucket—blends all data live.  
- `<conditions>`: Filters (e.g., `role = 'hero'`, or `"fast"` infers speed).  
- `<format>`: Output—`AS table`, `AS text` (default: table if multi-field, text if single).  
- `<definitions>`: CTEs for custom rules.

#### Sample
`SELECT name FROM [context: myths] WHERE role = 'trickster' AS table`  
- **Result**:  
```
  +------+
  | name |
  +------+
  | Loki |
  +------+
```

#### Complex Sample (CTEs)
`SELECT name, loud(name) FROM [context: myths] WITH funcs AS (DEFINE FUNCTION loud(x) AS "uppercase x with bang") AS table`  
- **Result**:
```
  +------+-----------+
  | name | loud(name)|
  +------+-----------+
  | Loki | LOKI!     |
  | Thor | THOR!     |
  +------+-----------+
```

### `SOLVE <task_description> FROM <context> [WITH <parameters>] [AS <format>]`
#### Intent
Tackles bigger asks—creative or practical—using context data. It’s your "do something cool" command—less about raw data, more about results.

#### Docs
- `<task_description>`: Goal in backticks (e.g., `"write a haiku"`).  
- `<context>`: Source—blends all data live.  
- `<parameters>`: Refines (e.g., `"use Thor"`).  
- `<format>`: Output—`AS text` (default), `AS table`.

#### Sample
`SOLVE "List heroes" FROM [context: myths] AS text`  
- **Result**: "Hercules stands tall among mythic heroes."  
#### Complex Sample
`SOLVE "Write a haiku" FROM [context: myths], [context: tunes] WITH "use Loki" AS text`  
- **Result**: "Loki twists fate’s thread, songs hum soft through trickster’s web, chaos reigns supreme."

### `PERSIST INTO <context> [WITH <options>]`
#### Intent
Locks dynamic data (pre-trained/web) into session state—makes it static for speed or stability. It’s your "keep this handy" move—optional, with TTLs for temp caching or permanent for keeps.

#### Docs
- `<context>`: Target bucket—must exist.  
- `<options>`: `"TTL 10 minutes"` caches for 10 minutes—expires, re-fetches live; no options = permanent.  
- **Behavior**: Without `PERSIST`, data’s live every query—web’s fresh, pre-trained’s consistent. With TTL, it’s cached ‘til expiry—fast but updates. Permanent? It’s yours forever, no re-fetch.

#### Sample
`PERSIST INTO [context: tunes] WITH "TTL 5 minutes"`  
- **Result**: "Context [context: tunes] persisted with TTL 5 minutes." (Caches songs for 5 min.)  
`PERSIST INTO [context: myths]`  
- **Result**: "Context [context: myths] persisted." (Myths stay put, no live pulls.)

## Operators

### `=` (Exact Match)
#### Intent
Pinpoints an exact value—your "this, not that" filter for precision.

#### Usage
Matches `<field>` to a literal—e.g., `role = "trickster"`. No wiggle room.

### `~` (Similarity/Inference Match)
#### Intent
Casts a wider net—finds "close enough" matches when exact won’t cut it, leaning on inference.

#### Usage
`<field> ~ <value>`—e.g., `title ~ "thunder"` grabs thunder-ish stuff. Infers from context if vague—e.g., "fast" might mean speed.

---
Back to [README](../README.md)
