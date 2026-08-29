# GitHub Issue Record Template for Epics, Features, Tasks/User stories in Requirements

Each identified **value** should be associated with at least one **Epic**. An epic may be decomposed into one or more **features**, and each feature may give rise to **tasks or user stories**. 

Create a GitHub issue for each meaningful Epic, Feature, User Story, or Task, using the appropriate issue category. Link related issues using GitHub’s parent–child relationship or sub-issue feature.

Use the **Value ID(s)** defined in the **Stakeholder & Value Elicitation Plan** to connect each **Epic** to the stakeholder values, concerns, priorities, and supporting elicitation evidence recorded in that plan.

Features, User Stories, and Tasks do not need to repeat the Value ID(s). Their relationship to stakeholder values is maintained through their link to the parent Epic.

If a field is genuinely not relevant, write **N/A**.


## Requirement Template


| Field | What to Record |
|---|---|
| **Category** | Select one: `Epic`, `Feature`, `User Story`, or `Task`. |
| **Title** | Brief description. Example: `Users can revoke consent for data collection at any time`. |
| **Parent Issue** | Link the immediate parent issue. Features must link to an Epic; User Stories and Tasks must link to a Feature, User Story, or Epic as appropriate. For a top-level Epic, write `N/A`. |
| **Description / Desired Outcome** | Explain what the requirement means and what should be true when it is completed. Describe the expected user, system, or project outcome. |
| **Related Value ID(s)** | **Epics only:** list the relevant Value ID(s) from the Stakeholder & Value Elicitation Plan, for example `VAL-01`, `VAL-03`. **Features, User Stories, and Tasks:** write `Inherited from parent issue`. |
| **Rationale / Concerns / Influences** | Briefly explain why this item matters. For an Epic, explain how it responds to the linked value, stakeholder concern, or priority. For lower-level issues, explain how it contributes to the parent item. |
| **Acceptance Criteria** | State what must be true for the issue to be considered complete. Use clear, observable, or testable conditions where possible. |
| **AI Contribution, if any** | State whether AI was used and what it contributed, such as ideation, drafting, refinement, analysis, coding, testing, or review. If AI was not used, write `None`. |
| **Stakeholder Review / Feedback** | If applicable, record who reviewed the item, the feedback received, and what changed as a result. If no review has occurred, write `Not yet reviewed`. |
| **Notes / Decisions / Trade-offs** | Record important assumptions, value conflicts, alternatives considered, prioritization decisions, constraints, or unresolved questions. |
| **Related Work** | Link relevant parent or child issues, pull requests, commits, tests, prototypes, design artefacts, research evidence, or supporting documentation. |


** Marking Notes: **

- Each identified stakeholder value should be associated with at least one Epic.
- Each Epic must include the relevant Value ID(s).
- Features, User Stories, and Tasks must link to their immediate parent issue and should record `Inherited from parent issue` rather than repeating Value ID(s).
- The decomposition should make sense: each Feature should contribute to its Epic, and each User Story or Task should contribute to its parent Feature or Story.
- All relevant fields in the template must be completed, with links or supporting information included where necessary.
- Acceptance criteria must be sufficiently clear to determine whether the requirement has been addressed.
- Important stakeholder feedback, use of AI, assumptions, value conflicts, and trade-offs should be recorded where relevant.
