# Phase 3 -> Day 2
## Claude Code Mental Model: Agent Loop, Tools, Context, Files, and Human Control
### Trainer Session Notes

**Session Duration:** 1 hour 30 minutes  
**Session Mode:** 20% Theory | 80% Hands-On Discussion / Demonstration  
**Primary Environment:** Antigravity  
**Primary Tool Focus:** Claude Code  
**Important Framing:** Claude Code is taught as a general-purpose agentic work assistant, not only a coding tool.

---

## 1. Session Goal for the Trainer

By the end of this session, learners should understand:

- how Claude Code works at a high level
- what an agent loop means
- how Claude Code uses context, files, instructions, and tools
- why agentic work is different from normal chat
- how Claude Code can support general professional workflows
- why human control is essential when an agent can read, write, or execute actions
- how Antigravity helps make agent work visible through editor, terminal, browser, and artifacts
- how to decide when a task needs stronger human review

**Trainer objective:**  
Today should give learners a mental model. They do not need deep technical internals yet. They need to understand the workflow logic:

**goal -> context -> plan -> tool use -> output -> review -> next step**

---

## 2. Recommended Session Flow

| Time | Segment | Mode |
|---|---|---|
| 0-8 min | Recap Day 1 + introduce Day 2 mental model | Theory |
| 8-22 min | What the agent loop means | Theory |
| 22-36 min | Context: prompt, files, instructions, memory, and environment | Theory + examples |
| 36-50 min | Tools: read, write, terminal, browser, search, external systems | Demonstration discussion |
| 50-62 min | Files and workspace understanding | Hands-on style discussion |
| 62-74 min | Human control, permission, approval, and safe boundaries | Discussion |
| 74-84 min | Activity: map tasks into an agent loop | Hands-on discussion |
| 84-88 min | Recap: how Day 2 connects to Day 3 | Recap |
| 88-90 min | Closing task | Wrap-up |

---

## 3. Opening Script Notes for Yourself

Start with:

“Yesterday we understood Claude Code as a general-purpose agentic work assistant, not only as a coding assistant. Today we will understand how this agent actually works at a high level.”

Then say:

“The most important idea today is the agent loop. Claude Code is useful because it can take a goal, inspect context, plan steps, use tools, create or modify outputs, and then wait for human review or continue.”

Then add:

“This is powerful, but it also means the human must define boundaries. When an assistant can act on files or tools, we need review, permission, and control.”

---

## 4. Core Theory: What Is a Mental Model?

Explain:

**A mental model is a simple way to understand how something works so that we can use it correctly.**

For Claude Code, the mental model is not:

“Ask question, get answer.”

The better mental model is:

“Give a goal, provide context, let the agent plan, use tools when permitted, produce output, and review before continuing.”

### Verbatim explanation
“Claude Code is not just a text box. It is closer to an assistant working inside a workspace. That assistant can read context, inspect files, use tools, and help complete multi-step work.”

---

## 5. The Claude Code Agent Loop

Teach this as the central concept.

### Simple agent loop

```text
User Goal
   ↓
Understand Task
   ↓
Read Context
   ↓
Plan Steps
   ↓
Use Allowed Tools
   ↓
Create / Modify / Analyze Output
   ↓
Human Review
   ↓
Continue / Correct / Stop
```

### Explain each stage

#### 1. User Goal
The human gives a goal.

Examples:
- “Review this folder and create a file index.”
- “Read this policy draft and create a checklist.”
- “Prepare a training plan from these notes.”
- “Build a small webpage for this requirement.”
- “Explain this project structure.”

#### 2. Understand Task
The agent interprets what is being asked.

It should identify:
- task type
- output expected
- files required
- tools needed
- risk level
- whether clarification is needed

#### 3. Read Context
The agent uses available context.

Context can include:
- user prompt
- open files
- project files
- instructions
- memory
- previous conversation
- workspace state
- terminal output
- browser output
- artifacts

#### 4. Plan Steps
The agent decides how to approach the task.

For example:
- inspect folder
- identify files
- read key documents
- create outline
- generate draft
- review draft
- save output

#### 5. Use Allowed Tools
The agent may use tools, depending on permissions.

Tools may include:
- read file
- write file
- edit file
- list directory
- run terminal command
- open browser
- generate artifact
- run tests
- call external integration

#### 6. Create / Modify / Analyze Output
The agent produces something useful.

Output can be:
- document
- report
- checklist
- summary
- plan
- code
- table
- file index
- test plan
- diff
- screenshot
- browser result
- task list

#### 7. Human Review
The human checks:
- accuracy
- safety
- privacy
- output quality
- whether changes are acceptable
- whether the agent should continue

#### 8. Continue / Correct / Stop
The user may:
- approve next step
- ask for changes
- reject output
- stop workflow
- request deeper analysis

---

## 6. Why the Agent Loop Matters

Explain:

The agent loop matters because it changes how we instruct AI.

In normal chat:
- prompt quality matters

In agentic work:
- prompt quality matters
- file context matters
- instructions matter
- permissions matter
- tool safety matters
- review matters
- workflow design matters

### Verbatim explanation
“Agentic work is not only about the first prompt. It is about the full loop: what the agent sees, what it does, what it changes, and what the human approves.”

---

## 7. Context: The Fuel of Agentic Work

Explain:

**Context is the information available to the agent when it works.**

If context is poor, the agent may:
- misunderstand task
- miss important files
- produce generic output
- make wrong assumptions
- modify wrong things
- ask unnecessary questions

If context is good, the agent can:
- understand project structure
- follow standards
- reuse existing work
- create consistent outputs
- reduce assumptions
- produce better results

---

## 8. Types of Context Claude Code May Use

### 8.1 User prompt context
The immediate instruction.

Example:
“Create a neutral summary of this document and list missing information.”

### 8.2 File context
Files inside the workspace.

Examples:
- Markdown files
- code files
- requirements
- notes
- reports
- checklists

### 8.3 Project instruction context
Rules such as `CLAUDE.md`.

Examples:
- output format
- writing tone
- review rules
- naming conventions
- coding standards
- safety constraints

### 8.4 Memory context
Reusable remembered preferences or project facts.

Examples:
- preferred file naming style
- trainer note structure
- output should be downloadable Markdown
- do not expose sensitive data
- always separate assumptions from facts

### 8.5 Tool output context
Information returned from tools.

Examples:
- terminal command output
- test results
- directory listing
- browser screenshot
- file search result
- linting report

### 8.6 Artifact context
Reviewable outputs.

Examples:
- plan
- task list
- diff
- screenshot
- generated report
- validation output

---

## 9. Context Quality Examples

### Weak context
“Make this better.”

Problem:
The agent does not know:
- what “this” is
- what better means
- output format
- audience
- constraints
- risk level

### Better context
“Review the attached meeting notes and create a 1-page action summary in Markdown. Use sections: decisions, pending items, risks, owners, and next steps. Do not invent missing owners. Mark missing information clearly.”

Why better:
- task is clear
- source is clear
- format is clear
- constraints are clear
- missing information rule is clear

### Trainer explanation
“Agentic work improves when we give the agent enough context to act, but not unnecessary sensitive information.”

---

## 10. Files and Workspace Understanding

Claude Code-style workflows become useful because the agent can work with files.

Explain:

Files are not just attachments. In an agentic workflow, files may become:
- source material
- instructions
- output destination
- evidence for validation
- configuration
- project memory
- generated artifact

### Examples

#### Document workflow
Input files:
- raw notes
- old draft
- checklist

Output files:
- final summary
- missing information list
- revised draft

#### File organization workflow
Input:
- folder tree
- filenames
- file metadata

Output:
- index file
- proposed restructure plan
- safe dry-run report
- rename script

#### Software testing workflow
Input:
- requirement document
- existing test cases
- bug reports

Output:
- test checklist
- missing scenarios
- test data plan
- traceability table

#### Content workflow
Input:
- topic notes
- audience profile
- rough script

Output:
- video outline
- script
- review checklist

---

## 11. Tools: What Tools Mean in Claude Code Thinking

Explain:

**A tool is something the agent can use to gather information, inspect the workspace, modify output, or perform an action.**

Claude Code is known for tool-based workflows such as reading a codebase, editing files, running commands, and integrating with development tools. In this course, teach tools as broader work capabilities.

### Tool categories

#### Read tools
Used to inspect:
- files
- folders
- documents
- logs
- previous outputs

#### Write tools
Used to create or modify:
- Markdown documents
- scripts
- configuration files
- reports
- README files
- checklists

#### Terminal tools
Used to:
- run commands
- execute scripts
- check file structure
- run tests
- install dependencies
- inspect outputs

#### Browser tools
Used to:
- preview websites
- validate UI
- inspect pages
- compare visual result
- review browser output

#### External integration tools
Used to connect to:
- APIs
- databases
- issue trackers
- documentation systems
- file systems
- internal tools

---

## 12. Tools Are Powerful, So Permission Matters

Explain:

When an AI can use tools, there is more value but also more risk.

### Low-risk tool usage
- reading a non-sensitive file
- summarizing a document
- creating a new draft file
- listing a directory
- generating a checklist

### Medium-risk tool usage
- editing existing files
- running a known script
- changing documentation
- creating multiple files
- renaming files in a controlled way

### High-risk tool usage
- deleting files
- moving large folder structures
- running unknown commands
- modifying production code
- sending data outside the workspace
- changing security settings
- installing packages without review
- executing commands that affect the system

### Trainer explanation
“Tool use must be reviewed based on risk. Reading a file and deleting a folder are not the same level of action.”

---

## 13. Human Control: The Central Safety Layer

Teach this strongly.

**Human control means the human defines goals, sets boundaries, approves risky actions, reviews outputs, and owns final use.**

### Human control points
- before giving sensitive data
- before allowing file edits
- before running commands
- before accepting generated output
- before applying final decision
- before sending communication
- before committing code
- before executing automation

### Verbatim explanation
“The agent may help do the work, but the human must remain the owner of the workflow.”

---

## 14. Antigravity and Visibility

Antigravity is useful because agentic work should be visible.

Antigravity should be taught as an environment where the agent can operate across:
- editor
- terminal
- browser
- artifacts
- task plans
- workspace outputs

For learners, explain:

Antigravity helps make agent work reviewable through:
- editor changes
- terminal outputs
- browser results
- plans
- task lists
- artifacts
- diffs
- screenshots or recordings where available
- agent manager view

### Trainer explanation
“Visibility is important. If an agent works invisibly, the user cannot properly review it. Antigravity helps show what the agent planned, did, and produced.”

---

## 15. Same Task: Chatbot vs Agent Loop

### Task
“Prepare a project summary from a folder.”

### Chatbot mode
1. User pastes text.
2. AI summarizes.
3. User manually saves output.

### Agent loop mode
1. User gives goal.
2. Agent lists folder files.
3. Agent reads relevant files.
4. Agent identifies structure.
5. Agent creates summary plan.
6. Human reviews plan.
7. Agent creates Markdown summary.
8. Agent lists missing information.
9. Human reviews file.
10. Agent revises if needed.

### Key teaching point
Agentic work is more structured and more powerful, but requires more review.

---

## 16. General Professional Task Examples

### Example 1: Document review
Goal:
“Review these documents and create a missing-information checklist.”

Agent loop:
- list files
- read documents
- identify required sections
- compare actual vs expected
- create checklist
- human validates

### Example 2: Planning
Goal:
“Create a 5-day implementation plan from this rough requirement.”

Agent loop:
- read requirement
- identify deliverables
- create plan
- identify risks
- create checklist
- human approves

### Example 3: File restructuring
Goal:
“Create a safe plan to flatten this folder structure.”

Agent loop:
- inspect folder
- generate current index
- propose rename rules
- create dry-run
- wait for approval
- execute only after permission
- create after-index

### Example 4: Testing support
Goal:
“Create test scenarios from this requirement file.”

Agent loop:
- read requirement
- identify features
- create positive/negative/edge cases
- map tests to requirements
- human validates

### Example 5: Content workflow
Goal:
“Create a video content plan from these notes.”

Agent loop:
- read notes
- identify audience
- create outline
- create script draft
- create review checklist
- human edits

---

## 17. Activity: Map a Task into an Agent Loop

Ask learners to pick one task and fill this structure:

| Agent Loop Stage | Learner Response |
|---|---|
| Goal | What is the task? |
| Context | What files or information are needed? |
| Instructions | What rules should the agent follow? |
| Tools | What tools may be needed? |
| Risk | What can go wrong? |
| Permission | What should require human approval? |
| Output | What should be created? |
| Review | What must the human check? |
| Next Step | Continue, revise, approve, or stop? |

### Example task
“Create an index of all files in a project folder.”

Expected mapping:
- Goal: create folder/file index
- Context: folder structure
- Instructions: include all levels, file type, path
- Tools: list directory, read metadata
- Risk: missing files, wrong path
- Permission: no deletion or movement
- Output: Markdown or Excel index
- Review: check completeness
- Next step: approve or ask for restructuring plan

---

## 18. Strong vs Weak Agent Instructions

### Weak instruction
“Check this project.”

### Better instruction
“Inspect the project folder. Create a Markdown summary of folder structure, important files, missing documentation, and suggested next steps. Do not modify files. Ask before running commands that change anything.”

### Weak instruction
“Fix this.”

### Better instruction
“Analyze the issue first. Explain likely cause, list files that may need changes, propose a plan, and wait for approval before editing.”

### Weak instruction
“Create final report.”

### Better instruction
“Create a first-draft report using only the provided documents. Separate confirmed facts, assumptions, missing information, and review questions. Do not make final decisions.”

### Trainer point
Agent instructions should include:
- task
- context
- allowed actions
- prohibited actions
- output format
- review requirement

---

## 19. Risk Thinking in the Agent Loop

Teach learners to ask:

### Before starting
- Is the data sensitive?
- Is the task high-risk?
- Should data be redacted?
- Should the agent only read files?

### During planning
- Is the agent planning safe steps?
- Is the plan too broad?
- Does it include risky commands?
- Does it need approval?

### During tool use
- Is the tool read-only or write-capable?
- Is the command reversible?
- Could it delete or expose data?
- Should the human approve first?

### After output
- Is the output accurate?
- Did it invent details?
- Did it change meaning?
- Does a human need to approve?

---

## 20. Common Mistakes to Correct

### Mistake 1
Giving a vague goal and expecting perfect output.

Correction:
Give clear task, context, constraints, and review expectations.

### Mistake 2
Allowing tool use without understanding risk.

Correction:
Separate read-only actions from write or execution actions.

### Mistake 3
Letting the agent decide final action.

Correction:
Use the agent for decision support, not final decision ownership.

### Mistake 4
Not checking what files the agent used.

Correction:
Ask for source list and output basis.

### Mistake 5
Treating Antigravity output as automatically correct.

Correction:
Artifacts and outputs must be reviewed.

---

## 21. Trainer Verbatim Blocks

### Verbatim Block 1
“The agent loop is the basic mental model: goal, context, plan, tool use, output, human review, and next step.”

### Verbatim Block 2
“Context is the fuel of agentic work. If the agent has poor context, it may produce poor output or make wrong assumptions.”

### Verbatim Block 3
“Tools make the agent powerful, but permissions make the agent safe.”

### Verbatim Block 4
“The human is not outside the workflow. The human is the control layer of the workflow.”

### Verbatim Block 5
“Agentic work is not about giving AI unlimited freedom. It is about giving AI useful work inside clear boundaries.”

---

## 22. Questions to Ask During Session

Use these questions throughout:

- What is the goal?
- What context does the agent need?
- What files should it inspect?
- What tools might be needed?
- What should it not do?
- What output should it create?
- What needs human approval?
- What could go wrong?
- What should be validated?
- Should this be a chatbot task or an agentic workflow?

---

## 23. Closing Recap

End with:

“Today we learned the Claude Code mental model. The main idea is the agent loop: the user gives a goal, the agent reads context, plans steps, uses allowed tools, creates output, and the human reviews before continuing.”

Then say:

“We also learned that context, files, tools, and permissions are central to agentic work. This is why Claude Code should be used with clear instructions and human control.”

Then close with:

“In the next session, we will focus on Antigravity as an agent workspace: editor, terminal, browser, artifacts, and agent manager.”

---

## 24. End-of-Session Learner Takeaway

Learners should leave with these five ideas:

1. Claude Code works through an agent loop.
2. Context quality strongly affects output quality.
3. Tools allow the agent to act, so permissions matter.
4. Files are part of the working environment, not just attachments.
5. Human review and approval are the control layer.

---

## 25. Suggested Homework

Ask learners to choose one real work task and map it into the agent loop:

- goal
- context
- files
- tools
- risk
- permission
- output
- review

They should bring this mapping to Day 3.

---

## 26. Final Trainer Reminder

Day 2 is successful if the learner can explain:

**Claude Code works through a loop of goal, context, planning, tool use, output, and human review.**

They should also understand:

**The agent is useful because it can act, but safe because the human controls what it can do.**
