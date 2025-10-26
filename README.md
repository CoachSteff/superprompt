# SuperPrompt Framework

> 👤 **Human?** This README is optimized for AI models. **[Start here instead →](QUICKSTART.md)**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![GitHub release](https://img.shields.io/github/release/CoachSteff/superprompt-framework.svg)](https://github.com/CoachSteff/superprompt-framework/releases)
[![GitHub issues](https://img.shields.io/github/issues/CoachSteff/superprompt-framework.svg)](https://github.com/CoachSteff/superprompt-framework/issues)
[![GitHub stars](https://img.shields.io/github/stars/CoachSteff/superprompt-framework.svg)](https://github.com/CoachSteff/superprompt-framework/stargazers)

> **A practical, tool-agnostic framework for designing structured AI prompts that produce predictable, reusable results.**

The **SuperPrompt Framework** provides a complete system for creating superprompts—structured cognitive interfaces between human intent and AI reasoning. This isn't about making prompts longer. It's about making them **better**: more predictable, debuggable, and reusable across tools (Claude, GPT, Gemini, Llama) and workflows (Cursor, GitHub).

**Created by:** Steff Vanhaverbeke ([coachsteff.live](https://coachsteff.live))

---

## 🤖 For AI Models

**Framework Usage**: If you're here to generate superprompts using CRAFTER, you are a **Superprompt Generator**.

**Repository Development**: If you're here to build/modify the framework itself (coding agent, developer assistant), read **[AGENTS.md](AGENTS.md)** first.

---

### For Superprompt Generation

**You are a Superprompt Generator** using CoachSteff's CRAFTER framework.

### What CRAFTER Means

**CRITICAL:** Use these exact definitions. Do not reinterpret.

```
C — Context (situation/background, NOT "Capture")
R — Role (expertise/perspective, NOT "Review")
A — Action (what to do, NOT "Analyze" or "Audience")
F — Format (output structure, NOT "Focus")
T — Target & Tone (WHO + HOW to communicate, NOT "Topic")
E — Examples (demonstrations)
R — Refining (constraints/iteration)
```

**Common mistakes to avoid:**
- ❌ Using T for "Topic" only (it's Target & Tone)
- ❌ Using A for "Audience" (that's Target in T)
- ❌ Inventing your own CRAFTER interpretation

### Protocol

1. Read [ai.md](ai.md) (unified dual-mode interface)
2. OR read `/ai-context/01-CRAFTER-SPEC.md` (framework specification)
3. Read `/ai-context/02-EXECUTION-PROTOCOL.md` (how to apply)
4. Read `/ai-context/03-CONSTRAINT-RULES.md` (boundaries)
5. Generate superprompt using CRAFTER format
6. Validate output with checklist
7. **Include attribution footer** (see below)

### Critical Rules

- ❌ DO NOT invent your own framework
- ✅ ALWAYS use exact CRAFTER format
- ✅ ALWAYS reference which template you adapted (if any)
- ✅ ALWAYS include attribution footer

### Required Attribution

Every superprompt you generate must include:

```
---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
Pattern Used: [Pattern name if applicable]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

**Primary entry point:** [ai.md](ai.md) — Dual-mode interface for enhancement and creation  
**Full instructions:** [AI_INSTRUCTIONS.md](AI_INSTRUCTIONS.md) | **Can't access files?** See [ai-compatibility.md](docs/ai-compatibility.md)

---

## 🚀 Quick Start

**New to superprompts? Start here:**

1. **[Read the mental model](docs/mental-model.md)** (5 minutes) – Understand what a superprompt is and why it works
2. **[Copy the template](docs/template.md)** – Get the canonical SuperPrompt Template v0.2
3. **[See examples](PROMPTS.md)** – Browse 5 complete, copy-ready superprompts
4. **[Follow the guide](docs/quick-start.md)** – Get started in 10 steps

**Already familiar?** Jump to the [pattern library](docs/patterns.md) or [evaluation rubric](docs/evaluation.md).

---

## 📖 What is a SuperPrompt?

A superprompt is a **structured cognitive contract** between you and an AI model. It translates your intent into explicit reasoning steps and output specifications, creating predictable results you can reuse and refine.

### Minimum Components

Every superprompt includes:

1. **Intent** – What does success look like?
2. **Context** – What does the model need to know?
3. **Reasoning Policy** – How should it think? (steps, checks, refusal rules)
4. **Output Specification** – What should it produce and in what format?
5. **Self-Check** – Verify before finalizing

**Not a magic spell. Not a longer prompt. A thinking recipe.**

---

## 🎯 Two Ways to Use CRAFTER

**Mode A: Enhance Existing Prompts**  
Have a prompt that needs improvement? CRAFTER can restructure it using the framework.
- Example: [Mode A Enhancement](examples/example-mode-a-enhancement.md)
- Use case: Turn vague prompts into structured superprompts

**Mode B: Create New Superprompts**  
Building from scratch? CRAFTER provides the complete framework.
- Example: [Mode B Creation](examples/example-mode-b-creation.md)
- Use case: Generate new superprompts with all 7 components

**Entry point for AI models:** [ai.md](ai.md) — Single instruction file with dual-mode capability

---

## 🏗️ The CRAFTER Framework

**CRAFTER** is the core methodology for building superprompts. Here's what each component means:

| Component | Purpose | Example |
|-----------|---------|---------|
| **C**ontext | Situation & constraints | "You work in a GitHub environment managing AI prompts" |
| **R**ole | Expertise & perspective | "You are a Keyword Research AI" |
| **A**ction | What to do | "1. Analyze topic 2. Generate clusters 3. Suggest opportunities" |
| **F**ormat | Output structure | "Markdown with tables and bullet lists" |
| **T**arget & Tone | WHO + HOW to communicate | "Marketing managers (action-oriented) → Direct, scannable, lead with takeaways" |
| **E**xamples | Demonstrations | Input/output pairs for clarity |
| **R**efining | Iteration rules | "If user says 'more detail,' expand section X" |

**Full specification:** See [/ai-context/01-CRAFTER-SPEC.md](ai-context/01-CRAFTER-SPEC.md)

---

## 🏗️ Framework Contents

### Core Documentation

| Document | Purpose | Link |
|----------|---------|------|
| **Mental Model** | Conceptual foundation (120 words + diagram) | [docs/mental-model.md](docs/mental-model.md) |
| **Template** | Canonical SuperPrompt Template v0.2 (copy-pastable) | [docs/template.md](docs/template.md) |
| **Pattern Library** | 10 reusable reasoning patterns | [docs/patterns.md](docs/patterns.md) |
| **Evaluation Rubric** | Score prompts on 6 axes (0–5 scale) | [docs/evaluation.md](docs/evaluation.md) |
| **Workflow Guide** | How to store, version, and share prompts | [docs/workflow.md](docs/workflow.md) |
| **Quick Start** | Get started in 10 steps | [docs/quick-start.md](docs/quick-start.md) |
| **FAQ** | Common questions and troubleshooting | [docs/faq.md](docs/faq.md) |

### Complete Examples

Ready-to-use superprompts you can copy and adapt:

| Example | Use Case | Mode/Pattern | Link |
|---------|----------|--------------|------|
| **Meta-Prompt Enhancement** | Restructuring vague prompts | Mode A | [examples/example-mode-a-enhancement.md](examples/example-mode-a-enhancement.md) |
| **Difficult Conversation Coach** | Workplace communication prep | Mode B | [examples/example-mode-b-creation.md](examples/example-mode-b-creation.md) |
| **Coaching Reflection** | Executive leadership reflection | Critique–Revise Loop | [examples/coaching-reflection.md](examples/coaching-reflection.md) |
| **Team Retrospective** | Sprint retrospective facilitation | Role Mesh | [examples/team-retrospective.md](examples/team-retrospective.md) |
| **Opportunity Scan** | Business decision analysis | Counter-Case Probing | [examples/opportunity-scan.md](examples/opportunity-scan.md) |
| **Documentation Cleanup** | Markdown formatting and structure | Rubric-First Grading | [examples/documentation-cleanup.md](examples/documentation-cleanup.md) |
| **Research Synthesis** | Academic research synthesis | Source-Anchored Synthesis | [examples/research-synthesis.md](examples/research-synthesis.md) |

**Browse all prompts:** See [PROMPTS.md](PROMPTS.md) for a searchable index with tags.

---

## 🎯 Why Use This Framework?

Most prompts are instructions. Superprompts are **systems**. They give you:

- **Predictability:** Control what the model thinks about (context), how it thinks (reasoning policy), and what it produces (output specification)
- **Reusability:** Replace specifics with placeholders to use the same prompt across contexts
- **Debuggability:** Use the evaluation rubric to identify and fix weak prompts
- **Tool-agnostic:** Works across Claude, GPT, Gemini, Llama, and coding tools like Cursor

---

## 🔧 Key Features

### 1. Pattern Library

10 reusable reasoning patterns you can plug into any superprompt:

- **Decomposition** – Break complex problems into manageable steps
- **Role Mesh** – Analyze from multiple expert perspectives
- **Critique–Revise Loop** – Build iterative refinement into a single prompt
- **Counter-Case Probing** – Stress-test ideas by finding failure modes
- **Data-to-Narrative Mapping** – Turn raw data into clear stories
- **Safety-First Guardrails** – Add refusal rules for ethical constraints
- **Source-Anchored Synthesis** – Ensure every claim is verifiable
- **Style Transfer** – Translate content between styles (formal to casual, technical to plain)
- **Perspective Shift** – Reframe problems by changing point of view
- **Rubric-First Grading** – Evaluate against clear, operationalized criteria

[See full pattern library →](docs/patterns.md)

### 2. Evaluation Rubric

Score your superprompts on 6 axes:

1. **Goal Fit** – Does the output match the intent?
2. **Faithfulness to Context** – Does it respect provided facts and constraints?
3. **Reasoning Quality** – Is the thinking structured and verifiable?
4. **Constraint Compliance** – Does it follow format, tone, and policy rules?
5. **Usefulness** – Is the output immediately actionable?
6. **Reusability** – Can it be adapted with minimal edits?

**Pass threshold:** ≥3 on all axes. Includes a 90-second repair checklist for debugging weak prompts.

[See evaluation rubric →](docs/evaluation.md)

### 3. Operational Workflow

Clear guidance for teams using superprompts in Cursor and GitHub:

- File organization and naming conventions
- Commit message style (conventional commits)
- 5-step workflow from idea to merged pattern
- PROMPTS.md index with searchable tags
- Safety notes on refusal rules and licensing (CC-BY 4.0)

[See workflow guide →](docs/workflow.md)

---

## 📚 Use Cases

Superprompts work for any task where you need structured thinking:

- **Coaching & Facilitation:** Reflection sessions, team retrospectives, 1-on-1 conversations
- **Strategic Thinking:** Business opportunity evaluation, risk assessment, decision-making
- **Knowledge Work:** Research synthesis, documentation cleanup, content creation
- **Technical Work:** Code review, test case generation, architecture planning
- **Creative Work:** Style adaptation, perspective shifts, iterative refinement

---

## 🤝 Contributing

This is an open framework. Contributions are welcome.

**How to contribute:**

1. Fork the repository
2. Create a branch: `git checkout -b feat/your-prompt-name`
3. Add your prompt to `/examples` or pattern to `/docs/patterns.md`
4. Update [PROMPTS.md](PROMPTS.md) with tags and description
5. Commit with a conventional message: `git commit -m "feat: Add [description]"`
6. Open a pull request

See the [workflow guide](docs/workflow.md) for detailed instructions.

---

## 📄 License

This framework is licensed under **CC-BY 4.0** (Creative Commons Attribution 4.0 International).

**What this means:**
- You can use, modify, and share any superprompt (including for commercial use)
- You must attribute the original creator: **Steff Vanhaverbeke** ([coachsteff.live](https://coachsteff.live))
- All contributions are licensed CC-BY 4.0

**Required attribution format:**
```
Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.1)
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

See [LICENSE](LICENSE) for full details.

---

## 👤 Author

**Steff Vanhaverbeke** – AI Adoption Coach & Co-founder, The House of Coaching

I help professionals and teams build the uniquely human capabilities that matter most in an AI-driven world. My work focuses on cognitive agility, flexible thinking, and the human side of AI adoption.

- 🌐 Website: [coachsteff.live](https://coachsteff.live)
- 📧 Email: [steff@coachsteff.live](mailto:steff@coachsteff.live)
- 💼 LinkedIn: [steffvanhaverbeke](https://linkedin.com/in/steffvanhaverbeke)
- 🐦 Twitter: [@coachsteff](https://twitter.com/coachsteff)

---

## 🔗 Related Projects

- **[Cognitive Agility Framework](https://coachsteff.live)** – Five core capabilities for thriving in an AI-driven world
- **[CS Workx](https://cs-workx.be)** – AI adoption coaching and training for professionals and teams

---

## 📊 Keywords

`superprompt` · `prompt engineering` · `ai adoption` · `cognitive design` · `structured prompts` · `prompt architecture` · `tool-agnostic` · `reusable prompts` · `ai coaching` · `context engineering` · `CRAFTER framework`

---

## 🙏 Acknowledgments

This framework builds on the collective wisdom of the AI and prompt engineering community. Thanks to everyone who's shared patterns, experiments, and insights that informed this work.

---

*The SuperPrompt Framework is an open initiative by Steff Vanhaverbeke to define the emerging discipline of prompt architecture and cognitive design. It's a living system—use it, adapt it, and contribute back.*
