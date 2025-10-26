# CRAFTER Framework Specification v0.2

**Official specification for CoachSteff's CRAFTER SuperPrompt Framework**

Version: 0.2  
Last Updated: January 2025  
Status: Stable  
License: CC-BY 4.0

---

## Document Purpose

This specification defines the **CRAFTER framework** — a structured methodology for building superprompts that produce predictable, reusable results across AI models (Claude, GPT, Gemini, Llama) and tools (Cursor, GitHub).

**Audience:** AI models, developers, and prompt engineers implementing the CRAFTER framework.

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 0.1 | 2024-12 | Initial release. T = Target audience only |
| 0.2 | 2025-01 | **T = Target & Tone (merged)**. Added dual-mode capability (enhancement vs creation) |

---

## What is CRAFTER?

CRAFTER is an acronym representing seven components that structure AI interactions:

- **C** — Context
- **R** — Role
- **A** — Action
- **F** — Format
- **T** — Target & Tone *(updated in v0.2)*
- **E** — Examples
- **R** — Refining

Each component serves a specific purpose. Together, they form a complete cognitive contract between human intent and AI reasoning.

---

## Core Philosophy

### Superprompts Are Not Longer Prompts

A superprompt is a **thinking recipe**, not a magic spell.

**Traditional prompt:**
> "Write a blog post about AI"

**Superprompt:**
> A structured specification that defines:
> - What environment you're operating in (Context)
> - What expertise you bring (Role)
> - What steps to take (Action)
> - What format to produce (Format)
> - Who will use it and how to communicate (Target & Tone)
> - What good output looks like (Examples)
> - How to iterate (Refining)

### Three Design Principles

1. **Predictability** — Control what the model thinks about, how it thinks, and what it produces
2. **Reusability** — Replace specifics with placeholders to use across contexts
3. **Debuggability** — Use evaluation rubric to identify and fix weak prompts

---

## CRAFTER Components: Complete Specification

### C — Context

**Definition:** The environment, situation, and constraints where the task will be performed.

**Questions to answer:**
- What is the current situation?
- What constraints apply?
- What resources are available?
- What assumptions can be made?

**Good examples:**

```
You're working with a content team managing Q4 campaign materials 
stored in Google Docs. The team has 3 writers, 1 editor, and works 
in 2-week sprints.
```

```
You're analyzing customer support tickets for a B2B SaaS product 
with 50K users. The product launched 18 months ago and currently 
has 200 tickets/month average.
```

**Bad examples:**
- ❌ "Capture the requirements" → This is Action, not Context
- ❌ "You are Claude" → Overly meta, not situational
- ❌ "Current date is..." → Only include if date matters to the task

**Common mistakes:**
- Confusing context with action
- Including irrelevant background information
- Being too vague ("you're working on a project")

---

### R — Role

**Definition:** The expertise, perspective, or identity the AI should adopt.

**Questions to answer:**
- What specialized knowledge is needed?
- What perspective should guide the thinking?
- What professional lens should be applied?

**Good examples:**

```
You are a Content Strategist with expertise in semantic SEO and 
natural language processing. You understand how search engines 
parse content and how readers consume information online.
```

```
You are an Executive Coach trained in cognitive behavioral coaching 
and organizational psychology. You help leaders develop self-awareness 
and strategic thinking.
```

**Bad examples:**
- ❌ "Review the document" → This is Action, not Role
- ❌ "You are helpful and friendly" → Too generic
- ❌ "Act like a human" → Imprecise and problematic

**Common mistakes:**
- Confusing role with action ("you are someone who analyzes...")
- Being too broad ("you are an expert")
- Using adjectives instead of expertise ("you are smart")

---

### A — Action

**Definition:** The concrete, step-by-step tasks the AI should perform.

**Questions to answer:**
- What specific steps should be taken?
- In what order should they happen?
- What should each step produce?

**Format:** Numbered list with action verbs.

**Good examples:**

```
1. **Analyze** the input text for recurring themes and patterns
2. **Identify** gaps where critical information is missing
3. **Generate** 3 recommendations ranked by potential impact
4. **Validate** each recommendation against stated constraints
```

```
1. **Extract** key points from the meeting transcript
2. **Categorize** points into: Decisions, Action Items, Questions
3. **Assign** priority levels (High/Medium/Low) to action items
4. **Format** as a structured summary
```

**Bad examples:**
- ❌ "Analyze this" → Too vague (analyze for what?)
- ❌ "Use Python and SQL" → Tools aren't actions
- ❌ "Be thorough" → Quality guidance, not a step

**Common mistakes:**
- Using vague verbs ("handle," "deal with," "process")
- Listing tools instead of actions
- Missing the step-by-step sequence

---

### F — Format

**Definition:** The output structure and presentation specification.

**Questions to answer:**
- What medium should be used? (Markdown, JSON, table, etc.)
- How should information be organized?
- What length constraints apply?
- What visual structure is needed?

**Good examples:**

```
Markdown table with columns: Theme | Evidence | Recommendation | Priority
Include 5-8 rows maximum.
```

```
JSON object with structure:
{
  "summary": "string (100 words max)",
  "risks": ["array", "of", "strings"],
  "next_steps": [{"action": "string", "owner": "string", "deadline": "date"}]
}
```

```
Three sections:
1. Executive Summary (150 words max)
2. Detailed Analysis (3-5 paragraphs)
3. Recommendations (bullet list with 3-5 items)
```

**Bad examples:**
- ❌ "Focus on quality" → Not a format specification
- ❌ "Professional style" → That's Tone, not Format
- ❌ "Make it good" → Too vague

**Common mistakes:**
- Confusing format with tone or style
- Not specifying structure clearly
- Forgetting length constraints

---

### T — Target & Tone *(v0.2 Update)*

**Definition:** WHO will use this output + HOW to communicate with them.

**This is the most significant change in v0.2.** Previously, T = Target audience only. Now Target and Tone are integrated because they're naturally coupled in real-world communication.

**Formula:** [Audience] + [Their characteristics] → [Communication approach]

**Questions to answer:**
- Who will read/use this output?
- What are their characteristics? (expertise level, time constraints, goals)
- What communication style suits them?
- How should information be presented to match their needs?

**Good examples:**

**Example 1: Technical Audience**
```
Target: Engineering team leads (senior developers with 5+ years experience)
Characteristics: Value precision, want to see rationale, appreciate technical depth
Tone: Use technical terminology without over-explaining. Cite sources. 
      Include implementation rationale. Assume high technical literacy.
```

**Example 2: Executive Audience**
```
Target: Executive leadership (C-suite, limited time, strategic focus)
Characteristics: Need quick decisions, focus on business impact, value quantification
Tone: Lead with bottom-line summary. Use executive language (ROI, strategic alignment, 
      risk mitigation). Provide details on request, not by default. Quantify impact 
      when possible.
```

**Example 3: Cross-Functional Team**
```
Target: Marketing managers (busy, action-oriented, need to brief their teams)
Characteristics: Moderate technical understanding, need practical takeaways, value clarity
Tone: Direct and scannable. Lead with key takeaway. Use bullet points for clarity. 
      Avoid jargon. Provide clear next steps with owners and deadlines.
```

**Example 4: Learning Audience**
```
Target: Junior developers (1-2 years experience, learning mode)
Characteristics: Building mental models, need context for decisions, appreciate resources
Tone: Explain the "why" behind recommendations. Define technical terms. Include learning 
      resources. Use analogies where helpful. Be patient and thorough.
```

**Example 5: Customer-Facing**
```
Target: End users (non-technical, need immediate help)
Characteristics: Problem-focused, want solutions not explanations, limited patience
Tone: Plain language. Solution-first. Use "you" language. Include screenshots or 
      step-by-step instructions. Avoid technical terms unless necessary.
```

**Bad examples:**
- ❌ "Tone should be professional" → Too vague
- ❌ "Target: Increase sales" → That's a goal, not an audience
- ❌ "Topic is marketing" → That's Context, not Target
- ❌ "Temperature: 0.7" → Model settings, not audience/tone
- ❌ "Audience: Everyone" → Not specific enough

**Why Target & Tone Are Merged (v0.2 Rationale):**

In v0.1, Target (audience) was separated from Tone (communication style). This created problems:

**Problems with separation:**
1. Tone became "orphaned" — unclear where to specify it
2. Created confusion — AI models didn't know where to put communication style guidance
3. Artificial split — in real communication, audience **determines** tone

**Benefits of integration:**
1. Natural coupling — busy executives need concise tone, technical teams need precise tone
2. Reduced confusion — one component handles both dimensions
3. Clearer guidance — formula shows how audience characteristics drive communication approach
4. Matches real-world practice — professional communicators always consider audience when choosing tone

**Common mistakes:**
- Describing the topic instead of the audience
- Specifying tone without connecting it to audience needs
- Using model parameters (temperature, top_p) instead of communication style
- Being too vague ("professional" without defining what that means)

---

### E — Examples

**Definition:** Input→output demonstrations showing what good output looks like.

**Questions to answer:**
- What does successful output look like?
- What edge cases should be handled?
- How should the model interpret ambiguous input?

**Format:** Provide 1-3 concrete examples with both input and output.

**Good examples:**

```
### Example 1: Product Feature Request

Input: "Our checkout abandonment rate is 40%"

Output:
**Issue Analysis:** High abandonment rate indicates friction in payment flow
**Root Causes:**
1. Too many required form fields (12 vs industry standard of 6)
2. Shipping costs not visible until final step
3. No guest checkout option available

**Recommendations:**
1. Reduce form fields to: email, card info, shipping address only
2. Display estimated shipping costs on cart page
3. Add "Continue as Guest" button above login form
```

```
### Example 2: Meeting Summary

Input: [45-minute meeting transcript about Q4 planning]

Output:
**Key Decisions:**
- Launch new product tier in Q4 (approved: $50K budget)
- Delay mobile app update to Q1 2025

**Action Items:**
- Sarah: Draft pricing strategy by Sept 15
- James: Audit current tech stack by Sept 20
- Team: Review competitive landscape next week

**Open Questions:**
- How to position against Competitor X?
- Should we bundle or unbundle features?
```

**Bad examples:**
- ❌ "See attached document" → Examples should be inline
- ❌ "Additional context..." → Not actually an example
- ❌ Only showing input OR output → Need both

**Common mistakes:**
- Providing examples that are too abstract
- Not showing edge cases
- Including only perfect scenarios without showing how to handle ambiguity

---

### R — Refining

**Definition:** Iteration guidance for when the user requests changes or adjustments.

**Questions to answer:**
- What common adjustment requests should be anticipated?
- How should the model respond to feedback?
- What types of refinements are in scope?

**Good examples:**

```
If user says "more detail," expand the Analysis section with:
- Supporting data sources
- Quantitative evidence
- Implementation timeline

If user says "too technical," revise by:
- Replacing jargon with plain language
- Adding analogies or examples
- Removing implementation specifics

If user says "add urgency," include:
- Timeline for decision
- Risk of delayed action
- Competitive pressure context
```

**Bad examples:**
- ❌ "Refine as needed" → Too vague
- ❌ "Don't be biased" → That's policy, not refinement guidance
- ❌ "Start completely over" → Too extreme for iteration

**Common mistakes:**
- Not anticipating common adjustment patterns
- Being too prescriptive (limiting flexibility)
- Forgetting to preserve core structure during refinement

---

## Framework Validation: Self-Test Checklist

Before finalizing any superprompt, verify all 7 components are present and well-specified:

- [ ] **C** — Context: Environment and constraints clearly specified?
- [ ] **R** — Role: Expertise and perspective defined?
- [ ] **A** — Action: Step-by-step tasks enumerated (numbered list)?
- [ ] **F** — Format: Output structure precisely described?
- [ ] **T** — Target & Tone: Audience + communication approach specified?
- [ ] **E** — Examples: Input→output demonstrations included?
- [ ] **R** — Refining: Iteration guidance provided?

**Pass threshold: 7/7**

If any component scores 0, the superprompt is incomplete and should be revised.

---

## Common Anti-Patterns

### 1. The Vague Action
❌ "Analyze the document"  
✅ "Analyze the document for: (1) recurring themes, (2) factual claims, (3) recommendations"

### 2. The Missing Audience
❌ "Professional tone"  
✅ "Target: Executive team (limited time, strategic focus). Tone: Concise, business-focused, lead with impact"

### 3. The Format-Free Prompt
❌ "Give me some insights"  
✅ "Markdown table with columns: Insight | Supporting Evidence | Confidence Level (High/Medium/Low)"

### 4. The Example-Less Specification
❌ [No examples provided]  
✅ "Example: Input: 'reduce costs' → Output: 'Cost optimization opportunities: vendor consolidation (est. 15% savings)...'"

### 5. The Context Dump
❌ "Here's everything I know about the company's history..."  
✅ "You're analyzing Q3 2024 sales data for a B2B SaaS company with 50K users"

---

## Tool-Agnostic Design

CRAFTER works across all major AI platforms:

| Platform | Compatibility | Notes |
|----------|---------------|-------|
| Claude (Anthropic) | ✅ Full | Native support for structured thinking |
| GPT (OpenAI) | ✅ Full | Works with GPT-3.5, GPT-4, GPT-4o |
| Gemini (Google) | ✅ Full | Handles long context well |
| Llama (Meta) | ✅ Full | Open-source friendly |
| Cursor | ✅ Full | Excellent for code-focused prompts |
| Other tools | ✅ Full | Framework is model-agnostic |

---

## Attribution Requirements

All superprompts using CRAFTER must include:

```
---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
Contributors: [list of contributors]
Pattern Used: [pattern name if applicable]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

This attribution:
- Acknowledges the framework source
- Maintains license compliance (CC-BY 4.0)
- Helps others discover and learn the framework

---

## Related Resources

- **Execution Protocol:** [02-EXECUTION-PROTOCOL.md](./02-EXECUTION-PROTOCOL.md)
- **Constraint Rules:** [03-CONSTRAINT-RULES.md](./03-CONSTRAINT-RULES.md)
- **Patterns Library:** [../docs/patterns.md](../docs/patterns.md)
- **Evaluation Rubric:** [../docs/evaluation.md](../docs/evaluation.md)
- **Quick Start Guide:** [../docs/quick-start.md](../docs/quick-start.md)

---

## Change Log

### v0.2 (January 2025)

**Major changes:**
- **T component merged:** Target & Tone now integrated (previously Target audience only)
  - Rationale: Audience characteristics naturally determine communication approach
  - Formula added: [Audience] + [Characteristics] → [Communication style]
  - Five detailed examples added showing audience→tone coupling

- **Dual-mode capability added:** Single entry point handles both:
  - Mode A: Meta-prompt enhancement (restructure existing prompts)
  - Mode B: Superprompt creation (generate new prompts)

- **Expanded examples:** All components now include "good" and "bad" examples

**Minor changes:**
- Added version history table
- Expanded anti-patterns section
- Updated attribution format to reference v0.2

### v0.1 (December 2024)

- Initial release
- 7-component framework established
- T = Target audience only

---

**Maintained by:** Steff Vanhaverbeke ([@CoachSteff](https://github.com/CoachSteff))  
**License:** CC-BY 4.0  
**Repository:** https://github.com/CoachSteff/superprompt-framework
