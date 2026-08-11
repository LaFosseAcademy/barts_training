# Module 3 (Continued) — Accelerating with Copilot, Chat-Only
### Barts Health NHS × La Fosse — Microsoft 365 Data Skills Training

**Follow-on Session | Duration: 2 hours | 09:00–11:00 | Platform: Microsoft 365 Copilot Chat**
**Six blocks, with a 10-minute break after Block 2**

## Pre-Session Setup

- Load Slide deck: barts_module_3_session2
- Confirm everyone can get to Microsoft 365 Copilot Chat directly (copilot.microsoft.com, or the Copilot icon in Teams / the taskbar) rather than the Copilot pane inside an open Excel, Word or PowerPoint file
- Files needed on OneDrive or SharePoint: `0923 BSc Student allocations (LSBU-Barts Health)` and `Apprentice KPI tables April 2026.xlsx`

## Training

- `Slide 1`

### Recap

Morning everyone, welcome back.

Last time we didn't quite make it through everything I'd planned due to a few technical challenges, so today is really a continuation rather than a brand new module. We're going to move a bit quicker because a lot of this will build directly on what we already covered.

Just to remind ourselves where we got to:

- We recapped modules 1 and 2, where we manually cleaned, analysed and presented data
- We covered what a Large Language Model actually is and why it can get things wrong
- We looked at effective prompting using role, context, task, constraints and output
- We started using Copilot chat inside Excel to clean data and build things like Pivot Tables and simple agents

Today, everything we do is going to happen from **Copilot Chat itself**, rather than from inside Excel, Word or PowerPoint. That's a deliberate constraint. On a lot of NHS devices and licences, chat is the one surface everyone can reliably get to, and it's also the fastest way to get a feel for what Copilot can and can't do without needing to open three different apps. Everything we did last time inside an app, we'll now do purely by attaching files to a chat window and reading what comes back.

I'd also like to emphasise that part of the role of this session is to ask questions and develop understanding so if, since the last session, you've tried things and they've worked well, I'd encourage you to share those.

## Block 1 - Recap: LLMs & Effective Prompting *(15 mins)*

Starter Prompt Questions - LLMs:

- *"Who can tell me the difference between how a human learns language and how an LLM does?"*
- *"What's a hallucination, and why does it matter more in a spreadsheet than in a casual chat?"*
- *"What are the five parts of a well-structured prompt?"*

### What is an LLM? (Quick Recap)

We covered this in detail last time, so just a short reminder:

- An LLM doesn't store facts like a database — it's learned patterns in language from enormous amounts of text
- It predicts the most likely next words based on those patterns, it doesn't "look things up"
- That means it can produce confident, fluent answers that are still wrong — we call this **hallucination**
- If the data it was trained on wasn't formatted to NHS standards, the patterns it's learned about spreadsheets won't be either

The takeaway from last time still holds: Copilot is only as trustworthy as the person reviewing its output.

### Effective Prompting Recap

- `Slide 3`

We also covered the five-part anatomy of a good prompt. It's worth repeating because everything in today's session depends on it:

- **Role**: what you want Copilot to behave as, e.g. *"Act as a training lead for NHS Barts Trust"*
- **Context**: what the data or document is actually about
- **Task**: the specific thing you want Copilot to do
- **Constraints**: limits on format, length, tone, what to ignore
- **Output**: how you want the result — a list, a table, a downloadable file, a short paragraph

The more complex or important the task, the more of these five you should be explicit about. For anything you're going to rely on or share with someone else, don't just type a one-line question — build the prompt properly.

## Block 2 - Cleaning Data in Copilot Chat Only *(25 mins)*

Last time, we cleaned `0923 BSc Student allocations (LSBU-Barts Health)` from inside Excel Online, using the Copilot pane in the corner of the screen. Today we're going to do the same job, but without opening Excel at all.

- *Open Microsoft 365 Copilot Chat*
- *Click the `+` symbol and attach* `0923 BSc Student allocations (LSBU-Barts Health)` *directly from OneDrive*

The difference is subtle but important: we're not opening the file first to look at it, we're handing it straight to chat and working entirely from prompts. This is closer to how most staff will actually use Copilot day-to-day — most people won't have Excel open on one screen and a chat pane open next to it, they'll just be working from chat.

We'll run the same three cleaning prompts as last time, one at a time.

#### Prompt 1 - Trim Whitespace

*"Remove all leading and trailing whitespace from every cell in this spreadsheet and give me a downloadable copy of the result."*

#### Prompt 2 - Standardise Casing in Column A

*"Standardise the text in column A to title case and give me a downloadable copy of the result."*

#### Prompt 3 - Add the Original Cohort Column

*"Insert one new column immediately to the right of column A. Name it 'Original Cohort'. For each row, copy the value from column A into this new column, then remove any suffixes including '-contin', '-continued', '-ext degree', and any similar variations, so that values read as their base cohort only. Give me a downloadable copy of the result."*

**NB Because we're chat-only, Copilot will hand back a new file each time rather than editing in place — the phrase "give me a downloadable copy" in the prompt is doing a lot of work here. Without it, you may just get a description of the changes rather than an actual file.**

Once you've got the file back, this is the point where you *would* open it — not to make the changes yourself, but purely to review what Copilot has done. Chat-only doesn't mean review-free. If anything, because you can't see the highlighted changes as they happen the way you could inside Excel, the review step matters more here, not less.

- *Open the returned file briefly to spot-check the whitespace, casing and new column*

### Break *(10 mins)*

## Block 3 - Building Pivot Tables in Copilot Chat *(25 mins)*

Now let's do the same thing with `Apprentice KPI tables April 2026.xlsx`, building the Pivot Table we made last time entirely from chat.

- *Open a new Copilot Chat window and attach* `Apprentice KPI tables April 2026.xlsx`

Same prompt as before, with one addition — we need to explicitly ask for something we can open and check, since we're not sat inside Excel watching it build.

*"Create a pivot table with a primary row of staff group and a column of ethnicity, then for values a count of name, ignoring staff groups of N/A and blank. Give me this as a downloadable Excel file."*

Once that comes back, open it briefly to check the structure looks right, then we'll go one step further and ask chat for the chart in the same way.

*"Using the pivot table you just created, generate a stacked bar chart showing total count in each staff group, broken down by ethnicity. Give me this as a downloadable file with the chart included."*

- *Wait for the file to be created*
- *Open the file to review the chart*

This is really the same workflow as Block 2 in the original session — the only thing that's changed is where we're sitting when we ask for it. That's worth naming explicitly to the group: **the skill isn't "using Copilot in Excel", it's writing a good prompt and reviewing what comes back. Where you happen to be sitting when you type the prompt matters much less than people assume.**

**NB If the chart title or formatting isn't quite right, you can either ask chat to redo it with a new instruction, or open the returned file and tidy it up yourself — both are valid, and for small formatting fixes, doing it yourself is often faster than round-tripping through another prompt.**

## Block 4 - Word & PowerPoint from Copilot Chat *(25 mins)*

Different people have different licenses on this but one thing I want to look at is how to build a PowerPoint and a Word summary from chat, without opening PowerPoint or Word at any point.

- *Stay in the same Copilot Chat window, with the pivot table and chart file still attached*

#### PowerPoint

*"Create a PowerPoint presentation with 3 slides: Slide 1 should contain the stacked bar chart of ethnicity by staff group. Slide 2 should give 3 key insights regarding the ethnic spread of apprentices amongst the staff groups. Slide 3 should be a short 'next steps for review' slide. Use a concise, minimal and professional tone throughout."*

- *Wait for the file to be created, then download and open it to review*

#### Word

*"Act as an NHS Barts Health administrator reviewing workforce equality data. Analyse the ethnicity by staff group data in the attached file and provide a concise summary of the overall pattern, focusing on whether ethnicity representation is broadly evenly distributed across staff groups and highlighting any notable variations. Present the output as a Word document containing a short professional paragraph followed by 3–4 key takeaway bullet points suitable for inclusion in a report."*

- *Wait for the file to be created, then download and open it to review*

Talk through what to expect here:

- Chat-generated Word and PowerPoint files tend to get the **structure and coverage** right — headings, sensible slide breakdown, a sensible paragraph-then-bullets shape
- **Formatting** is where it usually falls down — spacing, slide layout, chart placement will often need a manual pass once downloaded
- You still can't easily chain services automatically — Copilot Chat can see the file you attached, but it isn't independently going off and pulling live data from three different systems. You are still the one attaching the right file to the right prompt

**NB This is a good moment to flag: everything from Block 2 onwards has actually been the same three-step pattern repeated — attach the file, prompt for role/context/task/constraints/output, download and review. Once that pattern clicks, the specific app almost becomes irrelevant.**

## Block 5 - What to Use Copilot For, and Where It Falls Short *(10 mins)*

- `Slide 4`

Pulling together everything from both sessions, here's where Copilot chat earns its keep, and where it doesn't.

**Good uses of Copilot:**

- Drafting emails, meeting summaries or narrative copy from data you provide
- Summarising a spreadsheet, document or chat thread in plain English
- Suggesting Excel formula syntax
- Cleaning routine, repeatable issues — whitespace, casing, obvious duplicates
- Building a first-draft Pivot Table, chart, Word summary or slide deck to work from

**Where it's high-risk:**

- Anything involving a specific named individual — a typo in a name like Sophia, Layla or Muhammed can silently pull the wrong record
- Contracts, policy documents, or anything apprentices or staff need to read and sign — verify Copilot has the right document before it goes anywhere
- Any output that's about to be shared externally or relied on for a decision without you checking the underlying data yourself

**Where it's simply not worth it:**

- If you already know exactly where a piece of information lives and can find it faster than you could write and review a prompt, just go and get it manually

**The five-point check before anything created by Copilot is shared:**

1. **Accuracy** — are the numbers, names and figures actually correct?
2. **Completeness** — does it cover everything you know needs to be there?
3. **Tone and register** — will it land correctly with the intended audience?
4. **Specificity** — has it used Barts Health's own terms correctly (learners / students / apprentices, site names, staff group names)?
5. **Actionability** — if someone needs to *do* something, is that instruction actually clear?

Copilot won't understand Barts Health's reporting conventions, the specific context behind a set of numbers, or what a particular stakeholder cares about. What it will do is produce a plausible, well-structured first draft. Treat everything it gives you as a starting point, never the finished, sign-off-ready version.

## Block 6 - Extension Task *(10 mins, take-home if needed)*

To check and stretch what's landed today, work through this on your own before we next meet.

**Check your understanding:**

- In your own words, explain why an LLM can sound confident and still be wrong
- Write out a role / context / task / constraints / output prompt for a task you'd actually use at work — not one of today's examples
- Name one task you'd now trust to Copilot chat unsupervised, and one you never would, and say why

**Advance your understanding:**

Pick a spreadsheet you use regularly (or use `0923 BSc Student allocations (LSBU-Barts Health)` again) and, using Copilot Chat only:

1. Ask Copilot to identify any data quality issues, without you looking at the file first
2. Build one Pivot Table or chart answering a real question you have about that data
3. Turn the result into either a short Word summary or a 3-slide PowerPoint, entirely from chat
4. Run your own output through the five-point check from Block 5 and note down anything you'd change before sharing it

Bring what you produced to the next session — we'll compare notes on where Copilot got it right, where it needed correcting, and whether the chat-only approach felt faster or slower than working inside the app.
