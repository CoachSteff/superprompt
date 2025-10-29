# AGENTS.md

> **For AI Coding Agents**: Development guide for the SuperPrompt Framework repository

---

## Build & Test

### Quick Start

```bash
# Clone the repository
git clone https://github.com/CoachSteff/superprompt-framework.git
cd superprompt-framework

# Install dependencies (if Node.js tooling added in future)
npm install

# Currently no automated tests (documentation-focused framework)
# Manual validation: Review markdown files for consistency
```

### Development Commands

```bash
# Placeholder for future build process
npm run build

# Placeholder for future development server
npm run dev

# Run tests (not yet implemented)
npm test
```

**Current State**: This is a documentation and framework repository. There are no compiled artifacts or test suites yet. Development primarily involves:
- Writing and editing markdown files
- Maintaining documentation consistency
- Validating framework specifications
- Managing example prompts

---

## Architecture Overview

### Repository Structure

```
superprompt-framework/
├── .cursor/                    # Multi-agent AI system
│   ├── agents/                 # 7 specialized AI agents
│   │   ├── orchestrator/       # Central coordinator
│   │   ├── concierge/          # Contributor onboarding
│   │   ├── triage/             # Issue categorization
│   │   ├── lifecycle/          # PR validation
│   │   ├── scribe/             # Documentation maintenance
│   │   ├── community/          # Community health
│   │   └── repository-manager/ # Repository administration
│   ├── shared-context/         # Agent coordination
│   │   ├── guiding-principles.md
│   │   └── communication-protocols.md
│   └── GETTING_STARTED.md
│
├── ai-context/                 # AI-executable instructions (for framework USAGE)
│   ├── 01-CRAFTER-SPEC.md      # Framework specification
│   ├── 02-EXECUTION-PROTOCOL.md
│   ├── 03-CONSTRAINT-RULES.md
│   ├── 04-TEMPLATES-INDEX.md
│   ├── 05-VALIDATION-CHECKLIST.md
│   └── README.md
│
├── docs/                       # Human-readable documentation
│   ├── mental-model.md
│   ├── template.md
│   ├── patterns.md
│   ├── evaluation.md
│   ├── workflow.md
│   ├── quick-start.md
│   └── faq.md
│
├── examples/                   # Sample superprompts
│   ├── coaching-reflection.md
│   ├── team-retrospective.md
│   ├── opportunity-scan.md
│   ├── documentation-cleanup.md
│   └── research-synthesis.md
│
├── templates/                  # Reusable prompt templates
│   └── keyword-researcher.md
│
├── .github/                    # GitHub configuration
│   ├── workflows/              # CI/CD (future)
│   └── ISSUE_TEMPLATE/
│
├── README.md                   # AI-first instructions + human guide pointer
├── CONTRIBUTING.md             # Contribution guidelines
├── PROMPTS.md                  # Searchable prompt index
└── package.json                # Project metadata
```

### Multi-Agent System

This repository is **actively managed** by a sophisticated multi-agent AI system located in `.cursor/agents/`. Each agent has specific responsibilities:

| Agent | Domain | Key Functions |
|-------|--------|---------------|
| **Orchestrator** | Coordination | Routes tasks, coordinates agents, manages workflow |
| **Contributor Concierge** | Onboarding | Welcomes new contributors, provides guidance |
| **Triage & Prioritization** | Issue Management | Labels issues, assesses priority, categorizes |
| **Contribution Lifecycle** | PR Review | Validates PRs, runs checks, provides feedback |
| **Scribe & Archivist** | Documentation | Maintains docs, ensures consistency, generates content |
| **Community Health** | Community | Monitors engagement, enforces Code of Conduct |
| **Repository Manager** | Administration | Manages releases, configuration, statistics |

**CRITICAL**: When working in this repository:
- ✅ Read `.cursor/agents/README.md` to understand the agent system
- ✅ Respect agent domains (don't duplicate their work)
- ✅ Coordinate changes that affect multiple agents
- ⚠️ Do NOT modify `.cursor/agents/` files without explicit permission

**Agent commands** (for reference, not to execute):
- `/agent find-gfi` - Mark as good first issue
- `/agent summarize` - Generate PR summary
- `/agent draft-docs` - Generate documentation
- `/agent fix this` - Attempt autonomous bug fix
- `/agent prepare-release [version]` - Prepare release

---

## Security

### Sensitive Information

**NO credentials should ever be committed:**
- ❌ API keys or tokens
- ❌ Email addresses (except in CONTRIBUTING.md and LICENSE)
- ❌ Personal access tokens
- ❌ Private repository URLs

**Safe patterns:**
- ✅ Use environment variables (document in `.env.example`)
- ✅ Reference secrets generically ("your API key")
- ✅ Link to documentation for credential setup

### Content Safety

This framework is used across GenAI tools (Claude, ChatGPT, Gemini, etc.):
- ⚠️ Examples must be professional and appropriate
- ⚠️ Avoid controversial topics in sample prompts
- ⚠️ Ensure all examples follow ethical AI practices
- ⚠️ Test prompts for bias and fairness

### Data Privacy

- No personally identifiable information (PII) in examples
- Use fictional names and scenarios
- Sanitize any real-world data used for testing

---

## Git Workflows

### Branching Strategy

```
main              # Production-ready, stable releases
├── feat/*        # New features (feat/add-pattern-library)
├── fix/*         # Bug fixes (fix/broken-link-in-readme)
├── docs/*        # Documentation updates (docs/clarify-crafter)
├── refactor/*    # Code restructuring (refactor/reorganize-examples)
└── chore/*       # Maintenance tasks (chore/update-dependencies)
```

### Branch Naming

```bash
# Feature branches
git checkout -b feat/add-synthesis-pattern

# Bug fixes
git checkout -b fix/validation-checklist-typo

# Documentation
git checkout -b docs/expand-quick-start-guide

# Refactoring
git checkout -b refactor/simplify-agent-structure
```

### Commit Message Format

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <brief description>

<optional detailed description>

<optional footer with references>
```

**Types:**
- `feat`: New feature or capability
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Formatting, whitespace, etc.
- `refactor`: Code restructuring without behavior change
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

**Examples:**

```bash
# Good commits
git commit -m "feat(patterns): add counter-case probing pattern"
git commit -m "fix(validation): correct CRAFTER acronym interpretation"
git commit -m "docs(readme): clarify multi-agent system purpose"

# Detailed commit
git commit -m "feat(templates): add keyword researcher template

- Complete CRAFTER structure
- Examples for semantic clustering
- Integration with existing patterns
- Attribution footer included

Closes #42"
```

### Pull Request Requirements

Before submitting a PR:

1. **Branch is up to date** with `main`
2. **Commit messages** follow convention
3. **Documentation updated** if adding features
4. **Examples tested** manually (no automated tests yet)
5. **PROMPTS.md updated** if adding new prompts
6. **Attribution preserved** (CC-BY 4.0 footer)

**PR Title Format:**
```
feat: Add counter-case probing pattern
fix: Correct CRAFTER acronym in README.md
docs: Expand FAQ with agent system questions
```

**Lifecycle Agent will automatically:**
- Validate PR structure
- Check for documentation updates
- Verify attribution footers
- Run consistency checks

---

## Conventions & Patterns

### File Organization

#### Markdown Files

**Location rules:**
- `/docs/` - Human-readable guides and explanations
- `/ai-context/` - Machine-executable instructions (framework usage)
- `/examples/` - Complete, copy-ready superprompts
- `/templates/` - Reusable prompt templates with placeholders

**Naming conventions:**
- Use `kebab-case.md` for all files
- Be descriptive: `counter-case-probing.md` not `ccp.md`
- Group related files in subdirectories

#### CRAFTER Superprompts

**Every example must include:**

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
[Concrete steps, numbered]

### F – Format
[Output structure]

### T – Target Audience
[Who this is for]

### E – Examples (optional)
[Input/output demonstrations]

### R – Refining (optional)
[Iteration instructions]

---

**Framework:** CoachSteff's CRAFTER (SuperPrompt Framework v0.1)
**Pattern Used:** [Pattern name if applicable]
**License:** CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

**Attribution is MANDATORY** - do not omit the footer.

### Code Style (for future JavaScript/TypeScript)

When code is added:

```javascript
// Use clear, descriptive names
function validateCrafterStructure(prompt) {
  // Implementation
}

// JSDoc for all exported functions
/**
 * Validates that a prompt follows CRAFTER structure
 * @param {string} prompt - The prompt text to validate
 * @returns {Object} Validation result with errors array
 */
```

### Documentation Style

**Tone:**
- Clear and direct (avoid jargon)
- Professional but approachable
- Action-oriented (tell readers what to do)

**Formatting:**
- Use headers consistently (`#`, `##`, `###`)
- Code blocks with language hints: ` ```bash `
- Tables for comparisons
- Bullet lists for steps or options
- Bold for emphasis, not italics

**Links:**
- Relative paths for internal: `[see docs](docs/patterns.md)`
- Full URLs for external: `[Conventional Commits](https://www.conventionalcommits.org/)`
- Always use descriptive link text, not "click here"

### Multi-Agent Coordination

**When modifying files that agents interact with:**

1. **Read agent instructions first**: `.cursor/agents/[agent-name]/instructions.md`
2. **Check shared context**: `.cursor/shared-context/guiding-principles.md`
3. **Test agent behavior** after changes (manually trigger agent commands)
4. **Update agent documentation** if changing their domain

**Files agents depend on:**
- `README.md` - Scribe Agent references this
- `CONTRIBUTING.md` - Concierge Agent uses for onboarding
- `PROMPTS.md` - Scribe Agent maintains this index
- `.github/ISSUE_TEMPLATE/` - Triage Agent categorizes with these
- `CHANGELOG.md` - Repository Manager generates this

**Coordination example:**

If you add a new superprompt:
1. Create the file in `/examples/`
2. Update `/PROMPTS.md` with tags and description (Scribe Agent watches this)
3. Consider if it needs a template version in `/templates/`
4. Ensure attribution footer is present (Lifecycle Agent validates)

---

## Framework-Specific Considerations

### The Dual Nature of This Repository

This repository serves **two distinct purposes**:

1. **Framework Definition** (Development)
   - CRAFTER specification and documentation
   - Pattern library and examples
   - Multi-agent system for repository management
   - **YOU ARE HERE** when working on the framework itself

2. **Framework Usage** (Consumption)
   - AI models read `README.md` to learn CRAFTER
   - GenAI tools use `/ai-context/` files to generate prompts
   - Users copy `/examples/` and `/templates/` for their work
   - Governed by `README.md`, not `AGENTS.md`

**This file (AGENTS.md)** is for developers **building the framework**.

**README.md** is for AI models **using the framework**.

### CRAFTER Acronym Integrity

**CRITICAL**: The CRAFTER acronym is canonical and MUST NOT be changed:

```
C = Context (NOT "Capture")
R = Role (NOT "Review")
A = Action (NOT "Analyze", NOT "Audience")
F = Format (NOT "Focus")
T = Target audience (NOT "Topic", NOT "Tone")
E = Examples (NOT "Evolve")
R = Refining (NOT "Reprompt", NOT "Restrictions")
```

**When adding or editing content:**
- ✅ Use exact definitions from `/ai-context/01-CRAFTER-SPEC.md`
- ✅ Cross-reference when clarifying components
- ❌ Do NOT create alternative interpretations
- ❌ Do NOT merge with other frameworks (CREATE, PROMPT, etc.)

**If you find an inconsistency:**
1. Open an issue with `inconsistency` label
2. Reference the conflicting locations
3. Propose correction based on canonical spec

### Documentation Synchronization

**Files that must stay synchronized:**

| Change In | Must Update |
|-----------|-------------|
| `/ai-context/01-CRAFTER-SPEC.md` | `README.md` |
| `/examples/*.md` | `PROMPTS.md` index |
| `/docs/patterns.md` | Related examples in `/examples/` |
| New agent in `.cursor/agents/` | `.cursorrules`, agent README |

**Validation checklist** (before committing):
- [ ] CRAFTER definitions consistent across all files
- [ ] Attribution footers present on all examples
- [ ] PROMPTS.md index updated for new prompts
- [ ] README.md reflects new features or changes
- [ ] Agent documentation updated if domains changed

### Pattern Development

**When adding a new pattern to `/docs/patterns.md`:**

1. **Define the pattern clearly**:
   - Name (verb + noun: "Counter-Case Probing")
   - Purpose (what problem it solves)
   - When to use (context and triggers)
   - How to use (step-by-step)

2. **Create a complete example**:
   - Add to `/examples/` with full CRAFTER structure
   - Include real-world scenario (not toy example)
   - Show pattern in action

3. **Update the index**:
   - Add to `PROMPTS.md` with tags
   - Link from `/docs/patterns.md` to example
   - Cross-reference related patterns

4. **Consider template version**:
   - If pattern is reusable, create template in `/templates/`
   - Use placeholders: `[YOUR DOMAIN]`, `[TARGET AUDIENCE]`

---

## Testing Strategy

**Current State**: No automated testing (documentation framework)

**Manual validation checklist**:

### For Documentation Changes

- [ ] Markdown renders correctly on GitHub
- [ ] All links work (internal and external)
- [ ] Code blocks have language hints
- [ ] Tables display properly
- [ ] Headers use consistent hierarchy

### For New Prompts

- [ ] Follows CRAFTER structure exactly
- [ ] Attribution footer present
- [ ] Listed in PROMPTS.md
- [ ] Examples are clear and actionable
- [ ] No sensitive information

### For Agent System Changes

- [ ] Agent still responds to commands
- [ ] Instructions are clear and unambiguous
- [ ] Shared context is synchronized
- [ ] .cursorrules reflects changes

**Future automated tests** (when implemented):
```bash
npm test                    # Run all tests
npm run test:lint           # Markdown linting
npm run test:links          # Validate all links
npm run test:structure      # Check CRAFTER compliance
npm run test:agents         # Agent behavior tests
```

---

## Common Development Tasks

### Adding a New Example Superprompt

```bash
# 1. Create the example file
touch examples/my-new-prompt.md

# 2. Write the prompt following CRAFTER structure
# (Include attribution footer!)

# 3. Update the index
# Add entry to PROMPTS.md with tags

# 4. Commit with convention
git add examples/my-new-prompt.md PROMPTS.md
git commit -m "feat(examples): add my-new-prompt

- Complete CRAFTER structure
- Real-world use case
- Attribution included

Related: #123"

# 5. Push and create PR
git push origin feat/add-my-new-prompt
```

### Updating Documentation

```bash
# 1. Identify what needs to change
# Check if it affects other files

# 2. Make changes in correct location
# /docs/ for humans, /ai-context/ for machines

# 3. Verify synchronization
# Update README if needed

# 4. Commit
git commit -m "docs(quick-start): clarify installation steps"
```

### Fixing CRAFTER Inconsistency

```bash
# 1. Find all occurrences
grep -r "T = Tone" .

# 2. Fix to canonical definition
# T = Target audience

# 3. Update affected files
git add ai-context/01-CRAFTER-SPEC.md docs/mental-model.md

# 4. Commit with context
git commit -m "fix(spec): correct CRAFTER T component

Changed 'T = Tone' to 'T = Target audience' across:
- ai-context/01-CRAFTER-SPEC.md
- docs/mental-model.md

Ensures consistency with canonical specification."
```

### Working with the Agent System

```bash
# 1. Read agent documentation first
cat .cursor/agents/[agent-name]/instructions.md

# 2. Understand their domain
# Check what tasks they handle automatically

# 3. Make your changes
# Avoid duplicating agent functionality

# 4. Update agent docs if needed
# Only if their domain or behavior changes

# 5. Test agent still works
# Manually trigger agent commands or wait for automation
```

---

## Troubleshooting

### Common Issues

**Issue**: PR fails validation
- **Check**: Attribution footer present on all prompts
- **Check**: CRAFTER structure follows canonical spec
- **Check**: Commit messages follow convention

**Issue**: Documentation out of sync
- **Solution**: Use search to find all references
- **Solution**: Update all locations simultaneously
- **Solution**: Create issue to track if extensive

**Issue**: Agent doesn't respond to command
- **Check**: `.cursor/agents/[agent]/instructions.md` is correct
- **Check**: Shared context files are valid
- **Check**: Command syntax is correct

**Issue**: CRAFTER definitions inconsistent
- **Source of truth**: `/ai-context/01-CRAFTER-SPEC.md`
- **Fix**: Update all conflicting locations
- **Prevent**: Add to validation checklist

### Getting Help

1. **Check documentation**:
   - This file for development workflows
   - `CONTRIBUTING.md` for contribution guidelines
   - `.cursor/agents/README.md` for agent system

2. **Search issues**:
   - Existing issues might have solutions
   - Use labels to filter relevant discussions

3. **Ask in discussions**:
   - General questions about architecture
   - Clarifications on conventions
   - Proposals for improvements

4. **Contact maintainers**:
   - Email: steff@coachsteff.live
   - For urgent or sensitive issues

---

## For AI Coding Agents

### Quick Context Summary

**Repository purpose**: Framework for AI prompt engineering (CRAFTER methodology)

**Your role**: Help developers build and improve the framework itself (NOT use it for prompt generation)

**Key constraints**:
- Maintain CRAFTER specification integrity
- Preserve attribution footers (CC-BY 4.0)
- Coordinate with 7 specialized agents in `.cursor/agents/`
- Keep documentation synchronized
- Follow conventional commits

**When in doubt**:
1. Read `/ai-context/01-CRAFTER-SPEC.md` for canonical definitions
2. Check `.cursorrules` for agent coordination
3. Reference `CONTRIBUTING.md` for human processes
4. Ask for clarification rather than assume

**Do NOT**:
- Modify `.cursor/agents/` files without permission
- Change CRAFTER acronym definitions
- Remove attribution footers
- Create alternative framework interpretations
- Duplicate agent functionality

---

## Version & Maintenance

**Framework Version**: v1.0.0
**AGENTS.md Version**: 1.0
**Last Updated**: 2025-10-26

**Review triggers**:
- Major framework updates (CRAFTER changes)
- New agents added to system
- Development tooling added (tests, build process)
- Community feedback on development experience

**Maintainer**: Steff Vanhaverbeke ([coachsteff.live](https://coachsteff.live))

---

**Next Steps:**
- Read `CONTRIBUTING.md` for contribution workflow
- Explore `.cursor/agents/README.md` for agent system details
- Review `README.md` to understand framework usage
- Check `PROMPTS.md` for example superprompts

**Questions?** Open a discussion or issue.
