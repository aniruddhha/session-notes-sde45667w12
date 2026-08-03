# Phase 3 -> Day 6
## Skills in Claude Code: Reusable Capabilities for Writing, Review, Research, Documentation, Coding, Testing, and Analysis
### Trainer Session Notes

**Session Duration:** 1 hour 30 minutes  
**Session Mode:** 20% Theory | 80% Hands-On Discussion / Demonstration  
**Primary Environment:** VS Code  
**Primary Tool Focus:** Claude Code  
**Important Framing:** Claude Code is taught as a general-purpose agentic work assistant, not only a coding tool.

---

## 1. Session Goal for the Trainer

By the end of this session, learners should understand:

- what Skills are in Claude / Claude Code workflows
- why Skills are useful for repeated professional tasks
- how Skills differ from prompts, `CLAUDE.md`, memory, subagents, and tools
- how a Skill can encode a repeatable work method
- how Skills can support writing, review, research, documentation, testing, analysis, coding, and content workflows
- how Skills can be used inside a VS Code + Claude Code working setup
- what a `SKILL.md` file represents at a high level
- what should and should not go inside a Skill
- why Skills require careful design, testing, and review

**Trainer objective:**  
Day 6 should help learners understand Skills as **reusable work capabilities**. They should not think of Skills only as programming helpers. They should understand them as repeatable task patterns that make Claude Code follow a consistent workflow.

---

## 2. Recommended Session Flow

| Time | Segment | Mode |
|---|---|---|
| 0-8 min | Recap Day 5 and introduce Skills | Theory |
| 8-20 min | What Skills are and why they matter | Theory |
| 20-34 min | Prompt vs `CLAUDE.md` vs memory vs Skill | Theory + examples |
| 34-48 min | Anatomy of a Skill: name, description, instructions, supporting files | Demonstration discussion |
| 48-62 min | General-purpose Skill examples beyond coding | Hands-on style discussion |
| 62-74 min | Designing safe and useful Skills | Discussion |
| 74-84 min | Activity: design a Skill for a repeated work task | Hands-on discussion |
| 84-88 min | Recap and connection to Day 7 | Recap |
| 88-90 min | Closing task | Wrap-up |

---

## 3. Opening Script Notes for Yourself

Start with:

“On Day 5, we learned about memory. Memory helps Claude Code remember stable and useful context. Today we will learn about Skills, which are reusable capabilities for repeated types of work.”

Then say:

“Skills are different from memory. Memory stores useful context or preference. A Skill stores a repeatable method or capability.”

Then add:

“In this course, we are not looking at Skills only for coding. We will understand Skills for documentation, review, planning, research-style analysis, testing, content workflows, and small tools.”

---

## 4. Core Theory: What Is a Skill?

Explain simply:

**A Skill is a reusable capability that teaches Claude how to perform a specific type of task in a consistent way.**

A Skill can include:
- when to use it
- what workflow to follow
- what input to expect
- what output to produce
- what quality checks to perform
- what mistakes to avoid
- what tools may be useful
- what examples or supporting files may help

### Simple explanation
“A Skill is like a standard operating procedure for Claude.”

### Verbatim explanation
“When you find yourself giving the same long instruction again and again, that repeated method may become a Skill.”

---

## 5. Why Skills Matter

Skills matter because professional work often repeats.

Examples:
- reviewing documents
- summarizing meetings
- creating test cases
- generating checklists
- reviewing scripts
- preparing project plans
- creating README files
- writing release notes
- analyzing requirements
- preparing structured reports

Without a Skill:
- user repeats the same instructions
- output may vary each time
- quality checks may be forgotten
- format may change
- safety rules may be missed

With a Skill:
- workflow becomes repeatable
- output becomes consistent
- quality checks become standard
- repeated instructions are reduced
- specialized behavior can be reused

### Trainer explanation
“Skills help convert repeated work from ‘explain every time’ into ‘use the standard method’.”

---

## 6. Prompt vs `CLAUDE.md` vs Memory vs Skill

Review this distinction carefully.

| Concept | Main Purpose | Example |
|---|---|---|
| Prompt | Current task instruction | “Create test cases from this requirement.” |
| `CLAUDE.md` | Project-level working rulebook | “Save generated files in output/ and do not modify input/.” |
| Memory | Stable remembered preference or context | “User prefers Markdown trainer notes.” |
| Skill | Reusable method for a task type | “Use the standard test-case-generation workflow.” |

### Verbatim explanation
“A prompt gives the task. `CLAUDE.md` gives project rules. Memory gives repeated context. A Skill gives a reusable way to perform a kind of work.”

### Example

Prompt:
```text
Review this policy document.
```

`CLAUDE.md`:
```markdown
Use neutral language. Save review output in review/. Do not modify source files.
```

Memory:
```text
User prefers outputs as downloadable Markdown files.
```

Skill:
```text
Policy Review Skill:
- summarize purpose
- identify gaps
- separate facts and assumptions
- flag sensitive data
- create review questions
- create final checklist
```

---

## 7. What a Skill Contains at a High Level

Do not go too deep into implementation yet. Explain the concept first.

A Skill usually has:

### 7.1 Name
A clear name for the capability.

Examples:
- document-review
- test-case-generator
- meeting-summary
- security-checklist
- content-script-review
- project-plan-builder

### 7.2 Description
A short explanation that helps Claude know when the Skill is relevant.

Example:
```text
Use this skill when reviewing professional documents for clarity, missing information, assumptions, and review questions.
```

### 7.3 Instructions
The actual method Claude should follow.

Example:
```text
First identify document purpose. Then summarize key points. Then list missing information. Then flag assumptions. Then create final review checklist.
```

### 7.4 Output format
The required final structure.

Example:
```markdown
## Summary
## Missing Information
## Assumptions
## Risks
## Review Questions
## Final Checklist
```

### 7.5 Quality checks
Rules for reviewing the output.

Examples:
- do not invent facts
- separate facts from assumptions
- preserve meaning
- mark uncertainty
- validate source information
- check tone and formatting

### 7.6 Supporting files
Some Skills may include templates, examples, scripts, or references.

Examples:
- checklist template
- report template
- style guide
- script helper
- validation guide

---

## 8. `SKILL.md` Concept

Explain simply:

In Claude Skills, the instructions for a Skill are commonly written in a file called `SKILL.md`.

A simple Skill folder may look like:

```text
document-review/
  SKILL.md
```

A more advanced Skill may include supporting files:

```text
document-review/
  SKILL.md
  templates/
    review_report_template.md
  examples/
    sample_review.md
```

### Trainer explanation
“`SKILL.md` is to a Skill what `CLAUDE.md` is to a project. `CLAUDE.md` guides the project. `SKILL.md` guides a reusable capability.”

---

## 9. Simple Example Skill: Meeting Summary

### Skill name
```text
meeting-summary
```

### When to use
Use when converting rough meeting notes into a structured professional meeting summary.

### Workflow
1. Identify meeting purpose.
2. Extract decisions.
3. Extract action items.
4. Identify owners and deadlines if available.
5. Mark missing owners or missing dates.
6. Identify risks or open questions.
7. Create final summary in Markdown.

### Output format

```markdown
# Meeting Summary

## Purpose

## Key Discussion Points

## Decisions

## Action Items

| Action | Owner | Due Date | Notes |
|---|---|---|---|

## Risks / Concerns

## Missing Information

## Next Steps
```

### Quality rules
- Do not invent owners.
- Do not invent due dates.
- Preserve original meaning.
- Mark unclear items.
- Use professional language.

### Trainer point
This Skill is not coding. It is a repeatable documentation workflow.

---

## 10. Simple Example Skill: Document Review

### Skill name
```text
document-review
```

### When to use
Use when reviewing a document for clarity, completeness, missing information, unsupported assumptions, tone, and structure.

### Workflow
1. Identify document purpose.
2. Identify intended audience.
3. Summarize current structure.
4. List unclear sections.
5. List missing information.
6. Flag unsupported assumptions.
7. Suggest improvements.
8. Create review checklist.

### Output format

```markdown
# Document Review

## Document Purpose

## Strengths

## Missing Information

## Unclear Sections

## Unsupported Assumptions

## Suggested Improvements

## Review Questions

## Final Checklist
```

### Quality rules
- Do not rewrite meaning unless asked.
- Do not add new facts.
- Keep feedback constructive.
- Separate confirmed issues from suggestions.

---

## 11. Simple Example Skill: Test Case Generator

### Skill name
```text
test-case-generator
```

### When to use
Use when creating test cases from requirements, user stories, acceptance criteria, or feature descriptions.

### Workflow
1. Read requirement.
2. Identify functional areas.
3. Identify positive scenarios.
4. Identify negative scenarios.
5. Identify edge cases.
6. Identify validation rules.
7. Create traceability from requirement to test case.
8. Mark unclear requirements.

### Output format

```markdown
# Test Cases

| Test ID | Scenario | Preconditions | Steps | Expected Result | Priority |
|---|---|---|---|---|---|

## Missing / Unclear Requirements

## Edge Cases

## Review Notes
```

### Quality rules
- Do not assume hidden business rules.
- Mark unclear requirements.
- Include negative and edge scenarios.
- Keep test steps executable.

---

## 12. Simple Example Skill: Content Script Review

### Skill name
```text
content-script-review
```

### When to use
Use when reviewing video scripts, narration drafts, social posts, or content outlines.

### Workflow
1. Identify content purpose.
2. Identify target audience.
3. Check clarity.
4. Check flow.
5. Check tone.
6. Check unsupported claims.
7. Check repetition.
8. Suggest improvements.
9. Create final content checklist.

### Output format

```markdown
# Content Review

## Audience Fit

## Clarity

## Flow

## Tone

## Unsupported Claims

## Repetition

## Suggested Improvements

## Final Checklist
```

### Quality rules
- Avoid overclaiming.
- Avoid biased or offensive framing.
- Mark claims that need verification.
- Preserve intended message.

---

## 13. Simple Example Skill: Research Brief Builder

### Skill name
```text
research-brief-builder
```

### When to use
Use when converting collected notes or source material into a structured research-style brief.

### Workflow
1. Identify topic and scope.
2. Separate known facts from assumptions.
3. Summarize key points.
4. Identify source gaps.
5. Identify conflicting information.
6. Create questions for further verification.
7. Prepare concise brief.

### Output format

```markdown
# Research Brief

## Topic

## Scope

## Confirmed Points

## Unverified Points

## Conflicting Information

## Gaps

## Questions for Verification

## Summary
```

### Quality rules
- Do not present unverified information as fact.
- Mark uncertainty clearly.
- Avoid overconfident wording.
- Preserve source limitations.

---

## 14. Simple Example Skill: Small Tool Planning

### Skill name
```text
small-tool-planner
```

### When to use
Use when planning a small utility, helper script, website, automation helper, or internal tool.

### Workflow
1. Understand the purpose.
2. Define input and output.
3. Identify user steps.
4. Identify safe operating boundaries.
5. Propose folder structure.
6. Propose implementation approach.
7. Add dry-run or sample-data step where needed.
8. Create README outline.
9. Ask for approval before implementation.

### Output format

```markdown
# Tool Plan

## Purpose

## Inputs

## Outputs

## User Workflow

## Folder Structure

## Implementation Approach

## Safety Considerations

## Test Plan

## Approval Required Before
```

### Quality rules
- Do not implement before plan approval if risk exists.
- Prefer dry-run for file operations.
- Do not process real data before testing sample data.
- Include user instructions.

---

## 15. How Skills Support Work Inside VS Code

Explain:

In a VS Code workflow, Skills help Claude Code work repeatedly with the same method.

Example workspace:

```text
professional-workspace/
  input/
  output/
  review/
  CLAUDE.md
  skills-notes/
    meeting-summary-skill-design.md
```

Claude Code can use Skills to:
- create consistent outputs
- follow standard sections
- apply repeated review checks
- avoid repeating long instructions
- support different workflows from the same workspace

### Trainer explanation
“VS Code gives the workspace. `CLAUDE.md` gives project rules. Skills give reusable methods for common tasks.”

---

## 16. When to Create a Skill

Create a Skill when:

- the task repeats often
- the same workflow is used many times
- the same output format is required
- the same quality checks are needed
- the task is important enough to standardize
- multiple people may use the same method
- the instruction is too long to repeat every time

### Good candidates
- meeting summary generation
- document review
- test case generation
- project planning
- research brief preparation
- security checklist review
- content script review
- file indexing
- release note generation
- README creation

### Not good candidates
- one-time small request
- temporary instruction
- sensitive case-specific detail
- unclear workflow
- task with no repeated pattern

---

## 17. Skill Design Checklist

Teach learners this checklist.

Before creating a Skill, ask:

1. What repeated task does this Skill support?
2. When should Claude use it?
3. What inputs does it need?
4. What steps should it follow?
5. What output format should it produce?
6. What quality checks must it perform?
7. What should it never do?
8. What examples would help?
9. Does it need tools?
10. Does tool use require approval?

### Trainer explanation
“A Skill should be specific enough to be useful, but not so narrow that it works for only one file.”

---

## 18. Skill Safety Rules

Skills can be powerful, so they need boundaries.

Include safety rules such as:

- do not invent facts
- do not make final decisions
- do not expose sensitive information
- do not run destructive commands
- do not overwrite source files
- ask before editing important files
- ask before running scripts on real data
- separate facts, assumptions, and missing information
- mark uncertainty clearly
- include review checklist

### Trainer explanation
“If a Skill will be reused, any mistake in the Skill may also be reused. That is why Skill quality and safety matter.”

---

## 19. Skill vs Subagent

Give only a simple preview. Day 8 will cover subagents more deeply.

| Concept | Simple Meaning |
|---|---|
| Skill | A reusable method or capability |
| Subagent | A specialized assistant role for part of a task |

### Example
Skill:
```text
Use document-review workflow.
```

Subagent:
```text
Ask a reviewer agent to check the draft.
```

### Trainer explanation
“A Skill is a method. A subagent is a role. They can work together, but they are not the same.”

---

## 20. Skill vs Tool

Explain:

| Concept | Meaning |
|---|---|
| Skill | Teaches Claude how to perform a task |
| Tool | Lets Claude do something in the environment |

### Example
Skill:
```text
Follow this standard workflow to create test cases.
```

Tool:
```text
Read requirement file, write output file, run tests, open terminal.
```

### Trainer explanation
“A Skill tells Claude what method to follow. A tool allows Claude to act.”

---

## 21. Activity: Design a Skill

Ask learners to design one Skill from the options below:

1. Meeting summary Skill
2. Document review Skill
3. Test case generation Skill
4. Research brief Skill
5. Video script review Skill
6. Project planning Skill
7. Security checklist Skill
8. File indexing Skill

### Skill design template

```markdown
# Skill Name

## When to Use

## Inputs Needed

## Workflow Steps

## Output Format

## Quality Rules

## Do Not Do

## Human Review Required
```

### Review questions
Ask:
- Is the Skill name clear?
- Is the trigger/description clear?
- Are workflow steps specific?
- Is output format defined?
- Are safety rules included?
- Is human review included?
- Is this really reusable?

---

## 22. Example Completed Skill Design

```markdown
# Skill Name
document-review

## When to Use
Use this skill when reviewing a professional document for clarity, completeness, assumptions, and missing information.

## Inputs Needed
- Source document
- Intended audience if available
- Required output format if available

## Workflow Steps
1. Identify document purpose.
2. Summarize current structure.
3. Identify missing information.
4. Identify unclear sections.
5. Identify unsupported assumptions.
6. Suggest improvements.
7. Create review questions.
8. Create final checklist.

## Output Format
- Summary
- Missing Information
- Unclear Sections
- Unsupported Assumptions
- Suggested Improvements
- Review Questions
- Final Checklist

## Quality Rules
- Do not invent missing information.
- Preserve meaning.
- Mark uncertainty clearly.
- Keep tone professional.

## Do Not Do
- Do not make final decisions.
- Do not rewrite the document unless asked.
- Do not expose sensitive information.

## Human Review Required
Human must review the final output before use.
```

---

## 23. Common Mistakes to Correct

### Mistake 1
Making a Skill too vague.

Bad:
```text
Help with documents.
```

Better:
```text
Review documents for clarity, missing information, assumptions, and review questions.
```

### Mistake 2
Putting one-time task details into a Skill.

Correction:
Put reusable method in Skill. Put task-specific details in the prompt.

### Mistake 3
Confusing Skill with memory.

Correction:
Memory stores context. Skill stores method.

### Mistake 4
Confusing Skill with `CLAUDE.md`.

Correction:
`CLAUDE.md` guides project behavior. Skill guides a reusable task type.

### Mistake 5
No safety rules in the Skill.

Correction:
Every important Skill should include do-not-do and review rules.

### Mistake 6
Not testing whether the Skill gives useful output.

Correction:
Try the Skill with sample inputs and review if output is consistent.

---

## 24. Trainer Verbatim Blocks

### Verbatim Block 1
“A Skill is a reusable capability. It teaches Claude how to perform a repeated kind of work.”

### Verbatim Block 2
“If you are repeating the same long instruction again and again, that may be a good candidate for a Skill.”

### Verbatim Block 3
“Memory stores useful context. `CLAUDE.md` stores project rules. A Skill stores a repeatable method.”

### Verbatim Block 4
“Skills are not only for coding. They can support documentation, testing, review, planning, research, content, and analysis.”

### Verbatim Block 5
“A bad Skill can repeat bad behavior. So every Skill needs clear scope, quality rules, and safety boundaries.”

---

## 25. Questions to Ask During Session

Use these questions throughout:

- Is this task repeated often?
- Is there a standard method for doing it?
- What should trigger the Skill?
- What inputs are needed?
- What output format is required?
- What quality checks are required?
- What should the Skill never do?
- Does it need file access or tools?
- Does it require human review?
- Is this a Skill, memory, `CLAUDE.md`, prompt, tool, or subagent?

---

## 26. Day 6 Recap

End with:

“Today we learned that Skills are reusable capabilities. They help Claude Code follow a standard method for repeated tasks.”

Then say:

“We also learned that Skills are not only for coding. Skills can support documentation, planning, review, research-style analysis, testing, content work, small tools, and many professional workflows.”

Then close with:

“In the next session, we will focus on tools, permissions, safety modes, and human approval. That is important because Skills may guide how work is done, but tools allow the agent to act.”

---

## 27. End-of-Session Learner Takeaway

Learners should leave with these five ideas:

1. A Skill is a reusable task capability.
2. Skills reduce repeated long instructions.
3. Skills are different from prompts, memory, `CLAUDE.md`, tools, and subagents.
4. Skills can support general professional work, not only coding.
5. Good Skills need scope, workflow steps, output format, safety rules, and human review.

---

## 28. Suggested Homework

Ask learners to design one Skill for a repeated work task.

They should use this structure:

```markdown
# Skill Name

## When to Use

## Inputs Needed

## Workflow Steps

## Output Format

## Quality Rules

## Do Not Do

## Human Review Required
```

They should bring the Skill design to Day 7 discussion.

---

## 29. Final Trainer Reminder

Day 6 is successful if the learner can explain:

**A Skill is a reusable method that helps Claude Code perform a repeated type of work consistently.**

They should also understand:

**Skills are useful only when they are clear, safe, reviewable, and reusable.**
