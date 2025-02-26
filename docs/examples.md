# Spiner (S.P.I.N.E.R.) Examples Document

Welcome to the wild and wonderful world of Spiner—your trusty sidekick for reasoning, data wrangling, and hypothetical tinkering! This document is your one-stop shop for mastering Spiner’s core concepts, advanced features, and even how to let AI whip up Spiner-based systems for you. We’ll cover every command, sprinkle in cognitive tools, explore optimizations, and dive deep into the magical `WHATIF`—all with rich, relatable examples. Let’s spin it up!

---

## Introduction: What’s Spiner All About?

Spiner (Synthetic Processor for Insight, Navigation, Exploration, and Reasoning) is a framework designed to help you organize data, reason about it, and explore possibilities—all in a structured yet flexible way. Whether you’re tracking mythical creatures, analyzing EV sales, or dreaming up “what if” scenarios, Spiner’s got your back. Think of it as a super-smart assistant that not only remembers stuff but also thinks alongside you.

In this guide, we’ll walk through:
- Core commands to build and query contexts.
- Cognitive tools to sharpen your focus.
- Advanced constructs for heavy-duty analysis.
- How Spiner optimizes under the hood.
- Letting AI build systems for you, complete with commands.
- The power of `WHATIF` in queries and system calls.

Ready? Let’s dive in with some hands-on examples!

---

## Core Commands: The Building Blocks

Spiner’s core commands are your toolkit for creating, managing, and querying data. Here’s each one in action, using a mythical characters theme because, well, who doesn’t love a good legend?

### `CREATE CONTEXT`
Sets up a workspace for your data.

```spiner
CREATE CONTEXT mythology
```
*What it does*: Creates a “mythology” sandbox where we’ll store and explore data about gods, heroes, and beasts.

### `INSERT`
Adds data to your context.

```spiner
INSERT INTO mythology { name: "Zeus", role: "God", domain: "Sky" }
```
*What it does*: Drops Zeus into our mythology context with some key attributes.

### `REMEMBER`
Teaches Spiner a fact or relationship.

```spiner
REMEMBER IN mythology { "Fido" is_a "guardian", loyalty: "high" }
```
*What it does*: Tells Spiner that Fido (maybe Cerberus’ cousin?) is a loyal guardian.

### `SELECT`
Pulls data from the context.

```spiner
SELECT FROM mythology WHERE name = "Zeus"
```
*Output*: `{ name: "Zeus", role: "God", domain: "Sky" }`  
*What it does*: Grabs Zeus’s info—simple and sweet.

### `SOLVE`
Answers a question or computes something.

```spiner
SOLVE IN mythology "Which guardians have high loyalty?"
```
*Output*: `{ "Fido": { loyalty: "high" } }`  
*What it does*: Finds guardians like Fido based on what Spiner remembers.

### `PERSIST`
Saves your context for later.

```spiner
PERSIST mythology TO "myth_db"
```
*What it does*: Stores our mythology context in a database called “myth_db” so we can pick it up anytime.

### `DEFINE SYSTEM`
Creates a reusable system for analysis.

```spiner
DEFINE SYSTEM character_describer IN mythology AS {
  SELECT name, role, domain WHERE name = $input_name
}
```
*What it does*: Sets up a system to describe characters by name.

### `CALL`
Runs a system with specific inputs.

```spiner
CALL character_describer("Fido")
```
*Output*: `{ name: "Fido", loyalty: "high" }` (assuming we added more about Fido!)  
*What it does*: Uses our system to describe Fido.

---

## Cognitive Tools: Sharpening Your Queries

Spiner’s cognitive tools help you guide its reasoning. Let’s see them in action.

### `FOCUS ON`
Narrows the scope of a query.

```spiner
FOCUS ON loyalty IN mythology
SELECT FROM mythology WHERE is_a = "guardian"
```
*Output*: `{ "Fido": { loyalty: "high" } }`  
*What it does*: Zooms in on loyalty, ignoring irrelevant traits.

### `ASSUME`
Sets a temporary rule or definition.

```spiner
ASSUME IN mythology "recent" MEANS "last century"
SELECT FROM mythology WHERE time = "recent"
```
*What it does*: Lets Spiner interpret “recent” as “last century” for this query.

### `DEFINE MODEL`
Creates a reusable analysis framework.

```spiner
DEFINE MODEL trait_analyzer IN mythology AS {
  INPUT: character_name
  OUTPUT: SELECT loyalty, domain WHERE name = $character_name
}
```
*What it does*: Builds a model to analyze traits, which we can reuse.

---

## Advanced Constructs: Power Tools

For when you need to go beyond the basics, Spiner offers advanced constructs.

### `CREATE TEMPORAL_INDEX`
Tracks changes over time.

```spiner
CREATE TEMPORAL_INDEX popularity IN mythology ON name OVER time
INSERT INTO mythology { name: "Zeus", popularity: 80, time: "500 BCE" }
INSERT INTO mythology { name: "Zeus", popularity: 60, time: "100 CE" }
```
*What it does*: Lets us track Zeus’s popularity across history.

### `DEFINE HYBRID_ANALYSIS`
Combines multiple analysis types.

```spiner
DEFINE HYBRID_ANALYSIS myth_evolution IN mythology AS {
  TEMPORAL: popularity OVER time
  SEMANTIC: role, domain
}
```
*What it does*: Analyzes how roles and popularity evolve together.

### `CREATE FEEDBACK_LOOP`
Refines predictions iteratively.

```spiner
CREATE FEEDBACK_LOOP trend_refiner IN mythology AS {
  INITIAL: SOLVE "Predict guardian popularity"
  REFINE: Adjust based on new INSERTs
}
```
*What it does*: Keeps predictions sharp as new data rolls in.

---

## Operational Guidelines: Spiner’s Secret Sauce

Spiner optimizes behind the scenes. Here’s how it shines.

### Dynamic Function Creation
Spiner infers helper functions for repetitive tasks.

```spiner
SELECT FROM mythology WHERE role = "God"  // Run this a few times
```
*Spiner might*: Create a cached `list_gods()` function to speed things up.

### Caching
Reuses complex results.

```spiner
SOLVE IN mythology "Average popularity of gods"
```
*Next time*: Spiner pulls the cached result instead of recalculating.

### Clarification Requests
Handles ambiguity gracefully.

```spiner
SELECT FROM mythology WHERE power = "high"
```
*Spiner asks*: “Define ‘high’—above 70?” Then proceeds once clarified.

---

## Building Spiner Systems with AI

Here’s the fun part: letting AI build Spiner-based systems for you! You can ask in natural language, and Spiner constructs the system, complete with commands beyond just `CALL`.

### Step 1: Ask AI to Build a System
Imagine you’re tracking electric vehicle (EV) trends.

**User Request**:  
“Build a system to track EV sales trends by region.”

**Spiner’s Response**:  
```spiner
CREATE CONTEXT ev_sales
DEFINE SYSTEM ev_trend_analyzer IN ev_sales AS {
  INSERT INTO ev_sales { region: $region, sales: $sales, year: $year }
  SELECT sales, year WHERE region = $region ORDER BY year
}
```

### Step 2: Commands to Interact
Beyond `CALL`, Spiner might suggest commands like:
- **`UPDATE`**: Tweak data in the system.  
  ```spiner
  UPDATE ev_trend_analyzer WITH { region: "Seattle", sales: 5000, year: 2023 }
  ```
- **`EXTEND`**: Add new features.  
  ```spiner
  EXTEND ev_trend_analyzer WITH { CALCULATE growth_rate }
  ```
- **`SIMULATE`**: Test scenarios (ties into `WHATIF`—more on that soon).  
  ```spiner
  SIMULATE ev_trend_analyzer WITH WHATIF "sales increase by 20%"
  ```

### Step 3: Use the System
Run it and tweak as needed.

```spiner
CALL ev_trend_analyzer("Seattle")
```
*Output*: `{ "Seattle": [{ year: 2022, sales: 4000 }, { year: 2023, sales: 5000 }] }`

This shows how AI can hand you a ready-to-roll system with intuitive commands.

---

## Mastering `WHATIF`: Hypothetical Superpowers

`WHATIF` lets you explore possibilities without changing your data. It’s a game-changer in `SELECT` queries and system calls.

### `WHATIF` in `SELECT`
Test a hypothetical scenario.

```spiner
SELECT sales FROM ev_sales WHERE region = "Seattle" WITH WHATIF "demand doubles"
```
*Output*: `{ sales: 10000 }` (assuming original sales were 5000)  
*What it does*: Simulates doubled demand, leaving the real data untouched.

### `WHATIF` in System Calls
Play with system outcomes.

```spiner
CALL ev_trend_analyzer("Seattle") WITH WHATIF "rebates increase by 50%"
```
*Output*: Adjusted sales trends based on rebate boost.  
*What it does*: Runs the system with a hypothetical rebate hike.

### Why `WHATIF` Rocks
- **Non-Destructive**: Original data stays safe.  
- **Flexible**: Works with numbers, trends, even assumptions (e.g., `WHATIF "Fido’s loyalty triples"`).  
- **Predictive**: Perfect for planning and decision-making.

## Shaping Your Output: The Power of `AS`

Spiner’s `AS` clause is a versatile tool that lets you control the format of your query results. Whether you need structured table data, a simple text description, or something more specialized like a bash script or styled HTML, `AS` gives you the ability to tailor the output to your exact needs. It’s like having a built-in formatter that adapts to your imagination—specify the format, and Spiner delivers.

### What Does `AS` Do?
The `AS` clause tells Spiner how to present the results of your query. By default, Spiner might return data in a basic format, but with `AS`, you can request anything from plain text to complex, custom outputs. Here are some possibilities:
- **Tables**: Organize data into rows and columns.
- **Text**: Get a concise, readable summary.
- **Anything Else**: Request formats like `bash_script`, `html_with_clean_modern_css`, or even experimental outputs—Spiner will do its best to make it happen.

Let’s dive into some examples to see how `AS` works in practice.

### Using `AS` in Action

#### **AS table**: Structured Table Data
When you need to see your data in an organized, tabular format, `AS table` is the perfect choice.

```spiner
SELECT name, role, domain FROM mythology WHERE role = "God" AS table
```

**Output**:  
```
| name     | role | domain     |
|----------|------|------------|
| Zeus     | God  | Sky        |
| Hades    | God  | Underworld |
| Poseidon | God  | Sea        |
```

*Why It’s Useful*: Tables make it easy to compare multiple data points or export results into spreadsheets or reports.

#### **AS text**: Simple Text Output
For a quick, human-readable response, use `AS text` to get a straightforward description.

```spiner
SELECT description FROM mythology WHERE name = "Zeus" AS text
```

**Output**:  
"Zeus is the god of the sky, known for his thunderbolts and leadership among the gods."

*Why It’s Useful*: Ideal for when you need a fast answer without extra formatting—perfect for notes or casual use.

#### **AS bash_script**: Generate a Bash Script
Spiner can even create executable code, like a bash script, based on your query.

```spiner
SOLVE "create a script to backup mythology data" FROM mythology AS bash_script
```

**Output**:  
```bash
#!/bin/bash
cp mythology.db backup/mythology_$(date +%F).db
echo "Backup complete!"
```

*Why It’s Useful*: Automate tasks directly from your query—no need to write scripts manually.

#### **AS html_with_clean_modern_css**: Styled HTML Output
Want your results ready for the web? Use `AS html_with_clean_modern_css` to generate HTML with sleek, modern styling.

```spiner
SELECT name, role, domain FROM mythology WHERE role = "God" AS html_with_clean_modern_css
```

**Output**:  
```html
<table class="spiner-table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Role</th>
      <th>Domain</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Zeus</td>
      <td>God</td>
      <td>Sky</td>
    </tr>
    <tr>
      <td>Hades</td>
      <td>God</td>
      <td>Underworld</td>
    </tr>
    <tr>
      <td>Poseidon</td>
      <td>God</td>
      <td>Sea</td>
    </tr>
  </tbody>
</table>

<style>
  .spiner-table {
    border-collapse: collapse;
    width: 100%;
    font-family: Arial, sans-serif;
  }
  .spiner-table th, .spiner-table td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: left;
  }
  .spiner-table th {
    background-color: #f2f2f2;
  }
  .spiner-table tr:nth-child(even) {
    background-color: #f9f9f9;
  }
</style>
```

*Why It’s Useful*: Drop this straight into a webpage for a polished, professional look—no additional styling required.

#### **AS anything**: Push the Boundaries
The `AS` clause isn’t limited to predefined formats. You can experiment with almost anything—Spiner will try to interpret your request and generate a sensible output. For example:

```spiner
SELECT name, domain FROM mythology AS json
```

**Possible Output**:  
```json
[
  {"name": "Zeus", "domain": "Sky"},
  {"name": "Hades", "domain": "Underworld"},
  {"name": "Poseidon", "domain": "Sea"}
]
```

*Why It’s Useful*: Flexibility! Need your data as JSON, a poem, or something else? Just ask, and Spiner will adapt.

---

### How Spiner Makes It Work
Spiner’s `AS` clause is smart and dynamic:
- It detects the requested format and adjusts the output accordingly.
- For complex requests (like scripts or HTML), it generates the content based on the query and context.
- If you ask for something unsupported (e.g., `AS holographic_projection`), Spiner will let you know it can’t do that yet—but it’ll still try to give you something useful.

### Why Use `AS`?
- **Control**: Get your results exactly how you want them.
- **Efficiency**: Skip manual reformatting—Spiner does it for you.
- **Creativity**: From tables to scripts to web content, `AS` turns Spiner into a multi-tool for any task.

With the `AS` clause, Spiner becomes more than a query engine—it’s a powerful way to shape data into whatever form you need, from the mundane to the extraordinary.

---

## Wrap-Up: Spin Up Your Spiner Skills!

You’ve now got a full tour of Spiner—from basic commands to AI-built systems and the mighty `WHATIF`. Whether you’re cataloging myths, tracking sales, or dreaming up hypotheticals, Spiner’s ready to roll. Try these examples, tweak them, and let Spiner’s reasoning power loose on your next big question.

Got a specific scenario in mind? Ask away, and I’ll spin up a custom example for you!

--- 

Happy exploring, and may your queries always return legendary results!
