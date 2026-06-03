# Module 3 — Accelerating with Copilot
### Barts Health NHS × La Fosse — Microsoft 365 Data Skills Training

**Day 2 | 09:15–11:30 | Platform: Microsoft Copilot within Excel Online, PowerPoint Online, Word Online, Outlook, Teams**
**Four 30-minute blocks, with a 15-minute break after Block 3**

> **Day 2 opens (09:00–09:15)** with a brief facilitator-led recap of Day 1, covering the Context → Insight → Recommendation narrative framework introduced at the end of Module 2. This bridges the two days and frames how Copilot will accelerate the same workflow participants have already built manually.

---

## Overview

Module 3 builds directly on everything covered in Modules 1 and 2. Participants have already completed the full data workflow manually — accessing data, cleaning it, analysing it with formulas, and building formatted charts with insight-led titles. Module 3 asks: how much of that can be done faster, using Microsoft Copilot?

The honest answer is: quite a lot, for the right tasks, with the right prompts, and with a human reviewing everything before it is shared. Module 3 is about developing the judgement to know which parts of the workflow benefit most from AI assistance, how to prompt effectively to get useful outputs, and how to validate those outputs rigorously before they go anywhere near a stakeholder.

This is not a module about replacing the skills from Modules 1 and 2. It is about applying them with greater speed and less manual effort — and understanding that Copilot's outputs are only as trustworthy as the person reviewing them.

---

## Where Module 3 Sits in the Data Lifecycle

```
Collection → Storage → Access → Cleaning → Analysis → Visualisation → Communication → Action
```

Copilot operates across multiple stages of the lifecycle simultaneously, which is both its strength and the source of its main risk. It can help at the **Analysis** stage (suggesting formulas, summarising data), the **Visualisation** stage (generating first-draft slides from data), and the **Communication** stage (drafting emails, meeting summaries, narrative text). It can also move between these stages very quickly — which means errors made early can propagate into outputs that look finished before anyone has caught them.

Module 3 teaches participants to use Copilot as an accelerator at each of these stages, while maintaining the analytical discipline developed in Modules 1 and 2. The key shift is from Copilot as a shortcut to Copilot as a collaborator — one that produces useful first drafts that still require expert human review.

---

## Learning Goals

By the end of this module, participants will be able to:

- Write clear, structured prompts that produce useful outputs for common administrative and data tasks
- Use Copilot in Excel to generate formulas, summarise datasets, and surface anomalies
- Use Copilot in PowerPoint to produce first-draft slide content from a prompt or source document
- Use Copilot in Word, Outlook, and Teams to accelerate drafting, rewriting, and summarisation tasks
- Validate Copilot-generated outputs before sharing or using them
- Identify which tasks in their own role are best suited to Copilot assistance, and which still require full manual effort

---

## Main Areas Covered

- How Microsoft Copilot works within the M365 suite: what it has access to, what it cannot do, and its known limitations
- Effective prompting: the components of a well-structured prompt and common mistakes to avoid
- Copilot in Excel: formula generation, data summarisation, anomaly detection
- Copilot in PowerPoint: slide generation from prompts, documents, and existing data
- Copilot in Word: drafting, rewriting, and summarising documents
- Copilot in Outlook and Teams: email drafting, meeting summarisation, and action point generation
- Validation: what to check in any Copilot output before using or sharing it
- Identifying where Copilot adds value versus where it introduces risk or requires more effort to fix than to do manually

---

## Block Breakdown

---

### Block 1 — Effective Prompting & Copilot in Excel
**09:15–09:45**

#### What we cover

- A short orientation to how Copilot works within Microsoft 365: it has access to the file you are working in, and to other files and emails in your M365 environment depending on your organisation's settings; it generates responses based on context, not on a guaranteed understanding of your data
- The anatomy of a good prompt, with five components:
  - **Role**: who you are asking Copilot to be ("Act as a data analyst reviewing a compliance report…")
  - **Context**: what the data or document is about ("This is a monthly mandatory training completion tracker for Barts Health staff…")
  - **Task**: what you specifically want Copilot to do ("Summarise the key patterns in completion rates by directorate…")
  - **Constraints**: any limits on format, length, or scope ("in no more than three bullet points…")
  - **Output format**: how you want the result presented ("as a table" / "as a paragraph" / "as a slide title and three supporting bullets")
- Common prompting mistakes: being too vague, asking multiple unrelated questions in one prompt, not providing enough context about the data, accepting the first output without iterating
- Copilot in Excel: three specific use cases with demonstration:
  - Asking Copilot to explain what a dataset contains and identify any obvious quality issues
  - Asking Copilot to suggest a formula for a specific task (e.g. "write a formula that counts how many staff in column B have not completed training, based on the value in column C")
  - Asking Copilot to summarise a column or table in plain language
- Hands-on: use Copilot to generate two formulas from a provided dataset, then manually verify each one against the data and correct any errors

#### Why this matters

Prompting is a skill, not a knack. The difference between a prompt that produces a useful output and one that produces a vague or incorrect one is usually the amount of context and specificity provided. Most people's first instinct is to treat Copilot like a search engine — short, keyword-style inputs — and then be disappointed when the output is generic.

The five-component framework gives participants a repeatable structure they can apply to any task, not just the ones practised in this session. It also develops the habit of thinking clearly about what they actually want before they ask for it — which is a useful discipline regardless of whether AI is involved.

The focus on validation in the hands-on exercise is deliberate. Copilot can generate a syntactically correct formula that does the wrong thing — counting the wrong column, using the wrong comparison operator, returning a result that looks plausible but is not accurate. The only way to catch this is to understand what the formula should do and check it against a few known values manually. Participants who have worked through Module 1 already have the knowledge to do this. Module 3 reinforces that this knowledge is not optional even when Copilot is doing the writing.

#### Where you will use this in the data lifecycle

Copilot in Excel sits primarily at the **Analysis** stage. The most relevant applications at Barts Health are:

- Generating XLOOKUP or COUNTIFS formulas for datasets where the logic is clear but the syntax is unfamiliar or time-consuming to write from scratch
- Asking Copilot to describe a dataset on first open — a faster version of the first-look audit from Module 1, though not a replacement for it
- Surfacing potential data quality issues in large exports (e.g. "are there any rows where the date in column D is earlier than the date in column C?")
- Generating a natural language summary of a summary table to use as a starting point for a written narrative

Effective prompting applies across every block in this module and every tool in the M365 suite. The time invested in learning to prompt well in Block 1 pays dividends across Blocks 2, 3, and 4.

---

### Block 2 — Copilot in PowerPoint & Word
**09:45–10:15**

#### What we cover

- **Copilot in PowerPoint**: three use cases with demonstration:
  - Generating a first-draft slide deck from a written prompt ("Create a five-slide summary of mandatory training compliance for a clinical director audience, covering current completion rates, trends over the past quarter, and recommended actions")
  - Generating slides from an existing Word document or report summary — Copilot reads the document and proposes a slide structure
  - Asking Copilot to improve or reformat an existing slide ("Rewrite this slide title as an insight-led headline" / "Reduce this bullet list to three points without losing the key message")
- What Copilot-generated slides typically get right and where they consistently need improvement: structure and coverage are usually reasonable; specific data accuracy, Barts Health-specific language, and formatting standards almost always need manual correction
- **Copilot in Word**: three use cases with demonstration:
  - Drafting a narrative summary from a data table or bullet list ("Write a two-paragraph summary of these compliance figures for a monthly operational report, suitable for a non-technical audience")
  - Rewriting a section for a different tone or audience ("Rewrite this paragraph for a clinical lead rather than a finance manager")
  - Summarising a long document to extract key points and action items
- Hands-on: use Copilot in PowerPoint to generate a first-draft summary slide from the Module 2 charts and data, then edit it to meet an accurate, insight-led standard — applying the narrative framework and formatting principles from Modules 1 and 2

#### Why this matters

The most time-consuming part of producing a report or presentation is not the analysis — it is the drafting. Writing narrative text, structuring slides, and deciding how to frame findings for a specific audience are tasks that require cognitive effort and are often done under time pressure. Copilot can produce a useful first draft of all of these in seconds.

The critical word is first draft. Copilot does not know Barts Health's reporting conventions, the specific context behind the numbers, or the preferences and priorities of the stakeholder receiving the output. It will write in a plausible register, but plausible is not the same as correct, and it will frequently miss the specific finding that makes a report worth reading.

The skill being developed here is not how to use Copilot — it is how to use it as a starting point rather than an endpoint. Participants who can rapidly generate a Copilot draft and then efficiently edit it to the required standard will produce better outputs faster than those who either avoid Copilot entirely or accept its outputs without review.

#### Where you will use this in the data lifecycle

This block sits at the **Communication** stage of the lifecycle. At Barts Health, the most relevant applications are:

- Generating a first-draft narrative for a monthly directorate report, then editing it to ensure the specific findings and Barts Health context are accurate
- Producing a first-draft PowerPoint summary from an existing Word briefing note or data summary, saving the time of building a slide structure from scratch
- Rewriting technical or dense language from a compliance or finance report into plain English for a clinical audience
- Drafting a narrative introduction for a board paper that summarises the analytical findings developed in Modules 1 and 2

The connection back to Module 2 is explicit in the hands-on exercise: the charts built and formatted yesterday are the inputs. Copilot is the drafting accelerator. The participant's analytical judgement — informed by Modules 1 and 2 — is what makes the output trustworthy.

---

### Block 3 — Copilot Across Teams & Outlook
**10:15–10:45**

#### What we cover

- **Copilot in Microsoft Teams**: two use cases with demonstration:
  - After a meeting, using Copilot to generate a meeting summary including key discussion points, decisions made, and actions agreed — with owners and deadlines where identified
  - During a meeting, using Copilot to surface a question or summary from the meeting transcript in real time (where this feature is enabled)
- **Copilot in Outlook**: three use cases with demonstration:
  - Drafting an email from a brief prompt ("Draft an email to directorate leads summarising October's mandatory training completion figures and asking for a response on any teams below 80% by Friday")
  - Summarising a long email thread to extract the current status and any outstanding actions, without reading every message
  - Suggesting a reply to an email, which can then be edited for tone, accuracy, and specificity before sending
- The importance of editing Copilot-drafted communications before sending: tone, specificity, accuracy of any data referenced, and appropriateness for the specific recipient
- Hands-on: draft a stakeholder communication using Copilot in Outlook — a brief email to a clinical or operational lead summarising a finding from the training data — then edit it to ensure accuracy, appropriate tone, and a clear ask

#### Why this matters

Administrative staff in an NHS trust spend a significant proportion of their working day in Teams and Outlook — attending meetings, following up on actions, communicating findings and requests to clinical and operational colleagues. These are not peripheral tasks; they are how decisions get made and actions get driven. They are also cognitively demanding: finding the right tone for a sensitive message, summarising a complex situation clearly, or extracting the key action from a lengthy email chain all take time and focus.

Copilot can meaningfully reduce the effort of all of these tasks. A meeting summary that would have taken twenty minutes to write from notes can be generated in under a minute and edited in five. An email that needs careful drafting to strike the right tone with a senior clinical lead can be started from a Copilot draft and refined, rather than written from a blank page.

The discipline of reviewing before sending is non-negotiable. Copilot does not know the history of a relationship with a stakeholder, the sensitivity of a particular finding, or the specific ask that needs to be made clearly. It produces a plausible draft. The participant's knowledge and judgement produce the final version.

#### Where you will use this in the data lifecycle

This block sits at the **Communication → Action** stage — the final steps of the lifecycle, where findings are shared and responses are requested. At Barts Health:

- Following a data review meeting, using Copilot to generate action notes that can be shared with attendees immediately, rather than hours later when memory has faded
- Drafting follow-up emails to ward managers, directorate leads, or department heads that communicate a compliance or performance finding clearly and ask for a specific response
- Summarising a long email thread from a clinical or operational lead to quickly understand the current status of a request or issue before responding
- Generating a weekly or monthly update email from a brief bullet-point summary of the week's key data findings

These are tasks that happen every week, often multiple times a week. The cumulative time saving from using Copilot effectively on routine communications is significant — time that can be redirected to more complex analytical and stakeholder work.

---

*— Break 10:45–11:00 —*

---

### Block 4 — Validating Outputs & Building Repeatable Workflows
**11:00–11:30**

#### What we cover

- A structured validation checklist for any Copilot output before it is used or shared:
  - **Accuracy**: are any numbers, names, dates, or facts correct? Has Copilot invented anything that sounds plausible but cannot be verified?
  - **Completeness**: has Copilot captured everything that matters, or has it summarised in a way that omits a significant finding?
  - **Tone and register**: is the language appropriate for the intended audience and purpose?
  - **Barts Health specificity**: does the output reflect the specific context, standards, and terminology of Barts Health, or is it generic?
  - **Actionability**: if the output is a recommendation or communication, is the ask clear and specific?
- Understanding hallucination: what it is (Copilot generating plausible but incorrect content), why it happens, and why it is especially risky when the output contains specific data or statistics
- Identifying which tasks are high-value for Copilot and which are high-risk or low-value:
  - High-value: drafting, summarising, generating formula syntax, reformatting, rewriting for a different audience
  - High-risk without strong validation: any output containing specific numbers, named individuals, clinical references, or policy statements
  - Low-value: tasks where the manual version takes less time than writing a good prompt and reviewing the output
- Building simple, repeatable Copilot workflows: the concept of a prompt template — a reusable prompt structure for a recurring task that only requires updating the variable elements each time
- Hands-on: participants identify two recurring tasks in their own role, assess whether Copilot would add value to each, and draft a prompt template for one of them

#### Why this matters

The risk of Copilot is not that it fails obviously — it is that it fails convincingly. An incorrect formula that returns a plausible number, a meeting summary that omits a key action, an email that references a figure that Copilot has slightly misremembered: these are the failure modes that matter in an NHS administrative context, because they can lead to decisions being made on incorrect information.

The validation checklist is not bureaucracy — it is professional practice. Every output that leaves a participant's hands as their work, regardless of how it was generated, carries their name and their credibility. Developing the habit of reviewing Copilot outputs with the same critical eye applied to any other draft is what makes AI assistance safe to use in a healthcare setting.

The concept of prompt templates is practically valuable for exactly the recurring, time-consuming tasks that Copilot is best suited to. A compliance update email that needs to be sent monthly can be drafted in thirty seconds from a template, rather than written from scratch each time. Building those templates — once, carefully — is an investment that pays off repeatedly.

#### Where you will use this in the data lifecycle

Validation and workflow design are relevant across every stage of the lifecycle where Copilot is used. At Barts Health specifically:

- Any Copilot-generated formula used in a compliance or financial report must be verified against known values before the report is shared — the consequences of a wrong total in a board paper are significant
- Any Copilot-drafted communication to a clinical lead or senior manager must be reviewed for accuracy, tone, and Barts Health-specific context before sending
- Prompt templates can be built and shared across teams for the most common recurring tasks: monthly compliance summary emails, meeting action note formats, report narrative structures — creating consistency and saving time at scale
- Understanding the limits of Copilot helps participants know when to escalate, when to seek a second review, and when a task is genuinely better done manually

---

## Module Conclusion

By the end of Module 3, participants have a working understanding of Copilot across the M365 suite and a set of practical skills for using it to accelerate the most time-consuming parts of the data workflow. More importantly, they have a framework for using it safely — knowing what to check, what to distrust, and where manual effort remains essential.

The key principles from this module are:

- **Prompt with specificity.** Vague prompts produce vague outputs. The five-component prompt structure — role, context, task, constraints, output format — is the foundation of effective Copilot use.
- **Copilot is a first draft, not a final product.** Every output requires human review before it is used or shared. This is not optional in a healthcare administrative context.
- **Validate against reality.** For any output containing numbers, names, or specific facts, verify against the source before proceeding. Copilot hallucination is rare but real.
- **Build workflows, not one-off prompts.** The highest value from Copilot comes from reusable prompt templates for recurring tasks — not from using it ad hoc for whatever comes to hand.
- **Know your limits.** Some tasks are faster and safer done manually. Recognising which tasks those are is as important as knowing which tasks Copilot can accelerate.

---

*Module 3 is part of the Barts Health NHS × La Fosse Microsoft 365 Data Skills Training Programme. All datasets used in training are anonymised. Delivered using Microsoft Copilot within Microsoft 365 Online tools.*
