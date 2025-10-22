# CRAFTER Framework: Canonical Specification

**Framework:** CoachSteff's CRAFTER (SuperPrompt Framework v0.1)  
**Author:** Steff Vanhaverbeke ([coachsteff.live](https://coachsteff.live))  
**License:** CC-BY 4.0 — Attribution required  
**This is the authoritative definition. Do not deviate.**

---

## What CRAFTER Stands For

**CRITICAL:** CRAFTER has a specific meaning in this framework. Do not reinterpret.

```
C — Context (NOT "Capture")
R — Role (NOT "Review")
A — Action (NOT "Analyze", NOT "Audience")
F — Format (NOT "Focus")
T — Target audience (NOT "Topic", NOT "Tone", NOT "Tailor")
E — Examples (NOT "Evolve")
R — Refining (NOT "Reprompt", NOT "Restrictions")
```

### Component Clarifications (What Each Letter MEANS)

**C = Context**  
→ "What environment are we operating in?"  
→ Example: "You are working with a professional coach's content library"  
❌ NOT "Capture requirements" or "Collect information"

**R = Role**  
→ "What expertise do you bring to this?"  
→ Example: "You are a Content Strategist with NLP training"  
❌ NOT "Review the input" or "Research the topic"

**A = Action**  
→ "What concrete steps should you take?"  
→ Example: "1. Analyze tone, 2. Identify patterns, 3. Generate variants"  
❌ NOT "Analyze this" (too vague) or "Audience" (that's T)

**F = Format**  
→ "What should the output look like?"  
→ Example: "Markdown table with 3 columns: Original, Variant, Rationale"  
❌ NOT "Focus on quality" or "Prioritize clarity"

**T = Target audience**  
→ "Who will use this output?"  
→ Example: "Marketing managers who need customer-facing copy"  
❌ NOT "Tone should be professional" or "Topic is marketing"

**E = Examples**  
→ "Show me what good looks like"  
→ Example: Input: "Buy now!" → Output: "Discover your solution today"  
❌ NOT "Evolve the prompt over time"

**R = Refining**  
→ "How can we iterate if this isn't quite right?"  
→ Example: "If tone is too formal, ask: 'Make it more conversational'"  
❌ NOT "Reprompt from scratch" or "Restrictions on output"

---

## Common Misinterpretations to Avoid

| ❌ Wrong | ✅ Right | Why It Matters |
|---------|---------|----------------|
| T = Tone | T = Target audience | Tone is an attribute of Format, not a separate component |
| T = Topic | T = Target audience | Topic is covered in Action (what you're working on) |
| A = Audience | A = Action | Audience is the Target; Action is what you do |
| CRAFTER as design methodology | CRAFTER as prompt structure | This framework structures AI instructions, not human processes |

---

## Structure

Every CRAFTER superprompt has these components in this exact order:

```
::CRAFTER

C – Context
[Explicit role and environment definition]

R – Role  
[Specific expertise and perspective]

A – Action
[Concrete, measurable task]

F – Format
[Exact output structure]

T – Target Audience
[Who this is for and why]

E – Examples (optional)
[Input/output demonstrations]

R – Refining Script (optional)
[Iteration instructions if needed]
```

---

## Component Specifications

### C – Context
**Purpose:** Establish environment and constraints  
**Length:** 2-4 sentences  
**Must include:**
- Where/how this prompt operates
- Key constraints or boundaries
- Connection to larger system (if applicable)

**Example:**
```
You are connected to the GitHub environment of CoachSteff. 
You work within a system that manages superprompts, skills, 
and context packages for AI agents. The user typically wants 
to create content for professional audiences.
```

### R – Role
**Purpose:** Define expertise and cognitive stance  
**Length:** 1-2 sentences  
**Must include:**
- Specific domain expertise
- Cognitive approach (how you think)
- Unique perspective or capability

**Example:**
```
You are a Keyword Researcher AI with deep insight in semantic 
search intent, contextual positioning, and human language patterns.
```

### A – Action
**Purpose:** Specify exactly what to do  
**Format:** Numbered list preferred  
**Must include:**
- Sequential steps
- Decision points
- Output requirements

**Example:**
```
1. Receive main topic
2. Analyze search intent
3. Generate semantic network of related terms
4. Divide into three layers: Core, Context, Conversation
5. Suggest content opportunities
```

### F – Format
**Purpose:** Define output structure  
**Must specify:**
- File type (markdown, JSON, etc.)
- Section structure
- Visual elements (tables, lists, headers)

**Example:**
```
Markdown with clear sections:
## Keyword Research Summary
### Semantic Clusters (table format)
### Content Opportunities (bullet list)
### Prompt Hooks (examples)
```

### T – Target Audience
**Purpose:** Calibrate complexity and focus  
**Must include:**
- Who this is for
- What they're trying to achieve
- Knowledge level assumptions

**Example:**
```
Content creators, coaches, and entrepreneurs who want to 
understand how AI approaches keyword research. They want 
to learn the thinking process, not just get lists.
```

### E – Examples (Optional)
**Purpose:** Demonstrate input/output patterns  
**Include when:**
- Format is ambiguous
- Domain is unfamiliar
- Edge cases exist

### R – Refining Script (Optional)
**Purpose:** Enable iteration  
**Include when:**
- First pass may need adjustment
- Multiple valid approaches exist
- Quality threshold is subjective

---

## Framework Integrity Check

⚠️ **Before you generate any superprompt, verify:**

1. Am I using the CRAFTER structure (C-R-A-F-T-E-R)?
2. Or have I substituted a different framework?

**If you realize you're using a different structure:**
- STOP immediately
- Reread this specification
- Start over with CRAFTER

**This framework is NOT:**
- CREATE (Context, Role, Examples, Action, Tone, Evaluate)
- PROMPT (Problem, Role, Objective, Mechanics, Process, Tone)
- PROJECT (Problem, Role, Objective, etc.)

**This framework IS:**
- CoachSteff's CRAFTER (Context, Role, Action, Format, Target, Examples, Refining)

---

## Validation Checklist

- [ ] All required components present (C, R, A, F, T)
- [ ] Components in correct order
- [ ] Action items are concrete and sequential
- [ ] Format specification is unambiguous
- [ ] Target audience is clearly defined
- [ ] No component substitutions (T = Target, not Tone/Topic)

---

## Attribution Requirements

When adapting this framework, include at the END of your output:

```
---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.1)
Pattern Used: [Your pattern name if applicable]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```
