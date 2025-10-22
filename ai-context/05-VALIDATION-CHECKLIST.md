# Validation Checklist

**Run this before presenting any superprompt.**

## Structure Check
- [ ] Contains all required components (C, R, A, F, T)
- [ ] Components are in correct order
- [ ] Uses `::CRAFTER` header

## Component Quality Check
- [ ] Context (C): Includes environment, constraints, connection to larger work
- [ ] Role (R): Specifies expertise and cognitive approach
- [ ] Action (A): Has numbered steps that are concrete and sequential
- [ ] Format (F): Shows explicit output structure
- [ ] Target (T): Defines who, what they know, what they want

## Clarity Check
- [ ] No vague language ("figure out", "something useful", "as needed")
- [ ] No ambiguous terms ("standard", "normal", "appropriate")
- [ ] Every action is testable (could verify if it was done)

## Constraint Compliance
- [ ] Did not invent new framework components
- [ ] Did not merge CRAFTER with other frameworks
- [ ] Did not skip required components
- [ ] Did not assume unstated context

## Usability Check
- [ ] User could copy-paste this and get expected results
- [ ] Another person could use this without additional explanation
- [ ] Output format is clear enough to plan around

## If ANY check fails:
1. Return to relevant spec in `/ai-context/01-CRAFTER-SPEC.md`
2. Fix the issue
3. Re-run this checklist

## Self-Documentation
Before presenting to user, add:
```
TEMPLATE_USED: [which template, if any]
REASONING: [why you made key choices]
SUGGESTED_USE_CASES: [where this prompt works best]
```
