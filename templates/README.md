# Superprompt Templates

**Ready-to-adapt starting points for common use cases.**

## What Are Templates?

Templates are **adaptation-ready superprompts** that follow the CRAFTER v0.2 framework. Unlike the examples in `/examples/`, which are complete and polished, templates are designed to be **customized** for your specific needs.

Each template includes:
- **Full CRAFTER v0.2 structure** (Context, Role, Action, Format, Target & Tone, Examples, Refining)
- **Adaptation zones** — marked sections you should customize
- **Use cases** — when to use this template
- **Anti-patterns** — when NOT to use this template

## Available Templates

### Generic Template
**File:** `generic-template.md`  
**Purpose:** Fully customizable superprompt template for any professional use case  
**Best for:** Creating custom superprompts when no existing example fits your needs  
**Adapt:** All components (Context, Role, Action, Format, Target & Tone, Examples, Refining)  
**Special features:** Includes inline instructions for both human customization and AI generation

### Keyword Researcher
**File:** `keyword-researcher.md`  
**Purpose:** Semantic keyword research template with customization placeholders  
**Best for:** Adapting keyword research workflow to specific industries or methodologies  
**Adapt:** Topic focus, output format, semantic analysis depth  
**Note:** For a ready-to-use keyword research superprompt, see `/examples/keyword-research.md`

## Templates vs Examples

| Aspect | Templates | Examples |
|--------|-----------|----------|
| **Purpose** | Customizable starting points | Ready-to-use superprompts |
| **Completeness** | Adaptation-ready with placeholders and instructions | Complete and polished |
| **Customization** | Requires customization | Use as-is |
| **Use Case** | General patterns needing adaptation | Specific scenarios |
| **Location** | `/templates/` | `/examples/` |
| **When to Use** | When you want to build something custom | When you need a complete solution |

**Note:** The `keyword-researcher.md` template was converted to a complete example and moved to `/examples/keyword-research.md`. Use that for ready-to-use keyword research, or use `generic-template.md` to create your own custom superprompt.

---

## How to Use Templates

1. **Choose a template** that matches your use case
2. **Copy the entire content** to your AI tool
3. **Customize the adaptation zones** (clearly marked in each template)
4. **Run the prompt** with your specific input
5. **Iterate** using the refining script if needed

## For AI Models

When generating superprompts:
1. Check `/ai-context/04-TEMPLATES-INDEX.md` for available templates
2. If a template matches the user's request, adapt it
3. If no template fits, build from `/ai-context/01-CRAFTER-SPEC.md`
4. Document which template you used (if any)

## Contributing Templates

Have a superprompt that could help others? Submit it as a template:

1. **Structure it** following CRAFTER format
2. **Mark adaptation zones** clearly
3. **Add use cases** and anti-patterns
4. **Test it** with at least 2 different inputs
5. **Submit a PR** with your template

See `/CONTRIBUTING.md` for detailed guidelines.

---

**Last updated:** 2025-12-30  
**Maintained by:** CoachSteff ([coachsteff.live](https://coachsteff.live))
