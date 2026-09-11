#  Requirements & Values Elicitation Guidelines 


## Purpose

This guide helps your team:

- identify the people and groups (stakeholders) who use, influence, or may be affected by the product
- learn about their needs, goals, tasks, experiences, concerns, and expectations
- identify the values that matter to them, such as accessibility, privacy, security, fairness, inclusion, autonomy, trust, cultural relevance, sustainability
- understand the real-world environment in which the product will operate
- involve stakeholders throughout product development and
- keep records of interviews, meetings, observations, workshops, and other elicitation activities.

The purpose is to help your team understand what should be developed and why it matters to stakeholders.

## 1. Identifying and Engaging Stakeholders

Identify the people and groups who use, influence, support, or may be affected by the product. Consider both direct stakeholders, such as intended users and project partners, and indirect stakeholders, such as administrators, community members, support staff, or others affected by the product.

For each stakeholder or group, consider:
- their relationship to the project
- how they may use, influence, or be affected by the product
- why their knowledge, experiences, needs, or concerns matter
- how and when your team will engage with them


## 2. Requirements Elicitation 

Engage with stakeholders to understand:
- what they need the product to achieve
- the tasks and goals the product should support
- how they expect to interact with the product
- the environment in which the product will operate
- any expectations, constraints, risks, or concerns that may affect the product

Here is some [interviewing tips](https://github.com/inspireuvic/SENG480B-Fall2026/blob/main/requirements-values-documentation/interview-tips.md) for requirement elicitation. 

## 2.1 Hints for requirement elicitation questions
Use open-ended questions to understand stakeholders’ current experiences, goals, and difficulties before discussing possible features.

**Example elicitation Question:**
 
Can you describe how you currently submit an assignment using the existing application, from beginning to end? What works well, and what difficulties do you experience?

 **Example stakeholder answer:**

>_“I upload a PDF file assignment and wait for confirmation.  It is sometimes difficult to tell whether I uploaded the correct file or whether the submission was successful. I would like to see the submitted file name, preview or download the file afterward, and replace it before the deadline if I uploaded the wrong file”_

**Hints on how to  derive requirements**
From stakeholder discussions, identify:

The broad outcome or service the product should support (Epic).

The main product capabilities needed to support that outcome (Features).

Small, testable user needs that describe who needs something, what they need, and why (User Stories).


## 2.2 Requirements Details 
Students should maintain the hierarchy from broad outcomes to specific, testable needs:

Epic → Feature → User Story

**Epic** is  broad stakeholder outcome that is too large to implement at once and will require multiple features or user stories.

example:
_Assignment Submission Management_ — Enable students to submit assignment work confidently before a deadline.

**Feature** is a meaningful product capability that contributes to an epic.

example: 
_Assignment file submission_ — Allow students to upload and submit an assignment file for a course assessment.

**User story** is a small, user-focused need that can be implemented and tested independently.

example:
_Successful PDF submission_ — As a student, I want to upload my assignment as a PDF so that I can submit it electronically.

This is only one possible interpretation of the stakeholder’s response. Additional features and user stories may be identified for submission confirmation, file review, and file replacement. Review the derived requirements with the stakeholder before finalizing them.

## 2.3 Recording requirements in GitHub

Use the Epic, Feature, and User Story issue templates provided in the sample repository. Copy the entire `.github/ISSUE_TEMPLATE` folder into your team repository.

For every issue:

- use a clear, meaningful title
- complete all applicable template fields
- link each Feature and User Story to its parent issue
- link supporting evidence when it explains or supports the requirement

If AI contributed to eliciting, interpreting, refining, or writing an issue, use the template to record:

- what AI contributed
- how the team reviewed the contribution
- whether the contribution was accepted, revised, or rejected
- any stakeholder feedback that influenced the decision

The **Requirements and Values Document** should provide an overview of the requirements and links to the relevant GitHub issues.

## 3. Value Elicitation

Engage with stakeholders to understand what they consider important, desirable, worth protecting, or worth achieving.
Values may be expressed through stakeholders’ needs, goals, experiences, concerns, priorities, expectations, boundaries, or feedback.
Do not rely only on asking stakeholders, “What are your values?” Stakeholders may not describe what matters to them using terms such as privacy, fairness, or autonomy. Use open-ended questions, examples, experiences, discussions, and realistic situations to understand what matters to them and why.

### 3.1 Hints for value elicitation questions

**Initial questions before go in detail about values:**

1. Can you describe a recent experience with the current process that felt particularly positive or difficult? What happened, how did it make you feel, and what seemed most important to you in that situation?

2. Thinking about the experience you would want instead, how should it feel, and what would the process or system need to do or avoid doing to create that experience?


**Explore more on value alignment, you can ask questions like:**

1. Looking at the proposed process or system, which parts support the experience and outcomes that matter to you, and which parts work against them?

2. If your actual choices differ from what you previously said mattered, what explains the difference? Is it a contextual constraint, a trade-off between values, or a change in what is important to you?


## 3.2 Stakeholder Values Details 
You should collect the details of the identified values including:
- a brief description
- which stakeholder or stakeholder group's value is this
- what the team heard or observed on it
- any known conflicts with other values, their priorities
- any planned stakeholder follow-up or validation


**Guidance**

The **Value / Brief Description** should be short but specific enough to identify what the value means.

For example:

> `Privacy: control over who can access personal information`

Avoid listing only a generic word such as *privacy* or *transparency* without explaining what it means in the context of the project.


## 3.3 Recording Stakeholder Values in GitHub

Create one GitHub issue for each identified stakeholder value using the Value issue template. Complete all applicable fields and attach or link the supporting elicitation evidence.
If AI contributed to identifying, interpreting, or describing the value, record:
- what AI contributed
- All  the stakeholders’ feedback, including any revisions made

Record this information in the relevant fields of the Value issue template.

The **Requirements and Values Document** should provide a brief overview of the identified values and links to their corresponding GitHub issues with **Issue Type = Value**.

## 4. Retaining Elicitation Evidence

Keep the materials and records produced through stakeholder engagement. These may include:
- interview questions, responses, or notes;
- workshop and meeting note
- questionnaire responses or summaries
- observation notes
- co-design activity records
- stakeholder emails or written feedback and
- other records directly related to requirements or value elicitation.

Store these materials in the appropriate `supporting-documents` folder in GitHub. Link them to relevant GitHub issues when they explain or support a requirement or value.

**Do not include private, confidential, or personally identifying stakeholder information in the repository without appropriate permission.**

## 5. Keeping Project Records Updated

Following this guide, your team must regularly update and push the following project records to GitHub:
- Requirements and Values document
- Requirement and value GitHub issues
- The Tech–Value Alignment document and
- Relevant elicitation notes and supporting evidence.

