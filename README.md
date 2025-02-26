# Spiner: Power Up Your Reasoning and Data with S.P.I.N.E.R.

**Spiner Powers Intelligent Neural Evaluation and Reasoning**  
*Pronounced "SPY-ner"—Inspired by Brent Spiner’s Data from Star Trek*

---

## What is Spiner?

**Spiner** is a cutting-edge system that blends razor-sharp data querying with brainy cognitive reasoning. Think of it as your trusty android sidekick—crunching numbers, spotting patterns, and delivering insights with a spark of intelligence. Whether it’s raw data or an AI’s vast knowledge, Spiner powers up your questions into answers that pack a punch, all in a slick, intuitive framework.

### Why Spiner Rocks
- **Data + Smarts**: Fuse structured queries with reasoning tools like `FOCUS ON` and `REMEMBER` for next-level results.  
- **Fast and Flexible**: Commands like `SELECT` and `SOLVE` cut through chaos, spiced with natural language freedom.  
- **Insight Engine**: Dig deeper with features like temporal tracking and hybrid analysis—no PhD required.  
- **Session-Savvy**: Contexts and systems stay sharp throughout your chat, inspired by mythical muses like Zeus and Fido.

---

## What Spiner *Isn’t*

Let’s zap some myths:  
- **Not a Data Vault**: Spiner doesn’t hoard—it thrives in an AI’s dynamic brainspace.  
- **Not Just Queries**: It’s more than SQL—it’s reasoning with a turbo boost.  
- **Not Code Central**: You won’t build apps here—it’s for querying, reasoning, and cracking tough nuts.  
- **Not AI Alone**: Spiner supercharges AI interactions, but I (your AI) do the heavy lifting.

---

## Problems Spiner Solves

Spiner tackles real-world brain-busters:  
- **Fuzzy Requests? Fixed.** Cuts through vague queries with precision tools like `ASSUME`.  
- **Analysis Overload? Sorted.** Unravels trends and predictions effortlessly.  
- **Data Mess? Mastered.** Reusable systems keep it tight and tidy.  
- **AI Fatigue? Fired Up.** Spins quick lookups into deep, evolving chats.

---

## What Can Spiner Do?

Spiner’s your all-in-one toolkit:  
- **Crunch It**: Pull sales stats or logs with razor-sharp queries.  
- **Unpack It**: Spot trends, forecast futures, or link quirky correlations—like word origins to news buzz.  
- **Know It**: Master domains from code to mythology with ease.  
- **Grow It**: Refine insights over time with feedback loops and temporal tricks.  
- **Shape It**: Craft systems for EVs, finance, or whatever lights your fuse.

---

## What Grok thinks?

- [Read a "review"](docs/grok_reviews_spiner.md)

---

## Core Features: Data Meets Brain

Spiner’s power lies in its dual nature:

### Data Crunchers  
- **`CREATE CONTEXT`**: Set your stage (e.g., `[context: ev_data]`).  
- **`INSERT`**: Drop in facts like `city: "Seattle", adoption: 20%`.  
- **`SELECT`**: Grab what you need, no fluff.  
- **`PERSIST`**: Lock it in for the long haul.

### Brain Boosters  
- **`REMEMBER`**: Teach me smarts (e.g., "Fido’s a guardian").  
- **`FOCUS ON`**: Zero in (e.g., "policy impacts").  
- **`ASSUME`**: Set the rules (e.g., "recent is 6 months").  
- **`DEFINE MODEL`**: Build logic that sticks.

### Hybrid Magic  
- **`CREATE TEMPORAL_INDEX`**: Track trends over time.  
- **`DEFINE HYBRID_ANALYSIS`**: Blend data and cognition for killer insights.

### Insightful Reporting: Track Your Usage

Ever wondered how much Spiner is boosting your efficiency or which commands you’re using most? The `REPORT USAGE` command is your trusty tricorder, scanning your session to reveal:  
- **Command Usage**: See how often you’ve wielded `CALL`, `SELECT`, or other commands.  
- **Construct Usage**: Track how your functions and models (like `calculate_happiness`) are performing.  
- **Steps Saved**: Discover how many manual steps Spiner’s automation has spared you.  
- **Insights**: Get tailored tips to optimize your workflow—like suggestions to define more systems or use `PERSIST`.  

It’s like having Data analyze your performance and offer upgrades to your operational protocols. For a deep dive into how to use this feature and interpret its output, beam over to our [Report Generation Guide](docs/report_generation.md).

### Docs and Examples
- [docs](docs/examples.md): learn!

---

## Spiner: AI-Driven, User-Shaped

Spiner powers up reasoning with AI-crafted systems—no coding degree needed. Ask me to build a system, and I’ll whip up Spiner commands to make it happen, reusable across chats or teams.

- **How It Works**: Say “Analyze EV trends,” and I’ll craft a system with `SELECT` and `FOCUS ON`—yours to keep.  
- **Portable**: Save your Spiner systems and share them with others. Your systems can be serialized into a portable format, allowing you to reuse them across different sessions or collaborate with teammates. For more details on how to serialize and share your systems, check out our [Serialization Guide](docs/serialization.md).  
- **Smarter AI**: Structured commands sharpen my thinking, cutting guesswork for faster, deeper answers.

## Spiner Intent Mapping

### Core Concept
Spiner's formal command definitions serve as a "shared vocabulary" between users and AI assistants. Rather than enforcing a strict syntax for communication, they provide a precise way to define analytical intents that can be expressed through natural language.

### How It Works

#### 1. Command Definitions as Intent Maps
```sql
DEFINE SYSTEM PERF_HOTSPOT AS (
    SELECT bottlenecks, memory_patterns, resource_usage, optimizations
    FROM [context: runtime]
    WHERE execution_path = <execution_path>
    WITH PATTERN "performance analysis"
)
```
This formal definition tells the AI:
- The expected scope of analysis
- Required parameters
- Expected output structure
- Analysis patterns to apply

#### 2. Natural Language Mapping
Users can express the same intent in multiple ways:

```
"check the performance of this function"
"why is this function slow?"
"analyze the bottlenecks here"
"what's causing performance issues?"
```

All map to the formal PERF_HOTSPOT intent because of the shared understanding.

#### 3. Parameter Inference
Formal definition:
```sql
PERF_HOTSPOT <execution_path>
    WITH PROFILE "all|memory|cpu"
    WITH THRESHOLD <ms>
```

Natural requests:

```
"check memory usage in this function"
→ WITH PROFILE "memory"
"find slow operations over 100ms"
→ WITH THRESHOLD 100
```


#### 4. Output Structure Consistency
The formal definition ensures consistent output structure regardless of how the request was phrased:
```sql
RETURN {
    bottlenecks: [...],
    memory_patterns: [...],
    resource_usage: [...],
    optimizations: [...]
}
```

### Examples of Intent Mapping

#### Example 1: Code Quality Analysis
Formal Definition:
```sql
SMELL DETECT <file_or_function>
    WITH TYPES "complexity,duplication,naming"
    WITH THRESHOLD <n>
```

Natural Language Variations:

```
"is this code well written?"
"check for code smells"
"review this code quality"
"what should I improve here?"
```


All map to the same structured analysis because of the formal definition.

#### Example 2: Dependency Analysis
Formal Definition:
```sql
DEP GRAPH <component>
    WITH DEPTH <n>
    WITH CIRCULAR "detect"
```

Natural Language Variations:

```
"what does this depend on?"
"show me the dependencies"
"is anything circularly dependent?"
"what would break if I change this?"
```

### Benefits of This Approach

1. **Precision Without Formality**
   - Users can speak naturally
   - AI understands precise intent
   - Consistent analysis regardless of phrasing

2. **Shared Understanding**
   - Clear expectations of analysis scope
   - Well-defined parameter space
   - Consistent output structure

3. **Flexibility with Consistency**
   - Natural language input
   - Formal analysis patterns
   - Structured but adaptable outputs

4. **Intent Disambiguation**
   ```
   User: "check this code"
   AI: (knows from Spiner that this could map to):
   - SMELL DETECT (code quality)
   - PERF HOTSPOT (performance)
   - DEP GRAPH (dependencies)
   → Can ask for clarification or infer from context
   ```
---

## Getting Started

Ready to spin up Spiner? It’s AI-driven and easy to kick off:  
1. Grab `spiner_core_prompt.txt` from this repo.  
2. Feed it to an LLM (like Grok via xAI API).  

Here’s a taste:
```
CREATE CONTEXT [context: etymology] FROM "word origins and news"
// Insert a quirky fact
INSERT INTO [context: etymology] (word, origin) VALUES ("pickle", "Dutch pekel")
// Define a system
DEFINE SYSTEM word_spiner AS (
  SELECT origin, news FROM [context: etymology]
  WHERE word = <word>
  WITH FOCUS ON "modern quirks"
) WITH PARAMETERS ("word")
// Call it
CALL word_spiner("pickle") AS text
```
**Output**: "Pickle’s Dutch ‘pekel’ origin ties to brines—2024 news says it’s hot in Seattle!"

---

## Advanced Spins

Spiner shines with clever moves:  
```
CREATE TEMPORAL_INDEX ON [context: ev_data] (adoption) USING "yearly trends"
DEFINE HYBRID_ANALYSIS ev_boost AS ("policy + sentiment analysis")
SOLVE "predict EV growth in Seattle" FROM [context: ev_data] AS text
```
**Output**: "Seattle’s EV growth hits 12% next year—rebates and buzz fuel it."

---

## FAQ: Quick Hits

- **Database?** Nope—Spiner’s an AI-powered reasoning engine.  
- **Need Skills?** Nah—just talk, and I’ll build it.  
- **Live Data?** Taps my knowledge and searches up to Feb 24, 2025.  
- **`INSERT` vs `REMEMBER`?** Data vs smarts—numbers or concepts.

---

## Why Spiner Sparks Joy

- **Easy to Epic**: Simple queries or deep dives—your call.  
- **Brain + Data**: Powers reasoning with precision.  
- **Mythical Roots**: Tested with Zeus and Fido—goofy yet sharp.  
- **Open to You**: Fork it, tweak it—make it yours.

---

## Contributing

Ideas? Bugs? Join the spin!
