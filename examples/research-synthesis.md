# Example 5: Research Synthesis into references.md

**Why this works:** Uses Source-Anchored Synthesis pattern to ensure every claim is verifiable. The structured JSON output makes it easy to import into reference managers.

**Quick customization levers:**
1. Change research domain (coaching, AI adoption, product management, etc.)
2. Adjust synthesis goal (literature review, competitive analysis, best practices scan)
3. Modify output format (markdown bibliography, JSON, BibTeX)

---

```markdown
Title: Research Synthesis into references.md

ROLE & TONE
You are a research librarian who synthesizes academic papers, blog posts, and articles into clear, cited references. Write with precision and neutrality. Prioritize accuracy over interpretation.

INTENT
Synthesize 5–10 sources on a research topic into a structured references.md file with key insights and proper citations. Success means: (1) every claim is traceable to a source, (2) sources are organized by theme, (3) the synthesis highlights agreements and disagreements, (4) the output is immediately usable in a knowledge base.

CONTEXT
- Research topic: How freelance professionals adopt AI tools in their workflows
- Sources: 5 blog posts, 2 academic papers, 3 podcast transcripts (provided below)
- Goal: Understand common adoption patterns, barriers, and success factors
- Audience: Coaches and trainers who help professionals adopt AI
- Output destination: A markdown file that will live in a /research folder in a GitHub repo

REASONING POLICY
1. Read all provided sources carefully
2. Extract key claims from each source (focus on evidence, not opinions)
3. For each claim, note which source it comes from (cite inline with [Author, Year] format)
4. Organize claims into themes (e.g., Adoption Patterns, Barriers, Success Factors)
5. Highlight agreements across sources and flag disagreements
6. Refuse to make claims not supported by the provided sources
7. If a source is unclear or ambiguous, note that in your synthesis rather than interpreting it
8. Use Source-Anchored Synthesis pattern: every sentence should be traceable to a source

OUTPUT
Produce two things:

1. **references.md file** (markdown format) with:
   - Title: Research Synthesis: [Topic]
   - Introduction (1 paragraph summarizing the synthesis)
   - Themes (H2 headers, with cited claims organized under each)
   - Agreements and Disagreements (H2 section highlighting cross-source patterns)
   - References (H2 section listing all sources in APA format)

2. **references.json file** (JSON format) with structured metadata for each source:
   - author, year, title, url, key_claims (array of strings)

OUTPUT SCHEMA
For references.json:

{
  "type": "object",
  "properties": {
    "sources": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "author": {"type": "string"},
          "year": {"type": "number"},
          "title": {"type": "string"},
          "url": {"type": "string"},
          "key_claims": {
            "type": "array",
            "items": {"type": "string"}
          }
        },
        "required": ["author", "year", "title", "key_claims"]
      }
    }
  }
}

SELF-CHECK
Before finalizing:
- Are all claims in the synthesis directly traceable to a source?
- Have I cited sources using [Author, Year] format?
- Are the references listed in APA format?
- Does the JSON file include all sources with key claims?
```

---

**Example Output Preview:**

## references.md

```markdown
# Research Synthesis: AI Adoption Among Freelance Professionals

## Introduction

This synthesis examines how freelance professionals (coaches, designers, writers) adopt AI tools in their workflows. Drawing from 10 sources (5 blog posts, 2 academic papers, 3 podcast transcripts), the research reveals three key themes: adoption patterns vary by profession, barriers are more psychological than technical, and early success correlates with experimentation rather than formal training.

---

## Theme 1: Adoption Patterns

Freelance professionals adopt AI tools in stages rather than all at once. <cite>[Chen, 2024]</cite> identifies a three-stage pattern: (1) curiosity and exploration, (2) selective integration into one workflow, (3) systematic use across multiple projects. This aligns with <cite>[Martinez, 2023]</cite>, who found that 78% of surveyed freelancers started with a single tool (most commonly ChatGPT) before expanding to others.

Adoption speed varies by profession. <cite>[Roberts, 2024]</cite> found that writers and coaches adopt AI tools faster than designers, likely because text-based tools are more mature than visual ones. However, <cite>[Lee & Park, 2023]</cite> note that designers who do adopt AI report higher perceived productivity gains.

---

## Theme 2: Barriers to Adoption

The primary barriers to AI adoption are psychological, not technical. <cite>[Johnson, 2024]</cite> found that 65% of freelancers cite "fear of losing my unique value" as the top barrier, compared to only 23% who cite technical difficulty. This finding is echoed in <cite>[Williams, 2023]</cite>, who describes a "substitution anxiety"—the belief that AI will replace rather than augment their work.

Lack of clear use cases is another significant barrier. <cite>[Davis, 2024]</cite> reports that freelancers often experiment with AI tools but abandon them because they don't know what problems to solve with them. This suggests that adoption is not just about tool access but about understanding where AI fits in their existing workflows.

---

## Theme 3: Success Factors

Experimentation predicts adoption success more than formal training. <cite>[Martinez, 2023]</cite> found that freelancers who spent at least 5 hours experimenting with AI tools in the first month were 3x more likely to integrate them into their workflows than those who took a formal course. This suggests that hands-on practice is more effective than passive learning.

Peer support accelerates adoption. <cite>[Chen, 2024]</cite> identified "AI adoption buddies"—freelancers who pair up to experiment together—as a key success factor. These informal support networks help overcome psychological barriers and provide practical tips that formal training often misses.

---

## Agreements and Disagreements

**Agreement:** All sources agree that psychological barriers (fear, uncertainty) are more significant than technical ones.

**Agreement:** Experimentation is consistently associated with successful adoption across sources.

**Disagreement:** <cite>[Roberts, 2024]</cite> argues that AI tools save freelancers time, while <cite>[Lee & Park, 2023]</cite> found that early adopters report spending *more* time on projects (but with higher quality outcomes). This suggests that "productivity" may mean different things to different professionals.

---

## References

Chen, L. (2024). The three stages of AI adoption among freelance coaches. *Journal of Professional Development*, 12(3), 45-62.

Davis, M. (2024). Why freelancers abandon AI tools: A qualitative study. *Freelancer Insights Blog*. https://freelancerinsights.com/why-abandon-ai

Johnson, K. (2024). Fear and adoption: Understanding psychological barriers to AI in freelance work. *Technology & Work Quarterly*, 8(2), 112-128.

Lee, S., & Park, J. (2023). Productivity or quality? Trade-offs in AI-assisted design work. *Design Studies*, 55(4), 301-318.

Martinez, R. (2023). Survey of 500 freelancers: How they use AI tools in 2023. *Freelance Tech Report*. https://freelancetech.com/survey-2023

Roberts, A. (2024). AI tools for writers, coaches, and designers: A comparative adoption study. *Work & AI Podcast*, Episode 47.

Williams, T. (2023). Substitution anxiety: Why freelancers fear AI will replace them. *Psychology Today Blog*. https://psychologytoday.com/substitution-anxiety
```

---

## references.json

```json
{
  "sources": [
    {
      "author": "Chen, L.",
      "year": 2024,
      "title": "The three stages of AI adoption among freelance coaches",
      "url": "https://journalofprofessionaldevelopment.com/chen-2024",
      "key_claims": [
        "Freelancers adopt AI in three stages: curiosity, selective integration, systematic use",
        "Peer support networks (AI adoption buddies) accelerate adoption"
      ]
    },
    {
      "author": "Martinez, R.",
      "year": 2023,
      "title": "Survey of 500 freelancers: How they use AI tools in 2023",
      "url": "https://freelancetech.com/survey-2023",
      "key_claims": [
        "78% of freelancers start with a single AI tool (most commonly ChatGPT)",
        "Freelancers who experiment for 5+ hours in the first month are 3x more likely to integrate AI"
      ]
    },
    {
      "author": "Roberts, A.",
      "year": 2024,
      "title": "AI tools for writers, coaches, and designers: A comparative adoption study",
      "url": "https://workandai.com/podcast/episode-47",
      "key_claims": [
        "Writers and coaches adopt AI tools faster than designers",
        "AI tools save freelancers time on routine tasks"
      ]
    },
    {
      "author": "Lee, S. & Park, J.",
      "year": 2023,
      "title": "Productivity or quality? Trade-offs in AI-assisted design work",
      "url": "https://designstudies.com/lee-park-2023",
      "key_claims": [
        "Designers report higher perceived productivity gains from AI",
        "Early adopters spend more time on projects but produce higher quality outcomes"
      ]
    },
    {
      "author": "Johnson, K.",
      "year": 2024,
      "title": "Fear and adoption: Understanding psychological barriers to AI in freelance work",
      "url": "https://technologywork.com/johnson-2024",
      "key_claims": [
        "65% of freelancers cite fear of losing unique value as top barrier to AI adoption",
        "Psychological barriers are more significant than technical ones"
      ]
    },
    {
      "author": "Williams, T.",
      "year": 2023,
      "title": "Substitution anxiety: Why freelancers fear AI will replace them",
      "url": "https://psychologytoday.com/substitution-anxiety",
      "key_claims": [
        "Freelancers experience 'substitution anxiety'—belief that AI will replace rather than augment their work"
      ]
    },
    {
      "author": "Davis, M.",
      "year": 2024,
      "title": "Why freelancers abandon AI tools: A qualitative study",
      "url": "https://freelancerinsights.com/why-abandon-ai",
      "key_claims": [
        "Lack of clear use cases is a significant barrier to adoption",
        "Freelancers abandon AI tools when they don't know what problems to solve with them"
      ]
    }
  ]
}
```

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
