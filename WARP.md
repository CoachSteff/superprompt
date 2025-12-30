# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Repository Overview

The **SuperPrompt Framework** is a documentation-driven project that defines the **CRAFTER methodology** for AI prompt engineering. This is **not a traditional software project** — it's a framework specification repository with structured markdown documentation, examples, and a multi-agent management system.

**Key distinction:** This repository serves two audiences:
1. **Framework development** (you are here) — building/maintaining the framework itself
2. **Framework usage** — AI models using CRAFTER to generate prompts (governed by README.md)

## Multi-Agent System (CRITICAL)

This repository is actively managed by 7 specialized AI agents in `.cursor/agents/`:

| Agent | Domain |
|-------|--------|
| Orchestrator | Task routing and coordination |
| Contributor Concierge | New contributor onboarding |
| Triage & Prioritization | Issue labeling and categorization |
| Contribution Lifecycle | PR validation and review |
| Scribe & Archivist | Documentation maintenance |
| Community Health | Community monitoring |
| Repository Manager | Releases and configuration |

**⚠️ CRITICAL CONSTRAINTS:**
- **DO NOT modify** `.cursor/agents/` files without explicit permission
- **DO NOT duplicate** agent functionality (e.g., don't label issues, that's Triage Agent's job)
- **DO coordinate** changes that affect multiple agents
- Read `.cursor/agents/README.md` and `.cursor/shared-context/guiding-principles.md` before making changes

## Core Principles

All work in this repository follows five guiding principles:

1. **Augmentation over Automation** — Assist humans, never replace them. Defer architectural decisions to maintainers.
2. **Radical Transparency** — Explain reasoning, cite sources, acknowledge uncertainty.
3. **Community Over Code** — Prioritize community health over efficiency. Be welcoming and patient.
4. **Secure by Design** — Never generate secrets or credentials. Flag security concerns proactively.
5. **Meritocratic and Fair** — Provide consistent, high-quality assistance regardless of experience level.

## Development Workflow

### Currently No Automated Build/Test

This is a **documentation framework** with no compiled artifacts or automated tests yet.

**"Build" process:**
```bash
npm run build  # Currently echoes "Build process not yet implemented"
npm run dev    # Currently echoes "Development server not yet implemented"
npm test       # Currently echoes "Error: no test specified" && exit 1
```

### Manual Validation Workflow

When making changes:

1. **Verify markdown renders correctly** on GitHub
2. **Check all links** (internal and external)
3. **Ensure CRAFTER consistency** across all files
4. **Validate attribution footers** on all examples (required)
5. **Update PROMPTS.md index** if adding new examples
6. **Test superprompts manually** in target AI tools (Claude, GPT, etc.)

### Git Workflow

**Branch naming:**
```bash
feat/add-new-pattern
fix/broken-link-in-readme
docs/clarify-crafter-spec
refactor/reorganize-examples
chore/update-dependencies
```

**Commit message format** (Conventional Commits):
```bash
feat(examples): add counter-case probing pattern
fix(spec): correct CRAFTER T component definition
docs(readme): clarify multi-agent system purpose
```

**PR requirements:**
- Branch up to date with `main`
- Commit messages follow convention
- Documentation updated if adding features
- PROMPTS.md updated if adding new prompts
- Attribution preserved (CC-BY 4.0 footer)

## Architecture & Structure

### Repository Layout

```
superprompt/
├── .cursor/                    # Multi-agent system (READ-ONLY unless explicit permission)
│   ├── agents/                 # 7 specialized agents with instructions
│   └── shared-context/         # Agent coordination principles
│
├── ai-context/                 # AI-executable framework specification
│   ├── 01-CRAFTER-SPEC.md      # Canonical CRAFTER definitions (SOURCE OF TRUTH)
│   ├── 02-EXECUTION-PROTOCOL.md
│   ├── 03-CONSTRAINT-RULES.md
│   ├── 04-TEMPLATES-INDEX.md
│   └── 05-VALIDATION-CHECKLIST.md
│
├── docs/                       # Human-readable documentation
│   ├── mental-model.md
│   ├── patterns.md
│   ├── evaluation.md
│   ├── workflow.md
│   └── faq.md
│
├── examples/                   # Complete, copy-ready superprompts
│
├── templates/                  # Reusable prompt templates with placeholders
│
├── .github/                    # GitHub configuration and workflows
│
├── README.md                   # AI-first instructions + human guide pointer
├── CONTRIBUTING.md             # Contribution guidelines
└── PROMPTS.md                  # Searchable prompt index
```

### Key Architectural Concepts

#### 1. CRAFTER Framework (Non-Negotiable)

The **CRAFTER acronym is canonical** and MUST NOT be changed:

```
C = Context (NOT "Capture")
R = Role (NOT "Review")
A = Action (NOT "Analyze", NOT "Audience")
F = Format (NOT "Focus")
T = Target & Tone (NOT "Topic", NOT just "Tone")
E = Examples (NOT "Evolve")
R = Refining (NOT "Reprompt", NOT "Restrictions")
```

**Source of Truth:** `/ai-context/01-CRAFTER-SPEC.md`

When encountering inconsistencies:
1. Open an issue with `inconsistency` label
2. Reference conflicting locations
3. Propose correction based on canonical spec

#### 2. Documentation Synchronization

Files that must stay synchronized:

| Change In | Must Update |
|-----------|-------------|
| `/ai-context/01-CRAFTER-SPEC.md` | `README.md` |
| `/examples/*.md` | `PROMPTS.md` index |
| `/docs/patterns.md` | Related examples in `/examples/` |
| New agent in `.cursor/agents/` | `.cursorrules`, agent README |

#### 3. Attribution Requirements (MANDATORY)

Every superprompt in `/examples/` and `/templates/` MUST include:

```markdown
---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
Pattern Used: [pattern name if applicable]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

**DO NOT omit** this footer. It's required by CC-BY 4.0 license.

## Common Development Tasks

### Adding a New Example Superprompt

```bash
# 1. Create the example file
touch examples/my-new-prompt.md

# 2. Write prompt following CRAFTER structure (include attribution footer!)

# 3. Update PROMPTS.md with tags and description

# 4. Commit with convention
git add examples/my-new-prompt.md PROMPTS.md
git commit -m "feat(examples): add my-new-prompt

- Complete CRAFTER structure
- Real-world use case
- Attribution included

Related: #123"
```

### Updating Documentation

When modifying docs:
1. Identify if it affects other files (check synchronization table above)
2. Make changes in correct location (`/docs/` for humans, `/ai-context/` for machines)
3. Verify CRAFTER definitions remain consistent
4. Update README.md if needed

### Fixing CRAFTER Inconsistencies

```bash
# 1. Find all occurrences
grep -r "T = Tone" .

# 2. Fix to canonical definition (T = Target & Tone)

# 3. Update affected files and commit
git commit -m "fix(spec): correct CRAFTER T component

Changed 'T = Tone' to 'T = Target & Tone' across:
- ai-context/01-CRAFTER-SPEC.md
- docs/mental-model.md

Ensures consistency with canonical specification."
```

### Working with Patterns

When adding a new pattern to `/docs/patterns.md`:

1. **Define clearly:** Name, purpose, when to use, how to use
2. **Create complete example** in `/examples/` with full CRAFTER structure
3. **Update index:** Add to `PROMPTS.md` with tags
4. **Consider template version** in `/templates/` if reusable

## Security & Sensitive Information

**NEVER commit:**
- API keys or tokens
- Email addresses (except in CONTRIBUTING.md and LICENSE)
- Personal access tokens
- Private repository URLs

**Content safety:**
- Examples must be professional and appropriate
- Avoid controversial topics in sample prompts
- Ensure ethical AI practices in all examples
- Test prompts for bias and fairness
- No personally identifiable information (PII) in examples

## File Location Rules

**Human-readable guides** → `/docs/`
**Machine-executable instructions** → `/ai-context/`
**Complete superprompts** → `/examples/`
**Reusable templates** → `/templates/`

**Naming convention:** Use `kebab-case.md` for all files

## CRAFTER Superprompt Structure

Every example MUST include:

```markdown
# [Prompt Title]

## Purpose
[What this prompt does]

## CRAFTER Structure

### C – Context
[Environment and constraints]

### R – Role
[Expertise and perspective]

### A – Action
[Concrete numbered steps]

### F – Format
[Output structure]

### T – Target & Tone
**Target:** [Audience with characteristics]
**Tone:** [Communication approach suited to audience]

### E – Examples (optional)
[Input/output demonstrations]

### R – Refining (optional)
[Iteration instructions]

---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
Pattern Used: [Pattern name if applicable]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

## Agent Coordination

When modifying files that agents interact with:

1. **Read agent instructions first:** `.cursor/agents/[agent-name]/instructions.md`
2. **Check shared context:** `.cursor/shared-context/guiding-principles.md`
3. **Test agent behavior** after changes (manually trigger if possible)
4. **Update agent documentation** if changing their domain

**Files agents depend on:**
- `README.md` — Scribe Agent references
- `CONTRIBUTING.md` — Concierge Agent uses for onboarding
- `PROMPTS.md` — Scribe Agent maintains index
- `.github/ISSUE_TEMPLATE/` — Triage Agent categorizes
- `CHANGELOG.md` — Repository Manager generates

## Validation Checklist

Before committing:

- [ ] CRAFTER definitions consistent across all files
- [ ] Attribution footers present on all examples
- [ ] PROMPTS.md index updated for new prompts
- [ ] README.md reflects new features or changes
- [ ] Agent documentation updated if domains changed
- [ ] No sensitive information included
- [ ] Links work (internal and external)
- [ ] Markdown renders correctly

## Common Pitfalls

❌ **Don't:**
- Change CRAFTER acronym definitions
- Remove attribution footers
- Modify `.cursor/agents/` without permission
- Create alternative framework interpretations
- Duplicate agent functionality
- Commit secrets or credentials
- Use condescending language ("just do X", "simply Y")

✅ **Do:**
- Reference canonical spec (`/ai-context/01-CRAFTER-SPEC.md`)
- Maintain documentation synchronization
- Follow conventional commit format
- Include attribution on all examples
- Coordinate with agent system
- Be welcoming and patient

## Getting Help

1. **Check documentation:**
   - This file for development workflows
   - `CONTRIBUTING.md` for contribution guidelines
   - `.cursor/agents/README.md` for agent system

2. **Search existing issues** for similar problems

3. **Contact maintainer:**
   - Email: steff@coachsteff.live
   - For urgent or sensitive issues

## Project Metadata

- **License:** CC-BY 4.0 (Creative Commons Attribution 4.0 International)
- **Framework Version:** v1.0.0
- **Language:** Markdown (documentation framework, no compiled code)
- **Node.js:** >= 14.0.0 (for future tooling)
- **Repository:** https://github.com/CoachSteff/superprompt

## Version Control Commits

Include co-author line when committing on behalf of user:
```
Co-Authored-By: Warp <agent@warp.dev>
```

---

**For AI Agents:**

This is a framework definition project, not a traditional codebase. Your role is to help maintain the framework **itself**, not use it for prompt generation. Key constraints:
- Maintain CRAFTER specification integrity
- Preserve attribution footers
- Coordinate with specialized agents in `.cursor/agents/`
- Keep documentation synchronized
- Follow conventional commits

When in doubt: Read `/ai-context/01-CRAFTER-SPEC.md` for canonical definitions.
