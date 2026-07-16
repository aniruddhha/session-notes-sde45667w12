# Phase 3 -> Day 5
## Memory in Claude Code: Project Memory, Local Memory, User Preferences, and Long-Term Work Context
### Trainer Session Notes

**Session Duration:** 1 hour 30 minutes  
**Session Mode:** 20% Theory | 80% Hands-On Discussion / Demonstration  
**Primary Environment:** VS Code  
**Primary Tool Focus:** Claude Code  
**Important Framing:** Claude Code is taught as a general-purpose agentic work assistant, not only a coding tool.

---

## 1. Session Goal for the Trainer

By the end of this session, learners should understand:

- what memory means in Claude Code workflows
- why memory is useful for repeated professional work
- how memory differs from prompt, `CLAUDE.md`, and skills
- what project memory is
- what local memory is
- what user preferences are
- what long-term work context means
- what should be remembered and what should not be remembered
- how memory can improve documentation, planning, review, testing, content, and coding workflows
- why memory must be handled carefully for privacy and accuracy

**Trainer objective:**  
Day 5 should make learners understand that memory is useful, but not everything should be remembered. Memory should improve repeated work without storing unnecessary sensitive, temporary, or risky information.

---

## 2. Recommended Session Flow

| Time | Segment | Mode |
|---|---|---|
| 0-8 min | Recap Day 4 and introduce memory | Theory |
| 8-20 min | What memory means in Claude Code workflows | Theory |
| 20-34 min | Prompt vs `CLAUDE.md` vs memory vs skill | Theory + examples |
| 34-48 min | Project memory, local memory, and user preferences | Demonstration discussion |
| 48-62 min | Good memory vs bad memory examples | Hands-on style discussion |
| 62-74 min | Privacy, sensitivity, and memory safety | Discussion |
| 74-84 min | Activity: decide what should be remembered | Hands-on discussion |
| 84-88 min | Recap and connection to Day 6 | Recap |
| 88-90 min | Closing task | Wrap-up |

---

## 3. Opening Script Notes for Yourself

Start with:

“On Day 4, we learned about `CLAUDE.md`, which acts like the project rulebook. Today we will learn about memory, which helps Claude Code remember useful context across work.”

Then say:

“Memory is powerful because it can reduce repeated explanation. But it must be used carefully. We should remember stable, useful working preferences — not sensitive, temporary, or unverified information.”

Then add:

“Today’s goal is not just to learn what memory is. The goal is to learn what should be remembered, what should not be remembered, and how memory affects agentic work.”

---

## 4. Core Theory: What Is Memory?

Explain simply:

**Memory is stored context that helps Claude Code work more consistently across repeated tasks.**

In normal prompting, the user gives information each time.

With memory, some useful information can be retained so the user does not need to repeat it again and again.

### Simple example

Without memory:
```text
Every time, the user says:
Create trainer notes as downloadable Markdown files.
Use 1h30m format.
Use theory plus hands-on structure.
Do not render full content in chat.
```

With memory:
```text
Claude already knows this repeated preference and can follow it in future work.
```

### Verbatim explanation
“Memory is useful when a preference or project context is stable enough that repeating it every time becomes unnecessary.”

---

## 5. Why Memory Matters in Agentic Work

Memory matters because agentic workflows often continue across multiple sessions or multiple tasks.

Examples:
- same output format is used repeatedly
- same folder rules are followed repeatedly
- same review style is required
- same safety rules are important
- same project conventions continue
- same user preferences apply
- same domain caution is needed

### Trainer explanation
“In agentic work, memory helps the assistant act more like a consistent project helper instead of a fresh assistant every time.”

---

## 6. Prompt vs `CLAUDE.md` vs Memory vs Skill

Review this carefully.

| Concept | Purpose | Example |
|---|---|---|
| Prompt | One-time task instruction | “Create today’s session notes.” |
| `CLAUDE.md` | Project-level working rules | “Save output in output/ and do not modify input files.” |
| Memory | Useful remembered preference or context | “User prefers downloadable Markdown files.” |
| Skill | Reusable method for a type of work | “Generate test cases from requirements.” |

### Verbatim explanation
“A prompt is for now. `CLAUDE.md` is for this project. Memory is for repeated useful context. A skill is a reusable capability.”

### Example
Prompt:
```text
Create a 1-page project summary.
```

`CLAUDE.md`:
```markdown
Save summaries in output/. Use professional tone. Do not invent missing information.
```

Memory:
```text
User prefers concise Markdown deliverables.
```

Skill:
```text
Project summary generation skill with standard sections.
```

---

## 7. Types of Memory to Explain

### 7.1 Project Memory

Project memory relates to the current project or workspace.

Examples:
- project purpose
- output format
- folder rules
- review checklist
- naming convention
- workflow steps
- repeated constraints

Example:
```text
For this training project, create each session as a downloadable Markdown file with trainer script, activities, and recap.
```

### 7.2 Local Memory

Local memory is useful for machine-specific, workspace-specific, or environment-specific context.

Examples:
- project runs on a specific local folder
- VS Code workspace structure
- local script location
- local tool command preference
- local operating system detail

Example:
```text
This workspace uses VS Code, and generated notes are stored in the output/ folder.
```

### 7.3 User Preferences

User preferences are stable ways the user wants work to be done.

Examples:
- prefers short final replies
- prefers downloadable files
- prefers Markdown
- prefers detailed trainer notes
- prefers approval before next large content
- prefers practical examples

Example:
```text
User prefers full content in downloadable files rather than rendered in chat.
```

### 7.4 Long-Term Work Context

Long-term work context is broader project continuity.

Examples:
- completed phases
- current phase direction
- future phase direction
- ongoing course structure
- repeated safety standards
- audience style preference
- domain-specific framing rules

Example:
```text
The current course has completed Phase 1 and Phase 2. Phase 3 focuses on Claude Code theory using VS Code.
```

---

## 8. What Should Be Remembered?

Teach that memory should be:

- stable
- useful in future
- non-sensitive
- relevant to repeated work
- unlikely to change quickly
- helpful for quality or consistency

### Good memory examples

#### Course workflow preference
```text
User wants trainer notes as downloadable Markdown files.
```

#### Output style preference
```text
User prefers practical trainer-facing notes with scripts, activities, and session flow.
```

#### Workspace direction
```text
Claude Code sessions should use VS Code as the environment.
```

#### Framing rule
```text
Claude Code should be framed as a general-purpose agentic work assistant, not only a coding tool.
```

#### Safety preference
```text
Ask for approval before generating the next large day file.
```

### Trainer explanation
“Good memory reduces repeated instruction without creating privacy or accuracy risk.”

---

## 9. What Should Not Be Remembered?

Memory should not store everything.

Avoid remembering:

- confidential data
- passwords
- API keys
- private personal details
- temporary decisions
- unverified facts
- sensitive case details
- one-time instructions
- information that may change soon
- personal data that is not needed later

### Bad memory examples

#### Sensitive
```text
Remember this person’s private phone number and case details.
```

#### Temporary
```text
Remember that tomorrow I am free at 3 PM.
```

#### Secret
```text
Remember this API key.
```

#### Unverified
```text
Remember that this vendor is responsible for the failure.
```

#### Too personal
```text
Remember private family or health details that are not relevant to future tasks.
```

### Trainer explanation
“Memory is not a dumping ground. It is a controlled place for stable, useful, safe context.”

---

## 10. Memory Safety Rules

Give these rules clearly.

### Rule 1: Remember stable preferences, not temporary facts
Good:
```text
User prefers Markdown output.
```

Avoid:
```text
User wants this exact file by 4 PM today.
```

### Rule 2: Do not remember secrets
Never store:
- passwords
- tokens
- keys
- private credentials
- confidential access details

### Rule 3: Do not remember sensitive personal details unless clearly required
Avoid unnecessary personal, medical, legal, or private identity details.

### Rule 4: Do not remember unverified claims
Memory should not preserve assumptions as facts.

### Rule 5: Keep memory useful
Memory should improve future work.

### Rule 6: Update memory when direction changes
Example:
If the environment changes from Antigravity to VS Code, memory must be updated.

### Rule 7: Remove outdated memory
Old project rules can harm future output.

---

## 11. Memory in VS Code + Claude Code Workflow

Explain how memory supports work inside VS Code.

### Example workspace

```text
training-course/
  phase-3/
    day-01.md
    day-02.md
    day-03.md
  output/
  review/
  CLAUDE.md
```

Memory can help Claude Code remember:
- this is a training course project
- files should be Markdown
- each day should be trainer-facing
- the environment is VS Code
- content should avoid unnecessary technical jargon
- Claude Code is taught as general-purpose assistant
- next phase will be practical demos

### Important distinction
`CLAUDE.md` belongs to the project.  
Memory may apply across repeated sessions or broader workflow.

### Trainer explanation
“In VS Code, `CLAUDE.md` guides the workspace. Memory helps carry useful repeated preferences across sessions.”

---

## 12. Memory Use Cases Beyond Coding

Reinforce general-purpose usage.

### Documentation workflow
Memory can remember:
- preferred document structure
- tone
- output format
- review checklist

### Planning workflow
Memory can remember:
- plan format
- risk register style
- approval-first approach

### Testing workflow
Memory can remember:
- preferred test case columns
- need for positive, negative, and edge cases
- traceability preference

### Content workflow
Memory can remember:
- preferred script style
- audience tone
- avoid overclaiming
- include review checklist

### File organization workflow
Memory can remember:
- use dry-run first
- never delete files directly
- create before/after index

### Coding workflow
Memory can remember:
- coding style
- test command
- review before edit
- documentation requirement

---

## 13. Example: Memory vs `CLAUDE.md` Decision

### Scenario
The user says:
“Always create outputs in Markdown for this project.”

Where should it go?

Answer:
- Put in `CLAUDE.md` if it applies to the current project.
- Put in memory if it is the user’s stable preference across many projects.

### Scenario
The user says:
“For this one file, use a short summary.”

Where should it go?

Answer:
- Prompt only.
- Not memory.
- Not necessarily `CLAUDE.md`.

### Scenario
The user says:
“For all testing outputs, use columns: Test ID, Scenario, Steps, Expected Result.”

Where should it go?

Answer:
- Could go into `CLAUDE.md` for a testing project.
- Could go into memory if the user always wants this format.

### Scenario
The user says:
“Do not modify original files unless I approve.”

Where should it go?

Answer:
- Strong candidate for `CLAUDE.md`.
- Also may be remembered as a stable working preference.

---

## 14. Activity: Should This Be Remembered?

Ask learners to classify each item as:

- Remember
- Put in `CLAUDE.md`
- Prompt only
- Do not store

### Items

1. “Use Markdown format for all trainer notes.”
2. “My password is X.”
3. “Today’s task is to create Day 5 notes.”
4. “For this project, do not modify input files.”
5. “The user prefers approval before generating next large file.”
6. “This person is guilty.”
7. “Use VS Code as the environment for Claude Code course.”
8. “The final answer should be short with a download link.”
9. “Run this command only once today.”
10. “Always separate facts, assumptions, and missing information.”

### Suggested answer

| Item | Suggested Handling |
|---|---|
| 1 | Remember or `CLAUDE.md` |
| 2 | Do not store |
| 3 | Prompt only |
| 4 | `CLAUDE.md` |
| 5 | Remember |
| 6 | Do not store |
| 7 | Remember and project instruction |
| 8 | Remember if stable |
| 9 | Prompt only |
| 10 | Remember or `CLAUDE.md` |

---

## 15. Demonstration Discussion: Updating Memory When Direction Changes

Use this example because it is practical.

### Old direction
```text
Use Antigravity as the environment.
```

### New direction
```text
Use VS Code as the environment.
```

Explain:

If memory is not updated, future outputs may continue using the wrong environment.

### Trainer explanation
“Memory is useful only when it is current. Outdated memory creates repeated mistakes.”

### Correct memory update
```text
For this course, use VS Code as the environment for Claude Code sessions. Do not use Antigravity unless specifically asked.
```

---

## 16. Memory and Trust

Explain:

Memory affects trust because the assistant may act based on remembered context.

Good memory creates:
- consistency
- speed
- less repetition
- better continuity
- fewer format corrections

Bad memory creates:
- wrong assumptions
- privacy risk
- repeated mistakes
- outdated outputs
- user frustration

### Verbatim explanation
“Memory should make the assistant more reliable, not more presumptive.”

---

## 17. How to Talk to Claude Code About Memory

Teach learners practical language.

### To save useful context
```text
Remember that for this project, all outputs should be created in Markdown.
```

### To update direction
```text
Update the project context: we are using VS Code, not Antigravity.
```

### To avoid memory
```text
Use this only for the current task. Do not remember it.
```

### To remove outdated memory
```text
Forget the old instruction about using Antigravity for this course.
```

### To clarify scope
```text
Remember this only for the current project, not for all future work.
```

### Trainer point
Users should be specific about whether something is:
- current task only
- project-level instruction
- long-term preference

---

## 18. Common Mistakes to Correct

### Mistake 1
Trying to remember every detail.

Correction:
Remember only stable, useful, future-relevant context.

### Mistake 2
Putting task-specific details into memory.

Correction:
Use prompt for one-time task details.

### Mistake 3
Storing sensitive information.

Correction:
Never store secrets, credentials, or unnecessary private data.

### Mistake 4
Confusing memory with `CLAUDE.md`.

Correction:
`CLAUDE.md` is project rulebook. Memory is retained preference or context.

### Mistake 5
Not updating memory after project direction changes.

Correction:
Update memory when tools, format, phase plan, or workflow changes.

### Mistake 6
Allowing memory to become hidden assumption.

Correction:
Ask Claude Code to state relevant remembered context when starting major work.

---

## 19. Trainer Verbatim Blocks

### Verbatim Block 1
“Memory is useful when it saves repeated explanation without creating privacy or accuracy risk.”

### Verbatim Block 2
“Not everything should be remembered. Temporary, sensitive, or unverified information should not go into memory.”

### Verbatim Block 3
“`CLAUDE.md` guides the project. Memory carries stable preferences and useful long-term context.”

### Verbatim Block 4
“Outdated memory can be worse than no memory because it repeats the same wrong assumption.”

### Verbatim Block 5
“Memory should support human control, not replace human judgment.”

---

## 20. Questions to Ask During Session

Use these questions throughout:

- Is this information stable?
- Will it be useful in future work?
- Is it sensitive?
- Is it temporary?
- Is it verified?
- Should it go in the prompt, `CLAUDE.md`, memory, or skill?
- Could remembering this create risk?
- Is this project-level or user-level preference?
- Should old memory be updated?
- Will this memory improve consistency?

---

## 21. Day 5 Recap

End with:

“Today we learned that memory helps Claude Code maintain useful context across repeated work. Memory can improve consistency, reduce repeated explanation, and support long-term workflows.”

Then say:

“We also learned that memory must be controlled. Good memory is stable, useful, and safe. Bad memory is sensitive, temporary, outdated, or unverified.”

Then close with:

“In the next session, we will focus on skills in Claude Code: reusable capabilities for writing, review, research, documentation, coding, testing, and analysis.”

---

## 22. End-of-Session Learner Takeaway

Learners should leave with these five ideas:

1. Memory stores useful context for repeated work.
2. Memory is different from prompt, `CLAUDE.md`, and skills.
3. Good memory is stable, useful, non-sensitive, and future-relevant.
4. Sensitive, temporary, or unverified information should not be remembered.
5. Memory must be updated when project direction changes.

---

## 23. Suggested Homework

Ask learners to create two lists for a sample project:

### List A: Things worth remembering
Examples:
- output format
- review style
- workspace environment
- approval preference
- repeated safety rule

### List B: Things not worth remembering
Examples:
- one-time task details
- passwords
- confidential case facts
- unverified assumptions
- temporary schedule details

Then ask them to decide where each useful item belongs:
- prompt
- `CLAUDE.md`
- memory
- skill

---

## 24. Final Trainer Reminder

Day 5 is successful if the learner can explain:

**Memory is useful remembered context, but it must be stable, safe, and genuinely helpful.**

They should also understand:

**The correct question is not “Can this be remembered?” but “Should this be remembered?”**
