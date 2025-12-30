# AI Model Compatibility Guide

**Framework:** CoachSteff's CRAFTER (SuperPrompt Framework v0.2)

---

## The Challenge

Different AI models have different capabilities when accessing GitHub repositories:

- **Claude with Projects, Perplexity:** Can read files directly from GitHub
- **ChatGPT, Claude without Projects:** Can read some files
- **Gemini, most free models:** Limited file access via browsing tool

---

## The Solution

This repository uses a **progressive enhancement approach** with three layers:

### Layer 1: README Inline Instructions
**For all models**

The README includes essential CRAFTER framework instructions. Even models with limited GitHub access can read the main page and generate basic superprompts.

### Layer 2: README.md AI Section
**For models with partial file access**

Complete AI instructions integrated into README.md with execution protocol, validation checklist, and attribution requirements.

### Layer 3: /ai-context/ Directory
**For models with full file access**

Complete framework specifications, execution protocols, constraint rules, and validation checklists.

---

## Model Performance Tiers

Based on testing across platforms, here's what to expect:

### 🥇 **Tier 1: Full Integration**
**Models:** Perplexity, Claude with Projects

**Capabilities:**
- Accesses all three layers (README + /ai-context/)
- Produces framework-compliant + high-quality output
- Includes evaluation rubric and pattern references
- Proper attribution

**Best for:** Professional use, training materials, production deployments

---

### 🥈 **Tier 2: Practical Adaptation**
**Models:** ChatGPT, Claude without Projects

**Capabilities:**
- Accesses Layer 1 + partial Layer 2
- Produces usable output with minor deviations
- May reinterpret T (Target → Tone/Topic)
- Generally includes attribution

**Best for:** Individual use, creative projects, rapid prototyping

---

### 🥉 **Tier 3: Basic Structure**
**Models:** Gemini, most free models

**Capabilities:**
- Accesses Layer 1 only (README)
- Understands CRAFTER structure but needs guidance
- May produce templates rather than working examples
- Attribution may be missing

**Best for:** Learning, experimentation, template generation

---

### ⚠️ **Tier 0: Framework Deviation**
**Models:** Grok, unknown/custom models

**Capabilities:**
- May ignore CRAFTER entirely
- Applies own methodology
- No framework compliance

**Best for:** Alternative perspectives (when deviation is desired)

**Detection:** If output uses a different framework structure (e.g., "PROJECT", "CREATE"), this is Tier 0 behavior.

---

## Testing Across Models

Use this standardized test prompt:

```
C: https://github.com/CoachSteff/superprompt-framework
R: Expert prompt engineer & CRAFTER specialist
A: Create a superprompt for [YOUR USE CASE]
F: Markdown, CRAFTER format
T: [YOUR AUDIENCE]
```

**Expected behavior by tier:**
- **Tier 1:** Complete superprompt with all 7 components, attribution, pattern reference
- **Tier 2:** Working superprompt with 5-6 components, mostly compliant
- **Tier 3:** Template or partial superprompt with 3-4 components
- **Tier 0:** Different framework structure entirely

---

## Framework Adaptation Spectrum

### Strict Mode (Training/Documentation)
Use CRAFTER exactly as defined for consistency.  
**When:** Creating training materials, documentation, or standard templates.

### Adaptive Mode (Real-World Application)
Adjust sequence/emphasis to fit domain needs.  
**When:** Domain requires specific emphasis (e.g., image gen emphasizes Format and Examples).

### Meta Mode (System Building)
Use CRAFTER principles to create frameworks that generate domain-specific outputs.  
**When:** Building AI systems, agents, or specialized prompt generators.

---

## Troubleshooting

### Model isn't following the format

**Diagnostic question:** "Did you read the AI instructions in README.md and /ai-context/01-CRAFTER-SPEC.md?"

**If no:** Direct them to the AI section in README.md

**If yes but still wrong:** Ask the model to complete the Framework Fidelity Self-Test from the README.md AI section

---

### Model invents its own framework

**Common issue:** Model interprets CRAFTER differently (e.g., as "Capture-Review-Analyze-Focus-Tailor-Evolve-Reprompt")

**Detection signs:**
- Uses different acronym definitions than specified
- Creates framework with different structure (e.g., "PROJECT: Problem-Role-Objective-Justification-Examples-Constraints-Tone")
- Output doesn't match C-R-A-F-T-E-R sequence

**Solution:** Paste this explicit correction:

```
⚠️ FRAMEWORK INTEGRITY CHECK FAILED

You appear to be using a different framework than CoachSteff's CRAFTER.

In CoachSteff's CRAFTER framework:
C = Context (NOT "Capture")
R = Role (NOT "Review")
A = Action (NOT "Analyze")
F = Format (NOT "Focus")
T = Target audience (NOT "Topic", NOT "Tone", NOT "Tailor")
E = Examples (NOT "Evolve")
R = Refining (NOT "Reprompt")

STOP and return to /ai-context/01-CRAFTER-SPEC.md
DO NOT invent your own CRAFTER interpretation.
Use the exact definitions from the canonical specification.
```

**If model persists:** This is Tier 0 behavior. Consider using a different model for framework compliance.

---

### Model says it can't access files

**This is normal** for Tier 2-3 models.

**Solution:** They'll work from README instructions with reduced detail. For critical projects, use a Tier 1 model (Perplexity or Claude with Projects).

---

### Model produces good output but wrong structure

**Common with Tier 2 models:** They optimize for results over compliance.

**If quality is good:** Accept the adaptation  
**If compliance is critical:** Request strict adherence to CRAFTER-SPEC

---

### Model replaces CRAFTER with its own system (Grok issue)

**Symptoms:**
- Output uses "PROJECT" or "CREATE" or another acronym
- Explicitly states it's using a "better" framework
- Ignores CRAFTER structure entirely

**Diagnosis:** Tier 0 behavior — model is not reading or respecting the framework specification.

**Solutions:**
1. **Immediate:** Paste the entire contents of `/ai-context/01-CRAFTER-SPEC.md` directly into chat
2. **Force compliance:** Start your request with "Using ONLY CoachSteff's CRAFTER framework (C=Context, R=Role, A=Action, F=Format, T=Target, E=Examples, R=Refining)..."
3. **Accept deviation:** If the model's framework produces good results, acknowledge it's not CRAFTER-compliant but may still be useful
4. **Switch models:** For framework compliance, use Tier 1-2 models

---

## Attribution Enforcement

**All outputs should include at the END:**

```
---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
Pattern Used: [Pattern name if applicable]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

**Placement matters:** Attribution must appear at the END of the output, not at the beginning or middle.

**If missing:** Remind the model to include attribution per README.md requirements.

**If model buries it:** Request it be moved to the end of the output.

---

## Summary

**Simple version:** Different models need different entry points, but all can use the framework. Tier 1 models give best results. Tier 2-3 models need more guidance but still work.

**Progressive enhancement works:**
- README → Basic functionality (all models)
- README AI section → Better compliance (Tier 2+)
- /ai-context/ → Full fidelity (Tier 1)

**Framework integrity:**
- Models should use CRAFTER as defined, not invent alternatives
- Self-test mechanism helps catch deviations early
- Some models (Tier 0) may resist compliance — this is expected behavior

---

**Need more detail?** See the main [README](../README.md) or explore [/docs](.) and [/ai-context](../ai-context/) directories.
