# Quick Reference: Cross-Model AI Access

## The Problem We Solved

Different AI models have different capabilities for accessing GitHub files. This repository now uses a **three-layer accessibility strategy** to ensure all models can work with the SuperPrompt Framework.

---

## Three Access Layers

### 🟢 Layer 1: README Inline Instructions
**Accessible to:** All models (Gemini, Claude, ChatGPT)  
**Location:** Main README.md, section "AI Assistant Instructions"  
**Contains:** Quick protocol, critical rules, links to deeper files

**Why:** Every model can read the main GitHub page.

### 🟡 Layer 2: Standalone Instructions File
**Accessible to:** Claude, ChatGPT, some others  
**Location:** AI_INSTRUCTIONS.md or AI_INSTRUCTIONS.txt  
**Contains:** Full execution protocol, reading sequence, validation workflow

**Why:** Models with GitHub integration can fetch dedicated instruction files.

### 🔵 Layer 3: Contextual Deep Dive
**Accessible to:** Claude, ChatGPT with advanced access  
**Location:** /ai-context/ directory (CRAFTER-SPEC, EXECUTION-PROTOCOL, CONSTRAINT-RULES)  
**Contains:** Complete framework specification, detailed constraints, validation checklist

**Why:** Maximum fidelity for models that can navigate directory structures.

---

## Quick Diagnosis Table

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Model invents own format | Didn't read instructions | Paste AI_INSTRUCTIONS.txt directly |
| Model says "can't access files" | Gemini or limited access | Use README instructions, expect reduced fidelity |
| Output lacks CRAFTER structure | Missed constraint rules | Explicitly state: "Use EXACT CRAFTER format" |
| No validation performed | Skipped checklist | Request: "Run the 6-axis validation" |

---

## Test Prompt Template

```
C: https://github.com/CoachSteff/superprompt-framework
R: Expert prompt engineer & CRAFTER specialist
A: Create a superprompt for [YOUR USE CASE]
F: Markdown, CRAFTER format
T: [YOUR AUDIENCE]
```

---

## Model Cheat Sheet

| Model | Can Read Files? | Needs Manual Help? | Recommended Approach |
|-------|----------------|-------------------|---------------------|
| **Claude** | ✅ Yes, all layers | ❌ No | Just use the test prompt |
| **ChatGPT** | ✅ Yes, Layers 2-3 | ⚠️ Rarely | May need to ask "Did you read AI_INSTRUCTIONS?" |
| **Gemini** | ⚠️ Layer 1 only | ✅ Often | Expect to paste AI_INSTRUCTIONS.txt when needed |

---

## Recovery Steps for Gemini

If Gemini can't access the instruction files:

1. Ask: "Can you read AI_INSTRUCTIONS.md?"
2. If no, paste the contents of **AI_INSTRUCTIONS.txt**
3. Alternatively, manually specify CRAFTER format requirements

**AI_INSTRUCTIONS.txt location:**  
`https://github.com/CoachSteff/superprompt-framework/blob/main/AI_INSTRUCTIONS.txt`

---

## Success Checklist

A successful cross-model test means:

- ✅ Output uses CRAFTER structure (C-R-A-F-T-E-R)
- ✅ Model acknowledges framework guidelines
- ✅ Model doesn't invent its own format
- ✅ Output includes placeholders for reusability
- ✅ Validation is run or acknowledged

---

## Emergency Paste: Critical Rules

If a model is going off-track, paste this:

```
CRITICAL RULES FOR AI:
❌ DO NOT create your own framework interpretation
❌ DO NOT merge CRAFTER with other frameworks unless explicitly asked
❌ DO NOT skip the validation checklist
✅ ALWAYS use exact CRAFTER format: Context, Role, Action, Format, Target, Examples, Refining
✅ ALWAYS reference which template (if any) you adapted
✅ ALWAYS explain your reasoning if deviating from templates
```

---

## Files to Keep Handy

When testing with models that have limited GitHub access:

1. **AI_INSTRUCTIONS.txt** (plain text version, 2KB)
2. **This quick reference card**
3. **CRAFTER format specification** (from /ai-context/01-CRAFTER-SPEC.md)

---

## Documentation Links

- Full accessibility guide: `/docs/ai-accessibility.md`
- Testing guide: `/docs/testing-guide.md`
- Main framework docs: `/docs/`

---

**Pro Tip:** Bookmark this file for quick reference when testing new models or troubleshooting issues.

---

**Last Updated:** October 2025  
**Maintained by:** Steff Vanhaverbeke ([coachsteff.live](https://coachsteff.live))
