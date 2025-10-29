# Getting Started with the SuperPrompt Framework

**A practical guide to creating structured, reusable AI prompts that work across tools and contexts.**

---

## What Are Superprompts?

A superprompt is a **structured cognitive interface** between human intent and AI reasoning. It translates what you want into how the model should think, then specifies what it should produce. It's not about length—it's about architecture.

Think of it as a thinking contract: you define the goal, constraints, reasoning steps, and output format. The model follows that structure to deliver predictable, reusable results.

### The Key Insight

Most prompts are instructions. Superprompts are **systems**. They create predictability by controlling three variables:

1. **What to think about** (context)
2. **How to think** (reasoning policy)  
3. **What to produce** (output specification)

When you control these, you get consistent results you can reuse, refine, and share.

---

## The CRAFTER Framework

The SuperPrompt Framework uses **CRAFTER**—a 7-component structure for building reliable prompts:

| Component | Purpose | Example |
|-----------|---------|---------|
| **C**ontext | Environment & constraints | "You're analyzing Q3 sales data for an e-commerce company (50K transactions)" |
| **R**ole | Expertise & perspective | "You are a Data Analyst specializing in e-commerce analytics" |
| **A**ction | Step-by-step tasks | "1. Identify trends 2. Analyze anomalies 3. Generate recommendations" |
| **F**ormat | Output structure | "Markdown table: Theme \| Evidence \| Recommendation" |
| **T**arget & Tone | WHO + HOW to communicate | "Marketing managers (action-oriented) → Direct, scannable, lead with takeaways" |
| **E**xamples | Input→output demonstrations | "Input: 'reduce costs' → Output: 'Cost optimization: vendor consolidation (15% savings)'" |
| **R**efining | How to iterate | "If 'more detail' → expand Analysis with data sources and timeline" |

**Key insight**: T = Target & Tone (WHO uses this + HOW to communicate) — the most important component for getting the right output style.

---

## Your First Superprompt (5 Steps)

### 1. Browse Examples
Start by exploring complete, copy-ready superprompts in the `/examples` folder:
- [Coaching Reflection](examples/coaching-reflection.md) - Executive leadership reflection
- [Team Retrospective](examples/team-retrospective.md) - Sprint retrospective facilitation  
- [Opportunity Scan](examples/opportunity-scan.md) - Business decision analysis
- [Documentation Cleanup](examples/documentation-cleanup.md) - Markdown formatting
- [Research Synthesis](examples/research-synthesis.md) - Academic research synthesis

### 2. Copy a Template
Use the canonical template from [docs/template.md](docs/template.md) as your starting point. It includes all CRAFTER components with clear placeholders.

### 3. Adapt to Your Use Case
Replace the template placeholders with your specifics:
- **Context**: What environment and constraints apply?
- **Role**: What expertise should the AI bring?
- **Action**: What specific steps should it follow?
- **Format**: How should the output be structured?
- **Target & Tone**: Who will use this and how should it be communicated?
- **Examples**: What does good output look like?
- **Refining**: How should it adjust if you ask for changes?

### 4. Test with Your AI Tool
Paste your completed superprompt into your AI tool (Claude, ChatGPT, Gemini, etc.) and run it. Check the output: Does it match your intent?

### 5. Refine Based on Results
If the output isn't quite right, adjust the weak components and re-run. Use the [evaluation rubric](docs/evaluation.md) to identify which axis needs improvement.

---

## Example Gallery

### Quick Examples by Use Case

**For Content Creation:**
- [Documentation Cleanup](examples/documentation-cleanup.md) - Structure and format markdown content

**For Strategic Thinking:**
- [Opportunity Scan](examples/opportunity-scan.md) - Analyze business opportunities and risks

**For Team Facilitation:**
- [Team Retrospective](examples/team-retrospective.md) - Guide sprint retrospectives

**For Personal Development:**
- [Coaching Reflection](examples/coaching-reflection.md) - Executive leadership reflection

**For Research:**
- [Research Synthesis](examples/research-synthesis.md) - Synthesize academic research

### Templates Available

- [Keyword Researcher](templates/keyword-researcher.md) - Semantic keyword clustering and analysis

---

## Going Deeper

Once you understand the basics, explore these resources:

### Core Documentation
- **[Pattern Library](docs/patterns.md)** - 10 reusable reasoning patterns (Decomposition, Role Mesh, Counter-Case Probing, etc.)
- **[Evaluation Rubric](docs/evaluation.md)** - Score your prompts on 6 axes (Goal Fit, Reasoning Quality, etc.)
- **[Workflow Guide](docs/workflow.md)** - How to store, version, and share prompts
- **[FAQ](docs/faq.md)** - Common questions and troubleshooting

### Advanced Topics
- **[Mental Model](docs/mental-model.md)** - Deep dive into the cognitive architecture
- **[Template](docs/template.md)** - Complete canonical template with examples

---

## Why Use This Framework?

Superprompts work for any task where you need structured thinking:

- **Coaching & Facilitation:** Reflection sessions, team retrospectives, 1-on-1 conversations
- **Strategic Thinking:** Business opportunity evaluation, risk assessment, decision-making  
- **Knowledge Work:** Research synthesis, documentation cleanup, content creation
- **Technical Work:** Code review, test case generation, architecture planning
- **Creative Work:** Style adaptation, perspective shifts, iterative refinement

### Key Benefits

- **Predictability:** Control what the model thinks about, how it thinks, and what it produces
- **Reusability:** Replace specifics with placeholders to use across contexts
- **Debuggability:** Use the evaluation rubric to identify and fix weak prompts
- **Tool-agnostic:** Works across Claude, GPT, Gemini, Llama, and coding tools like Cursor

---

## Contributing

This is an open framework. Contributions are welcome!

**How to contribute:**
1. Fork the repository
2. Create a branch: `git checkout -b feat/your-prompt-name`
3. Add your prompt to `/examples` or pattern to `/docs/patterns.md`
4. Update [PROMPTS.md](PROMPTS.md) with tags and description
5. Commit with a conventional message: `git commit -m "feat: Add [description]"`
6. Open a pull request

See the [workflow guide](docs/workflow.md) for detailed instructions.

---

## License

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

---

## Author

**Steff Vanhaverbeke** – AI Adoption Coach & Co-founder, The House of Coaching

I help professionals and teams build the uniquely human capabilities that matter most in an AI-driven world. My work focuses on cognitive agility, flexible thinking, and the human side of AI adoption.

- 🌐 Website: [coachsteff.live](https://coachsteff.live)
- 📧 Email: [steff@coachsteff.live](mailto:steff@coachsteff.live)
- 💼 LinkedIn: [steffvanhaverbeke](https://linkedin.com/in/steffvanhaverbeke)
- 🐦 Twitter: [@coachsteff](https://twitter.com/coachsteff)

---

*The SuperPrompt Framework is an open initiative by Steff Vanhaverbeke to define the emerging discipline of prompt architecture and cognitive design. It's a living system—use it, adapt it, and contribute back.*
