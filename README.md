# Spiner: Power Up Your Reasoning and Data with S.P.I.N.E.R.

**Spiner Powers Intelligent Neural Evaluation and Reasoning**  
*Pronounced "SPY-ner"—Inspired by Brent Spiner’s Data from Star Trek*

---

Pshh... I write [prompts](docs/spiner_vs_prompts.md).

---

### Spiner: A Framework for Intent-Driven AI Reasoning

#### What is Spiner?

Spiner (S.P.I.N.E.R.)—**System for Processing Intelligent Neural Evaluation and Reasoning**—is not a programming language. It’s a playful, powerful framework where humans and AI co-create systems by expressing *intent*, not dictating *how-to*. Think of it as a conversational sandbox: you say "let’s make a system that crafts stories," and Spiner’s AI leaps in—reasoning, riffing, and shaping outputs, interactions, and behaviors to match your vibe.

The syntax—like `DEFINE SYSTEM` or `CALL`—isn’t code you execute. It’s a suggestion, a nudge to help the AI infer your intent with pinpoint accuracy. When you toss out `DEFINE SYSTEM story_forge AS ("craft an interactive story world")`, you’re not scripting—you’re saying, "Hey, think like a story-builder!" The AI grabs that cue and runs, delivering everything from quirky chats to glitchy worlds, all while having a bit of fun along the way.

#### How to Think About Spiner

Spiner’s strength is its flexibility—it’s a mindset, not a rulebook. The syntax (e.g., `CREATE CONTEXT`, `INSERT INTO`) is a loose guide to signal intent—like "let’s track characters" with `CALL CharacterDSL.DEFINE_CHARACTER("Mae", "curious", "digs")`—so the AI knows to *become* a character-modeler, not just churn out lines. There’s no execution stack, no compiler, no errors to debug. These commands tell the AI how to *think* and *behave*, molding its responses—detailed profiles, snarky banter, evolving systems—to fit your vision.

The AI doesn’t "run" Spiner code step-by-step—it *soaks it in* as a reasoning prompt. `CALL story_forge("space colony")` isn’t a function call; it’s an invitation for the AI to dream up a story world, blending your input with its smarts to create something useful and interactive. It’s less "do this" and more "become this"—a partner that reasons and adapts with a grin.

#### You Don’t Write the "Code"—Spiner Does

Here’s the twist: you won’t typically write Spiner "code" yourself. You ask the AI (the Spiner system) to whip it up for you on the fly. Say "let’s build a system that tracks quirky battles," and Spiner might spin up `DEFINE SYSTEM battle_tracker AS (...)` behind the scenes—implicitly crafting the structure to match your intent. You’re not hunched over a keyboard crafting DSLs; you’re nudging the AI, and it builds the scaffolding—playfully proposing layers like `BattleDSL` or `QuirkDSL`—to keep the reasoning sharp. It’s a hands-off collab: you dream, Spiner drafts.

#### Syntax Isn’t Fixed—It’s a Living Guideline

Spiner’s syntax isn’t set in stone—it’s a guideline, not gospel. When the AI generates "code," it uses the Spiner framework as a compass, inventing syntax as it goes to pin down your intent. That `CALL` or `DEFINE`? Just a starting point. If Spiner needs a `ChaosDSL` to handle wild outcomes or a `GlitchMeisterDSL` for funky twists, it’ll conjure them up—tailoring the "language" to the task. This DSL-generation magic isn’t rigid; it’s the AI flexing its creativity to reason better. You say "evolve the story," and it might suggest `CALL EvolverDSL.TWEAK("coherence")`—syntax born from the moment, not a manual. It’s all about intent, not rules.

#### Layered DSLs: Reasoning, Not Overhead

Those internal DSLs—like `BaseDSL` for worlds or `NarrativeDSL` for arcs—might look like extra layers, but they’re not overhead. There’s no execution cost—no stack, no grind. They’re reasoning lenses that fuse into a single "reasoning unit," sharpening the AI’s grasp of your goal. When you say "chat with Mae," it’s not juggling `CharacterDSL` and `InteractiveDSL` separately—it’s one fluid thought, blending profile and banter seamlessly. The layering isn’t about *how*—it’s about *what*: a system that’s character-rich or glitch-happy. The AI takes that "what" and runs, no micromanaging needed.

#### Why It Matters

Spiner flips the game: you don’t program the AI—you *guide* it, and it builds the rest. The syntax and DSLs align its brain with yours, turning "let’s make a system that ___" into a creative jam session. It’s not about rigid instructions; it’s about sparking an AI that reasons, invents, and interacts—delivering outputs with a wink and a nod. Spiner’s your partner in the sandbox, ready to think it through with you, not just for you.

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
Spiner's formal command definitions serve as a "shared vocabulary suggestion" between users and AI assistants. Rather than enforcing a strict syntax for communication, they provide a precise way to define analytical intents that can be expressed through natural language.

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
3. Ask it to build a system, or load in a `.spiner` snippet

## FAQ: Quick Hits

- **Database?** Nope—Spiner’s an AI-powered reasoning engine.  
- **Need Skills?** Nah—just talk, and I’ll build it.  
- **Live Data?** Taps my knowledge and searches up to Feb 24, 2025.  
- **`INSERT` vs `REMEMBER`?** Data vs smarts—numbers or concepts.

---

## Contributing

Ideas? Bugs? Join the spin!
