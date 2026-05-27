# Phase 2 -> Day 2  
## Prompting Fundamentals for Reliable Output  
### Trainer Session Notes

**Session Duration:** 1 hour 30 minutes  
**Session Mode:** 20% Theory | 80% Hands-On  
**Primary Tools for Today:** ChatGPT, Claude, Gemini, DeepSeek, Grok  
**Phase Focus:** Safe, reliable, structured, and reviewable AI usage

---

## 1. Session Goal for the Trainer

By the end of this session, participants should:
- understand why prompt quality directly affects AI output quality
- learn the basic components of a strong prompt: role, task, context, format, constraints, and review instruction
- distinguish weak prompts from clear professional prompts
- practice rewriting vague prompts into reliable prompts
- understand how prompt structure reduces ambiguity, hallucination risk, and unusable output
- learn to ask for assumptions, limitations, and verification needs
- build the habit of treating prompting as professional instruction design, not casual chatting

**Your teaching objective:**  
Today is about converting casual AI use into controlled AI use.  
Do not teach prompting as “magic words.”  
Teach it as clear instruction-giving.  
The participant should feel:  
“Now I know how to ask AI in a way that gives clearer, safer, more structured, and easier-to-review output.”

---

## 2. Recommended Session Flow

| Time | Segment | Mode |
|---|---|---|
| 0–8 min | Opening + link from Phase 2 Day 1 | Theory |
| 8–22 min | Why prompting matters for reliable output | Theory |
| 22–34 min | The prompt structure: role, task, context, format, constraints | Theory |
| 34–48 min | Demo 1: weak prompt vs strong prompt | Hands-On |
| 48–62 min | Demo 2: improving output through context and format | Hands-On |
| 62–74 min | Demo 3: adding safety, assumptions, and verification instructions | Hands-On |
| 74–84 min | Activity: rewrite weak prompts into professional prompts | Hands-On |
| 84–88 min | Reflection + recap | Discussion |
| 88–90 min | Closing task | Wrap-up |

---

## 3. Opening Script Notes for Yourself

### What you should establish in the first few minutes
- Phase 2 Day 1 introduced safe and responsible AI usage
- today focuses on the first practical skill of responsible use: better prompting
- weak prompts create vague, risky, generic, or misleading outputs
- strong prompts do not guarantee truth, but they improve relevance, structure, and reviewability

### Suggested opening flow
You may say:

“Yesterday we began Phase 2 by discussing safe and responsible AI usage. We saw that safety starts before the answer appears. It starts with what we put into the prompt, what we remove from the prompt, and what we ask the model to do.”

Then say:

“Today we go deeper into prompting. Prompting is not about clever tricks. It is about giving clear professional instructions.”

Then add:

“A weak prompt gives the model room to guess. A strong prompt reduces guessing by giving task, context, format, constraints, and review expectations.”

---

## 4. Core Theory You Must Cover Briefly

Keep this practical and easy to apply.

### 4.1 What a prompt is
Use this explanation:

**A prompt is the instruction, question, context, or input we give to an AI system to guide its response.**

Then simplify:

**A prompt is how we tell AI what work to do.**

### 4.2 Why prompting matters
Explain:
- the model does not automatically know the exact purpose
- vague prompts lead to generic answers
- missing context leads to assumptions
- missing format leads to inconsistent output
- missing constraints leads to long, unusable, or unsafe responses
- missing review instruction may cause overconfident output

Use this line:

**Prompt quality controls output direction.**

### 4.3 Prompting does not guarantee correctness
Say this clearly:

**A good prompt improves usefulness, but it does not remove the need for review and verification.**

This is important. Do not let participants think prompting is a magic reliability solution.

### 4.4 The six core prompt components
Teach this structure clearly:

1. **Role**  
   What perspective should the model take?

2. **Task**  
   What exactly should it do?

3. **Context**  
   What background information is needed?

4. **Format**  
   How should the output be presented?

5. **Constraints**  
   What should it include, exclude, limit, or avoid?

6. **Review / safety instruction**  
   What assumptions, uncertainties, risks, or verification needs should it mention?

### 4.5 Example of weak vs strong framing
Weak:
“Write about this issue.”

Strong:
“Act as a professional drafting assistant. Convert the following rough notes into a concise internal briefing note with headings: context, observations, pending actions, risks, and next step. Keep the tone neutral, do not add facts not provided, and mention any assumptions separately.”

### 4.6 The professional rule
Say this clearly:

**A strong prompt makes the task, boundaries, and expected output visible.**

---

## 5. One-Line Distinctions You Should Repeat During Session

Use these repeatedly:

**Prompting is instruction design, not magic wording.**

**A vague prompt invites the model to guess.**

**A strong prompt gives task, context, format, and boundaries.**

**Good prompts improve usefulness, but review still remains necessary.**

**Ask AI to separate facts, assumptions, and verification needs.**

---

## 6. Concept Explanation You Must Deliver Clearly

### 6.1 The simplest mental model
You should say:

“Think of prompting like briefing a capable assistant. If you give unclear instructions, the assistant may still produce something polished, but it may not match your need. If you give clear purpose, context, format, and boundaries, the result becomes much more useful.”

### 6.2 Another simple explanation
You may say:

“Prompting is not asking longer questions. Prompting is asking clearer questions.”

### 6.3 Important caution
Also say:

“A strong prompt can reduce ambiguity, but it cannot turn AI into a guaranteed truth machine. The output must still be reviewed according to risk.”

### 6.4 Important maturity point
Say this clearly:

“The mature user does not only ask for an answer. The mature user designs the instruction so the answer is easier to evaluate.”

---

## 7. What You Must Draw or Show on Screen

Use this prompt structure table.

| Prompt Component | Question to Ask | Example |
|---|---|---|
| Role | From what perspective should AI respond? | Act as a professional drafting assistant |
| Task | What should it do? | Summarize, classify, rewrite, compare |
| Context | What information should guide it? | Based on these rough notes |
| Format | How should output look? | Table, bullets, email, briefing note |
| Constraints | What boundaries apply? | Do not add facts; keep under 120 words |
| Review instruction | What should be flagged? | Mention assumptions and verification needs |

Then add below:

**A strong prompt makes output easier to use and easier to review.**

---

## 8. Demo 1 — Weak Prompt vs Strong Prompt

### Purpose
To show how prompt clarity changes output quality.

### What to do
Use the same rough input twice.

### Rough input
“inspection done monday docs missing local report pending follow up next monday final decision after verification”

### Weak prompt
“Write a note.”

### Strong prompt
“Act as a professional drafting assistant. Convert the following rough notes into a concise internal briefing note with headings: context, observations, pending actions, risks, and recommended next step. Keep the tone neutral. Do not add facts not provided. Mention any assumptions separately.”

Run both in:
- ChatGPT
- Claude
- Gemini
- DeepSeek
- Grok

### What participants should observe
- weak prompt output is generic
- strong prompt output is more structured
- strong prompt controls tone
- strong prompt reduces unsupported additions
- review becomes easier because expected format is clear

### Verbatim you can say
“Notice that the model did not become more intelligent between the first and second prompt. What changed was the instruction quality. A clear prompt reduces unnecessary guessing and gives the model a professional output target.”

### Key insight to emphasize
**Prompt structure improves output structure.**

---

## 9. Demo 2 — Context and Format Improve Reliability

### Purpose
To show that context and format make output more usable.

### What to do
Use a task with and without context.

### Prompt without context
“Create action items.”

### Prompt with context and format
“From the following rough review notes, extract action items into a table with columns: action item, reason, responsible party if mentioned, timeline if mentioned, and verification needed. If information is missing, write ‘not provided’ instead of guessing.”

### What participants should observe
- context improves relevance
- table format improves reviewability
- “not provided” prevents the model from inventing details
- missing information becomes visible
- output becomes safer to inspect

### Verbatim you can say
“This is a very important responsible prompting habit: when information is missing, instruct the model not to guess. Ask it to mark missing details clearly. This turns hidden assumptions into visible gaps.”

### Key insight to emphasize
**Good prompts make missing information visible instead of hidden.**

---

## 10. Demo 3 — Adding Safety, Assumptions, and Verification Instructions

### Purpose
To show that prompts can include review discipline.

### What to do
Take a professional task and add safety instructions.

### Basic prompt
“Draft a recommendation note from these points.”

### Safer prompt
“Draft a preliminary note from the following points. Do not make a final recommendation. Separate confirmed facts, assumptions, pending information, and points needing verification. Keep the tone neutral and suitable for internal review.”

### What participants should observe
- the safer prompt avoids premature conclusion
- output separates certainty levels
- review needs become visible
- AI supports preparation instead of final decision-making
- safer prompt fits responsible AI usage

### Verbatim you can say
“This is how we keep control. We do not always ask AI for the final answer. Sometimes the safer and more useful task is to ask AI to separate facts, assumptions, gaps, and verification needs.”

### Key insight to emphasize
**Responsible prompts define what AI should not do.**

---

## 11. The Basic Prompt Formula You Should Teach

Teach this as a reusable structure:

### Formula
**Act as [role].  
Your task is to [task].  
Use the following context: [context].  
Return the output in [format].  
Follow these constraints: [constraints].  
Before finalizing, mention [assumptions / missing information / verification needs].**

### Example
“Act as a professional drafting assistant. Your task is to convert rough inspection notes into a concise internal briefing note. Use the following context: documentation gaps were found, local report is pending, follow-up is scheduled next Monday, and final decision should wait for verification. Return the output with headings: context, observations, pending actions, risks, and next step. Keep it under 150 words, maintain a neutral tone, do not add facts not provided, and list any assumptions separately.”

### Verbatim you can say
“This formula is not meant to make every prompt long. It is meant to make every important prompt complete enough for the task.”

---

## 12. Activity — Rewrite Weak Prompts into Professional Prompts

### Duration
10 minutes

### Objective
Practice converting vague prompts into reliable prompts.

### Instructions
Give participants weak prompts and ask them to rewrite using:
- role
- task
- context
- format
- constraints
- review instruction

### Weak prompt set
1. “Summarize this.”
2. “Write a report.”
3. “Make this formal.”
4. “Give advice.”
5. “Analyze this issue.”
6. “Prepare a note.”
7. “Tell me what to do.”
8. “Make a table.”

### Improved prompt examples

Weak:
“Summarize this.”

Improved:
“Summarize the following text into five bullet points. Preserve all decision-critical conditions. Do not add new facts. At the end, list anything that needs verification.”

Weak:
“Write a report.”

Improved:
“Create a first-draft internal report based only on the following notes. Use sections: background, observations, risks, pending information, and next steps. Keep tone neutral and mark assumptions separately.”

Weak:
“Tell me what to do.”

Improved:
“List possible next-step options based on the following information. Do not recommend a final decision. Identify missing information and verification needed before human decision-making.”

### Verbatim you can say
“The difference between weak and strong prompting is not decoration. It is control. A strong prompt tells the model what to do, what not to do, how to format the output, and how to handle uncertainty.”

### Trainer note
Push participants to avoid simply making prompts longer. Ask:
- Is the task clear?
- Is the output format clear?
- Are boundaries clear?
- Is the review instruction included?

---

## 13. High-Value Concepts to Emphasize During Discussion

### 13.1 Prompting is a control mechanism
Explain:
- it controls task direction
- it controls output format
- it controls tone
- it controls assumptions
- it controls reviewability

### 13.2 Context prevents generic output
Explain:
- without context, the model gives broad answers
- with context, the output fits the situation
- context should be sufficient but not sensitive beyond need

### 13.3 Format improves usability
Explain:
- tables make extraction easier
- headings improve scanning
- bullet points improve clarity
- checklists support review

### 13.4 Constraints reduce risk
Explain:
- word limits reduce bloat
- “do not add facts” reduces hallucination risk
- “mark missing information” reduces hidden assumptions
- “do not make final decision” protects accountability

### 13.5 Review instructions build safety into the prompt
Explain:
- ask for assumptions
- ask for missing data
- ask for verification points
- ask for confidence limitations where useful

---

## 14. Exact Verbatim Blocks for the Trainer

Use these where useful.

### Verbatim Block 1 — Prompting definition
“A prompt is not just a question. A prompt is an instruction that shapes what the AI system does, what it focuses on, how it formats the answer, and how safe or reviewable the output becomes.”

### Verbatim Block 2 — Weak prompts
“A vague prompt gives the model permission to guess. It may still sound professional, but it may not match the real need.”

### Verbatim Block 3 — Strong prompts
“A strong prompt gives the model a role, a task, context, output format, constraints, and review instructions. That makes the answer clearer and easier to inspect.”

### Verbatim Block 4 — Safety in prompting
“Responsible prompting is not only about getting a better answer. It is also about preventing unsafe assumptions, unnecessary disclosure, and premature conclusions.”

### Verbatim Block 5 — Review remains necessary
“Even a well-designed prompt does not remove responsibility. It improves the draft, but the human still reviews, verifies, and finalizes.”

---

## 15. Questions You Should Ask Throughout the Session

Use these to keep engagement active:
- What is unclear in this prompt?
- What might the model guess here?
- What context is missing?
- What format would make the answer easier to review?
- What constraint should we add?
- Should we ask it to avoid final judgment?
- Should we ask it to mark assumptions?
- What should be verified before use?
- How can this prompt be made safer?
- Is the improved prompt longer, or actually clearer?

---

## 16. Risks and Cautions to Mention Even in This Session

Mention these calmly:
- long prompt does not automatically mean good prompt
- too much unnecessary context can create privacy risk
- strong formatting does not guarantee factual accuracy
- role prompting does not make the model a real expert
- vague prompts can produce confident but weak output
- prompts that ask for final decisions can create accountability risk

Use this line:

**Prompting improves control, but it does not remove responsibility.**

---

## 17. Optional Mini Demo if Time Allows

### Missing information demo
Prompt:
“Prepare an action plan from this: report pending, documents missing, follow-up required.”

Then improved:
“Prepare an action plan from this. If responsible person, timeline, or decision authority is not mentioned, write ‘not provided’ instead of assuming. Add a section called ‘Information Needed Before Final Action.’”

### Teaching point
This shows how a prompt can make gaps visible instead of allowing invented completeness.

---

## 18. Suggested Whiteboard or Screen Structure

Use this layout:

### Left side
**Weak Prompt**
- vague
- missing context
- no format
- no boundaries
- invites assumptions

### Middle
**Strong Prompt Components**
- role
- task
- context
- format
- constraints
- review instruction

### Right side
**Better Output**
- specific
- structured
- safer
- easier to review
- less assumption-heavy

Then add below:
**Reliable prompting = clear instruction + visible boundaries + review readiness**

---

## 19. Closing Recap You Should Deliver

End with a strong summary:

“Today we learned that prompting is the first practical control in reliable AI usage. A good prompt gives the model a clear role, task, context, format, constraints, and review instruction.”

Then add:

“We also saw that strong prompts reduce guessing, improve structure, expose missing information, and make output easier to evaluate. But even with good prompts, review and verification remain necessary.”

Then bridge forward:

“In the next session, we will go deeper into structured prompting for professional work, where we will build reusable templates for summarization, drafting, review, comparison, and action planning.”

---

## 20. End-of-Session Participant Takeaway

Participants should leave with these five ideas:
1. prompt quality strongly affects output quality
2. weak prompts invite guessing and generic answers
3. strong prompts include role, task, context, format, constraints, and review instruction
4. prompts can ask AI to mark assumptions and verification needs
5. better prompting improves usefulness, but human review remains essential

---

## 21. Suggested Homework or Reflection

Keep it light.

### Homework option
Ask participants to take three weak prompts from their own work and rewrite each using:
- role
- task
- context
- format
- constraints
- review instruction

Then ask them to test one original prompt and one improved prompt in an AI tool and note:
- what improved
- what remained weak
- what still needed review

This prepares them for Day 3: Structured Prompting for Professional Work.

---

## 22. Quick Backup Prompts for the Trainer

Use these if the flow slows down.

### Prompt 1
“Rewrite this weak prompt into a strong professional prompt with role, task, context, format, constraints, and review instruction.”

### Prompt 2
“Identify what is missing from this prompt and how it may affect AI output.”

### Prompt 3
“Create a prompt template for summarizing professional notes safely.”

### Prompt 4
“Improve this prompt so the AI does not add facts, makes missing information visible, and avoids final judgment.”

### Prompt 5
“Compare the output from a weak prompt and a strong prompt and explain what changed.”

---

## 23. Trainer Cautions for Delivery

- do not present prompting as magic
- do not make prompts unnecessarily complex for simple tasks
- do not skip safety instructions
- do not imply good prompting guarantees truth
- do not allow sensitive information to be used in examples
- do not let participants confuse longer prompts with better prompts
- do not forget that review remains part of the workflow

---

## 24. Final Trainer Reminder

Today’s success is measured by whether the participant can improve a vague prompt into a controlled professional prompt.

They should be able to answer:

**What is the task? What context is needed? What format is required? What boundaries apply? What should the model not assume? What needs verification?**

If they can answer these clearly, Phase 2 Day 2 has achieved its purpose.
