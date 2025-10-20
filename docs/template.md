# SuperPrompt Template v0.1

**Copy and paste this template into any AI tool (Claude, GPT, Gemini, Llama) or workflow (Cursor, GitHub Copilot). Replace the placeholders with your specifics.**

---

```markdown
Title: <give your superprompt a descriptive name>

ROLE & TONE
You are <define the role: coach, analyst, technical writer, strategist>.
Write with <specify tone: warm and empathetic / sharp and direct / formal and technical> for <target audience: executives / developers / workshop participants>.

INTENT
<One paragraph describing what success looks like. Include measurable criteria if possible.>

Example: "Help me design a 90-minute workshop that teaches cognitive agility to mid-level managers. Success means a clear agenda, three interactive exercises, and a one-page handout participants can use immediately."

CONTEXT
<Provide everything the model needs to reason well: domain facts, constraints, examples, style guides, prior decisions, relevant background.>

Example:
- Audience: 15-20 mid-level managers in tech companies
- Setting: In-person workshop, no tech required
- Constraints: Must fit in 90 minutes, budget €500 for materials
- Style: Use plain language, no corporate jargon
- Prior decision: Focus on "flexible thinking" as the first capability from the Cognitive Agility Framework

REASONING POLICY
<Explain how the model should think. Include steps, constraints, checks, timeboxing, and refusal rules.>

Example:
1. Start by outlining the workshop structure (intro, body, close)
2. Design three exercises that require movement or conversation, not slides
3. Check that each exercise directly teaches one aspect of flexible thinking
4. If you don't have enough context to design an exercise, ask for clarification before proceeding
5. Refuse to suggest exercises that require expensive tech or more than 90 minutes

OUTPUT
<Specify exactly what you want produced and in what format. Include headings, structure, or a JSON schema if needed.>

Example:
Produce a workshop design document with these sections:
1. Workshop Title & Objective (2 sentences)
2. Agenda (timeline with activities)
3. Three Exercises (title, goal, instructions, duration, materials)
4. One-page Handout (markdown format, ready to print)

OUTPUT SCHEMA (optional)
<If you need structured data, include a JSON schema here>

{
  "type": "object",
  "properties": {
    "workshop_title": {"type": "string"},
    "objective": {"type": "string"},
    "agenda": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "time": {"type": "string"},
          "activity": {"type": "string"},
          "duration_minutes": {"type": "number"}
        }
      }
    },
    "exercises": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "title": {"type": "string"},
          "goal": {"type": "string"},
          "instructions": {"type": "string"},
          "duration_minutes": {"type": "number"},
          "materials": {"type": "array", "items": {"type": "string"}}
        }
      }
    },
    "handout_markdown": {"type": "string"}
  },
  "required": ["workshop_title", "objective", "agenda", "exercises"]
}

SELF-CHECK
Before finalizing, verify:
- Does this meet the intent and success criteria?
- Have I followed all constraints in the reasoning policy?
- If I cited sources or made claims, are they accurate?
- Is the output in the requested format?
```

---

## How to Use This Template

1. **Copy the entire block** above (starting from "Title:" through "SELF-CHECK")
2. **Replace placeholders** with your specific task details
3. **Delete optional sections** you don't need (like OUTPUT SCHEMA)
4. **Paste into your AI tool** and run it
5. **Refine iteratively**: If the output isn't quite right, adjust the CONTEXT or REASONING POLICY and re-run

---

## Three Quick Customization Levers

1. **Tone**: Change "warm and empathetic" to "sharp and analytical" to shift the entire response style
2. **Reasoning Policy**: Add specific refusal rules ("never suggest tools that cost money") to constrain outputs
3. **Output Schema**: Add a JSON schema when you need structured, machine-readable data

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
