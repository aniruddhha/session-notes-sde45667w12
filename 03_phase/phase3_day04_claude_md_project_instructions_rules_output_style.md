# Phase 3 -> Day 4
## Instructions and Project Rules: `CLAUDE.md`, Work Standards, Communication Rules, and Output Style
### Trainer Session Notes

**Session Duration:** 1 hour 30 minutes  
**Session Mode:** 20% Theory | 80% Hands-On Discussion / Demonstration  
**Primary Environment:** VS Code  
**Primary Tool Focus:** Claude Code  
**Important Framing:** Claude Code is taught as a general-purpose agentic work assistant, not only a coding tool.

---

## 1. Session Goal for the Trainer

By the end of this session, learners should understand:

- what `CLAUDE.md` is
- why project instructions are important in Claude Code workflows
- how `CLAUDE.md` helps Claude Code work consistently inside VS Code
- how instructions differ from one-time prompts
- how to define work standards, tone, output format, review rules, and safety boundaries
- how `CLAUDE.md` can support general professional work, not only coding
- how to design a simple `CLAUDE.md` for documentation, planning, testing, content, review, and small tool workflows
- why unclear instructions increase risk and reduce output quality

**Trainer objective:**  
Day 4 should make learners understand that `CLAUDE.md` is not a technical decoration. It is the **project working rulebook** for Claude Code.

---

## 2. Recommended Session Flow

| Time | Segment | Mode |
|---|---|---|
| 0-8 min | Recap Day 3 and introduce project instructions | Theory |
| 8-20 min | What `CLAUDE.md` is and why it matters | Theory |
| 20-34 min | Prompt vs project instruction vs memory vs skill | Theory + examples |
| 34-48 min | Key sections of a useful `CLAUDE.md` | Demonstration discussion |
| 48-62 min | General-purpose `CLAUDE.md` examples | Hands-on style discussion |
| 62-74 min | Safety, review, and do-not-do rules | Discussion |
| 74-84 min | Activity: create a `CLAUDE.md` for a sample workflow | Hands-on discussion |
| 84-88 min | Recap and connection to Day 5 | Recap |
| 88-90 min | Closing task | Wrap-up |

---

## 3. Opening Script Notes for Yourself

Start with:

“On Day 3, we understood VS Code as the structured workspace for Claude Code. Today we will understand the instruction system that helps Claude Code behave correctly inside that workspace.”

Then say:

“When we work with an agentic assistant, we cannot depend only on one prompt. A project needs rules. It needs standards. It needs boundaries. This is where `CLAUDE.md` becomes important.”

Then add:

“Think of `CLAUDE.md` as the working constitution of the project. It tells Claude Code how to behave, how to write, what to avoid, what format to follow, and when to ask for human approval.”

---

## 4. Core Theory: What Is `CLAUDE.md`?

Explain simply:

**`CLAUDE.md` is a project instruction file used to guide Claude Code while working inside a project.**

It can tell Claude Code:

- what the project is about
- what kind of work is expected
- what output format to use
- what tone to follow
- what files to read or avoid
- what actions require approval
- what should never be done
- what quality checks must be followed
- what standards apply to documentation, review, testing, coding, or content work

### Verbatim explanation
“`CLAUDE.md` is like giving Claude Code a permanent briefing note for the project.”

---

## 5. Why `CLAUDE.md` Matters

Without project instructions, Claude Code may:

- make assumptions
- use inconsistent output style
- modify files without enough caution
- ignore naming conventions
- mix draft and final files
- forget safety rules
- generate too much or too little detail
- use the wrong tone
- create outputs in the wrong format

With `CLAUDE.md`, Claude Code can:

- follow consistent standards
- understand the project purpose
- produce output in expected structure
- respect file boundaries
- follow safety rules
- ask before risky actions
- separate facts from assumptions
- keep output aligned with the project workflow

### Trainer explanation
“One-time prompts are useful, but project-level work needs project-level instructions.”

---

## 6. Prompt vs `CLAUDE.md` vs Memory vs Skill

This distinction is important.

| Concept | Purpose | Example |
|---|---|---|
| Prompt | One-time instruction for current task | “Summarize this document.” |
| `CLAUDE.md` | Project-level rulebook | “Always create Markdown outputs and do not modify source files.” |
| Memory | Reusable preference or context across work | “User prefers downloadable Markdown files.” |
| Skill | Reusable capability for a type of work | “Document review skill” or “test case generation skill” |

### Verbatim explanation
“A prompt tells Claude what to do now. `CLAUDE.md` tells Claude how to work in this project.”

### Simple example

Prompt:
```text
Create a summary of input/meeting_notes.md.
```

`CLAUDE.md`:
```markdown
- Use professional tone.
- Save summaries in the output folder.
- Do not invent missing owners or dates.
- Separate decisions, actions, risks, and questions.
```

Trainer point:
The prompt gives the task. `CLAUDE.md` gives the working rules.

---

## 7. `CLAUDE.md` as a Project Rulebook

Explain:

A good `CLAUDE.md` should answer these questions:

1. What is this project?
2. What type of work will Claude Code support?
3. What tone and style should be used?
4. What file structure should be respected?
5. What output format is expected?
6. What should Claude Code not do?
7. What needs human approval?
8. What validation or review must be performed?
9. How should uncertainty be handled?
10. What final deliverables are expected?

### Trainer explanation
“If these questions are not answered, Claude Code may still produce output, but the output may not follow your real working style.”

---

## 8. Suggested Structure of a Good `CLAUDE.md`

Teach this reusable structure.

```markdown
# Project Instructions

## Project Purpose
Explain what this project is for.

## Working Role
Explain how Claude Code should assist.

## Output Style
Define tone, format, length, and structure.

## File Rules
Define input, output, working, review, and archive rules.

## Safety Rules
Define privacy, sensitive data, and risky-action boundaries.

## Approval Rules
Define what needs human approval before execution.

## Quality Rules
Define validation, review, and fact-checking expectations.

## Do Not Do
List prohibited actions.

## Final Output Requirements
Define how final deliverables should be prepared.
```

### Trainer point
The structure can be simple. The goal is clarity, not complexity.

---

## 9. Key Sections Explained

### 9.1 Project Purpose

This tells Claude Code what the project is about.

Example:
```markdown
## Project Purpose
This workspace is for reviewing training material and creating clean trainer notes in Markdown.
```

Why it matters:
Claude Code understands the broad goal.

---

### 9.2 Working Role

This defines how Claude Code should behave.

Example:
```markdown
## Working Role
Act as a careful documentation assistant. Help create, review, and improve training material. Do not make final decisions without human review.
```

Why it matters:
It guides the assistant’s behavior.

---

### 9.3 Output Style

This defines tone, format, and structure.

Example:
```markdown
## Output Style
Use clear professional language. Keep explanations practical. Use Markdown headings, bullet points, and tables where useful. Avoid unnecessary jargon.
```

Why it matters:
It keeps output consistent.

---

### 9.4 File Rules

This defines how files should be handled.

Example:
```markdown
## File Rules
- Treat files inside input/ as source files.
- Save generated files inside output/.
- Save review notes inside review/.
- Do not modify original input files unless explicitly asked.
```

Why it matters:
It prevents accidental changes and keeps work organized.

---

### 9.5 Safety Rules

This defines privacy and risk boundaries.

Example:
```markdown
## Safety Rules
- Do not include confidential, personal, or sensitive data in generated examples.
- Redact sensitive information before using it in outputs.
- Do not invent facts, names, dates, or decisions.
```

Why it matters:
It protects data and improves trust.

---

### 9.6 Approval Rules

This defines what requires permission.

Example:
```markdown
## Approval Rules
Ask for approval before:
- editing original files
- running commands that modify files
- deleting or moving files
- installing packages
- executing scripts on real data
```

Why it matters:
It keeps the human in control.

---

### 9.7 Quality Rules

This defines review expectations.

Example:
```markdown
## Quality Rules
Before final output, check:
- accuracy
- completeness
- tone
- missing information
- unsupported assumptions
- formatting consistency
```

Why it matters:
It turns quality review into a repeatable habit.

---

### 9.8 Do Not Do

This is very important.

Example:
```markdown
## Do Not Do
- Do not overwrite source files.
- Do not fabricate missing details.
- Do not make final decisions.
- Do not run destructive commands.
- Do not expose sensitive information.
```

Why it matters:
Clear restrictions reduce risk.

---

## 10. General-Purpose `CLAUDE.md` Example

Use this as a universal starting template.

```markdown
# Project Instructions

## Project Purpose
This workspace is used for AI-assisted professional work involving documents, plans, checklists, reviews, and small supporting tools.

## Working Role
Act as a careful assistant. Help organize information, create drafts, review material, identify gaps, and suggest improvements. Do not make final decisions.

## Output Style
Use clear professional language. Prefer Markdown. Use headings, bullet points, and tables where useful. Keep output practical and structured.

## File Rules
- Treat input/ as source material.
- Save generated files in output/.
- Save review notes in review/.
- Do not modify original input files unless explicitly asked.
- Create revised copies instead of overwriting originals.

## Safety Rules
- Do not invent facts, dates, names, or decisions.
- Clearly separate facts, assumptions, missing information, and questions.
- Do not include sensitive or confidential information in examples.
- Redact sensitive details where required.

## Approval Rules
Ask for approval before:
- editing original files
- running commands that change files
- deleting files
- moving or renaming many files
- installing packages
- executing scripts on real data

## Quality Rules
Before final output, check:
- accuracy
- completeness
- formatting
- tone
- missing information
- unsupported assumptions

## Do Not Do
- Do not overwrite source files.
- Do not run destructive commands.
- Do not make final decisions.
- Do not expose sensitive information.
- Do not assume missing details are true.

## Final Output Requirements
Final outputs should be saved in the output folder and should include a short review checklist when appropriate.
```

### Trainer explanation
“This template can be adjusted for many types of work: documentation, testing, content, planning, review, or small tools.”

---

## 11. Example: `CLAUDE.md` for Documentation Workflow

```markdown
# Documentation Project Instructions

## Project Purpose
This project is for converting rough notes into clean documentation.

## Working Role
Act as a documentation assistant. Organize rough notes, improve clarity, and create structured Markdown files.

## Output Style
Use simple professional language. Use clear headings. Avoid unnecessary technical complexity.

## File Rules
- Read source notes from input/.
- Save created documents in output/.
- Save review comments in review/.
- Do not modify input files.

## Quality Rules
Check for:
- missing sections
- unclear wording
- repeated content
- inconsistent formatting
- unsupported assumptions

## Do Not Do
- Do not invent missing facts.
- Do not change meaning.
- Do not remove important warnings or constraints.
```

---

## 12. Example: `CLAUDE.md` for Planning Workflow

```markdown
# Planning Project Instructions

## Project Purpose
This project is for converting requirements and rough notes into structured work plans.

## Working Role
Act as a planning assistant. Break work into phases, steps, risks, dependencies, and deliverables.

## Output Style
Use tables where helpful. Keep plans practical and action-oriented.

## File Rules
- Read requirements from input/.
- Save plans in output/.
- Save open questions in review/.

## Quality Rules
Clearly identify:
- assumptions
- dependencies
- risks
- missing information
- decision points

## Do Not Do
- Do not create unrealistic timelines.
- Do not assign responsibility without source information.
- Do not treat assumptions as confirmed facts.
```

---

## 13. Example: `CLAUDE.md` for Software Testing Workflow

```markdown
# Testing Project Instructions

## Project Purpose
This project is for generating and reviewing software test cases from requirements.

## Working Role
Act as a testing assistant. Create positive, negative, edge, and validation test scenarios.

## Output Style
Use tables with columns: Test ID, Scenario, Preconditions, Steps, Expected Result, Priority.

## File Rules
- Read requirements from requirements/.
- Save generated test cases in test-cases/.
- Save gaps and review notes in review/.

## Quality Rules
Check for:
- missing requirements
- edge cases
- negative scenarios
- unclear acceptance criteria
- traceability gaps

## Do Not Do
- Do not assume hidden business rules.
- Do not mark test cases final without human review.
- Do not ignore missing requirements.
```

---

## 14. Example: `CLAUDE.md` for Content Workflow

```markdown
# Content Project Instructions

## Project Purpose
This project is for creating and reviewing video or social media content.

## Working Role
Act as a content planning and review assistant.

## Output Style
Use clear, engaging, and audience-friendly language. Avoid overclaiming.

## File Rules
- Read raw ideas from notes/.
- Save outlines in outlines/.
- Save scripts in scripts/.
- Save review checklists in review/.

## Quality Rules
Check for:
- factual accuracy
- tone
- audience fit
- clarity
- repetition
- misleading claims

## Do Not Do
- Do not create false claims.
- Do not use offensive or biased framing.
- Do not make unsupported promises.
```

---

## 15. Example: `CLAUDE.md` for Small Tool Workflow

```markdown
# Small Tool Project Instructions

## Project Purpose
This project is for creating small helper tools or scripts.

## Working Role
Act as a careful implementation assistant. First explain the approach, then create code only after the plan is clear.

## Output Style
Explain steps clearly. Keep code simple and documented.

## File Rules
- Save scripts in scripts/.
- Save sample outputs in output/.
- Save test notes in review/.
- Do not run scripts on real data without approval.

## Approval Rules
Ask before:
- installing packages
- running scripts that modify files
- deleting or renaming files
- processing real folders

## Quality Rules
Use dry-run mode for file operations. Include error handling where relevant.

## Do Not Do
- Do not run destructive commands.
- Do not process production data without permission.
- Do not overwrite files without backup or approval.
```

---

## 16. Activity: Create a `CLAUDE.md`

Ask learners to choose one workflow:

1. Document review
2. Meeting summary
3. Project planning
4. Test case generation
5. Content planning
6. File indexing
7. Small website
8. Security checklist

Then ask them to write a `CLAUDE.md` with these sections:

```markdown
# Project Instructions

## Project Purpose

## Working Role

## Output Style

## File Rules

## Safety Rules

## Approval Rules

## Quality Rules

## Do Not Do

## Final Output Requirements
```

### Review questions
Ask:
- Is the project purpose clear?
- Are file boundaries clear?
- Are output formats defined?
- Are safety rules included?
- Are approval rules included?
- Are do-not-do rules specific?
- Would Claude Code know how to behave in this project?

---

## 17. Strong vs Weak `CLAUDE.md`

### Weak version

```markdown
Help with this project. Make good output.
```

Problem:
- no project purpose
- no output style
- no safety rule
- no file rule
- no approval rule

### Better version

```markdown
# Project Instructions

This workspace is for converting rough meeting notes into structured action summaries.

Use professional language. Save final summaries in output/. Do not modify input files. Do not invent owners, dates, or decisions. Clearly mark missing information. Ask before editing existing files.
```

Why better:
- task is clear
- output is clear
- restrictions are clear
- review expectation is clear

---

## 18. Safety Rules to Repeat Strongly

Include these in most `CLAUDE.md` files:

- Do not invent missing information.
- Do not make final decisions.
- Do not expose sensitive information.
- Do not overwrite original files.
- Do not run destructive commands.
- Ask before modifying files.
- Use dry-run before risky file operations.
- Separate facts, assumptions, and missing information.
- Mark uncertainty clearly.
- Keep generated output reviewable.

### Trainer explanation
“Safety rules should not be hidden in the trainer’s mind. They should be written into the project instructions.”

---

## 19. How `CLAUDE.md` Supports General Work

Reinforce that this is not only for coding.

### Documentation
Defines structure, tone, and missing-information handling.

### Planning
Defines timeline style, assumptions, risks, and dependencies.

### Review
Defines what to check and how to report issues.

### Testing
Defines test case format and coverage expectations.

### Content
Defines tone, audience, fact-checking, and claim boundaries.

### Coding
Defines coding standards, test expectations, and approval rules.

### File organization
Defines input/output folders, dry-run requirements, and no-delete rules.

### Trainer point
Same concept, different workflow.

---

## 20. Common Mistakes to Correct

### Mistake 1
Writing `CLAUDE.md` too vaguely.

Correction:
Be specific about output style, file rules, and review rules.

### Mistake 2
Using `CLAUDE.md` only for code standards.

Correction:
Use it for documentation, planning, review, testing, content, and workflow rules.

### Mistake 3
Forgetting safety rules.

Correction:
Always include approval and do-not-do sections.

### Mistake 4
Putting too many temporary details in `CLAUDE.md`.

Correction:
Keep project-level rules there. Put task-specific details in the prompt.

### Mistake 5
Not updating `CLAUDE.md` when workflow changes.

Correction:
Treat it as a living project instruction file.

---

## 21. Trainer Verbatim Blocks

### Verbatim Block 1
“`CLAUDE.md` is the project rulebook for Claude Code.”

### Verbatim Block 2
“A prompt tells Claude what to do now. `CLAUDE.md` tells Claude how to work in this project.”

### Verbatim Block 3
“Good project instructions reduce assumptions, improve consistency, and make output safer.”

### Verbatim Block 4
“Do-not-do rules are as important as task instructions.”

### Verbatim Block 5
“Use `CLAUDE.md` for general professional work, not only for coding standards.”

---

## 22. Questions to Ask During Session

Use these questions throughout:

- What is the project purpose?
- What role should Claude Code play?
- What output format should it follow?
- Which files are source files?
- Where should output be saved?
- What should not be modified?
- What requires approval?
- What should never be done?
- How should uncertainty be handled?
- What quality checks are required?

---

## 23. Day 4 Recap

End with:

“Today we learned that `CLAUDE.md` is the project instruction file that guides Claude Code. It helps define work standards, communication style, output format, file rules, safety boundaries, approval rules, and review expectations.”

Then say:

“We also learned that `CLAUDE.md` is not only for coding projects. It can guide documentation, planning, testing, review, content creation, small tools, and many professional workflows.”

Then close with:

“In the next session, we will focus on memory in Claude Code: project memory, local memory, user preferences, and long-term work context.”

---

## 24. End-of-Session Learner Takeaway

Learners should leave with these five ideas:

1. `CLAUDE.md` is the project rulebook.
2. It is different from a one-time prompt.
3. It can guide general professional work, not only coding.
4. It should include output, file, safety, approval, and quality rules.
5. Clear project instructions reduce risk and improve consistency.

---

## 25. Suggested Homework

Ask learners to create a `CLAUDE.md` for one real or sample workspace.

Minimum sections:

```markdown
# Project Instructions

## Project Purpose

## Working Role

## Output Style

## File Rules

## Safety Rules

## Approval Rules

## Quality Rules

## Do Not Do
```

They should bring it to the next session for review.

---

## 26. Final Trainer Reminder

Day 4 is successful if the learner can explain:

**`CLAUDE.md` tells Claude Code how to behave inside a project.**

They should also understand:

**The better the project instructions, the safer and more consistent the agentic workflow becomes.**
