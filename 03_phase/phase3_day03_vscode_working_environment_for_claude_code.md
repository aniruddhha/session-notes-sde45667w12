# Phase 3 -> Day 3
## VS Code as the Working Environment for Claude Code
### Trainer Session Notes

**Session Duration:** 1 hour 30 minutes  
**Session Mode:** 20% Theory | 80% Hands-On Discussion / Demonstration  
**Primary Environment:** VS Code  
**Primary Tool Focus:** Claude Code  
**Important Framing:** Claude Code is taught as a general-purpose agentic work assistant, not only a coding tool.

---

## 1. Session Goal for the Trainer

By the end of this session, learners should understand:

- why VS Code is a useful working environment for Claude Code
- how VS Code supports file-based, project-based, and workflow-based AI work
- how Claude Code can work with project folders, files, terminal, and instructions
- why folder structure matters when working with an agentic assistant
- how VS Code helps users review files, changes, outputs, and project context
- how Claude Code can support documentation, planning, review, testing, automation support, content work, and coding inside VS Code
- why human review is still required even when the agent works inside a familiar editor

**Trainer objective:**  
Day 3 should make learners comfortable with the idea that VS Code is not only a coding editor. In this course, VS Code should be presented as a **professional workspace** where Claude Code can help with many types of work involving files, folders, instructions, terminal commands, and generated outputs.

---

## 2. Recommended Session Flow

| Time | Segment | Mode |
|---|---|---|
| 0-8 min | Recap Day 2 and introduce VS Code workspace idea | Theory |
| 8-20 min | Why VS Code is useful for Claude Code workflows | Theory |
| 20-34 min | VS Code workspace basics: folders, files, explorer, editor, terminal | Demonstration |
| 34-48 min | Claude Code working model inside a project folder | Demonstration discussion |
| 48-62 min | General-purpose work examples in VS Code | Hands-on style discussion |
| 62-74 min | Reviewing outputs, file changes, and terminal results | Demonstration discussion |
| 74-84 min | Activity: design a clean workspace for an agent task | Hands-on discussion |
| 84-88 min | Recap and connection to Day 4 | Recap |
| 88-90 min | Closing task | Wrap-up |

---

## 3. Opening Script Notes for Yourself

Start with:

“On Day 1, we understood Claude Code as a general-purpose agentic assistant. On Day 2, we understood the agent loop: goal, context, plan, tool use, output, and human review. Today we will understand the workspace where this kind of work can happen: VS Code.”

Then say:

“Many people think VS Code is only for software development. In this course, we will use VS Code more broadly. It can become a structured workspace for documents, notes, project files, checklists, scripts, websites, test plans, and AI-assisted workflows.”

Then add:

“Claude Code becomes more useful when the workspace is clean, files are organized, instructions are clear, and the human can review what the agent is doing.”

---

## 4. Core Theory: Why VS Code?

Explain:

**VS Code is useful because it brings files, folders, editor, terminal, extensions, and project workspace into one place.**

For Claude Code, this matters because agentic work often depends on:

- reading files
- understanding folder structure
- creating new files
- editing existing files
- using terminal commands
- reviewing generated output
- maintaining project-level instructions
- validating the result

### Trainer explanation
“Claude Code works better when the work is organized as a project. VS Code helps us create that project workspace.”

---

## 5. VS Code as a Professional Workspace

Make this point clear:

VS Code is not only for writing code.

It can be used for:

- Markdown documentation
- project plans
- meeting notes
- requirements
- test cases
- checklists
- training material
- data-cleaning scripts
- content scripts
- website files
- automation helpers
- security notes
- review reports

### Verbatim explanation
“In this course, VS Code is our workbench. Coding is one activity on that workbench, but documentation, planning, reviewing, organizing, and testing are also important activities.”

---

## 6. Main VS Code Areas to Explain

### 6.1 Explorer
The Explorer shows the project folder, files, and subfolders.

Explain:
- It helps users see the project structure.
- It helps Claude Code understand available files when working in the folder.
- It makes file organization visible.

### 6.2 Editor
The editor is where files are opened, read, edited, and reviewed.

Explain:
- Markdown files can be written and reviewed.
- Code files can be created or updated.
- Notes and plans can be refined.
- Output from Claude Code should be reviewed here.

### 6.3 Integrated Terminal
The terminal allows commands to be run inside the workspace.

Explain:
- Claude Code may suggest or run commands depending on permissions.
- Terminal output becomes useful context.
- Commands must be reviewed before running if they are risky.

### 6.4 Search
VS Code search helps find words, files, TODOs, headings, references, and project content.

Explain:
- Search helps humans verify agent output.
- Search helps locate files before asking Claude Code to work.
- Search can be used for review and validation.

### 6.5 Source Control
Source control helps track changes.

Explain:
- It is especially useful when Claude Code edits files.
- Users can inspect changes before accepting them.
- It helps avoid losing control over modifications.

### 6.6 Extensions
Extensions can support Markdown preview, formatting, testing, language support, and productivity.

Explain:
- Extensions improve the workspace.
- But unnecessary extensions should be avoided.
- Security and permissions matter.

---

## 7. Claude Code Working Model in VS Code

Explain the flow:

1. Open a clear project folder in VS Code.
2. Place relevant files inside the folder.
3. Add project instructions where needed.
4. Use Claude Code to understand the task.
5. Let Claude Code inspect context.
6. Ask Claude Code to propose a plan.
7. Review the plan.
8. Allow safe actions step by step.
9. Review created or modified files.
10. Validate before final use.

### Verbatim explanation
“Claude Code should not be asked to randomly work on an unclear folder. The better method is to create a clean workspace, give clear instructions, let it plan, and then review every important output.”

---

## 8. Project Folder Thinking

A project folder is the boundary of work.

Explain:

When using Claude Code, the project folder should contain:
- input files
- working notes
- instructions
- drafts
- outputs
- logs or reports if needed
- scripts if needed
- final deliverables

### Example folder for document workflow

```text
policy-review-workspace/
  input/
    policy_draft.md
    reference_notes.md
  output/
    review_summary.md
    missing_information_checklist.md
  CLAUDE.md
  README.md
```

### Example folder for content workflow

```text
video-content-workspace/
  notes/
    topic_notes.md
    audience_notes.md
  scripts/
    draft_script.md
  review/
    fact_check_checklist.md
    tone_review.md
  CLAUDE.md
```

### Example folder for testing workflow

```text
testing-workspace/
  requirements/
    feature_requirement.md
  test-cases/
    generated_test_cases.md
  review/
    missing_scenarios.md
  CLAUDE.md
```

### Example folder for small tool workflow

```text
file-index-tool/
  sample-input/
  scripts/
    create_file_index.py
  output/
    file_index.md
  README.md
  CLAUDE.md
```

### Trainer emphasis
A clean folder helps the human and the agent. Messy folders increase the chance of wrong assumptions and incomplete outputs.

---

## 9. Why File Structure Matters for Agentic Work

Explain:

File structure affects AI work because the agent may need to:
- locate source files
- understand which files are input
- know where output should be saved
- avoid editing wrong files
- separate draft and final work
- understand project rules

### Poor structure

```text
project/
  final.docx
  final_new.docx
  final_latest_revised.docx
  notes1.txt
  notes_old.txt
  random/
  copy/
```

Problem:
- unclear source
- unclear latest version
- difficult to review
- higher risk of wrong output

### Better structure

```text
project/
  input/
  working/
  output/
  review/
  archive/
  CLAUDE.md
  README.md
```

Benefit:
- input is clear
- output is clear
- review is easier
- agent instructions are visible
- human remains in control

---

## 10. `CLAUDE.md` Preview

Do not teach this fully today; Day 4 will cover it deeply.

Introduce it briefly:

**`CLAUDE.md` is a project instruction file that tells Claude Code how to behave in the project.**

It may include:
- project purpose
- output format
- tone
- file naming rules
- safety rules
- review rules
- do-not-do rules
- domain-specific instructions

### Example simple `CLAUDE.md`

```markdown
# Project Instructions

- Use clear professional language.
- Do not invent missing information.
- Separate facts, assumptions, and questions.
- Create output in Markdown.
- Do not modify source files unless asked.
- Ask before running commands that change files.
```

### Trainer explanation
“Tomorrow we will study `CLAUDE.md` properly. Today just remember that a project without instructions is like asking an assistant to work without standards.”

---

## 11. General-Purpose Work Examples in VS Code

### Example 1: Documentation assistant

Task:
“Create a user guide from these rough notes.”

Workspace:
```text
documentation-work/
  input/
    rough_notes.md
  output/
    user_guide.md
  CLAUDE.md
```

Claude Code can:
- read notes
- create outline
- draft user guide
- identify missing details
- create review checklist

Human must:
- verify correctness
- approve final wording
- check missing details

---

### Example 2: Planning assistant

Task:
“Convert this requirement into a 5-day work plan.”

Workspace:
```text
planning-work/
  input/
    requirement.md
  output/
    implementation_plan.md
    risk_register.md
```

Claude Code can:
- read requirement
- identify tasks
- create timeline
- list dependencies
- identify risks

Human must:
- validate feasibility
- adjust dates
- approve priorities

---

### Example 3: Review assistant

Task:
“Review this draft and identify unclear sections.”

Workspace:
```text
review-work/
  input/
    draft_note.md
  output/
    review_comments.md
    revised_draft.md
```

Claude Code can:
- identify unclear wording
- suggest structure
- find missing sections
- rewrite in neutral tone

Human must:
- confirm meaning
- approve changes
- ensure sensitive content is handled properly

---

### Example 4: Testing assistant

Task:
“Generate test cases from this requirement.”

Workspace:
```text
testing-work/
  requirements/
    login_feature.md
  output/
    test_cases.md
    edge_cases.md
```

Claude Code can:
- extract requirements
- create positive test cases
- create negative test cases
- list edge cases
- create traceability table

Human must:
- verify business logic
- add domain-specific cases
- approve final test cases

---

### Example 5: Small tool assistant

Task:
“Create a script that generates an index of files in a folder.”

Workspace:
```text
file-index-work/
  sample-data/
  scripts/
    file_index_generator.py
  output/
    index.md
```

Claude Code can:
- create script
- explain how it works
- run dry-run if allowed
- fix errors
- create README

Human must:
- check file paths
- review commands
- test on sample data before real data

---

## 12. How to Review Claude Code Work in VS Code

Teach learners to review at multiple levels.

### 12.1 Review the plan
Before work begins:
- Is the plan correct?
- Is the scope clear?
- Are risky steps included?
- Are files identified correctly?

### 12.2 Review file changes
After output:
- What files were created?
- What files were edited?
- Was anything overwritten?
- Are outputs saved in the right folder?

### 12.3 Review terminal commands
Before execution:
- What command will run?
- Is it read-only?
- Can it delete or modify files?
- Can it expose data?
- Is it reversible?

### 12.4 Review generated content
After content creation:
- Is it accurate?
- Does it invent facts?
- Is it in the required tone?
- Are assumptions separated?
- Is sensitive information protected?

### 12.5 Review final deliverable
Before using:
- Is it complete?
- Is it verified?
- Is it approved by the human?
- Is it ready to share?

---

## 13. Safe Workspace Rules

Give these rules clearly.

### Rule 1: Keep source files separate
Do not mix original input and generated output.

### Rule 2: Use an output folder
Generated files should go into a clear output folder.

### Rule 3: Use a review folder
Review notes, checklists, and validation outputs should be separate.

### Rule 4: Avoid direct edits to important originals
Ask Claude Code to create revised copies unless direct editing is intentional.

### Rule 5: Use dry-run for risky operations
For file movement, renaming, deletion, or scripts, start with dry-run.

### Rule 6: Review commands before execution
Never blindly run commands suggested by AI.

### Rule 7: Keep instructions visible
Use project-level instructions such as `CLAUDE.md`.

### Rule 8: Validate final outputs
Do not accept generated output without review.

---

## 14. Hands-On Discussion: Build a Workspace

Ask learners to create a workspace design for one task.

### Task options
1. Document review
2. Meeting summary
3. File indexing
4. Test case generation
5. Website draft
6. Video script planning
7. Security checklist
8. Small automation helper

### Template

```text
project-name/
  input/
  working/
  output/
  review/
  CLAUDE.md
  README.md
```

Ask them to answer:
- What goes into input?
- What output should be created?
- What should Claude Code not modify?
- What instructions are needed?
- What should require approval?
- What should be reviewed before final use?

---

## 15. Mini Demonstration Script for Trainer

Use this example verbally or practically.

### Scenario
“We want Claude Code to review a rough document and create a clean action summary.”

### Step 1: Create folder

```text
action-summary-work/
  input/
  output/
  review/
  CLAUDE.md
```

### Step 2: Put rough note in input

```text
input/rough_meeting_notes.md
```

### Step 3: Add simple instruction

```markdown
# Project Instructions

- Create outputs in Markdown.
- Use neutral professional language.
- Do not invent missing owners or dates.
- Separate decisions, actions, risks, and questions.
- Save final output in the output folder.
```

### Step 4: Give Claude Code task

```text
Read input/rough_meeting_notes.md and create output/action_summary.md.
Use sections: decisions, action items, risks, missing information, and next steps.
Do not modify the original input file.
```

### Step 5: Review output

Check:
- Did it preserve meaning?
- Did it invent owners?
- Did it save output correctly?
- Did it mark missing information?
- Is it ready for use?

### Trainer point
This is not coding, but it is a strong Claude Code workflow inside VS Code.

---

## 16. Common Mistakes to Correct

### Mistake 1
Opening a random folder and asking Claude Code to work without structure.

Correction:
Create a clean workspace with input, output, review, and instructions.

### Mistake 2
Allowing edits directly on original files.

Correction:
Ask for revised copies unless direct editing is required.

### Mistake 3
Using VS Code only as a code editor.

Correction:
Use VS Code as a project workspace for many types of professional work.

### Mistake 4
Ignoring terminal command risk.

Correction:
Review every command before running, especially commands that modify files.

### Mistake 5
Not checking generated files.

Correction:
Always review created and edited files before final use.

---

## 17. Trainer Verbatim Blocks

### Verbatim Block 1
“VS Code is not only a coding editor for this course. It is our structured workspace for agentic work.”

### Verbatim Block 2
“Claude Code becomes more reliable when the workspace is clean, files are organized, and instructions are clear.”

### Verbatim Block 3
“Input, output, and review should be separated. This helps both the human and the AI agent.”

### Verbatim Block 4
“Do not allow an agent to work freely in a messy folder. First create boundaries.”

### Verbatim Block 5
“VS Code helps us see files, edits, terminal output, and project structure, so we can review Claude Code work properly.”

---

## 18. Questions to Ask During Session

Use these questions throughout:

- What is the project folder?
- Which files are source input?
- Where should output be saved?
- What should Claude Code not modify?
- What instructions are required?
- What actions should require approval?
- Which terminal commands are safe?
- How will the human review the result?
- Is the workspace clean enough for agentic work?
- Is this workflow only coding, or general professional work?

---

## 19. Day 3 Recap

End with:

“Today we understood VS Code as the working environment for Claude Code. VS Code gives us a place to organize files, write instructions, review outputs, inspect terminal results, and control agentic workflows.”

Then say:

“The key point is that a clean workspace improves AI work. Messy files and unclear instructions increase risk. Clear folders, clear instructions, and reviewable outputs make Claude Code more useful.”

Then close with:

“In the next session, we will focus on `CLAUDE.md`, project instructions, work standards, communication rules, and output style.”

---

## 20. End-of-Session Learner Takeaway

Learners should leave with these five ideas:

1. VS Code can be used as a general professional workspace, not only a coding editor.
2. Claude Code works better when the project folder is clean and structured.
3. Input, output, and review files should be separated.
4. Terminal commands and file changes must be reviewed.
5. Project instructions such as `CLAUDE.md` are essential for consistent agent behavior.

---

## 21. Suggested Homework

Ask learners to create a sample workspace structure for one real work task.

They should prepare:

```text
project-name/
  input/
  output/
  review/
  CLAUDE.md
  README.md
```

They should also write five instructions they would put inside `CLAUDE.md`.

---

## 22. Final Trainer Reminder

Day 3 is successful if the learner understands:

**VS Code is the controlled workspace where Claude Code can work with files, instructions, terminal, and outputs under human supervision.**

They should also understand:

**Good workspace structure is a safety and quality practice, not just an organization habit.**
