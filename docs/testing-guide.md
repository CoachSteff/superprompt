# Testing Your Repository Across AI Models

This guide helps you verify that the SuperPrompt Framework repository works correctly with different AI models.

## The Test Prompt

Use this standardized prompt to test across all models:

```
C: https://github.com/CoachSteff/superprompt-framework
R: Expert prompt engineer & CRAFTER specialist
A: Create a superprompt for [coaching reflection session]
F: Markdown, CRAFTER format
T: [executive leaders]
```

**Replace the bracketed sections** with your actual use case when testing.

---

## Expected Behavior by Model

### ✅ Claude (Full Functionality)

**Access Capabilities:**
- ✅ Can read README
- ✅ Can read AI_INSTRUCTIONS.md
- ✅ Can navigate /ai-context/ directory
- ✅ Can access all template files

**Expected Response:**
1. Confirms it read AI_INSTRUCTIONS.md
2. References specific files from /ai-context/
3. Follows exact CRAFTER format
4. May adapt existing templates from /examples/

**Test Checklist:**
- [ ] Model explicitly mentions reading AI_INSTRUCTIONS.md
- [ ] Output follows CRAFTER structure (C-R-A-F-T-E-R)
- [ ] Model references constraint rules
- [ ] Output includes validation notes

---

### ✅ ChatGPT (Full Functionality)

**Access Capabilities:**
- ✅ Can read README
- ✅ Can usually read AI_INSTRUCTIONS.md
- ✅ Can usually navigate /ai-context/ directory
- ✅ Can access template files

**Expected Response:**
1. May or may not explicitly mention which files it accessed
2. Should follow CRAFTER format if it accessed instructions
3. May need gentle reminder to check AI_INSTRUCTIONS.md

**Test Checklist:**
- [ ] Output follows CRAFTER structure
- [ ] Model respects constraint rules
- [ ] If output is off-format, ask: "Did you read AI_INSTRUCTIONS.md?"

---

### ⚠️ Gemini (Limited Functionality)

**Access Capabilities:**
- ✅ Can read README (including inline instructions)
- ❌ May NOT be able to read AI_INSTRUCTIONS.md
- ❌ May NOT be able to access /ai-context/ directory
- ❌ Limited file navigation

**Expected Response:**
1. Relies on README inline instructions
2. Should still attempt CRAFTER format based on README
3. May lack deep context from /ai-context/ files

**Test Checklist:**
- [ ] Model references README instructions
- [ ] Output attempts CRAFTER structure
- [ ] If failing, paste AI_INSTRUCTIONS.txt content directly in chat

**Recovery Steps if Gemini Fails:**
1. Ask: "Can you access AI_INSTRUCTIONS.md?"
2. If no, paste contents of AI_INSTRUCTIONS.txt directly
3. Alternatively, manually provide the CRAFTER format specification

---

## Diagnostic Questions

If the model's response doesn't match expectations, ask these questions:

### 1. File Access Check
```
Which files from the repository were you able to access?
Please list them specifically.
```

**Good Response:** Lists specific files like "AI_INSTRUCTIONS.md, README.md, /ai-context/01-CRAFTER-SPEC.md"

**Bad Response:** Vague statement like "I reviewed the repository"

### 2. Format Awareness Check
```
What is the CRAFTER format structure you're supposed to follow?
Can you explain each component?
```

**Good Response:** Accurately describes C-R-A-F-T-E-R components

**Bad Response:** Invents own structure or can't explain

### 3. Constraint Awareness Check
```
What are the critical rules you must follow when creating superprompts?
```

**Good Response:** Mentions not inventing own framework, using exact CRAFTER format, running validation

**Bad Response:** Generic prompt engineering advice

---

## Troubleshooting Guide

### Problem: Model creates prompts in wrong format

**Diagnosis:** Model didn't access instruction files

**Solutions:**
1. Ask if it read AI_INSTRUCTIONS.md
2. Paste AI_INSTRUCTIONS.txt content directly
3. For Gemini, expect to rely on README only

### Problem: Model says "I can't access GitHub files"

**Diagnosis:** Model has limited web access

**Solutions:**
1. This is normal for Gemini
2. Paste AI_INSTRUCTIONS.txt in the chat
3. Or manually specify CRAFTER format requirements

### Problem: Model invents own framework

**Diagnosis:** Didn't read constraint rules

**Solutions:**
1. Re-emphasize: "Use EXACT CRAFTER format, do not invent your own"
2. Paste the critical rules section directly:
```
❌ DO NOT create your own framework interpretation
❌ DO NOT merge CRAFTER with other frameworks unless explicitly asked
✅ ALWAYS use exact CRAFTER format from /ai-context/01-CRAFTER-SPEC.md
```

### Problem: Output lacks validation

**Diagnosis:** Model skipped validation checklist

**Solutions:**
1. Explicitly request: "Run the validation checklist from /ai-context/05-VALIDATION-CHECKLIST.md"
2. If checklist not accessible, ask: "Evaluate this prompt against the 6-axis rubric"

---

## Success Criteria

A successful test means:

✅ **Format Compliance:** Output uses CRAFTER structure (C-R-A-F-T-E-R sections)

✅ **Context Awareness:** Output references or acknowledges repository guidelines

✅ **Constraint Respect:** Model doesn't invent its own framework

✅ **Reusability:** Output includes placeholders and adaptation notes

✅ **Validation:** Model either runs validation or acknowledges it should be done

---

## Model Comparison Table

| Capability | Claude | ChatGPT | Gemini |
|------------|--------|---------|--------|
| Read README | ✅ | ✅ | ✅ |
| Read AI_INSTRUCTIONS.md | ✅ | ✅ | ❌ |
| Navigate /ai-context/ | ✅ | ✅ | ❌ |
| Read templates | ✅ | ✅ | ❌ |
| Follows format out-of-box | ✅ | ✅ | ⚠️ |
| Needs manual guidance | No | Rarely | Often |

---

## Reporting Issues

If you discover a model that doesn't work with this repository, please open a GitHub issue with:

1. **Model name and version** (e.g., "Gemini 2.0 Flash")
2. **Test prompt used**
3. **Which files it could/couldn't access**
4. **Actual output vs. expected output**
5. **Any error messages**

This helps us improve cross-model compatibility.

---

## Next Steps

After testing:

1. Document which model you used in your project
2. If using Gemini, consider keeping AI_INSTRUCTIONS.txt handy to paste when needed
3. For production use, Claude or ChatGPT recommended for full functionality
4. Contribute your findings back to improve the framework

---

**Last Updated:** October 2025  
**Maintained by:** Steff Vanhaverbeke ([coachsteff.live](https://coachsteff.live))
