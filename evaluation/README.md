# Training Follow-Up — Recap, Clean Data Habits & Your Prompt Dictionary
### Barts Health NHS × La Fosse — Microsoft 365 Data Skills Training

**Follow-on Session | Duration: ~65–75 minutes (Questions block is open-ended) | Platform: Microsoft Excel Online + Microsoft 365 Copilot Chat**

## Pre-Session Setup

- Load [Slide deck](./slidee/barts_evaluation.slides.md)
- Open `Dirty_Data_Activity.xlsx` on the shared screen — **remove or hide the "Facilitator Answer Key" tab before sharing this file with participants**
- Have `Prompt_Dictionary_Template.xlsx` ready to send to each participant, either before the session or at the start of Block 4
- Files referenced from earlier modules, in case anyone wants to see the "clean" version again: `0923 BSc Student allocations (LSBU-Barts Health)`, `Apprentice KPI tables April 2026.xlsx`

## 0. Welcome 

Susana to welcome participants and go through schedule.

## Training

- `Slide 1`

## 1. Recap - Introduction *(10 mins)*

Morning everyone, good to have you all back.

This is the last session in the series, so today's a bit different in shape to the others. We're not covering new ground — everything we're doing today pulls together what you've already seen across Modules 1, 2, 3 and 4. The idea is to leave you with two things: sharper instincts for spotting bad data before it causes a problem, and a personal reference you'll actually keep using once this course is finished.

So today, in short:

- We'll recap why the data lifecycle and clean data still matter, even with Copilot in the picture
- We'll run a group activity spotting real data quality issues on a live spreadsheet
- We'll open the floor for questions — anything from earlier sessions you want to revisit
- And we'll close by building the start of your own personal Prompt Dictionary, based on your actual day-to-day work rather than our training examples

**NB This is also our evaluation point for the course as a whole — we'll be asking you throughout to reflect on what's landed and what you'd still like to look at, so keep that at the back of your mind as we go.**

## 2. Recap *(20 mins)*

### Why data still matters

- `Slide 2`

Quick reminder of where we've been. In Module 1 and 2 we manually worked through a full data workflow — accessing, cleaning, analysing with formulas and PivotTables, then presenting. In Modules 3 and 4 we looked at how much of that Copilot can speed up.

None of that changes one basic fact: whoever — or whatever — is doing the analysis, the quality of the output is bounded by the quality of the input. Copilot doesn't fix that, it just does the next step faster. If the input's wrong, you now get a wrong answer delivered with more confidence and less effort than before.

### The data lifecycle

- `Slide 3`

We've seen this diagram a few times now: Collection → Storage → Access → Cleaning → Analysis → Visualisation → Communication → Action.

The reason it keeps coming back is that Cleaning sits right in the middle, before Analysis, not after it. Skip it, or do it badly, and every stage downstream — the formula, the Pivot Table, the chart, the slide, the email — inherits the same problem. With Copilot in the loop across multiple stages at once, that inheritance happens faster than it used to.

### Garbage in, garbage out

This is the phrase I want you to leave with today. An LLM analysing a messy spreadsheet won't tell you the spreadsheet was messy — it'll just give you a fluent, confident, plausible-sounding answer regardless. It's on you to know what "trustworthy data" looks like before you ever ask Copilot a question about it.

Which brings us to the activity.

### Activity — Spot the Dirty Data *(8–10 mins)* - Simon / Emile

- *Open* `Dirty_Data_Activity.xlsx`

I've put together a version of a spreadsheet you've seen before. I want you to find things you'd want to check or fix before you'd trust this sheet enough to analyse it or hand it to Copilot.

**Run as Paired Activity**

**Aim for 8 things.** They range from the obvious to the easy-to-miss. A nudge if you get stuck: think back to the First-Look Audit Checklist from Module 1 — duplicates, blanks, number formats, date formats, inconsistent text, trailing spaces. Every issue on this sheet falls into one of those six buckets.

- *Give people 4–5 minutes to look write down, then take answers from the room*
- *Reveal each issue as it's called out, using the categories above to group similar answers together*

**NB Don't rush to confirm or deny an answer the instant it's raised — ask the room "does everyone agree that's an issue, and why?" first. The discussion is worth more than the answer.**

### Communicating what you find

Once you've cleaned and analysed something, the job isn't done. The penultimate stage of the lifecycle — Communication — is just as easy to get wrong as Cleaning is, and it's where a lot of good analysis goes to waste.

Choosing the right evidence and the right format matters: a chart when someone needs to see a pattern at a glance, a one-page summary when someone needs the headline without the detail, a full table when someone needs to audit the numbers themselves. We covered generating all three of these through Copilot chat in the last session — today's reminder is just that the choice of format is a decision, not an afterthought.

## 3. Questions - Susana / Simon / Emile

This is open floor — anything from any of the sessions so far is fair game, not just today's recap.

A few prompts to seed the discussion if the room's quiet:

- *"Has anyone tried using Copilot chat for something at work since the last session? How did it go?"*
- *"Is there a task you're still not sure whether to hand to Copilot or do manually?"*

## 4. Next Steps *(20 mins)*

- `Slide 4`

### Building your Prompt Dictionary

Everything so far has used our examples. This last block is about turning that into something that's actually yours.

- *Share* `Prompt_Dictionary_Template.xlsx` *with each participant*

Talk through the file briefly:

- The **Instructions** tab explains the five-part framework again — role, context, task, constraints, output — and how the sheet works
- The **Prompt Dictionary** tab has five categories already started: Data Quality Checks, Formulas, Summarising, Drafting Emails/Reports, and Meeting & Teams Notes — each with one example row already filled in, shaded green, showing the expected format
- The yellow cells are where they type. As soon as they fill in Role, Context, Task, Constraints and Output, the **Full Prompt** column builds itself automatically using a formula — so this doubles as one more example of a formula doing useful work for them

### Task *(10 mins)*

- *Individually or in pairs, participants pick 2–3 tasks from their own day-to-day work — not today's examples — and complete a row for each*
- Encourage them to fill in the Value Level column too (High-Value, High-Risk, Low-Value) as a reminder of how much scrutiny that output will need

**NB If someone's stuck for a real example, ask them what the last email, spreadsheet or summary was that they personally put together this week — there's almost always a prompt hiding in that.**

### Share-back *(5 mins)*

- *Ask for 2–3 volunteers to read out one prompt each*
- As a group, stress-test it: is this actually a High-Value use of Copilot, or could it just as easily be Low-Value? Would the group trust the output unchecked, or does it need the five-point validation check first?

### Close-out *(2–3 mins)*

Two closing asks:

1. Save this file somewhere you'll actually reopen — OneDrive, Teams, wherever you already keep working notes — and keep adding to it as new tasks come up
2. Before we finish, a quick show of hands or a word each: what's one thing from this course you're going to change about how you work, and is there anything you'd still like to go deeper on — Copilot Agents, more advanced formulas, or anything else? That's genuinely useful for us to hear, and it's the last piece of evaluation for the course.

Thanks everyone — that's the series done.
