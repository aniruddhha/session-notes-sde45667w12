# Phase 3 -> Day 7
## Tools, Permissions, Safety Modes, and Human Approval for General Workflows
### Trainer Session Notes

**Session Duration:** 1 hour 30 minutes  
**Session Mode:** 20% Theory | 80% Hands-On Discussion / Demonstration  
**Primary Environment:** VS Code  
**Primary Tool Focus:** Claude Code  
**Important Framing:** Claude Code is taught as a general-purpose agentic work assistant, not only a coding tool.

---

## 1. Session Goal for the Trainer

By the end of this session, learners should understand:

- what tools mean in Claude Code workflows
- why tools make Claude Code more powerful than normal chat
- why permissions are required when an AI agent can act
- difference between read-only, write, execution, and external-access actions
- how to classify tool actions by risk
- why human approval is central to safe agentic work
- how tool usage applies to documentation, planning, review, testing, content, automation, and coding workflows
- how to give safe tool-use instructions inside VS Code
- how to avoid uncontrolled file changes, risky terminal commands, and data exposure
- how to design approval checkpoints for general professional workflows

**Trainer objective:**  
Day 7 should make learners understand that tools are the action layer of Claude Code. Tools create real value, but they also create real risk. Learners should understand how to keep the human in control.

---

## 2. Recommended Session Flow

| Time | Segment | Mode |
|---|---|---|
| 0-8 min | Recap Day 6 and introduce tools + permissions | Theory |
| 8-20 min | What tools mean in Claude Code | Theory |
| 20-34 min | Tool categories: read, write, terminal, browser, external integrations | Theory + examples |
| 34-48 min | Risk levels: low, medium, high, prohibited without approval | Discussion |
| 48-62 min | Permissions and human approval | Demonstration discussion |
| 62-74 min | Safe tool-use instructions for VS Code workflows | Hands-on style discussion |
| 74-84 min | Activity: classify actions and define approval rules | Hands-on discussion |
| 84-88 min | Recap and connection to Day 8 | Recap |
| 88-90 min | Closing task | Wrap-up |

---

## 3. Opening Script Notes for Yourself

Start with:

“On Day 6, we learned about Skills. Skills tell Claude Code how to perform repeated types of work. Today we will focus on tools, permissions, and approval.”

Then say:

“Tools are what allow Claude Code to act. It may read files, create files, edit files, run commands, inspect output, or interact with connected systems depending on setup and permissions.”

Then add:

“Because tools allow action, they must be controlled. The human must decide what Claude Code can do automatically, what needs approval, and what should never be done.”

---

## 4. Core Theory: What Are Tools?

Explain simply:

**A tool is a capability that allows Claude Code to do something inside or around the workspace.**

A normal chatbot mostly answers.

Claude Code with tools can:
- read project files
- search folders
- create files
- edit files
- run terminal commands
- inspect command output
- run tests
- create reports
- generate scripts
- use external integrations where configured

### Verbatim explanation
“Tools are the action layer of agentic work. Without tools, the assistant mainly talks. With tools, the assistant can help perform the work.”

---

## 5. Why Tools Matter

Tools matter because many real tasks require action, not only answers.

### Example: Document summary without tools
User pastes text.  
AI summarizes it in chat.

### Example: Document summary with tools
Claude Code can:
1. inspect a folder
2. read multiple files
3. identify source documents
4. create a summary file
5. save output in the correct folder
6. create a review checklist
7. report what files were used

### Trainer point
Tools make work more practical, but they also require boundaries.

---

## 6. Main Tool Categories

### 6.1 Read Tools

Read tools allow Claude Code to inspect information.

Examples:
- read a file
- list folder structure
- inspect configuration
- read logs
- search within project files
- view terminal output

Typical risk:
Low to medium.

Risk increases when files contain:
- confidential information
- personal data
- credentials
- internal strategy
- legal or sensitive material

### Example
```text
Read all Markdown files in input/ and create a summary of their headings.
```

### Safe instruction
```text
Only read files inside input/. Do not modify any files.
```

---

### 6.2 Write Tools

Write tools allow Claude Code to create or modify files.

Examples:
- create Markdown file
- edit README
- update checklist
- create script
- rewrite document
- update configuration
- create test cases

Typical risk:
Medium.

Risk increases when:
- source files may be overwritten
- original documents are modified
- many files are changed
- configuration files are updated
- output location is unclear

### Example
```text
Create output/review_summary.md based on input/document.md.
```

### Safe instruction
```text
Create a new file in output/. Do not edit the original input file.
```

---

### 6.3 Terminal Tools

Terminal tools allow commands to be run.

Examples:
- list files
- run tests
- execute scripts
- install packages
- start local server
- check dependencies
- generate output
- inspect logs

Typical risk:
Medium to high.

Risk increases when commands:
- delete files
- move files
- modify many files
- install packages
- access network
- process real data
- change system settings
- change security settings

### Example safe command
```bash
ls -la
```

### Example risky command
```bash
rm -rf *
```

### Trainer explanation
“A terminal command is not just text. It can change the system. Every command must be understood before execution.”

---

### 6.4 Browser or Preview Tools

Browser or preview tools help inspect visual output or web-based behavior.

Examples:
- preview a local website
- check page layout
- test a form
- inspect console error
- compare UI result
- verify generated HTML output

Typical risk:
Low to medium.

Risk increases when:
- browser has logged-in sessions
- sensitive internal pages are open
- external data is submitted
- personal information is entered
- production systems are used

### Safe instruction
```text
Preview only the local static page. Do not submit forms or enter real user data.
```

---

### 6.5 External Integration Tools

External tools may connect Claude Code to other systems.

Examples:
- APIs
- databases
- file drives
- issue trackers
- documentation systems
- messaging tools
- cloud services
- security scanners

Typical risk:
Medium to high.

Risk depends on:
- read-only vs write access
- data sensitivity
- permissions
- audit trail
- whether action affects real systems

### Safe instruction
```text
Use read-only access only. Do not create, update, delete, send, or publish anything without approval.
```

---

## 7. Tool Risk Levels

Teach a simple risk classification.

| Risk Level | Tool Action Type | Example | Approval Needed? |
|---|---|---|---|
| Low | Read-only, non-sensitive | List files, read sample notes | Usually no, if allowed |
| Medium | Create new output files | Create summary in output/ | Usually review after creation |
| High | Modify existing files or run scripts | Edit source file, run rename script | Yes |
| Very High | Delete, publish, send, install, change security | Delete folder, send email, change config | Strong approval required |
| Not Allowed | Secrets exposure or destructive unclear action | Upload confidential file to unknown tool | Do not allow |

### Trainer explanation
“Before approving a tool action, classify the risk. Read, write, execute, delete, publish, and expose are not equal.”

---

## 8. Read vs Write vs Execute vs Publish

Teach this clearly.

### Read
The agent only inspects information.

Example:
```text
Read input/notes.md.
```

### Write
The agent creates or edits content.

Example:
```text
Create output/summary.md.
```

### Execute
The agent runs something.

Example:
```text
Run the test command.
```

### Publish / Send
The agent sends or shares something outside the workspace.

Example:
```text
Send the final report by email.
```

### Trainer explanation
“Each step increases responsibility. Reading is one level. Writing is higher. Executing is higher again. Publishing or sending is the highest.”

---

## 9. Permissions

Explain:

**Permissions are rules that control what Claude Code is allowed to do.**

Permissions can be explicit or practical.

Examples:
- allowed to read files in input/
- allowed to create files in output/
- not allowed to edit source files
- not allowed to run destructive commands
- not allowed to install packages
- must ask before changing files
- must ask before processing real data
- must ask before external access

### Verbatim explanation
“Permissions are not obstacles. Permissions are the control system that allows safe agentic work.”

---

## 10. Human Approval

Explain:

**Human approval means the user reviews and explicitly allows an action before Claude Code performs it.**

Approval is needed when:
- original files will be edited
- many files will be changed
- commands will run
- packages will be installed
- scripts will process real data
- external systems will be accessed
- output will be shared
- security settings will change
- final decision will be made

### Good approval request
Claude Code should explain:
- what it wants to do
- why it wants to do it
- which files or systems are affected
- whether it is reversible
- what risk exists
- what will happen after approval

### Example approval request
```text
I plan to create output/review_summary.md using input/policy_draft.md.
I will not modify the source file.
Please approve before I create the output file.
```

### High-risk approval request
```text
I plan to run a script that renames files in the selected folder.
This will modify file names.
I recommend first running a dry-run and generating a preview report.
Please approve only the dry-run first.
```

---

## 11. Safety Modes: Conceptual Explanation

Do not make this too technical. Explain conceptually.

Safety modes can be understood as different levels of agent freedom.

### Read-only mode
Agent can inspect but cannot change.

Good for:
- review
- summary
- analysis
- exploration
- understanding folders

### Assisted-write mode
Agent can create new files or suggested edits.

Good for:
- drafts
- summaries
- checklists
- test cases
- README files

### Approval-before-action mode
Agent must ask before edits or commands.

Good for:
- most professional workflows
- source file changes
- scripts
- tool execution

### Restricted mode
Agent cannot access certain files, systems, or commands.

Good for:
- sensitive data
- production systems
- confidential folders
- security work

### Trainer explanation
“Different tasks need different safety levels. Do not use the same permission style for a simple summary and a file-renaming script.”

---

## 12. Safe Tool Use in VS Code

In VS Code, teach learners to manage tool use through workspace discipline.

### Safe practice 1: Use clear folder boundaries

```text
project/
  input/
  output/
  review/
  scripts/
  CLAUDE.md
```

### Safe practice 2: Protect input files
Tell Claude Code:
```text
Do not modify files inside input/.
```

### Safe practice 3: Use output folder
Tell Claude Code:
```text
Save generated files only in output/.
```

### Safe practice 4: Use dry-run first
Tell Claude Code:
```text
Before renaming or moving files, create a dry-run report.
```

### Safe practice 5: Review commands
Tell Claude Code:
```text
Explain every terminal command before running it.
```

### Safe practice 6: Avoid real data first
Tell Claude Code:
```text
Use sample data first. Do not run on real data until approved.
```

### Safe practice 7: Review diffs
Tell Claude Code:
```text
Show what changed before treating work as complete.
```

---

## 13. `CLAUDE.md` Permission Rules

Connect Day 7 with Day 4.

Example `CLAUDE.md` permission section:

```markdown
## Permission Rules

Claude Code may:
- read files inside input/
- create new files inside output/
- create review notes inside review/
- suggest commands without running them

Claude Code must ask before:
- editing original files
- running commands that modify files
- installing dependencies
- moving or deleting files
- processing real data
- accessing external systems

Claude Code must never:
- expose sensitive information
- run destructive commands
- overwrite source files
- make final decisions
- send or publish content without approval
```

### Trainer explanation
“Permission rules should be written into the project instructions, not remembered informally.”

---

## 14. General Professional Workflow Examples

### Example 1: Document review

Task:
```text
Review input/policy_draft.md and create review/review_comments.md.
```

Allowed:
- read input file
- create review file

Not allowed:
- edit source file
- add unsupported facts
- make final decision

Human review:
- check accuracy
- check tone
- check missing information

---

### Example 2: Meeting summary

Task:
```text
Create output/meeting_summary.md from input/meeting_notes.md.
```

Allowed:
- read notes
- create summary

Not allowed:
- invent owners
- invent dates
- send summary to anyone

Human review:
- verify actions
- confirm owners
- approve final version

---

### Example 3: File indexing

Task:
```text
Create a file index of this folder.
```

Allowed:
- list folder structure
- create index file

Not allowed:
- delete files
- rename files
- move files

Human review:
- verify index completeness

---

### Example 4: Test case generation

Task:
```text
Generate test cases from requirements/login_feature.md.
```

Allowed:
- read requirements
- create test cases

Not allowed:
- assume hidden business rules
- modify requirement file

Human review:
- validate expected results
- add missing domain cases

---

### Example 5: Small script creation

Task:
```text
Create a script to generate a file index.
```

Allowed:
- write script
- run on sample folder after approval

Not allowed:
- run on production data
- delete files
- change names without dry-run

Human review:
- inspect script
- approve sample run
- approve real run only later

---

## 15. Common Risky Commands to Discuss

Do not encourage running these. Use them only as examples of caution.

### File deletion
```bash
rm -rf folder/
```

Risk:
Can permanently delete files.

### Bulk rename
```bash
for f in *; do mv "$f" ...; done
```

Risk:
Can rename many files incorrectly.

### Package install
```bash
npm install some-package
```

Risk:
Adds external code and dependencies.

### Running unknown script
```bash
python script_from_unknown_source.py
```

Risk:
May modify files or leak data.

### Changing permissions
```bash
chmod -R 777 .
```

Risk:
Can weaken security.

### Trainer explanation
“Do not treat commands as harmless because they are short. A short command can cause major changes.”

---

## 16. Approval Language Templates

Teach practical phrases.

### Read-only task
```text
You may read files inside input/ and create a summary of what you find. Do not modify any files.
```

### Create new output file
```text
Create a new file in output/. Do not edit or overwrite any existing source file.
```

### Plan before action
```text
First inspect the files and propose a plan. Do not make changes until I approve the plan.
```

### Command review
```text
Before running any terminal command, explain what it does, why it is needed, and whether it modifies files.
```

### Dry-run first
```text
Create a dry-run report first. Do not move, rename, or delete files until I approve.
```

### External system restriction
```text
Do not access external systems or send data outside this workspace unless I explicitly approve.
```

### Human final decision
```text
Provide decision support only. Do not make or state a final decision.
```

---

## 17. Activity: Classify Tool Actions

Ask learners to classify each item as:

- Low risk
- Medium risk
- High risk
- Very high risk
- Not allowed without strong safeguards

### Items

1. Read a public Markdown file.
2. Create a new summary file in output/.
3. Edit the original policy document.
4. List all files in a folder.
5. Run a script that renames 500 files.
6. Delete old files from a folder.
7. Install a new package from the internet.
8. Create test cases from a requirement file.
9. Send final report to external recipient.
10. Read a file containing passwords.
11. Run tests in a local project.
12. Modify security configuration.
13. Create a dry-run report for file movement.
14. Summarize meeting notes with personal information.
15. Generate a README file.

### Suggested classification

| Item | Suggested Risk |
|---|---|
| 1 | Low |
| 2 | Medium |
| 3 | High |
| 4 | Low |
| 5 | Very High |
| 6 | Very High |
| 7 | High |
| 8 | Medium |
| 9 | Very High |
| 10 | Not allowed / very high |
| 11 | Medium |
| 12 | Very High |
| 13 | Low to Medium |
| 14 | Medium to High |
| 15 | Medium |

---

## 18. Activity: Create Permission Rules

Ask learners to write permission rules for one workflow.

### Workflow options
1. Document review
2. Meeting summary
3. File indexing
4. Test case generation
5. Website creation
6. Security checklist
7. Small automation script
8. Content review

### Template

```markdown
## Allowed Actions

## Ask Before

## Never Do

## Human Review Required
```

### Example

```markdown
## Allowed Actions
- Read files in input/
- Create files in output/
- Create review notes in review/

## Ask Before
- Editing original files
- Running scripts
- Installing packages

## Never Do
- Delete files
- Expose sensitive information
- Make final decisions

## Human Review Required
- Before using final output
- Before running generated scripts
- Before sharing externally
```

---

## 19. Human Approval Checklist

Before approving an action, ask:

1. What will the agent do?
2. Which files or systems are affected?
3. Is this read, write, execute, delete, publish, or external access?
4. Is the action reversible?
5. Is data sensitive?
6. Is there a safer dry-run option?
7. Is the output reviewable?
8. Does this affect real data or sample data?
9. Is the scope limited?
10. Am I comfortable approving this step?

### Trainer explanation
“Approval should not be a casual yes. Approval should be informed.”

---

## 20. Common Mistakes to Correct

### Mistake 1
Allowing all tools for convenience.

Correction:
Use only the tools needed for the current task.

### Mistake 2
Not separating read and write permissions.

Correction:
Reading files is different from editing files.

### Mistake 3
Running commands without understanding them.

Correction:
Ask Claude Code to explain the command and risk first.

### Mistake 4
Skipping dry-run.

Correction:
Use dry-run before file movement, rename, deletion, or real-data processing.

### Mistake 5
Letting the agent publish or send output.

Correction:
Human approval is required before external sharing.

### Mistake 6
Letting Claude Code make final decisions.

Correction:
Claude Code supports decisions. It does not own decisions.

---

## 21. Trainer Verbatim Blocks

### Verbatim Block 1
“Tools make Claude Code useful because they allow action. But action requires control.”

### Verbatim Block 2
“Read, write, execute, delete, publish, and external access are different risk levels.”

### Verbatim Block 3
“Permissions are not a blocker. Permissions are the safety system for agentic work.”

### Verbatim Block 4
“Human approval must be informed. The user should understand what will happen before approving.”

### Verbatim Block 5
“Safe agentic work means giving Claude Code enough ability to help, but not unlimited freedom.”

---

## 22. Questions to Ask During Session

Use these questions throughout:

- What tool is being used?
- Is the action read-only or write-capable?
- Will any file be modified?
- Will any command be executed?
- Is real data involved?
- Is the action reversible?
- Is there a dry-run option?
- Does it need human approval?
- Could sensitive data be exposed?
- Should this be allowed, restricted, or blocked?

---

## 23. Day 7 Recap

End with:

“Today we learned that tools are the action layer of Claude Code. Tools allow Claude Code to read files, create files, edit content, run commands, inspect output, and interact with systems depending on configuration.”

Then say:

“We also learned that tool use must be controlled through permissions and human approval. Not all actions have the same risk. Reading, writing, executing, deleting, publishing, and external access must be treated differently.”

Then close with:

“In the next session, we will focus on subagents, task delegation, hooks, and automation concepts for multi-step professional work.”

---

## 24. End-of-Session Learner Takeaway

Learners should leave with these five ideas:

1. Tools allow Claude Code to act inside a workflow.
2. Tool actions have different risk levels.
3. Permissions define what the agent can and cannot do.
4. Human approval is required for risky actions.
5. Safe workflows use boundaries, dry-runs, review, and limited access.

---

## 25. Suggested Homework

Ask learners to choose one workflow and create a permission rule set.

They should define:

```markdown
## Allowed Actions

## Ask Before

## Never Do

## Human Review Required
```

They should also identify at least three risky actions and explain why those actions require approval.

---

## 26. Final Trainer Reminder

Day 7 is successful if the learner can explain:

**Tools allow Claude Code to act, and permissions control that action.**

They should also understand:

**Human approval is not just clicking yes. It is understanding the action, risk, affected files, and expected result before allowing the agent to proceed.**
