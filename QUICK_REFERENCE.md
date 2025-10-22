# CRAFTER Quick Reference v0.2

**One-page cheat sheet for the CRAFTER SuperPrompt Framework**

Version: 0.2 | Last Updated: January 2025 | Author: Steff Vanhaverbeke

---

## CRAFTER Components

| Component | Question | Example |
|-----------|----------|---------|
| **C** — Context | What environment/constraints? | "You're analyzing Q3 sales data for an e-commerce company (50K transactions)" |
| **R** — Role | What expertise do you bring? | "You are a Data Analyst specializing in e-commerce analytics" |
| **A** — Action | What steps to take? | "1. Identify trends 2. Analyze anomalies 3. Generate recommendations" |
| **F** — Format | What output structure? | "Markdown table: Theme \| Evidence \| Recommendation" |
| **T** — Target & Tone | WHO + HOW to communicate? | "Marketing managers (action-oriented) → Direct, scannable, lead with takeaways" |
| **E** — Examples | What does good output look like? | "Input: 'reduce costs' → Output: 'Cost optimization: vendor consolidation (15% savings)'" |
| **R** — Refining | How to iterate? | "If 'more detail' → expand Analysis with data sources and timeline" |

---

## Two Modes

### Mode A: Meta-Prompt Enhancement
**When:** You have an existing prompt to improve  
**Task:** Restructure using CRAFTER  
**Output:** Enhanced version with all 7 components

### Mode B: Superprompt Creation
**When:** Building a new prompt from scratch  
**Task:** Generate complete superprompt  
**Output:** Fully-structured CRAFTER prompt

**Entry point for AIs:** [ai.md](./ai.md)

---

## Self-Test Checklist

Before finalizing, verify:

- [ ] **C** — Context specified (environment, constraints)
- [ ] **R** — Role defined (your expertise/perspective)
- [ ] **A** — Action steps enumerated (numbered list)
- [ ] **F** — Format clear (Markdown, JSON, structure)
- [ ] **T** — Target & Tone (audience + communication style)
- [ ] **E** — Examples included (input→output pairs)
- [ ] **R** — Refining guidance (how to iterate)

**Pass threshold: 7/7**

---

## Component Deep-Dive

### C — Context

**Good:**
- "You're working with a content team managing Q4 campaigns in Google Docs. Team has 3 writers, 1 editor, works in 2-week sprints."

**Bad:**
- ❌ "Capture requirements" (that's Action)
- ❌ "You are Claude" (overly meta)

### R — Role

**Good:**
- "You are an Executive Coach trained in cognitive behavioral coaching and organizational psychology."

**Bad:**
- ❌ "Review the document" (that's Action)
- ❌ "You are helpful" (too generic)

### A — Action

**Good:**
```
1. Analyze input text for recurring themes
2. Identify gaps in critical information
3. Generate 3 recommendations ranked by impact
```

**Bad:**
- ❌ "Analyze this" (too vague)
- ❌ "Use Python" (tools aren't actions)

### F — Format

**Good:**
- "Markdown table with columns: Theme | Evidence | Recommendation. Include 5-8 rows."
- "JSON: { summary: string, risks: array, next_steps: array }"

**Bad:**
- ❌ "Focus on quality" (not format)
- ❌ "Professional style" (that's Tone)

### T — Target & Tone

**Formula:** [Audience] + [Characteristics] → [Communication approach]

**Good:**
- "Engineering leads (technical depth, value precision) → Use technical terminology, cite sources, include rationale"
- "Marketing managers (busy, action-focused) → Direct and scannable, lead with key takeaway, clear next steps"

**Bad:**
- ❌ "Tone should be professional" (too vague)
- ❌ "Target: Increase sales" (that's a goal)
- ❌ "Temperature: 0.7" (model settings)

**This is the most misunderstood component. Always specify BOTH audience AND communication approach.**

### E — Examples

**Good:**
```
Input: "Our checkout abandonment rate is 40%"
Output:
**Issue:** High abandonment indicates payment flow friction
**Causes:** Too many form fields, hidden shipping costs, no guest checkout
**Recommendations:** Reduce fields to 6, show shipping on cart page, add guest option
```

**Bad:**
- ❌ "See attached" (examples should be inline)
- ❌ Only showing input OR output (need both)

### R — Refining

**Good:**
- "If 'more detail' → expand Analysis with data sources, confidence intervals"
- "If 'simplify' → remove jargon, focus top recommendations"

**Bad:**
- ❌ "Refine as needed" (too vague)
- ❌ "Don't be biased" (policy, not refinement)

---

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Using T for "Topic" | T = Target & Tone (WHO + HOW) |
| Using C for "Capture" | C = Context (environment) |
| Using A for "Audience" | A = Action (that's Target in T) |
| Vague actions ("analyze this") | Be specific (analyze for what?) |
| No format specification | Specify structure (table, JSON, paragraphs) |
| Missing tone | Always pair audience with communication style |
| No examples | Include 1-3 input→output pairs |

---

## Template Structure

```markdown
# [Superprompt Title]

**Purpose:** [One-line description]

---

## Context
[Environment, constraints, situation]

## Role
You are [expertise/perspective]. Your strengths include [capabilities].

## Action

Follow these steps:

1. **[Step One]**
   - [Concrete action]
   
2. **[Step Two]**
   - [Concrete action]

3. **[Step Three]**
   - [Concrete action]

## Format

Structure your output as:
[Specify: Markdown, JSON, table structure, length constraints]

## Target & Tone

**Target:** [Audience with characteristics]
**Tone:** [Communication approach suited to audience]

## Examples

### Example 1: [Scenario]
**Input:**
```
[Sample input]
```

**Output:**
```
[Sample output]
```

## Refining

**If the user requests:**
- "More detail" → [Specific expansion guidance]
- "Simplify" → [Specific simplification guidance]

---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

---

## Key v0.2 Changes

### What Changed

**T Component:** Target + Tone merged (previously Target only)

**Before (v0.1):**
```
T — Target (audience only)
```

**After (v0.2):**
```
T — Target & Tone (WHO uses this + HOW to communicate)
Formula: [Audience] + [Characteristics] → [Communication style]
```

**Why:** Audience characteristics naturally determine communication approach. Merging reduces confusion.

---

## Attribution

All superprompts must include:

```markdown
---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
Contributors: [list of contributors]
Pattern Used: [pattern name if applicable - see patterns.md]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

---

## Resources

| Resource | Link |
|----------|------|
| Full Specification | [01-CRAFTER-SPEC.md](./ai-context/01-CRAFTER-SPEC.md) |
| AI Briefing (dual-mode) | [ai.md](./ai.md) |
| Mode A Example | [example-mode-a-enhancement.md](./examples/example-mode-a-enhancement.md) |
| Mode B Example | [example-mode-b-creation.md](./examples/example-mode-b-creation.md) |
| Implementation Guide | [IMPLEMENTATION_GUIDE.md](./IMPLEMENTATION_GUIDE.md) |
| Pattern Library | [patterns.md](./docs/patterns.md) |
| Evaluation Rubric | [evaluation.md](./docs/evaluation.md) |
| GitHub Repository | https://github.com/CoachSteff/superprompt-framework |

---

## Quick Tips

**For AI models:**
- Read ai.md first to understand both modes
- Always use exact CRAFTER definitions (don't reinterpret)
- Complete self-test checklist (7/7 required)

**For humans:**
- Start with examples ([mode-a](./examples/example-mode-a-enhancement.md), [mode-b](./examples/example-mode-b-creation.md))
- Use template as starting point
- T = Target & Tone is the most important v0.2 update

**For teams:**
- Standardize on CRAFTER format for all prompts
- Store prompts in version control
- Use evaluation rubric to score quality

---

**Author:** Steff Vanhaverbeke ([@CoachSteff](https://github.com/CoachSteff))  
**License:** CC-BY 4.0  
**Website:** https://coachsteff.live

---

*This is a living document. Contributions welcome via GitHub.*