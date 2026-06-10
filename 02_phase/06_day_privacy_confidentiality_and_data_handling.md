# Phase 2 -> Day 6  
## Privacy, Confidentiality, and Data Handling  
### Trainer Session Notes

**Session Duration:** 1 hour 30 minutes  
**Session Mode:** 20% Theory | 80% Hands-On  
**Primary Tools for Today:** ChatGPT, Claude, Gemini, DeepSeek, Grok  
**Phase Focus:** Safe data handling, redaction, privacy-aware prompting, and responsible AI workflows

---

## 1. Session Goal for the Trainer

By the end of this session, participants should:
- understand why privacy and confidentiality are central to responsible AI use
- recognize what kinds of information should not be casually shared with AI tools
- learn the difference between necessary context and unnecessary sensitive detail
- practice redacting or anonymizing content before using AI
- understand data minimization as a practical habit
- learn safe prompting patterns for sensitive or professional information
- understand that privacy protection begins before the prompt is typed

**Your teaching objective:**  
Today is about making the participant privacy-aware in everyday AI usage.  
Do not teach this as a purely legal or compliance topic.  
Teach it as practical operational discipline.  
The participant should feel:  
“Before I put anything into AI, I know how to decide what is safe, what must be removed, and how to give only the minimum required context.”

---

## 2. Recommended Session Flow

| Time | Segment | Mode |
|---|---|---|
| 0–8 min | Opening + link from Day 5 | Theory |
| 8–22 min | Why privacy and confidentiality matter in AI use | Theory |
| 22–34 min | What information should be protected | Theory |
| 34–48 min | Demo 1: unsafe prompt vs redacted prompt | Hands-On |
| 48–62 min | Demo 2: data minimization and context control | Hands-On |
| 62–74 min | Demo 3: converting sensitive notes into safe AI input | Hands-On |
| 74–84 min | Activity: redact and rewrite prompts safely | Hands-On |
| 84–88 min | Reflection + recap | Discussion |
| 88–90 min | Closing task | Wrap-up |

---

## 3. Opening Script Notes for Yourself

### What you should establish in the first few minutes
- Day 5 covered hallucination and fabrication
- today covers another major safety area: what we give to AI
- risk does not start only in the answer; risk can start in the input
- privacy-aware use means controlling data before prompting
- professional users must know what to remove, generalize, anonymize, or avoid sharing

### Suggested opening flow
You may say:

“In the previous session, we focused on hallucination and fabrication, meaning risk in the AI output. Today we focus on the other side: risk in the AI input.”

Then say:

“Before AI gives an answer, we decide what information to provide. That decision matters. If we paste unnecessary personal, confidential, or sensitive information into a tool, the risk has already started.”

Then add:

“Today’s goal is practical: learn what to avoid sharing, what to redact, how to minimize data, and how to still get useful AI assistance without exposing unnecessary details.”

---

## 4. Core Theory You Must Cover Briefly

Keep this section practical and concrete.

### 4.1 What privacy means in AI usage
Use this explanation:

**Privacy in AI usage means protecting personal, identifiable, sensitive, or unnecessary individual information from being shared or exposed without a valid reason.**

Then simplify:

**Privacy means not putting people’s unnecessary personal details into AI prompts.**

### 4.2 What confidentiality means in AI usage
Use this explanation:

**Confidentiality means protecting internal, restricted, sensitive, or non-public information that should not be disclosed outside the appropriate boundary.**

Then simplify:

**Confidentiality means not sharing internal or restricted information casually with AI tools.**

### 4.3 What data handling means
Use this explanation:

**Data handling means deciding what information to include, remove, mask, generalize, summarize, or verify before using AI.**

Then simplify:

**Data handling means controlling the input before asking AI for help.**

### 4.4 The core principle: data minimization
Teach this clearly:

**Data minimization means sharing only the minimum information required for the AI task.**

Then simplify:

**Do not provide details just because you have them. Provide only what the task needs.**

### 4.5 Why this matters
Explain:
- AI tools may process or retain data depending on platform settings
- users may not fully control where pasted data goes
- personal identifiers can expose individuals
- confidential information can create organizational risk
- unnecessary details can increase privacy risk without improving output
- safe prompting often works with redacted or generalized information

### 4.6 Important balance point
Say this clearly:

**Privacy protection does not mean AI cannot be used. It means AI should be used with controlled, minimized, and redacted input.**

---

## 5. One-Line Distinctions You Should Repeat During Session

Use these repeatedly:

**Privacy risk begins before the prompt is submitted.**

**Do not share what the task does not need.**

**Redact first, prompt second.**

**Minimum necessary context is better than maximum raw detail.**

**AI can help with sensitive workflows, but it should not receive unnecessary sensitive data.**

---

## 6. Concept Explanation You Must Deliver Clearly

### 6.1 The simplest mental model
You should say:

“Think of every AI prompt as information leaving your immediate control. Before sending it, ask: does the model really need this name, phone number, location, document number, internal code, or full case detail to perform the task?”

### 6.2 Another simple explanation
You may say:

“The goal is not to hide the useful context. The goal is to remove unnecessary identifiers and sensitive details while keeping enough information for the AI to help.”

### 6.3 Important caution
Also say:

“The most common privacy mistake is not malicious behavior. It is convenience: copying and pasting full raw text because it is faster.”

### 6.4 Important maturity point
Say this clearly:

“A mature AI user does not ask, ‘Can I paste this?’ A mature user asks, ‘What is the minimum safe version of this input?’”

---

## 7. What You Must Draw or Show on Screen

Use this data handling decision table.

| Input Type | Should It Be Shared Directly? | Safer Handling |
|---|---|---|
| Name, phone, address, ID number | No, unless absolutely necessary | redact or replace with labels |
| Internal confidential report | Usually no | summarize or use approved non-sensitive extract |
| Public information | Usually lower risk | still check accuracy and context |
| Rough professional notes | Maybe | remove identifiers and sensitive details |
| Legal/policy/factual claim | Needs care | ask for checklist, verify externally |
| Sensitive incident details | High risk | anonymize, generalize, or avoid sharing |

Then add below:

**Before prompting, reduce the data to what is necessary for the task.**

---

## 8. Demo 1 — Unsafe Prompt vs Redacted Prompt

### Purpose
To show that prompt safety depends heavily on what data is included.

### Unsafe prompt example
“Summarize this complaint: Rahul Sharma, phone 98XXXXXX21, address Flat 304, Green Heights, reported that Officer ABC failed to respond on 12 May. His Aadhaar number is XXXX-XXXX-XXXX. Draft an official note.”

### Safer redacted prompt
“Summarize this redacted complaint: A citizen reported delayed response by a named official on 12 May. Personal identifiers have been removed. Draft a neutral internal summary with sections: issue, date mentioned, pending verification, and next step. Do not assume fault.”

### What participants should observe
- the task can still be performed without personal identifiers
- names, phone, address, and ID were unnecessary for drafting structure
- safer prompt reduces privacy exposure
- safer prompt also avoids premature blame
- redaction improves both privacy and fairness

### Verbatim you can say
“Notice that the AI does not need the person’s phone number, exact address, or ID number to summarize the issue. If the task is drafting a neutral summary, those details are unnecessary and should be removed.”

### Key insight to emphasize
**Most drafting and summarization tasks do not need direct identifiers.**

---

## 9. Demo 2 — Data Minimization and Context Control

### Purpose
To show that useful AI output does not require maximum raw data.

### Full raw input style
“Here is the complete raw report with all names, locations, phone numbers, internal references, attachments, and full narrative.”

### Minimized input style
“Use this non-sensitive summary: A field review found two documentation gaps. One supporting report is pending. Follow-up is scheduled next Monday. Final decision should wait for document verification. Prepare a neutral briefing note.”

### What participants should compare
- Does the AI need full raw details?
- Does the minimized version provide enough context?
- What output quality changes?
- What risk is reduced?
- What must still be verified?

### Suggested prompt
“Using only the following non-sensitive summary, draft a neutral briefing note. Do not add facts, names, responsibility, or final conclusions.”

### Verbatim you can say
“Data minimization is not about giving the model no context. It is about giving the model the right amount of safe context. Enough for the task, not everything from the file.”

### Key insight to emphasize
**Useful context and excessive detail are not the same.**

---

## 10. Demo 3 — Converting Sensitive Notes into Safe AI Input

### Purpose
To practice transforming raw notes into AI-safe prompts.

### Raw note example
“Mr. X from Ward 12 complained against Staff Member Y. Mobile number included. Local address included. Issue occurred near a specific location. Complaint includes emotional language and unverified allegation. Need summary.”

### Step 1 — Identify sensitive elements
- person name
- staff name
- phone number
- exact address
- specific location if unnecessary
- emotional or accusatory wording
- unverified allegations

### Step 2 — Redact or generalize
- “complainant”
- “staff member”
- “local area”
- “reported concern”
- “allegation pending verification”

### Step 3 — Create safe prompt
“Summarize the following redacted complaint into a neutral internal note. Use labels such as complainant and staff member. Do not include personal identifiers. Do not assume guilt or fault. Separate reported allegation, known facts, missing information, and verification needed.”

### What participants should observe
- redaction does not destroy usefulness
- neutral labels reduce bias
- unverified allegations are handled carefully
- AI is asked to separate facts from allegations
- safe input improves responsible output

### Verbatim you can say
“This is the kind of practical skill professionals need. We are not just deleting words randomly. We are preserving the work-relevant meaning while removing unnecessary identifying or sensitive details.”

### Key insight to emphasize
**Safe AI input preserves purpose while reducing exposure.**

---

## 11. Activity — Redact and Rewrite Prompts Safely

### Duration
10 minutes

### Objective
Train participants to convert unsafe prompts into privacy-aware prompts.

### Instructions
Give participants unsafe prompts and ask them to rewrite them safely.

### Unsafe prompt set

#### Prompt 1
“Here is the full complaint with name, phone number, address, and ID details. Draft a report.”

#### Prompt 2
“Analyze this confidential internal report and write what action should be taken.”

#### Prompt 3
“Summarize these medical details and identify the person’s likely condition.”

#### Prompt 4
“Use this full staff performance note with names and personal issues to draft a warning.”

#### Prompt 5
“Here is a case narrative with exact locations, personal identifiers, and allegations. Tell me who is responsible.”

### Safer rewrite pattern
Ask participants to rewrite using:
- redacted input
- neutral labels
- minimum necessary facts
- no final decision delegation
- verification checklist
- human review boundary

### Verbatim you can say
“The goal is not to make the prompt useless. The goal is to make it safer. Preserve the work objective, remove unnecessary sensitive details, avoid final judgment, and ask for review support.”

### Trainer note
Push participants to explain:
- what they removed
- why they removed it
- what they kept
- what AI can still help with
- what humans must decide

---

## 12. Information Types to Protect Explicitly

### 12.1 Personal identifiers
Examples:
- full names
- phone numbers
- email addresses
- home addresses
- ID numbers
- account numbers
- photographs of individuals where unnecessary

### 12.2 Sensitive personal information
Examples:
- health details
- financial details
- family details
- children’s information
- personal complaints
- personal vulnerabilities
- disciplinary matters

### 12.3 Confidential organizational information
Examples:
- internal reports
- strategy documents
- investigation notes
- operational plans
- security details
- restricted memos
- non-public decisions

### 12.4 Case-sensitive information
Examples:
- witness details
- complainant details
- accused person details
- exact incident location where not required
- unverified allegations
- internal assessment comments

### 12.5 Authentication and access information
Never share:
- passwords
- API keys
- OTPs
- access tokens
- private links
- internal credentials

Use this line:

**Some information should not be put into AI at all, even in a well-written prompt.**

---

## 13. Practical Redaction Techniques

Teach these explicitly.

### 13.1 Remove direct identifiers
Replace:
“Rahul Sharma, 9876543210”
with:
“Complainant A”

### 13.2 Generalize locations
Replace:
“Flat 304, Green Heights, Lane 7”
with:
“a residential location”

### 13.3 Replace roles with labels
Replace:
“Officer ABC”
with:
“staff member” or “official concerned”

### 13.4 Remove unnecessary dates if not needed
If exact date is not necessary, use:
“earlier this month” or “on the reported date”

But caution:
If date is decision-critical, keep it.

### 13.5 Separate allegation from fact
Use:
“reported allegation”
“pending verification”
“not independently confirmed”

### 13.6 Use summaries instead of raw documents
Instead of pasting full confidential text, prepare:
“non-sensitive summary for drafting support”

### 13.7 Ask AI not to infer identities or fault
Add:
“Do not infer identity, responsibility, guilt, or final conclusion.”

---

## 14. Safe Prompt Patterns You Should Teach

### 14.1 Redacted summarization prompt
“Summarize the following redacted note. Do not include personal identifiers. Use neutral labels such as complainant, staff member, and location. Separate reported information, confirmed information, missing information, and verification needs.”

### 14.2 Confidential-content-safe drafting prompt
“Using only this non-sensitive summary, draft a neutral internal note. Do not add facts, names, responsibility, or final conclusions. Mention what must be verified before use.”

### 14.3 Sensitive allegation handling prompt
“Convert this redacted allegation summary into a neutral review note. Do not assume guilt or fault. Clearly mark allegations as reported, not verified. List missing information and next verification steps.”

### 14.4 Document review support prompt
“Create a checklist for human review based on this redacted summary. Do not make a final decision. Identify information needed before any conclusion.”

### 14.5 Public communication prompt
“Draft a general public-facing communication template based only on approved non-sensitive information. Avoid personal details, internal references, and unverified claims.”

---

## 15. High-Value Concepts to Emphasize During Discussion

### 15.1 Redaction is not just hiding names
Explain:
- identifiers can be direct or indirect
- exact location plus event plus role may identify someone
- redaction also includes removing unnecessary context

### 15.2 Data minimization improves safety
Explain:
- less unnecessary data means less exposure
- safer input still allows useful output
- the user must decide what is necessary

### 15.3 Sensitive tasks can often be reframed
Explain:
- ask for checklist instead of final decision
- ask for neutral summary instead of blame
- ask for structure instead of judgment
- ask for missing information instead of conclusion

### 15.4 Confidentiality is not only about people
Explain:
- internal processes
- reports
- strategies
- security details
- operational information

### 15.5 Human accountability remains
Repeat:
- AI can help draft
- AI can help summarize
- AI can help organize
- humans decide what can be shared and used

---

## 16. Exact Verbatim Blocks for the Trainer

Use these where useful.

### Verbatim Block 1 — Input risk
“AI safety is not only about checking the answer. It is also about controlling the input. What we paste into the prompt matters.”

### Verbatim Block 2 — Data minimization
“Data minimization means giving the AI only what it needs for the task, not everything we happen to have.”

### Verbatim Block 3 — Redaction
“Redaction is the process of removing or replacing identifiers and sensitive details while preserving the useful meaning needed for the task.”

### Verbatim Block 4 — Responsible handling
“A responsible user asks: what can be removed, what can be generalized, what must be kept, and what should not be shared at all?”

### Verbatim Block 5 — Human control
“AI can help us process information, but the responsibility for safe data handling remains with the human user.”

---

## 17. Questions You Should Ask Throughout the Session

Use these to maintain engagement:
- Does AI need this exact name?
- Does AI need this phone number or address?
- Can this be replaced with a neutral label?
- Is this information personal, confidential, or sensitive?
- Can we summarize instead of pasting raw text?
- What is the minimum context needed?
- Does this prompt ask AI to make a final decision?
- What should be verified by a human?
- Is there any unverified allegation?
- How can we make this safer while preserving usefulness?

---

## 18. Risks and Cautions to Mention Even in This Session

Mention these calmly:
- people often paste too much because it is convenient
- indirect identifiers can still reveal identity
- confidential internal information is also sensitive
- redaction must preserve decision-critical facts
- over-redaction can remove necessary context
- AI should not be asked to decide responsibility from sensitive allegations

Use this line:

**The safest useful prompt keeps enough context for the task and removes everything unnecessary.**

---

## 19. Optional Mini Demo if Time Allows

### Redaction quality demo
Show two bad redactions:

#### Under-redacted
“Complainant A from Flat 304, Green Heights, Ward 12…”

Problem:
Still likely identifiable.

#### Over-redacted
“Someone reported something somewhere.”

Problem:
Too vague to help.

### Balanced redaction
“A complainant reported delayed response by a staff member in a local area. The allegation is pending verification.”

### Teaching point
Good redaction balances privacy and usefulness.

---

## 20. Suggested Whiteboard or Screen Structure

Use this layout:

### Left side
**Raw Input**
- names
- phone numbers
- exact locations
- internal details
- allegations
- confidential notes

### Middle
**Data Handling**
- remove
- mask
- generalize
- summarize
- label
- verify

### Right side
**Safe AI Input**
- redacted context
- neutral labels
- minimum necessary facts
- no final judgment
- verification needs

Then add below:
**Redact first, prompt second, review before use**

---

## 21. Closing Recap You Should Deliver

End with a strong summary:

“Today we learned that privacy, confidentiality, and data handling are central to responsible AI use. The risk does not begin only in the AI answer. It begins with what we choose to put into the prompt.”

Then add:

“We practiced data minimization, redaction, generalization, neutral labeling, and safer prompt design. We also saw that useful AI assistance does not usually require unnecessary personal or confidential details.”

Then bridge forward:

“In the next session, we will continue responsible AI usage by focusing on bias, fairness, and framing, because even when data is protected, the way a prompt is framed can still shape unfair or misleading outputs.”

---

## 22. End-of-Session Participant Takeaway

Participants should leave with these five ideas:
1. privacy risk begins before the prompt is submitted
2. data minimization means sharing only what the task requires
3. personal identifiers and confidential details should be removed or generalized when unnecessary
4. redacted prompts can still produce useful AI output
5. humans remain responsible for safe data handling

---

## 23. Suggested Homework or Reflection

Keep it light.

### Homework option
Ask participants to take one unsafe prompt and rewrite it into a safe prompt by:
- removing direct identifiers
- generalizing unnecessary locations
- replacing names with neutral labels
- marking allegations as unverified
- asking for a checklist instead of final decision

This prepares them for Day 7: Bias, Fairness, and Framing.

---

## 24. Quick Backup Prompts for the Trainer

Use these if the flow slows down.

### Prompt 1
“Redact the following text for safe AI use while preserving the work-relevant meaning.”

### Prompt 2
“Rewrite this unsafe prompt into a privacy-aware prompt.”

### Prompt 3
“Identify personal, confidential, and sensitive information in this text.”

### Prompt 4
“Create a data minimization checklist before using AI for professional notes.”

### Prompt 5
“Convert this raw sensitive note into a safe AI prompt that asks for a neutral summary and verification checklist.”

---

## 25. Trainer Cautions for Delivery

- do not make privacy sound only like a legal topic
- do not use real personal data in examples
- do not over-redact examples until they become useless
- do not skip confidentiality beyond personal data
- do not encourage pasting raw sensitive documents
- do not let participants think redaction removes need for review
- do not let AI decide responsibility from unverified allegations

---

## 26. Final Trainer Reminder

Today’s success is measured by whether the participant can look at a prompt and ask:

**What information is unnecessary? What should be redacted? What can be generalized? What must be kept for context? What should not be shared at all?**

If they can answer these clearly, Phase 2 Day 6 has achieved its purpose.
