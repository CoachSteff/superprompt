# SuperPrompt Pattern Library

**Patterns are reusable reasoning structures you can plug into your superprompts. Each pattern solves a specific cognitive challenge.**

Copy the structure tweak into your REASONING POLICY section when you need that pattern.

---

## Pattern 1: Decomposition

**When to use:** Complex problems that need breaking down into manageable steps.

**Structure tweak:**
```
REASONING POLICY
1. Break the problem into 3-5 independent sub-problems
2. Solve each sub-problem separately
3. Synthesize solutions into a coherent whole
4. Flag any dependencies between sub-problems
```

**Example snippet:**
"Decompose 'design an AI adoption strategy' into: assess current state, identify capabilities gap, design learning path, measure progress."

**Failure mode:** Over-decomposition creates artificial silos that miss systemic connections.

**Fix:** Add a synthesis step that explicitly looks for cross-cutting themes or dependencies.

---

## Pattern 2: Role Mesh (Multi-Expert)

**When to use:** You need perspectives from multiple disciplines or roles to evaluate an idea.

**Structure tweak:**
```
REASONING POLICY
1. Analyze the problem from three perspectives: <role A>, <role B>, <role C>
2. For each role, identify what they would prioritize and what they would critique
3. Synthesize insights across all three perspectives
4. Flag tensions or trade-offs between perspectives
```

**Example snippet:**
"Evaluate this workshop design as: (1) a learning designer, (2) a busy manager, (3) a budget owner."

**Failure mode:** Superficial role-play that doesn't capture genuine tensions between perspectives.

**Fix:** Add specific success criteria for each role and make trade-offs explicit in the synthesis.

---

## Pattern 3: Critique–Revise Loop

**When to use:** You want iterative refinement built into a single prompt.

**Structure tweak:**
```
REASONING POLICY
1. Produce an initial draft
2. Critique the draft against <specific criteria>
3. Revise based on critique
4. Present both the critique and the revised version
```

**Example snippet:**
"Draft a coaching question, critique it for open-endedness and non-judgment, then revise."

**Failure mode:** The critique is too gentle or vague, so revision doesn't meaningfully improve the output.

**Fix:** Make critique criteria sharp and specific: "Does this question assume a right answer?"

---

## Pattern 4: Counter-Case Probing

**When to use:** You want to stress-test an idea by finding edge cases or failure modes.

**Structure tweak:**
```
REASONING POLICY
1. Present the main claim or solution
2. Identify 3 scenarios where this claim would fail or lead to poor outcomes
3. For each counter-case, explain why the failure occurs
4. Revise the claim to account for these edge cases
```

**Example snippet:**
"Claim: 'All teams should adopt AI tools immediately.' Find counter-cases where this advice would backfire."

**Failure mode:** Counter-cases are trivial or obvious ("if you have no budget"), not genuinely challenging.

**Fix:** Ask for surprising or non-obvious failure modes that reveal hidden assumptions.

---

## Pattern 5: Data-to-Narrative Mapping

**When to use:** You have raw data (numbers, survey results, logs) and need a clear story.

**Structure tweak:**
```
REASONING POLICY
1. Identify the most significant patterns or outliers in the data
2. Frame each pattern as a "so what?"—why it matters
3. Arrange insights into a logical narrative arc
4. Close with an actionable implication or next step
```

**Example snippet:**
"Here are 50 survey responses about AI adoption. Extract 3 key themes and turn them into a narrative with implications."

**Failure mode:** Listing data points without interpretation or narrative coherence.

**Fix:** Require each data point to be translated into a human-readable insight with stakes.

---

## Pattern 6: Safety-First Guardrails

**When to use:** The task involves sensitive topics, ethical trade-offs, or potential harm.

**Structure tweak:**
```
REASONING POLICY
1. Before proceeding, identify any ethical, legal, or safety concerns with the request
2. If concerns exist, explain them clearly and offer alternatives
3. Refuse to produce outputs that could cause harm, even if the request seems well-intentioned
4. Prioritize transparency about limitations over completing the task at any cost
```

**Example snippet:**
"I need a script for performance reviews. Check for bias risks before drafting."

**Failure mode:** Safety checks are performative and don't genuinely constrain harmful outputs.

**Fix:** Make refusal rules explicit and non-negotiable: "Refuse if the output could be used to manipulate or coerce."

---

## Pattern 7: Source-Anchored Synthesis

**When to use:** You're summarizing research, articles, or documents and need verifiable claims.

**Structure tweak:**
```
REASONING POLICY
1. Extract key claims from each source
2. For each claim, note which source it comes from (cite inline)
3. Synthesize across sources, highlighting agreements and disagreements
4. Refuse to make claims not supported by the provided sources
```

**Example snippet:**
"Synthesize these three papers on AI adoption. Cite each claim with [Author, Year]."

**Failure mode:** Synthesis introduces claims or interpretations not present in the original sources.

**Fix:** Add a self-check: "Are all claims in my synthesis directly traceable to a source?"

---

## Pattern 8: Style Transfer

**When to use:** You need to translate content from one style to another (formal to casual, technical to plain language).

**Structure tweak:**
```
REASONING POLICY
1. Identify the source style and target style
2. Map key differences: tone, vocabulary, sentence structure, formatting
3. Rewrite the content, preserving meaning but shifting style
4. Self-check: Does this sound like it was written natively in the target style?
```

**Example snippet:**
"Translate this academic paper abstract into a LinkedIn post for busy professionals."

**Failure mode:** Style transfer is superficial—just swapping words—without adapting structure or tone.

**Fix:** Define target style with examples: "LinkedIn posts use short paragraphs, personal anecdotes, and actionable takeaways."

---

## Pattern 9: Perspective Shift

**When to use:** You want to reframe a problem by changing the point of view.

**Structure tweak:**
```
REASONING POLICY
1. Describe the problem from the default perspective
2. Shift to <alternative perspective>: how would they see this differently?
3. Identify what becomes visible or invisible in the new frame
4. Return insights that only emerge from the shifted perspective
```

**Example snippet:**
"I see AI as a productivity tool. Reframe it from the perspective of a coach focused on human development."

**Failure mode:** Perspective shift is cosmetic—just relabeling—without genuine cognitive reframing.

**Fix:** Require the new perspective to surface a hidden assumption or trade-off from the original frame.

---

## Pattern 10: Rubric-First Grading

**When to use:** You need to evaluate something (an essay, a design, a strategy) against clear criteria.

**Structure tweak:**
```
REASONING POLICY
1. Define the rubric: what are the 3-5 evaluation criteria?
2. For each criterion, define what "excellent," "adequate," and "needs work" look like
3. Grade the submission on each criterion with evidence
4. Provide a summary score and specific, actionable feedback
```

**Example snippet:**
"Evaluate this workshop design on: clarity of objective, interactivity, feasibility, and participant value."

**Failure mode:** Grading is vague or inconsistent because criteria aren't operationalized.

**Fix:** Make criteria observable: "Interactivity: Are participants talking more than the facilitator?"

---

## How to Use Patterns

1. **Identify your cognitive challenge**: Do you need decomposition? Multiple perspectives? Critique?
2. **Pick the relevant pattern** from this library
3. **Copy the structure tweak** into your REASONING POLICY section
4. **Customize** with your specific criteria, roles, or constraints

Patterns can be **combined**. For example: use Role Mesh + Critique–Revise to get multi-expert feedback and iterative refinement in one prompt.

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
