# AI Model Compatibility Guide

**Framework:** CoachSteff's CRAFTER (SuperPrompt Framework v0.1)

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

### Layer 2: AI_INSTRUCTIONS.md
**For models with partial file access**

Full execution protocol, validation checklist, and attribution requirements.

### Layer 3: /ai-context/ Directory
**For models with full file access**

Complete framework specifications, execution protocols, constraint rules, and validation checklists.

---

## Model Performance Tiers

Based on testing across platforms, here's what to expect:

### 🥇 **Tier 1: Full Integration**
**Models:** Perplexity, Claude with Projects

**Capabilities:**
- Accesses all three layers (README + AI_INSTRUCTIONS + /ai-context/)
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

**Diagnostic question:** "Did you read AI_INSTRUCTIONS.md and /ai-context/01-CRAFTER-SPEC.md?"

**If no:** Paste the contents of AI_INSTRUCTIONS.md directly in chat

**If yes but still wrong:** Use the Framework Fidelity Self-Test from AI_INSTRUCTIONS.md

---

### Model invents its own framework

**Common issue:** Model interprets CRAFTER differently (e.g., as "Capture-Review-Analyze-Focus-Tailor-Evolve-Reprompt")

**Solution:** Paste this explicit correction:

```
CRITICAL CORRECTION:

In CoachSteff's CRAFTER framework:
C = Context (not Capture)
R = Role (not Review)
A = Action (not Analyze)
F = Format (not Focus)
T = Target audience (not Topic, not Tone, not Tailor)
E = Examples (not Evolve)
R = Refining (not Reprompt)

DO NOT invent your own CRAFTER interpretation.
Use the exact definitions from ai-context/01-CRAFTER-SPEC.md
```

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

## Attribution Enforcement

**All outputs should include:**

```
Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.1)
Pattern Used: [Pattern name if applicable]
License: CC-BY 4.0 — Attribution: Steff Vanhaverbeke (coachsteff.live)
```

**If missing:** Remind the model to include attribution per AI_INSTRUCTIONS.md requirements.

---

## Summary

**Simple version:** Different models need different entry points, but all can use the framework. Tier 1 models give best results. Tier 2-3 models need more guidance but still work.

**Progressive enhancement works:**
- README → Basic functionality (all models)
- AI_INSTRUCTIONS → Better compliance (Tier 2+)
- /ai-context/ → Full fidelity (Tier 1)

---

**Need more detail?** See the main [README](../README.md) or explore [/docs](.) and [/ai-context](../ai-context/) directories.
