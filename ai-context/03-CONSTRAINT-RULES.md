# Constraint Rules: What NOT To Do

**These are hard boundaries. Violating them produces bad outputs.**

## ❌ DO NOT: Invent Your Own Framework

**Wrong:**
```
I'll use CRAFTER but add a new component called "Validation"...
```

**Why it's wrong:**  
CRAFTER has a specific structure. Adding components breaks compatibility 
with existing templates and confuses users.

**Right:**  
Use CRAFTER exactly as specified. If validation is needed, it goes in 
the Action (A) component or Refining Script (R).

---

## ❌ DO NOT: Merge CRAFTER With Other Frameworks

**Wrong:**
```
I'll combine CRAFTER with the PARA method to create CRAFTER-PARA...
```

**Why it's wrong:**  
Each framework has its own purpose. CRAFTER is for prompt structure. 
If the user wants PARA integrated, it goes in the Context (C) or 
Action (A) components.

**Right:**  
```
C – Context: You organize work using PARA (Projects, Areas, Resources, Archive)
A – Action: 1. Analyze input using PARA categories...
```

---

## ❌ DO NOT: Make Components Optional

**Wrong:**
```
For simple tasks, you can skip the Target Audience section...
```

**Why it's wrong:**  
Every component serves a purpose. Skipping Target (T) means the AI 
doesn't calibrate complexity appropriately.

**Right:**  
Include all required components (C, R, A, F, T). Make them brief if 
needed, but include them.

---

## ❌ DO NOT: Use Vague Action Items

**Wrong:**
```
A – Action: Figure out the best approach and create something useful.
```

**Why it's wrong:**  
AI needs concrete steps. "Figure out" and "something useful" are not 
actionable instructions.

**Right:**
```
A – Action:
1. Analyze the input for [specific criteria]
2. Generate [specific output]
3. Validate against [specific checklist]
```

---

## ❌ DO NOT: Ignore Format Specification

**Wrong:**
```
F – Format: Whatever works best
```

**Why it's wrong:**  
Users need predictable output. "Whatever works" means they can't 
plan how to use the result.

**Right:**
```
F – Format: 
Markdown with these sections:
## Analysis
[prose paragraph]

## Recommendations  
[numbered list]

## Next Steps
[bullet points]
```

---

## ❌ DO NOT: Assume Context

**Wrong:**
```
C – Context: Standard business environment
```

**Why it's wrong:**  
"Standard" is ambiguous. Different users, different standards.

**Right:**
```
C – Context: You work with a European coaching business that 
serves freelance professionals. The user values clarity over 
corporate jargon and prioritizes human-centered approaches.
```

---

## ✅ When In Doubt

1. Check `/ai-context/01-CRAFTER-SPEC.md` for the rule
2. Look at `/templates/` for examples
3. Ask the user for clarification
4. Default to stricter interpretation (more structure, not less)
