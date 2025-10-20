# The SuperPrompt Mental Model

## What is a SuperPrompt?

A superprompt is a **structured cognitive interface** between human intent and AI reasoning. It translates what you want into how the model should think, then specifies what it should produce. It's not about length—it's about architecture.

Think of it as a thinking contract: you define the goal, constraints, reasoning steps, and output format. The model follows that structure to deliver predictable, reusable results.

A superprompt has six minimum components:

**Intent** → what success looks like  
**Context** → facts, examples, constraints  
**Reasoning Policy** → how to think (steps, checks, refusal rules)  
**Output Schema** → what to produce and in what format  
**Self-Check** → verify before finalizing  

It's a recipe for structured thinking, not a magic spell.

---

## Visual Model

```
┌──────────────────────────────────────────────────────────┐
│                    SUPERPROMPT FLOW                      │
├──────────────────────────────────────────────────────────┤
│                                                          │
│  1. INTENT                                               │
│     ↓                                                    │
│     "What does success look like?"                       │
│     Define goal + success criteria                       │
│                                                          │
│  2. CONTEXT                                              │
│     ↓                                                    │
│     "What does the model need to know?"                  │
│     Domain facts, examples, constraints                  │
│                                                          │
│  3. REASONING POLICY                                     │
│     ↓                                                    │
│     "How should it think?"                               │
│     Steps, checks, refusal rules                         │
│                                                          │
│  4. OUTPUT                                               │
│     ↓                                                    │
│     "What should it produce?"                            │
│     Format, structure, length                            │
│                                                          │
│  5. SELF-CHECK                                           │
│     ↓                                                    │
│     "Did it meet the intent?"                            │
│     Verify constraints before finalizing                 │
│                                                          │
│  → RESULT: Predictable, structured, reusable output     │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

---

## One-Sentence Definition

> A superprompt is a cognitive contract that structures AI reasoning through explicit intent, context, policy, output specification, and verification.

---

## Why This Matters

Most prompts are instructions. Superprompts are **systems**. They create predictability by controlling three variables:

1. **What to think about** (context)
2. **How to think** (reasoning policy)
3. **What to produce** (output specification)

When you control these, you get consistent results you can reuse, refine, and share.

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
