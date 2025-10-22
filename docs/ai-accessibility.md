# Cross-Model AI Accessibility Guide

## The Problem

Different AI models have different web access capabilities when reading GitHub repositories:

- **Claude:** Has GitHub MCP integration, can read repos programmatically via API
- **ChatGPT:** Can access GitHub files directly via web scraping or API
- **Gemini:** Uses a browsing tool with limitations—cannot always fetch raw GitHub files or access certain URL patterns

This means a repository that works perfectly with Claude or ChatGPT might be completely inaccessible to Gemini.

## The Solution: Multi-Layer Entry Points

This repository uses a **three-layer accessibility strategy** to ensure all AI models can read and execute instructions:

### Layer 1: Inline README Instructions ✅ (For models with limited GitHub access)

**Location:** Main README.md  
**Purpose:** Embed critical AI instructions directly in the README  
**Accessible to:** All AI models (Gemini, Claude, ChatGPT, etc.)

The README now includes an **"AI Assistant Instructions"** section with:
- Your role as a Superprompt Generator
- Quick execution protocol
- Critical rules
- Links to deeper context files

**Why this works:** Every AI model can read the main README page, even if they can't access raw files.

### Layer 2: Standalone Instructions File ✅ (For models with file access)

**Location:** AI_INSTRUCTIONS.md  
**Purpose:** Dedicated instruction file for AI models  
**Accessible to:** Claude, ChatGPT, and other models with GitHub file access

This file provides:
- Complete execution protocol
- Reading sequence for `/ai-context/` files
- Critical rules and boundaries
- Validation workflow

**Why this works:** Models with GitHub integration can fetch this file directly and follow a structured learning path.

### Layer 3: Contextual Deep Dive ✅ (For advanced model workflows)

**Location:** `/ai-context/` directory  
**Purpose:** Full specification files for detailed understanding  
**Accessible to:** Claude, ChatGPT, advanced MCP-enabled workflows

Contains:
- `01-CRAFTER-SPEC.md` — Canonical framework
- `02-EXECUTION-PROTOCOL.md` — How to apply it
- `03-CONSTRAINT-RULES.md` — Boundaries and rules
- `05-VALIDATION-CHECKLIST.md` — Quality assurance

**Why this works:** Models that can navigate directory structures can load the complete context for maximum fidelity.

---

## Testing Your Prompt Across Models

When testing the repository with different AI models, use this prompt:

```
C: https://github.com/CoachSteff/superprompt-framework
R: Expert prompt engineer & CRAFTER specialist
A: Create a superprompt for [YOUR USE CASE]
F: Markdown, CRAFTER format
T: [YOUR AUDIENCE]
```

### Expected Behaviors by Model

**Gemini:**
- Reads README inline instructions
- May not be able to fetch AI_INSTRUCTIONS.md or `/ai-context/` files
- Should still function based on README guidance alone

**Claude:**
- Can access all three layers
- Reads AI_INSTRUCTIONS.md first
- Loads `/ai-context/` files as needed
- Full fidelity execution

**ChatGPT:**
- Can typically access Layer 2 and Layer 3
- May prefer AI_INSTRUCTIONS.md as entry point
- Can navigate `/ai-context/` directory

---

## Design Principles

This multi-layer approach follows these principles:

1. **Progressive Enhancement:** Each layer adds more detail, but Layer 1 is sufficient for basic functionality
2. **No Redundancy:** Each layer references the next rather than duplicating content
3. **Graceful Degradation:** If a model can't access deeper layers, it still gets essential instructions
4. **Model-Agnostic:** No assumptions about which model will be used

---

## Troubleshooting

### "The AI isn't following the framework"

**Possible causes:**
- Model couldn't access AI_INSTRUCTIONS.md
- Model is relying only on README (Layer 1)

**Solution:** Explicitly ask the model: "Did you read the AI_INSTRUCTIONS.md file?" If not, paste the contents directly in your prompt.

### "The AI says it can't access GitHub files"

**Solution:** This is a Gemini-specific limitation. The model should still work using README instructions. For full fidelity, switch to Claude or ChatGPT.

### "The AI is inventing its own framework"

**Solution:** The model didn't read the constraint rules. Paste this directly:

```
CRITICAL RULES:
❌ DO NOT create your own framework interpretation
❌ DO NOT merge CRAFTER with other frameworks unless explicitly asked
✅ ALWAYS use exact CRAFTER format from /ai-context/01-CRAFTER-SPEC.md
```

---

## Maintenance Checklist

When updating the framework, ensure all three layers stay synchronized:

- [ ] Update README inline instructions if core protocol changes
- [ ] Update AI_INSTRUCTIONS.md if execution flow changes
- [ ] Update `/ai-context/` files for detailed specifications
- [ ] Test with Gemini, Claude, and ChatGPT
- [ ] Verify all links work

---

## Future Improvements

Potential enhancements for even better cross-model accessibility:

1. **Plain Text Fallback:** Create a `.txt` version of AI_INSTRUCTIONS.md for models that struggle with markdown
2. **JSON Schema:** Add a machine-readable schema file for structured data parsing
3. **Explicit Model Detection:** Add logic to detect which model is being used and adjust instructions accordingly
4. **CDN Hosting:** Mirror critical files on a CDN for models with GitHub access issues

---

## Questions?

If you encounter a model that can't access this repository effectively, please open an issue with:
- Model name and version
- What files it could/couldn't access
- Error messages or behaviors observed

This helps us improve cross-model compatibility.

---

**Last Updated:** October 2025  
**Maintained by:** Steff Vanhaverbeke ([coachsteff.live](https://coachsteff.live))
