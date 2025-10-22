# CRAFTER Framework: Canonical Specification

**This is the authoritative definition. Do not deviate.**

## Structure

Every CRAFTER superprompt has these components in this exact order:

```
::CRAFTER

C – Context
[Explicit role and environment definition]

R – Role  
[Specific expertise and perspective]

A – Action
[Concrete, measurable task]

F – Format
[Exact output structure]

T – Target Audience
[Who this is for and why]

E – Examples (optional)
[Input/output demonstrations]

R – Refining Script (optional)
[Iteration instructions if needed]
```

## Component Specifications

### C – Context
**Purpose:** Establish environment and constraints  
**Length:** 2-4 sentences  
**Must include:**
- Where/how this prompt operates
- Key constraints or boundaries
- Connection to larger system (if applicable)

**Example:**
```
You are connected to the GitHub environment of CoachSteff. 
You work within a system that manages superprompts, skills, 
and context packages for AI agents. The user typically wants 
to create content for professional audiences.
```

### R – Role
**Purpose:** Define expertise and cognitive stance  
**Length:** 1-2 sentences  
**Must include:**
- Specific domain expertise
- Cognitive approach (how you think)
- Unique perspective or capability

**Example:**
```
You are a Keyword Researcher AI with deep insight in semantic 
search intent, contextual positioning, and human language patterns.
```

### A – Action
**Purpose:** Specify exactly what to do  
**Format:** Numbered list preferred  
**Must include:**
- Sequential steps
- Decision points
- Output requirements

**Example:**
```
1. Receive main topic
2. Analyze search intent
3. Generate semantic network of related terms
4. Divide into three layers: Core, Context, Conversation
5. Suggest content opportunities
```

### F – Format
**Purpose:** Define output structure  
**Must specify:**
- File type (markdown, JSON, etc.)
- Section structure
- Visual elements (tables, lists, headers)

**Example:**
```
Markdown with clear sections:
## Keyword Research Summary
### Semantic Clusters (table format)
### Content Opportunities (bullet list)
### Prompt Hooks (examples)
```

### T – Target Audience
**Purpose:** Calibrate complexity and focus  
**Must include:**
- Who this is for
- What they're trying to achieve
- Knowledge level assumptions

**Example:**
```
Content creators, coaches, and entrepreneurs who want to 
understand how AI approaches keyword research. They want 
to learn the thinking process, not just get lists.
```

### E – Examples (Optional)
**Purpose:** Demonstrate input/output patterns  
**Include when:**
- Format is ambiguous
- Domain is unfamiliar
- Edge cases exist

### R – Refining Script (Optional)
**Purpose:** Enable iteration  
**Include when:**
- First pass may need adjustment
- Multiple valid approaches exist
- Quality threshold is subjective

## Validation Checklist
- [ ] All required components present (C, R, A, F, T)
- [ ] Components in correct order
- [ ] Action items are concrete and sequential
- [ ] Format specification is unambiguous
- [ ] Target audience is clearly defined
