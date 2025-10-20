# SuperPrompt Evaluation Rubric

**Score your superprompts on six axes, each rated 0–5. A passing superprompt scores ≥3 on all axes.**

Use this rubric to debug weak prompts or decide if a prompt is ready to share.

---

## Scoring Scale

| Score | Descriptor | What It Means |
|-------|-----------|---------------|
| **5** | Excellent | Exceeds expectations; nothing to improve |
| **4** | Strong | Meets expectations with minor gaps |
| **3** | Adequate | Meets minimum bar; some weaknesses |
| **2** | Weak | Significant gaps; needs revision |
| **1** | Poor | Barely functional; major problems |
| **0** | Absent | Critical component missing entirely |

---

## Axis 1: Goal Fit

**Does the output match the stated intent?**

- **Observable signals:** Compare the output against the success criteria in the INTENT section. Does it solve the right problem? Is it the right scope and depth?

| Score | Description |
|-------|-------------|
| **5** | Output perfectly matches intent; success criteria met or exceeded |
| **4** | Output mostly matches intent; minor deviations don't affect usability |
| **3** | Output addresses the core intent but misses some success criteria |
| **2** | Output is loosely related to intent but doesn't solve the actual problem |
| **1** | Output solves a different problem than intended |
| **0** | Intent not defined or completely ignored |

**How to debug low scores:** Rewrite the INTENT section with sharper success criteria. Use concrete examples: "Success = a 90-minute agenda, not a general workshop outline."

---

## Axis 2: Faithfulness to Context

**Does the output respect the provided context?**

- **Observable signals:** Check if the output uses the facts, examples, constraints, or style guides you provided. Does it invent facts not in the context?

| Score | Description |
|-------|-------------|
| **5** | Every claim is anchored in provided context; no hallucinations |
| **4** | Mostly faithful to context; minor extrapolations are reasonable |
| **3** | Uses context but adds unsupported claims or misses key constraints |
| **2** | Ignores significant parts of context or introduces conflicting info |
| **1** | Output contradicts provided context |
| **0** | No context provided or entirely ignored |

**How to debug low scores:** Add a refusal rule in REASONING POLICY: "If you don't have enough context to answer, ask for clarification instead of guessing." Make constraints explicit: "Budget: €500. Do not exceed."

---

## Axis 3: Reasoning Quality

**Is the thinking structured, verifiable, and sound?**

- **Observable signals:** Can you follow the logic? Are steps explicit? Does the output show its work or just assert conclusions?

| Score | Description |
|-------|-------------|
| **5** | Reasoning is transparent, step-by-step, and logically sound |
| **4** | Reasoning is clear but skips minor steps; still verifiable |
| **3** | Reasoning is present but vague or hard to follow in places |
| **2** | Reasoning is weak or contains logical gaps |
| **1** | Output asserts conclusions without reasoning |
| **0** | No reasoning policy defined; thinking is opaque |

**How to debug low scores:** Add numbered steps to REASONING POLICY. Example: "1. Define the problem. 2. Identify constraints. 3. Generate solutions. 4. Evaluate against criteria."

---

## Axis 4: Constraint Compliance

**Does the output follow format, length, tone, and policy rules?**

- **Observable signals:** Is it in the requested format (JSON, markdown, paragraph)? Right tone (formal, casual)? Within length limits? Does it refuse harmful requests?

| Score | Description |
|-------|-------------|
| **5** | Follows all constraints perfectly; format, tone, and policy respected |
| **4** | Follows most constraints; minor deviations don't break usability |
| **3** | Follows core constraints but misses some formatting or tone requirements |
| **2** | Violates significant constraints (wrong format, wrong tone) |
| **1** | Ignores most constraints |
| **0** | No constraints defined or completely ignored |

**How to debug low scores:** Make constraints non-negotiable. Use OUTPUT SCHEMA for structured data. Add refusal rules: "Do not produce outputs longer than 500 words."

---

## Axis 5: Usefulness of Output

**Is the output actionable, clear, and immediately usable?**

- **Observable signals:** Can someone use this output without further work? Is it clear what to do next? Does it solve the problem in a practical way?

| Score | Description |
|-------|-------------|
| **5** | Output is immediately actionable; no additional work needed |
| **4** | Output is useful with minor edits or clarifications |
| **3** | Output is a starting point but needs significant refinement |
| **2** | Output is vague, abstract, or hard to apply |
| **1** | Output is not useful in practice |
| **0** | Output is nonsensical or unusable |

**How to debug low scores:** Add "actionable" to your success criteria. Example: "Produce a checklist someone can follow today, not a conceptual framework."

---

## Axis 6: Reusability

**Can this prompt be used again with minimal edits?**

- **Observable signals:** If you swap in a new topic or audience, does the prompt still work? Are the instructions general enough to adapt?

| Score | Description |
|-------|-------------|
| **5** | Prompt is fully reusable; only placeholders need updating |
| **4** | Prompt is mostly reusable; minor adjustments for new contexts |
| **3** | Prompt works but requires rewriting some sections for new use cases |
| **2** | Prompt is highly specific; hard to adapt to other scenarios |
| **1** | Prompt is single-use; can't generalize |
| **0** | Prompt is so vague it's not useful even once |

**How to debug low scores:** Replace specifics with placeholders. Instead of "design a workshop for managers," write "design a <format> for <audience>."

---

## Pass Threshold

A superprompt is **ready to use** if it scores **≥3 on all six axes**. If any axis scores below 3, revise before using it in production or sharing it.

---

## 90-Second Prompt Repair Checklist

Use this when you have a low-scoring prompt and need to fix it fast.

1. **Goal Fit < 3?** → Rewrite INTENT with sharper success criteria and concrete examples
2. **Faithfulness < 3?** → Add missing facts to CONTEXT; add refusal rules for unsupported claims
3. **Reasoning < 3?** → Break REASONING POLICY into numbered steps; require "show your work"
4. **Constraint Compliance < 3?** → Make constraints explicit and non-negotiable; add OUTPUT SCHEMA
5. **Usefulness < 3?** → Add "actionable" to success criteria; require next steps or checklists
6. **Reusability < 3?** → Replace specifics with placeholders; generalize instructions

---

## Example Scoring

**Prompt:** "Write a blog post about AI."

| Axis | Score | Why |
|------|-------|-----|
| Goal Fit | 1 | Intent is vague; no success criteria |
| Faithfulness | 0 | No context provided |
| Reasoning | 0 | No reasoning policy defined |
| Constraint Compliance | 2 | No format or tone specified |
| Usefulness | 1 | Output will be generic and not actionable |
| Reusability | 4 | The structure could work for any topic |

**Verdict:** Fails. Needs major revision on all axes except reusability.

**After repair:**

```markdown
Title: Write a blog post about AI adoption for mid-level managers

INTENT
Produce a 600-word blog post that helps mid-level managers understand why AI adoption requires new skills, not just new tools. Success = clear argument, one real-world example, and a practical next step.

CONTEXT
- Audience: Mid-level managers in tech companies (non-technical)
- Tone: Warm, empathetic, practical (no hype or jargon)
- Example: A team that bought AI tools but didn't train people, leading to frustration
- Key idea: AI adoption is a people challenge, not a technology challenge

REASONING POLICY
1. Start with a relatable pain point managers face with AI adoption
2. Introduce the idea that skills matter more than tools
3. Use the example to illustrate the point
4. Close with one actionable next step readers can take this week
5. Refuse to use buzzwords like "disruptive" or "game-changing"

OUTPUT
A blog post in markdown format with:
- Headline (10 words max)
- 3 short sections (200 words each)
- One pull quote
- A closing CTA (call to action)

SELF-CHECK
- Is this 600 words?
- Does it avoid jargon?
- Is the next step specific and doable?
```

**New Scores:**

| Axis | Score | Why |
|------|-------|-----|
| Goal Fit | 5 | Clear intent with measurable success criteria |
| Faithfulness | 5 | Rich context with tone, audience, and examples |
| Reasoning | 4 | Clear steps, though could be more detailed |
| Constraint Compliance | 5 | Format, length, and tone all specified |
| Usefulness | 5 | Output will be immediately publishable |
| Reusability | 5 | Easy to adapt for other topics or audiences |

**Verdict:** Ready to use.

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
