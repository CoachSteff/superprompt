# Templates Index: When to Use Each

**Templates are adaptation-ready starting points.**

## Template: Keyword Researcher
**Path:** `/templates/keyword-researcher.md`  
**Use when:** 
- User needs semantic keyword research for content planning
- User wants to understand search intent and keyword clusters
- User is building content strategy around a central topic
- User needs prompt hooks for AI-assisted content creation

**Don't use when:** 
- User needs technical SEO audits (crawling, indexing, site structure)
- User wants exact search volume metrics or competitive analysis
- Query is about paid search or PPC keyword research

**Adaptation zones:** 
- Main topic (Context section)
- Output format structure (Format section)
- Audience knowledge level and goals (Target section)

**Key features:**
- Three-layer keyword classification (Core, Context, Conversation)
- Search intent analysis
- Content opportunity generation
- Natural language focus (avoids technical SEO jargon)

---

## No Template Match?

If no template fits:
1. Build from `/ai-context/01-CRAFTER-SPEC.md`
2. Document why no template matched
3. Suggest this could become a new template

**Example:**
```
TEMPLATE_USED: Built from CRAFTER-SPEC
REASONING: User requested workshop facilitation prompt, 
no existing template covers group dynamics and real-time 
interaction. This could become "workshop-facilitator" template.
```

---

## Adding New Templates

When you identify a pattern that could be reusable:
1. Document the template following CRAFTER format
2. Mark clear "Adaptation zones" in the template
3. Add use cases and anti-patterns
4. Add it to `/templates/` folder
5. Update this index
6. Test with at least 2 different inputs

---

## Quick Reference: Template Selection

| User Need | Template | Notes |
|-----------|----------|-------|
| Keyword research, content planning | `keyword-researcher.md` | Semantic focus, not technical SEO |
| [Future template] | [filename] | [When to use] |

---

**Last updated:** 2025-10-22
