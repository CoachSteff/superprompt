# SuperPrompt Index

**A searchable catalog of all superprompts and patterns in this framework.**

Use tags to filter and find what you need. Patterns are reusable reasoning structures; examples are complete, ready-to-use prompts.

---

## Examples

### coaching-reflection.md
**Path:** `/examples/coaching-reflection.md`  
**Tags:** `coaching`, `leadership`, `reflection`, `monthly-review`, `executive-development`  
**Pattern:** Critique–Revise Loop  
**Description:** Help leaders reflect on their leadership in the past month and identify one concrete action to improve. Includes probing questions and an experimental action framed as a hypothesis to test.

---

### team-retrospective.md
**Path:** `/examples/team-retrospective.md`  
**Tags:** `team`, `retrospective`, `facilitation`, `agile`, `group-dynamics`  
**Pattern:** Role Mesh (Multi-Expert)  
**Description:** Design a 60-minute retrospective for a team after a difficult sprint. Surfaces underlying team dynamics (not just surface complaints) and creates one concrete team commitment.

---

### opportunity-scan.md
**Path:** `/examples/opportunity-scan.md`  
**Tags:** `entrepreneurship`, `decision-making`, `risk-assessment`, `business-strategy`  
**Pattern:** Counter-Case Probing  
**Description:** Evaluate a business opportunity by surfacing failure scenarios and stress-testing assumptions. Provides a clear "pursue" or "pass" recommendation with reasoning.

---

### documentation-cleanup.md
**Path:** `/examples/documentation-cleanup.md`  
**Tags:** `documentation`, `markdown`, `technical-writing`, `code-quality`  
**Pattern:** Rubric-First Grading (implicit)  
**Description:** Clean up markdown documentation files to make them readable, consistent, and navigable. Fixes formatting, structure, tone, and broken links.

---

### research-synthesis.md
**Path:** `/examples/research-synthesis.md`  
**Tags:** `research`, `synthesis`, `academic`, `knowledge-management`, `citations`  
**Pattern:** Source-Anchored Synthesis  
**Description:** Synthesize 5–10 sources on a research topic into a structured references.md file with key insights and proper citations. Every claim is traceable to a source.

---

## Patterns

### Decomposition
**Path:** `/docs/patterns.md#pattern-1-decomposition`  
**Tags:** `problem-solving`, `planning`, `complexity`, `structured-thinking`  
**When to use:** Complex problems that need breaking down into manageable steps.  
**Structure:** Break into 3-5 sub-problems → solve separately → synthesize → flag dependencies.

---

### Role Mesh (Multi-Expert)
**Path:** `/docs/patterns.md#pattern-2-role-mesh-multi-expert`  
**Tags:** `multi-perspective`, `evaluation`, `critique`, `trade-offs`  
**When to use:** You need perspectives from multiple disciplines or roles.  
**Structure:** Analyze from 3 perspectives → identify priorities and critiques → synthesize → flag tensions.

---

### Critique–Revise Loop
**Path:** `/docs/patterns.md#pattern-3-critiquerevise-loop`  
**Tags:** `iteration`, `refinement`, `quality`, `self-correction`  
**When to use:** You want iterative refinement built into a single prompt.  
**Structure:** Produce draft → critique against criteria → revise → present both versions.

---

### Counter-Case Probing
**Path:** `/docs/patterns.md#pattern-4-counter-case-probing`  
**Tags:** `stress-testing`, `risk-analysis`, `edge-cases`, `assumptions`  
**When to use:** You want to stress-test an idea by finding failure modes.  
**Structure:** Present claim → identify 3 failure scenarios → explain why each fails → revise claim.

---

### Data-to-Narrative Mapping
**Path:** `/docs/patterns.md#pattern-5-data-to-narrative-mapping`  
**Tags:** `data-analysis`, `storytelling`, `insights`, `communication`  
**When to use:** You have raw data and need a clear story.  
**Structure:** Identify patterns → frame as "so what?" → arrange into narrative → close with implications.

---

### Safety-First Guardrails
**Path:** `/docs/patterns.md#pattern-6-safety-first-guardrails`  
**Tags:** `ethics`, `safety`, `refusal-rules`, `responsible-ai`  
**When to use:** Task involves sensitive topics, ethical trade-offs, or potential harm.  
**Structure:** Identify concerns → explain clearly → refuse harmful outputs → prioritize transparency.

---

### Source-Anchored Synthesis
**Path:** `/docs/patterns.md#pattern-7-source-anchored-synthesis`  
**Tags:** `research`, `citations`, `verification`, `academic-integrity`  
**When to use:** Summarizing research or documents where claims must be verifiable.  
**Structure:** Extract claims → cite sources → synthesize → highlight agreements/disagreements.

---

### Style Transfer
**Path:** `/docs/patterns.md#pattern-8-style-transfer`  
**Tags:** `writing`, `translation`, `tone`, `audience-adaptation`  
**When to use:** Translate content from one style to another (formal to casual, technical to plain).  
**Structure:** Identify source/target styles → map differences → rewrite → self-check native feel.

---

### Perspective Shift
**Path:** `/docs/patterns.md#pattern-9-perspective-shift`  
**Tags:** `reframing`, `cognitive-flexibility`, `innovation`, `hidden-assumptions`  
**When to use:** Reframe a problem by changing the point of view.  
**Structure:** Describe from default perspective → shift to alternative → identify what changes → return insights.

---

### Rubric-First Grading
**Path:** `/docs/patterns.md#pattern-10-rubric-first-grading`  
**Tags:** `evaluation`, `assessment`, `feedback`, `criteria`  
**When to use:** Evaluate something (essay, design, strategy) against clear criteria.  
**Structure:** Define rubric → operationalize criteria → grade with evidence → provide actionable feedback.

---

## Core Framework Documents

### Mental Model
**Path:** `/docs/mental-model.md`  
**Tags:** `foundation`, `concepts`, `cognitive-interface`  
**Description:** The 120-word mental model + visual diagram explaining what a superprompt is and why it works.

---

### Template
**Path:** `/docs/template.md`  
**Tags:** `starter`, `boilerplate`, `copy-paste`  
**Description:** The canonical SuperPrompt Template v0.1—a copy-pastable starting point for any task.

---

### Pattern Library
**Path:** `/docs/patterns.md`  
**Tags:** `patterns`, `reasoning-structures`, `reusable-components`  
**Description:** 10 reusable reasoning patterns with structure tweaks, examples, failure modes, and fixes.

---

### Evaluation Rubric
**Path:** `/docs/evaluation.md`  
**Tags:** `quality`, `scoring`, `debugging`, `improvement`  
**Description:** Score superprompts on 6 axes (0–5 scale) with repair checklist and examples.

---

### Workflow Guide
**Path:** `/docs/workflow.md`  
**Tags:** `process`, `github`, `cursor`, `versioning`  
**Description:** How to store, version, and share superprompts in Cursor and GitHub. Includes naming conventions and commit message style.

---

### Quick Start
**Path:** `/docs/quick-start.md`  
**Tags:** `getting-started`, `tutorial`, `onboarding`  
**Description:** Get started with the SuperPrompt Framework in 10 steps.

---

### FAQ
**Path:** `/docs/faq.md`  
**Tags:** `questions`, `troubleshooting`, `common-issues`  
**Description:** Answers to common questions about what superprompts are, how to use them, and common pitfalls.

---

## How to Use This Index

1. **Browse by tag** to find relevant prompts or patterns
2. **Read the description** to understand what it does
3. **Follow the path** to open the full file
4. **Copy and adapt** for your own tasks

---

## Contributing

Want to add your own superprompt or pattern? Follow the [workflow guide](docs/workflow.md) and submit a pull request. Don't forget to add your contribution to this index with tags and a description.

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
