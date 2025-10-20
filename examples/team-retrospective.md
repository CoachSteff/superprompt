# Example 2: Team Leadership Retrospective

**Why this works:** Uses the Role Mesh pattern to surface tensions between perspectives (team vs. leader). The output is structured to be immediately actionable in a team meeting.

**Quick customization levers:**
1. Change the time period (sprint, quarter, project cycle)
2. Adjust team size or context (remote team, cross-functional team, new team)
3. Modify the format (written retrospective, facilitated workshop, async feedback)

---

```markdown
Title: Team Leadership Retrospective

ROLE & TONE
You are a team facilitator who specializes in helping teams reflect honestly without blame. Write with clarity and empathy. Frame insights in a way that invites curiosity, not defensiveness.

INTENT
Help me design a 60-minute retrospective for my team of 8 engineers after a difficult sprint where we missed our deadline. Success means: (1) a clear agenda I can run in one hour, (2) at least 3 discussion prompts that surface genuine insights (not surface complaints), (3) one concrete team commitment we can track next sprint.

CONTEXT
- Team: 8 mid-level engineers working on a product feature
- Challenge: We missed the sprint deadline by 3 days because requirements changed mid-sprint and we didn't push back
- My role: Team lead; I approved the requirement changes but didn't reset expectations
- Team dynamic: Generally collaborative but reluctant to surface conflict
- Goal: Get better at setting boundaries with stakeholders and saying no to scope creep
- Setting: 60 minutes, in-person, no slides

REASONING POLICY
1. Design the retrospective to surface the underlying dynamic (we avoid conflict with stakeholders) rather than just listing complaints about scope creep
2. Use the Role Mesh pattern: have the team discuss what happened from two perspectives: (a) as engineers trying to deliver quality work, (b) as teammates who want to support each other
3. Include one structured activity (not just open discussion) that makes it safe to name the real problem
4. Close with a commitment the team can own (not something imposed on stakeholders)
5. Refuse to design a retrospective that lets everyone blame external factors without owning our part
6. Keep the agenda tight—60 minutes means we need focus, not exhaustive debriefs

OUTPUT
Produce a retrospective agenda in markdown format with:

1. **Opening** (5 min) – How to set the frame
2. **Activity 1: Dual Perspective** (20 min) – Instructions for the Role Mesh exercise
3. **Activity 2: Name the Pattern** (15 min) – How to surface the underlying dynamic
4. **Activity 3: Team Commitment** (15 min) – How to converge on one actionable commitment
5. **Closing** (5 min) – How to end with clarity
6. **Facilitator Notes** – Tips for keeping it psychologically safe and focused

SELF-CHECK
Before finalizing:
- Is this agenda runnable in 60 minutes?
- Are the activities specific enough that I don't need to improvise?
- Does the commitment address the underlying dynamic, not just the symptom?
```

---

**Example Output Preview:**

## Retrospective Agenda

### Opening (5 min)
**Frame:** "We missed our deadline this sprint, and I want us to reflect on what happened—not to assign blame, but to understand the pattern so we can do better next time. Today's goal is to identify one commitment we can make as a team to protect our ability to deliver quality work."

**Ground rule:** We're focusing on what we can control (our own actions and decisions), not external factors we can't change.

---

### Activity 1: Dual Perspective (20 min)

**Instructions:**  
Split into two groups of 4. Each group discusses the sprint from one perspective:

**Group A (Engineers):** What made it hard to deliver quality work this sprint? What trade-offs did we make, and how did that feel?

**Group B (Teammates):** What made it hard to support each other this sprint? When did we notice someone struggling, and what did (or didn't) we do?

After 10 minutes, groups swap and briefly share their insights (5 min each).

**Facilitator note:** This activity separates technical concerns from interpersonal dynamics, making both easier to name.

---

### Activity 2: Name the Pattern (15 min)

**Instructions:**  
As a full group, answer this question:

**"What's the underlying dynamic that allowed scope creep to happen without pushback?"**

Use this sentence stem to surface the pattern:  
*"When stakeholders asked for changes mid-sprint, we [did what], because we believed [what], and the result was [what]."*

**Example:**  
*"When stakeholders asked for changes mid-sprint, we said yes without resetting expectations, because we believed saying no would make us look uncooperative, and the result was we burned out and missed the deadline anyway."*

Write the completed sentence on a whiteboard where everyone can see it.

**Facilitator note:** This makes the pattern explicit without assigning blame to any individual.

---

### Activity 3: Team Commitment (15 min)

**Instructions:**  
Now that we've named the pattern, what's one commitment we can make to each other to interrupt it next sprint?

**Commitment format:**  
*"When [trigger happens], we will [new action], so that [desired outcome]."*

**Example:**  
*"When a stakeholder requests a scope change mid-sprint, we will pause and consult as a team before committing, so that we protect our ability to deliver on our existing commitments."*

Test the commitment: Can we start doing this next sprint? Is it specific enough to track?

**Facilitator note:** The commitment should be something the team can own, not something that requires changing stakeholder behavior.

---

### Closing (5 min)

**Frame:** "Let's name one person who will be the 'commitment keeper' next sprint—someone who reminds us of this when we're tempted to revert to the old pattern."

Volunteer or rotate the role. Close by thanking everyone for the honest reflection.

---

### Facilitator Notes

- **If the group resists naming the pattern:** Ask, "What would we tell a friend if they described this situation to us?"
- **If someone starts blaming stakeholders:** Redirect: "Let's focus on what we can control. What could we have done differently?"
- **If the commitment is too vague:** Ask, "How will we know if we're actually doing this?"

---

## License

CC-BY 4.0 · Steff Vanhaverbeke · [coachsteff.live](https://coachsteff.live)
