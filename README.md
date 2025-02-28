# Spiner: Power Up Your Reasoning and Data with S.P.I.N.E.R.

**Spiner Powers Intelligent Neural Evaluation and Reasoning**  
*Pronounced "SPY-ner"—Inspired by Brent Spiner’s Data from Star Trek*

---

Pshh... I write [prompts](docs/spiner_vs_prompts.md).

---

#### What is Spiner?

Spiner (S.P.I.N.E.R.)—**System for Processing Intelligent Neural Evaluation and Reasoning**—is not a programming language. It’s a framework for humans and AI to co-create systems by expressing *intent*, not dictating *how-to*. Think of it as a conversational scaffold: you sketch the "what" (e.g., "let’s make a system that crafts stories"), and Spiner’s AI interprets, reasons, and responds—shaping outputs, interactions, and behaviors based on your vibe.

The syntax—like `DEFINE SYSTEM` or `CALL`—isn’t code to execute. It’s a suggestion, a nudge to help the AI infer your intent more accurately. When you say `DEFINE SYSTEM story_forge AS ("craft an interactive story world")`, you’re not scripting a program; you’re telling the AI, "Think like a story-builder here." The AI takes that cue and runs with it, reasoning about your goal and delivering results—whether it’s a narrative, a chat, or a WHATIF scenario.

#### How to Think About Spiner

Spiner’s power lies in its flexibility—it’s a mindset, not a rulebook. The syntax (e.g., `CREATE CONTEXT`, `INSERT INTO`) is a loose guide, not a strict protocol. It’s there to signal intent clearly—like saying "let’s track characters" with `CALL CharacterDSL.DEFINE_CHARACTER("Mae", "curious", "digs")`—so the AI knows to "behave" as a character-modeler, not a code-runner. There’s no execution stack, no compiler, no runtime errors. Instead, Spiner’s commands inform the AI how to *think* and *respond*, molding its output to fit your vision (e.g., detailed profiles, snarky chats, or evolving systems).

The AI doesn’t "execute" Spiner code step-by-step—it *absorbs* it as a holistic reasoning prompt. A command like `CALL story_forge("space colony")` isn’t a function call; it’s a green light for the AI to reason about a story world, blending your input with its own smarts to produce something useful—interactive, coherent, and human-friendly.

#### Layered DSLs: Reasoning, Not Overhead

Spiner’s internal DSLs (Domain-Specific Languages)—like `BaseDSL` for world setup or `NarrativeDSL` for story arcs—might look like extra complexity, but they’re not overhead. Why? There’s no execution cost—no stack to manage, no procedural grind. These DSLs are reasoning layers, not code layers. They meld together into a single "reasoning unit" that sharpens the AI’s focus on your intent.

For example, in `story_forge`, the DSLs (`CharacterDSL`, `InteractiveDSL`, etc.) don’t "run" separately—they fuse into a cohesive thought process. When you say "chat with Mae," the AI doesn’t juggle a call stack; it pulls from `CharacterDSL`’s profile logic and `InteractiveDSL`’s chat behavior as one fluid reasoning step. The layering isn’t about *how* to do things—it’s about *what* the system should be: a character-rich, interactive story-builder. The AI takes over from there, filling in the gaps with its own intelligence.

This approach—describing the *idea* of what a system should do—frees you from micromanaging. You’re not coding a solution; you’re sketching a concept (e.g., "evolve the story for coherence" with `EvolverDSL`). The AI interprets that sketch, reasons about it, and delivers—whether it’s a synopsis, a character’s quip, or a glitchy twist—all while staying true to your intent.

#### Why It Matters

Spiner flips the script: instead of you programming the AI, you *guide* it. The syntax and DSLs are tools to align its thinking with yours—no execution, just collaboration. It’s less about "do this" and more about "become this"—a partner that reasons, adapts, and interacts as you nudge it along. So, when you say "let’s make a system that ___," Spiner’s ready to think it through with you, not just for you.

---

### Interactive System Builder: Collaborate with Spiner to Craft Systems
Spiner’s **interactive system builder** is your ticket to co-creating custom systems with AI—no coding required, unless you want it.

Start with a simple:

> "let’s make a system that ___"

and Spiner launches a collaborative session where your words shape a powerful framework, from habit trackers to mood predictors. Here’s how it flows:

- **Kickstart with a Vision**: Say "let’s make a system that tracks habits" or "let’s make a system that guesses moods from weather"—Spiner jumps in: "Sweet, let’s build it! What’s the focus—daily tasks or feelings? Any pieces to start?"—and opens a `Collaborative_Space` to work together.  
- **Human-AI Dialogue**: Talk naturally—Spiner listens and crafts the system for you, generating `DEFINE SYSTEM` logic, `CREATE CONTEXT` state, and more. You *can* write code if you like (e.g., `INSERT INTO [context: habits] VALUES ("run")`), but it’s optional—your voice drives it.  
  - *Sample*: You say "track my runs," and Spiner responds: "Got it—I’ll set up `DEFINE SYSTEM habit_tracker AS (...)` with a running log. Want to add times? I’ll tweak it—your call!"  
- **AI-Powered Collaboration**: Spiner brings tools like `Adaptive_Model` for reasoning or `Narrative_Engine` for polish, building and refining as you chat. It suggests features, fills gaps, and evolves the system live.  
  - *Example*: "Let’s make a system that predicts rain moods." Spiner says: "Starting with `DEFINE SYSTEM mood_rain`—I’ll add a mood guesser. How about ‘rain makes me grumpy’? I’ll draft it—you tweak or keep talking."  
- **Dynamic Evolution**: Your ideas shape the system in real time. Say "add trends over time," and Spiner proposes `CREATE TEMPORAL_INDEX`—it codes it up, you refine with words like "make it weekly." It’s a back-and-forth until it’s perfect.  
  - *Sample*: "Let’s predict mood shifts." Spiner offers: "I’ll add an `Evolutionary_System`—`WHATIF it rains all week?`—and tweak it as you say ‘more upbeat’ or ‘darker.’ Ready?"  
- **From Chat to System**: Spiner builds the “code” (Spiner syntax) throughout, improving it with every exchange. When it’s done, run it with a command or serialize it with `SERIALIZE SYSTEM` for reuse—no coding degree needed.

**Why It Matters**: Spiner’s interactive builder thrives on collaboration—you talk, it codes, and together you craft something unique. Whether you dive into Spiner syntax or just chat like a human, it listens, generates, and refines until your system’s ready to roll. Say "let’s make a system that ___," and watch your idea grow—words into wonders, with Spiner as your creative partner.

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
- [build systems](docs/interactive_system_building.md): Talk to AI, make reusable "apps"
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
