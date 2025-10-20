# Operational Workflow: Cursor & GitHub

**How to store, version, and share superprompts in a team or personal workflow.**

This guide covers: file organization, naming conventions, commit messages, and a 5-step workflow from idea to merged pattern.

---

## File Organization

Store superprompts in a structured repo with these conventions:

```
/framework/
  patterns.md         # Pattern library (reusable reasoning structures)
  template.md         # Canonical template
  evaluation.md       # Rubric for scoring prompts

/examples/
  coaching-reflection.md
  team-retrospective.md
  opportunity-scan.md
  documentation-cleanup.md
  research-synthesis.md

/docs/
  mental-model.md     # Conceptual foundation
  faq.md              # Common questions
  quick-start.md      # 10-line getting started guide
  workflow.md         # This file

README.md             # Overview and navigation
PROMPTS.md            # Index of all prompts with tags
```

---

## Naming Conventions

**For prompt files:**
- Use kebab-case: `coaching-reflection.md`, `team-retrospective.md`
- Name after the task, not the tool: `documentation-cleanup.md` (not `gpt-doc-fixer.md`)
- Keep names descriptive and searchable: `research-synthesis.md` (not `example5.md`)

**For patterns:**
- Store all patterns in `/framework/patterns.md` as sections
- Use Title Case for pattern names: `Decomposition`, `Role Mesh`, `Counter-Case Probing`

---

## Commit Message Style

Use conventional commits for clarity and searchability:

```
feat: Add Counter-Case Probing pattern
fix: Correct evaluation rubric scoring scale
docs: Update quick start with new examples
refactor: Reorganize pattern library by category
```

**Conventional commit types:**
- `feat`: New pattern, template, or example
- `fix`: Correction to existing prompt or documentation
- `docs`: Documentation updates (README, FAQ, guides)
- `refactor`: Restructure without changing functionality
- `chore`: Maintenance (file cleanup, typo fixes)

---

## 5-Step Workflow: From Idea to Merged Pattern

### Step 1: Draft the Prompt

Start in Cursor or your editor of choice. Use the canonical template from `/framework/template.md` as your starting point.

**What to include:**
- Clear INTENT with success criteria
- Rich CONTEXT with examples and constraints
- Structured REASONING POLICY with numbered steps
- Specific OUTPUT format or schema
- SELF-CHECK to verify quality

**Tip:** Don't try to make it perfect on the first pass. Just get the structure in place.

---

### Step 2: Test the Prompt

Run your superprompt in at least two AI tools (Claude, GPT, Gemini, Llama) to verify it's tool-agnostic.

**What to check:**
- Does it produce the desired output consistently?
- Are there formatting issues or ambiguities?
- Does it handle edge cases (missing context, unclear input)?

**If it fails:** Revise the REASONING POLICY or add constraints. Use the evaluation rubric to identify weak axes.

---

### Step 3: Score with the Rubric

Use the evaluation rubric from `/framework/evaluation.md` to score your prompt on six axes:

1. Goal Fit
2. Faithfulness to Context
3. Reasoning Quality
4. Constraint Compliance
5. Usefulness of Output
6. Reusability

**Pass threshold:** ≥3 on all axes.

If any axis scores below 3, revise before proceeding to Step 4.

---

### Step 4: Document and Tag

Add your prompt to the appropriate folder:

- **Reusable patterns** → `/framework/patterns.md` (as a new section)
- **Complete examples** → `/examples/your-prompt-name.md`

Add an entry to `PROMPTS.md` with tags for discoverability:

```markdown
## coaching-reflection.md
**Tags:** coaching, leadership, reflection, monthly-review  
**Pattern used:** Critique–Revise Loop  
**Description:** Help leaders reflect on their month and identify one concrete action to improve.
```

---

### Step 5: Commit and Share

Commit your prompt with a conventional commit message:

```bash
git add examples/your-prompt-name.md PROMPTS.md
git commit -m "feat: Add leadership reflection prompt with critique-revise pattern"
git push origin main
```

**If working in a team:** Open a pull request and tag a reviewer. Include:
- A brief description of what the prompt does
- Which pattern(s) it uses
- A sample output (optional but helpful)

---

## PROMPTS.md Index

The `PROMPTS.md` file serves as a searchable index of all prompts in the repo. Each entry should include:

- **Filename and path**
- **Tags** (comma-separated for filtering)
- **Pattern used** (if applicable)
- **One-line description**

**Example:**

```markdown
# SuperPrompt Index

## Examples

### coaching-reflection.md
**Path:** `/examples/coaching-reflection.md`  
**Tags:** coaching, leadership, reflection, monthly-review  
**Pattern:** Critique–Revise Loop  
**Description:** Help leaders reflect on their month and identify one concrete action to improve.

### team-retrospective.md
**Path:** `/examples/team-retrospective.md`  
**Tags:** team, retrospective, facilitation, agile  
**Pattern:** Role Mesh  
**Description:** Design a 60-minute retrospective that surfaces team dynamics and creates a concrete commitment.

### opportunity-scan.md
**Path:** `/examples/opportunity-scan.md`  
**Tags:** entrepreneurship, decision-making, risk-assessment  
**Pattern:** Counter-Case Probing  
**Description:** Evaluate a business opportunity by surfacing failure scenarios and stress-testing assumptions.

## Patterns

### Decomposition
**Path:** `/framework/patterns.md#decomposition`  
**Tags:** problem-solving, planning, complexity  
**Description:** Break complex problems into 3-5 independent sub-problems, solve separately, then synthesize.

### Role Mesh (Multi-Expert)
**Path:** `/framework/patterns.md#role-mesh`  
**Tags:** multi-perspective, evaluation, critique  
**Description:** Analyze a problem from multiple expert perspectives to surface tensions and trade-offs.
```

---

## Safety Note: Refusal Rules

Superprompts should include explicit refusal rules in the REASONING POLICY to prevent harmful outputs.

**Examples of refusal rules:**
- "Refuse to produce outputs that could be used to manipulate or coerce."
- "Refuse to make claims not supported by the provided sources."
- "Refuse to generate content that violates the style guide."

When designing refusal rules:
- Make them specific and actionable
- Explain *why* the refusal matters (not just "don't do X")
- Test edge cases: what happens if someone tries to bypass the rule?

---

## IP and Licensing

All superprompts in this repo are licensed **CC-BY 4.0** (Creative Commons Attribution 4.0 International).

**What this means:**
- You can use, modify, and share any superprompt
- You must attribute the original creator: Steff Vanhaverbeke (coachsteff.live)
- You can use superprompts in commercial projects

**When contributing:**
- By submitting a prompt, you agree to license it under CC-BY 4.0
- You retain copyright but grant others the right to use your work with attribution
- If you're adapting someone else's prompt, credit them in your file

---

## Quick Reference: Common Commands

```bash
# Create a new branch for your prompt
git checkout -b feat/your-prompt-name

# Add your files
git add examples/your-prompt-name.md PROMPTS.md

# Commit with conventional message
git commit -m "feat: Add [description]"

# Push and open a pull request
git push origin feat/your-prompt-name
```

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
