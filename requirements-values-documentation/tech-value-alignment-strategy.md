# Tech–Value Alignment Strategy

Technology–value alignment means ensuring that the product’s technical artifacts: such as requirements, designs, code, and test cases reflect the values of the stakeholders who use or may be affected by the product.

Teams must show how each stakeholder value moves from elicitation into product decisions, technical work, and implemented outcomes.

For each value-related GitHub issue, use the template that matches its issue type: Value, Epic, Feature, User Story, or Task and complete all applicable sections.


### 1. Add Values as a gitHub issue 
Create a separate GitHub issue for each identified stakeholder value. Select the **Value template** in GitHub issues and complete all applicable fields.

### 2. Connect values to technical artifacts 

Use the following hierarchy to connect stakeholder values to technical work:

<img src="values-artifact.png" alt="Description of the image" width="500">

Source: Adapted from [Agbese M. et al., 2025](https://link.springer.com/content/pdf/10.1007/978-3-032-14518-5_8.pdf)

Maintain the Following Hierarchy:

- One stakeholder **Value** must be linked to one or more **Epics**.
- One **Epic** may address one or more stakeholder **Values**.
- Each **Epic** should contain one or more **Features**.
- Each **Feature** should contain one or more **User Stories**.

  
### 2.1. Connect Each value to GitHub Epics and break down the work

For each stakeholder value:
1. Review the existing epics and identify which ones should address the value.
2. Link the Value issue to each relevant epic.
3. If no existing epic addresses the value, create a new epic using the **Epic** issue template
4. Break the epic down into appropriate features, user stories, and their sub tasks.
5. Use the appropriate Epic, Feature, User Story, or Task template in GitHub issues and complete all applicable fields.

## 3. Validation of Tech-Value Alignment
Use this table to record how stakeholders reviewed the alignment between their values and the related technical artifacts, such as requirements, designs, prototypes, implemented features, and test results.

Update the table whenever stakeholder feedback or project changes affect the alignment. Use the same Value ID assigned in the corresponding GitHub Value issue.


| Value ID | Related Technical Artifact / GitHub Issue | Validation Method | Stakeholder / Reviewer | Review Date | Feedback and Evidence | Changes Made or Planned | Alignment Status |
|---|---|---|---|---|---|---|---|
| VAL-01 |  |  |  |  |  |  | Not reviewed / Partially aligned / Aligned |
| VAL-02 |  |  |  |  |  |  | Not reviewed / Partially aligned / Aligned |
| VAL-03 |  |  |  |  |  |  | Not reviewed / Partially aligned / Aligned |


### 4. Sprints contributions to tech-value alignment
If you addressed any value-alignment issues or made value-related decisions during the sprint, record the update here for the relevant sprint. You may also provide the related GitHub Issue IDs.

Sprint 1 - Record the decisions and actions taken to translate stakeholder values into requirements and implementation tasks, including any contributions made by AI.
> 

---

Sprint 2 - 
Record the Tech-Value Alignment decisions made during Sprint 2, including relevant design and architecture decisions for Tech-Value Alignment, and document how AI contributed to these decisions.
>

---
Sprint 3 - 
Record the Tech-Value Alignment decisions made during Sprint 3, including relevant implementation decisions for Tech-Value Alignment, and document how AI contributed to these decisions.
>

---
Sprint 4 - 
Record the Tech-Value Alignment decisions made during Sprint 4, including relevant testing and verification decisions for Tech-Value Alignment, and document how AI contributed to these decisions.
>

---

### 5. Tech-Value Alignment submissions
At each required submission point:

- Export the Epics and their related task for value related epics.
- Commit the export to the project repository as tech-value-alignment-export.csv or tech-value-alignment-export.md.
- Add the export date and a link below.

**Tech-Value Alignment export date:** [YYYY-MM-DD]  
**Tech-Value Alignment export:** [Add link]  
**Live GitHub Tech-Value Alignment view:** [Add link]

## Related Project Documents

1. **Requirements and Values Elicitation Guidelines**
2. **Requirements and Values Document**
