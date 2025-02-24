# LexiQL (LQL) Examples

LexiQL (LQL) bends chaos into brilliance—here’s a mix of useful, intriguing, and silly examples to prove it. From practical wins to weird flexes, these show how LQL blends explicit data, pre-trained smarts, and live web juice—say it, query it, laugh or profit.

## Useful: Tech Trend Tracker
### Intent
Snag the latest tech breakthroughs—structured, fresh, and ready for your next pitch deck.

### Example
`CREATE CONTEXT [context: tech] FROM "latest tech breakthroughs"`  
`INSERT INTO [context: tech] (title, focus) VALUES ("Neural Net X", "speed")`  
`SELECT title, focus FROM [context: tech] WHERE focus ~ "speed" AS table`  
- **Result**:
```
  +---------------+-------+
  | title         | focus |
  +---------------+-------+
  | Neural Net X  | speed |
  | Quantum Boost | speed |
  +---------------+-------+
```

- **Why It’s Cool**: Blends your "Neural Net X" with live web finds—e.g., "Quantum Boost" from 2025—speedy tech, no stale data.

## Intriguing: Mythic Song Mashup
### Intent
Pair myths with songs for a haiku showdown—history meets modern tunes, poetically.

### Example
`CREATE CONTEXT [context: myths] FROM "world mythologies"`  
`INSERT INTO [context: myths] (name, role) VALUES ("Loki", "trickster")`  
`CREATE CONTEXT [context: tunes] FROM "songs referencing mythical characters"`  
`SELECT name, title, year, haiku_for_song('[context: myths]', title, lyric, year) AS haiku FROM [context: myths], [context: tunes] WITH haiku_gen AS (DEFINE FUNCTION haiku_for_song(chars, t, l, y) AS "haiku blending chars with t, l, and y") WHERE name IN ("Thor", "Loki") LIMIT 2 AS table`  
- **Result**:  
```
  +------+---------------+------+--------------------------------+
  | name | title         | year | haiku                          |
  +------+---------------+------+--------------------------------+
  | Thor | Thunder Road  | 1975 | Thor’s hammer cracks the sky,   |
  |      |               |      | Seventy-five storms roll free, |
  |      |               |      | Loki laughs at thunder’s spree.|
  +------+---------------+------+--------------------------------+
  | Loki | Immigrant Song| 1970 | Loki twists Thor’s battle cry, |
  |      |               |      | Seventy hums with tricks so sly,|
  |      |               |      | Gods dance wild beneath the sky.|
  +------+---------------+------+--------------------------------+
```

- **Why It’s Cool**: Explicit "Loki" meets pre-trained "Thor" and web-sourced songs—CTEs craft haikus, operators (`IN`) filter—history sings!

## Silly: Alien Pet Fashion Show
### Intent
Dress hypothetical alien pets in absurd outfits from web trends—because why not?

### Example
`CREATE CONTEXT [context: aliens] FROM "fictional alien species"`  
`INSERT INTO [context: aliens] (name, trait) VALUES ("Zorgon", "slimy")`  
`CREATE CONTEXT [context: fashion] FROM "latest pet fashion trends on the web"`  
`SELECT name, trend, glam(name, trend) AS runway FROM [context: aliens], [context: fashion] WITH glam_gen AS (DEFINE FUNCTION glam(n, t) AS "pair n with t in a flashy outfit") WHERE trait ~ "slimy" OR trend ~ "sparkle" LIMIT 3 AS table`  
- **Result**:  
```
  +--------+----------------+--------------------------------+
  | name   | trend          | runway                         |
  +--------+----------------+--------------------------------+
  | Zorgon | Glitter Bowtie | Zorgon slimes in a glitter bowtie |
  |        |                | —sparkles drip off every ooze!  |
  +--------+----------------+--------------------------------+
  | Klybor | Sparkle Vest   | Klybor struts a sparkle vest—   |
  |        |                | shiny scales catch every eye!   |
  +--------+----------------+--------------------------------+
  | Zorgon | Neon Tutu      | Zorgon rocks a neon tutu—     |
  |        |                | slimy flair meets cosmic chic!  |
  +--------+----------------+--------------------------------+
```

- **Why It’s Cool**: Pre-trained "Klybor" joins explicit "Zorgon" with web trends—`~` infers slimy/sparkly matches, CTEs go wild. Silly? Yes. Flexible? Oh yeah.

---
Back to [README](../README.md)
