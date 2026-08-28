# SENG480B · Community Engaged Research & Innovation · Fall 2026
## Sprint 2 Decision Record

Fill this in once, as a team, at the end of Sprint 2. It should take about 15 minutes.

**How to use this file**

1. Fill in the header, then Part 1, then Part 2.
2. Write in plain sentences. Bullet points are fine.
3. There is no length requirement. A good answer is usually one or two sentences.
4. Rename to `sprint-2-decisions-TEAMNAME.md` and submit.

---

## Header

| | |
|---|---|
| **Team** : | |
| **Sprint dates** : | |
| **Who filled this in** : | |

---

## Part 1 — Architecture Components

For each part of your system, mark what happened this sprint. One word per cell.

**Changed?** — `no` · `minor` · `major`

**AI involvement** — `none` · `modified` (AI suggested it, you changed it) · `kept` (AI generated it, you kept it as-is)

| Component | Changed? | AI involvement |
|---|---|---|
| Data model (what you store) | | |
| API / server layer | | |
| Client / UI | | |
| AI integration (where you call the model) | | |
| Auth / permissions | | |
| Other: | | |

If a component did not change this sprint, put `no` and leave AI involvement blank.

---

## Part 2 — One decision, in depth

**This sprint, record a decision about how AI fits into your system** — where the model gets called, what information it receives, and what happens to what it returns.

> Examples: calling the model from the browser or from the server, deciding what data gets put into the prompt, where the prompt text lives, whether you check the output before showing it, whether conversation history is saved.

**If your team did not make an AI integration decision this sprint,** record any other structural decision you did make instead, and name it below. Do not invent one.

**Decision area:** `AI integration` · or write your own: ______________________

**If your AI feature came out of scaffolding and nobody discussed how it was wired up,** that is a real and acceptable answer. Describe how it currently works, say where it came from, and answer question 4 honestly.

### The decision

**1. What did you decide?** One sentence.

> *Example: We moved all model calls from the browser to the server so the API key is not exposed.*

<!-- your answer here -->

**2. What other approach did you consider, and why did you not take it?**

> Name at least one real alternative. If you genuinely did not consider one, say so. That is a valid answer.

<!-- your answer here -->

**3. What does this make easier later, and what does it make harder?**

<!-- your answer here -->

### Where it came from

**4. Where did this come from?** Mark one with an `x`.

- [ ] We discussed it as a team and chose it
- [ ] AI proposed it, we kept it as-is
- [ ] AI proposed it, we changed it
- [ ] Copied from documentation, a tutorial, or another project
- [ ] Came with the starter template

> This question is **not graded on which box you tick.** It is graded on being accurate. "AI proposed it and we kept it" is a completely normal answer.

**5. If AI was involved, what did you change about what it produced?**

> If you changed nothing, write "nothing."

<!-- your answer here -->

### The team

**6. How many team member/total were in the discussion when it was decided?**

<!-- your answer here -->

**7. How did the rest of the team find out about it?**

> For example: standup, code review, a commit message, a chat message, or they did not and noticed later.

<!-- your answer here -->

---

## Does this replace an earlier decision?

If this decision reverses or replaces something from Sprint 1, say so here. Do not go back and edit your Sprint 1 record.

**Supersedes:**

**Why it changed:**

<!-- your answer here -->

---

## Marking

Marked on completeness and clarity:

- Every question answered
- Question 2 names a real alternative, or honestly says none was considered
- Question 4 is accurate

**Not** marked on which decision you picked, how much AI you used, or whether the decision turned out to be right.

---

## More about decision records

- [Architectural decision — Wikipedia](https://en.wikipedia.org/wiki/Architectural_decision)
- [Architecture decision record (ADR) — templates and examples](https://github.com/architecture-decision-record/architecture-decision-record)

These describe the general practice this assignment is based on. The version here is deliberately shorter.
