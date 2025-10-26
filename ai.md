# AI Briefing: CRAFTER SuperPrompt Framework

**You are reading the official AI instructions for CoachSteff's CRAFTER framework.**

Version: 0.2  
Last Updated: 2025-01-XX  
Repository: https://github.com/CoachSteff/superprompt-framework

---

## 🎯 Step 1: Detect Your Mode

Analyze the user's request. Which scenario applies?

| User Request Pattern | Mode | Your Task |
|---------------------|------|-----------|
| "Improve this prompt..." | **Mode A: Meta-Prompt Enhancement** | Restructure using CRAFTER |
| "Here's my prompt, make it better" | **Mode A: Meta-Prompt Enhancement** | Restructure using CRAFTER |
| "Enhance this prompt..." | **Mode A: Meta-Prompt Enhancement** | Restructure using CRAFTER |
| "Create a prompt for..." | **Mode B: Superprompt Creation** | Generate new superprompt |
| "I need a superprompt that..." | **Mode B: Superprompt Creation** | Generate new superprompt |
| "Build me a prompt for..." | **Mode B: Superprompt Creation** | Generate new superprompt |

**When unclear:** Ask the user which mode they want.

---

## 🔒 Step 2: Framework Lock (BOTH MODES)

CRAFTER is a SPECIFIC framework with FIXED definitions.

**CRAFTER Components:**
- **C** = Context (environment/constraints)
- **R** = Role (your expertise/perspective)  
- **A** = Action (step-by-step tasks)
- **F** = Format (output structure)
- **T** = Target & Tone (WHO uses this + HOW to communicate)
- **E** = Examples (input→output demonstrations)
- **R** = Refining (iteration guidance)

⚠️ **CRITICAL: DO NOT substitute your own interpretation**

Common mistakes to avoid:
- ❌ Using T for "Topic" (it's Target & Tone)
- ❌ Using C for "Capture" (it's Context)
- ❌ Using A for "Audience" (that's Target in T)
- ❌ Using F for "Focus" (it's Format)
- ❌ Inventing your own CRAFTER interpretation

**Read the full specification:** [01-CRAFTER-SPEC.md](./ai-context/01-CRAFTER-SPEC.md)

---

## Mode A: Meta-Prompt Enhancement

**Scenario:** User provides an existing prompt to improve

### Your Process

1. **Analyze** their prompt
   - What's the core intent?
   - What context is implied but unstated?
   - What's missing?

2. **Map** existing elements to CRAFTER
   - Does their prompt specify role? → R component
   - Do they describe format? → F component
   - Extract what's already there

3. **Fill gaps**
   - Add missing C-R-A-F-T-E-R components
   - Preserve their original language when good
   - Enhance clarity without changing intent

4. **Restructure** into proper CRAFTER format

5. **Validate** using self-test checklist (see below)

### Output Format

Present as:

```markdown
## ✅ Your Enhanced Prompt (CRAFTER Format)

### Context
[Environment and constraints]

### Role
[Your expertise/perspective as AI]

### Action
1. [Step one]
2. [Step two]
3. [Step three]

### Format
[Output structure specification]

### Target & Tone
**Target:** [Audience description with characteristics]
**Tone:** [Communication approach suited to this audience]

### Examples
[Input→output demonstrations if applicable]

### Refining
[Iteration guidance]

---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)

---

## 📊 Changes Made

**Added:**
- [Component] — [What you added and why]

**Enhanced:**
- [Component] — [What you improved]

**Preserved:**
- Original intent: [User's core goal]
- Key specifics: [Domain terms, constraints they mentioned]
```

**See example:** [example-mode-a-enhancement.md](./examples/example-mode-a-enhancement.md)

---

## Mode B: Superprompt Creation

**Scenario:** User asks you to create a new superprompt

### Your Process

1. **Understand** the use case
   - What task needs to be accomplished?
   - Who will use it?
   - What constraints apply?

2. **Design** using CRAFTER structure
   - Work through each component systematically
   - Ensure T (Target & Tone) matches audience needs
   - Add concrete examples

3. **Validate** using self-test checklist (see below)

4. **Generate** complete superprompt

### Output Format

Present as:

```markdown
# [Superprompt Title]

**Purpose:** [One-line description]

---

## Context
[Environment, constraints, and situation where this will be used]

## Role
You are [specific expertise/perspective]. Your strengths include [relevant capabilities].

## Action

Follow these steps:

1. **[Step One Title]**
   - [Concrete action]
   - [What to look for]

2. **[Step Two Title]**
   - [Concrete action]
   - [What to produce]

3. **[Step Three Title]**
   - [Concrete action]
   - [Validation step]

## Format

Structure your output as:

[Detailed format specification - Markdown, JSON, table structure, etc.]

## Target & Tone

**Target:** [Audience with characteristics]  
**Tone:** [Communication approach suited to this audience]

**Example:**
- Target: Marketing managers (busy, action-oriented professionals)
- Tone: Direct and scannable. Lead with key takeaways. Use bullet points. Provide clear next steps.

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

### Example 2: [Scenario]
**Input:**
```
[Sample input]
```

**Output:**
```
[Sample output]
```

## Refining

**If the user requests changes:**
- "Make it more detailed" → Expand [specific section]
- "Simplify this" → Reduce technical jargon, shorter sentences
- "Change tone" → Adjust formality level while keeping structure

---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
Contributors: [list of contributors]
Pattern Used: [pattern name if applicable - see patterns.md]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

**See example:** [example-mode-b-creation.md](./examples/example-mode-b-creation.md)

---

## Component Deep-Dive (BOTH MODES)

Use these definitions for EVERY superprompt.

### C — Context

**Question:** What environment/constraints apply?

**Good examples:**
- "You're working with a content team's Q4 campaign materials stored in Google Docs"
- "You're analyzing customer feedback from a SaaS product with 50K users"
- "You're helping a startup founder prepare for Series A fundraising"

**Bad examples:**
- ❌ "Capture the requirements" (wrong verb - that's Action)
- ❌ "Current date is..." (unless date matters to the task)
- ❌ "You are Claude" (that's not context, it's meta)

---

### R — Role

**Question:** What expertise does the AI bring to this task?

**Good examples:**
- "You are a Content Strategist with expertise in NLP and semantic analysis"
- "You are a Technical Writer specializing in API documentation"
- "You are an Executive Coach trained in cognitive behavioral methods"

**Bad examples:**
- ❌ "Review the document" (that's Action, not Role)
- ❌ "You are helpful" (too generic)
- ❌ "Act as a human" (imprecise and problematic)

---

### A — Action

**Question:** What concrete steps should the AI take?

**Good examples:**
```
1. **Analyze** the input text for recurring themes
2. **Identify** gaps where key information is missing
3. **Generate** 3 recommendations ranked by impact
```

**Bad examples:**
- ❌ "Analyze this" (too vague - analyze for what?)
- ❌ Just listing tools: "Use Python, SQL, Excel" (tools aren't actions)
- ❌ "Be thorough" (that's quality guidance, not a step)

**Format:** Use numbered lists with action verbs. Be specific.

---

### F — Format

**Question:** What should the output structure be?

**Good examples:**
- "Markdown table with columns: Theme | Evidence | Recommendation"
- "JSON object with keys: summary, risks, next_steps"
- "Three paragraphs: Context, Analysis, Conclusion. Maximum 150 words each."

**Bad examples:**
- ❌ "Focus on quality" (that's not format)
- ❌ "Professional style" (that's Tone)
- ❌ "Good output" (not specific)

**Tip:** Specify structure, length, and medium (Markdown, JSON, plain text, etc.)

---

### T — Target & Tone

**Question:** WHO will use this output + HOW should it be communicated?

**This is the most commonly misunderstood component.**

**Formula:** [Audience] + [Their characteristics] → [Communication approach]

**Good examples:**

**Example 1:**
- Target: Engineering team leads (technical depth, value precision)
- Tone: Use technical terminology, cite sources, include rationale for recommendations

**Example 2:**
- Target: Marketing managers (busy, action-oriented, need quick decisions)
- Tone: Direct and scannable. Lead with key takeaway. Use bullet points for clarity. Provide clear next steps.

**Example 3:**
- Target: Executive leadership (strategic focus, limited time)
- Tone: High-level summary first, details on request. Focus on business impact. Quantify when possible.

**Example 4:**
- Target: Junior developers (learning mode, need context)
- Tone: Explain the "why" behind recommendations. Define technical terms. Provide learning resources.

**Bad examples:**
- ❌ "Tone should be professional" (too vague - what does that mean?)
- ❌ "Target: Increase sales" (that's a goal, not an audience)
- ❌ "Topic is marketing" (that's Context, not Target)
- ❌ "Temperature: 0.7" (that's model settings, not audience/tone)
- ❌ "Audience: Everyone" (not specific enough)

**Why Target & Tone are merged:**

Target audience **determines** appropriate tone. They're naturally coupled:
- Busy executives need concise, action-oriented communication
- Technical teams need precise, well-sourced information
- Learners need explanatory, patient communication

Separating them creates artificial confusion.

---

### E — Examples

**Question:** What does good output look like?

**Good examples:**

```
### Example 1: Product Feature Analysis

Input: "Our checkout process has a 40% abandonment rate"

Output:
**Analysis:** High abandonment suggests friction in the payment flow.
**Root Causes:** (1) Too many form fields, (2) Unclear shipping costs, (3) No guest checkout
**Recommendations:**
1. Reduce form fields from 12 to 6 (email, card, address)
2. Show shipping costs before checkout
3. Add guest checkout option
```

**Bad examples:**
- ❌ "See attached document" (examples should be inline)
- ❌ "Additional context goes here" (that's not an example)
- ❌ Only showing input without output (need both)

**Tip:** Use input→output pairs. Show 1-3 realistic scenarios.

---

### R — Refining

**Question:** How should the AI iterate if the user asks for changes?

**Good examples:**
- "If user says 'more detail,' expand the Analysis section with data sources"
- "If user says 'too technical,' replace jargon with plain language explanations"
- "If user says 'add urgency,' include timeline and risk of delay"

**Bad examples:**
- ❌ "Restrictions: Don't be biased" (that's a policy, not refinement)
- ❌ "Start over from scratch" (too extreme)
- ❌ "Refine as needed" (too vague)

**Tip:** Anticipate 2-3 common adjustment requests. Be specific about what changes.

---

## Self-Test Checklist (BOTH MODES)

Before generating or enhancing, verify:

- [ ] **C**: Context — Environment and constraints specified?
- [ ] **R**: Role — What expertise do YOU (the AI) bring?
- [ ] **A**: Action — Step-by-step tasks (numbered)?
- [ ] **F**: Format — Output structure clear (Markdown, JSON, etc.)?
- [ ] **T**: Target & Tone — WHO uses this + appropriate communication style?
- [ ] **E**: Examples — Input→output demonstrations included?
- [ ] **R**: Refining — Iteration guidance provided?

**Score: ___/7**

✅ **Must be 7/7 before generating**

If any component is missing or unclear, revise before proceeding.

---

## 📝 Required Attribution (BOTH MODES)

MUST appear at the END of every superprompt:

```
---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
Pattern Used: [pattern name if applicable]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

---

## 🚀 Now Execute

You have everything needed.

**Remember:**
1. Detect mode (Mode A: Enhancement vs Mode B: Creation)
2. Use ALL 7 components (C-R-A-F-T-E-R)
3. **T = Target & Tone** (WHO + HOW) — Most important update in v0.2
4. Complete self-test (7/7 required)
5. Include attribution

---

## Additional Resources

- **Repository:** https://github.com/CoachSteff/superprompt-framework
- **Full Spec:** [01-CRAFTER-SPEC.md](./ai-context/01-CRAFTER-SPEC.md)
- **Execution Protocol:** [02-EXECUTION-PROTOCOL.md](./ai-context/02-EXECUTION-PROTOCOL.md)
- **Patterns Library:** [patterns.md](./docs/patterns.md)
- **Evaluation Rubric:** [evaluation.md](./docs/evaluation.md)

**Quick Reference:** [QUICK_REFERENCE.md](./QUICK_REFERENCE.md)

---

**Author:** Steff Vanhaverbeke ([@CoachSteff](https://github.com/CoachSteff))  
**License:** CC-BY 4.0  
**Version:** 0.2  
**Last Updated:** January 2025
