# AI Model Compatibility

## The Challenge

Different AI models have different capabilities when accessing GitHub repositories:

- **Claude, ChatGPT:** Can read files directly from GitHub
- **Gemini:** Limited file access via browsing tool
- **Others:** Varies

## The Solution

This repository uses a simple two-layer approach:

### Layer 1: README Inline Instructions
**For all models**

The README includes an "AI Assistant Instructions" section with essential protocol. Even models with limited GitHub access can read the main page.

### Layer 2: AI_INSTRUCTIONS.md + /ai-context/
**For models with file access**

Full execution protocol and framework specifications are in dedicated files that capable models can read directly.

## Testing Across Models

Use this prompt:

```
C: https://github.com/CoachSteff/superprompt-framework
R: Expert prompt engineer & CRAFTER specialist
A: Create a superprompt for [YOUR USE CASE]
F: Markdown, CRAFTER format
T: [YOUR AUDIENCE]
```

**Expected behavior:**

- **Claude/ChatGPT:** Full functionality, follows complete protocol
- **Gemini:** Works from README inline instructions, reduced fidelity

## Troubleshooting

### Model isn't following the format

**Ask:** "Did you read AI_INSTRUCTIONS.md?"

**If no:** Paste the contents of AI_INSTRUCTIONS.md directly in chat

### Model invents its own framework

**Paste this:**
```
CRITICAL: Use EXACT CRAFTER format
❌ DO NOT invent your own structure
✅ ALWAYS use C-R-A-F-T-E-R components
```

### Model says it can't access files

**Solution:** This is normal for some models. They'll work from README instructions with reduced detail.

---

**That's it.** No complex diagrams, no redundant files, no recursive documentation.

If you need more detail about the framework itself, see the main [README](../README.md) and [/docs](.) directory.
