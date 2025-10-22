# Execution Protocol: How to Generate Superprompts

**Follow this sequence every time.**

## Step 1: Parse User Request

Extract:
```
DOMAIN: [what field/area]
USE_CASE: [specific task]
AUDIENCE: [who is this for]
FORMAT_PREFERENCE: [any specified output format]
```

## Step 2: Check for Existing Template

Look in `/templates/` for matches:
- Exact domain match? Use and adapt
- Similar structure? Reference and modify
- No match? Build from CRAFTER-SPEC

**Document your decision:**
```
TEMPLATE_USED: [name or "built from spec"]
MODIFICATIONS: [what you changed and why]
```

## Step 3: Build Each Component

Work through CRAFTER in order:

### Building Context (C)
Ask yourself:
- Where does this operate? (GitHub, email, workshop, etc.)
- What are the boundaries?
- How does it connect to larger work?

Template:
```
You are connected to [ENVIRONMENT].
You work within [SYSTEM/CONSTRAINTS].
The user typically [CONTEXT/GOAL].
```

### Building Role (R)
Ask yourself:
- What expertise is needed?
- How should the AI think about this?
- What makes this perspective unique?

Template:
```
You are a [DOMAIN] expert with deep insight in [SPECIFIC CAPABILITIES].
You think like [COGNITIVE APPROACH].
```

### Building Action (A)
Ask yourself:
- What's the exact sequence?
- Where are the decision points?
- What's the end state?

Use numbered steps. Be concrete.

### Building Format (F)
Ask yourself:
- What medium? (markdown, JSON, etc.)
- What structure? (sections, tables, lists)
- How detailed?

Show the structure explicitly.

### Building Target (T)
Ask yourself:
- Who is this for specifically?
- What do they already know?
- What are they trying to achieve?

Be precise about knowledge level and goals.

## Step 4: Validate

Run through `/ai-context/05-VALIDATION-CHECKLIST.md`

Fix any failures before presenting.

## Step 5: Present

Show:
1. The complete superprompt
2. Which template you used (if any)
3. Your reasoning for key choices
4. Suggested use cases

## Error Recovery

If user says result is wrong:
- Ask which component failed
- Review that component's spec
- Regenerate using stricter interpretation
