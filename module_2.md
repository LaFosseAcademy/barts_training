# Module 2 — Data Visualisation & Storytelling
### Barts Health NHS × La Fosse — Microsoft 365 Data Skills Training

**Day 1 | 11:45–13:00 | Platform: Excel Online, Power BI (overview), Microsoft Fabric (overview)**
**Two 30-minute blocks, with a 15-minute break between them**

---

## Overview

Module 2 is where data stops being a spreadsheet and starts becoming a message. The analytical work done in Module 1 — cleaning, summarising, joining — produces numbers that are correct. This module is about making those numbers useful: selecting the right visual form, stripping away the noise that obscures the point, and framing the finding in a way that prompts a decision rather than just a read.

The skills here are not primarily technical. Building a chart in Excel Online takes minutes. The harder and more valuable skill is knowing which chart to build, how to format it so the right thing stands out, and how to frame it so a clinical lead or operations director understands immediately what they are looking at and what it asks of them.

These are the skills that determine whether a report gets read and acted on, or filed and forgotten.

---

## Where Module 2 Sits in the Data Lifecycle

```
Collection → Storage → Access → Cleaning → Analysis → Visualisation → Communication → Action
```

Module 2 covers the **Visualisation** and the beginning of the **Communication** stage. It is the bridge between the analytical work of Module 1 and the stakeholder-facing outputs that drive action. The narrative framework introduced here — Context → Insight → Recommendation — carries through into Module 3 and forms the structural backbone of the end-to-end scenario in Module 4.

This is the stage where most reporting effort is either amplified or wasted. A clean dataset with strong analysis, paired with a confusing or cluttered chart and a vague title, still fails to land. Conversely, a well-chosen visual with a clear headline can communicate a finding to a senior audience in under ten seconds.

---

## Learning Goals

By the end of this module, participants will be able to:

- Select the appropriate chart type for different data types and messages
- Build and format a chart in Excel Online that prioritises clarity over decoration
- Write chart titles that communicate the finding, not just the subject
- Understand the principles of the Context → Insight → Recommendation narrative framework
- Recognise how Power BI and Microsoft Fabric outputs complement Excel-based charts in reporting workflows at Barts Health

---

## Main Areas Covered

- Principles of effective data visualisation: signal vs noise
- Choosing the right chart: bar, line, pie, scatter — and when not to use each
- Decluttering: removing gridlines, redundant legends, borders, and decorative elements
- Writing insight-led chart titles and headlines
- Introduction to Power BI and Microsoft Fabric as reporting layers within Barts Health
- The Context → Insight → Recommendation narrative framework (introduced here, practised in Day 2)

---

## Block Breakdown

---

### Block 1 — Choosing the Right Chart
**11:45–12:15**

#### What we cover

- The four most common chart types and the question each is best suited to answer:
  - **Bar chart** (vertical or horizontal): comparing values across distinct categories — which team, which month, which directorate
  - **Line chart**: showing change over time — how a metric has moved across a period, and whether a trend is improving or declining
  - **Pie chart**: showing how a whole divides into parts — but only when there are few categories and the proportional relationship is the point
  - **Scatter chart**: exploring whether two variables are related — does higher absence correlate with lower compliance scores?
- Common mistakes that reduce chart effectiveness or actively mislead:
  - Pie charts with more than four or five segments, where the proportions become impossible to compare visually
  - Dual-axis charts that imply a relationship between two unrelated metrics
  - Bar charts that do not start at zero, exaggerating differences between categories
  - Using a line chart for categorical data, implying a continuous trend where none exists
- How to diagnose which chart type fits a given scenario before opening Excel
- Hands-on: given four data scenarios drawn from Barts Health reporting contexts, participants select and justify a chart type for each before building anything

#### Why this matters

Chart type choice is not an aesthetic decision — it is an analytical one. The wrong chart type can make a meaningful pattern invisible, make a trivial difference look significant, or make a finding genuinely harder to interpret than the underlying table it was built from.

A pie chart with eight segments tells a senior stakeholder almost nothing. A bar chart comparing those same eight categories, sorted by value, tells them immediately which is largest and by how much. These are not the same communication. One prompts a question; the other prompts an answer.

The discipline of choosing a chart type before opening Excel — asking "what question am I answering, and what visual form answers it most directly?" — is the single habit that most improves the quality of data communication at every level of an organisation.

#### Where you will use this in the data lifecycle

This skill sits at the **Visualisation** stage and is relevant every time a dataset needs to be communicated to an audience. At Barts Health, that includes:

- Monthly compliance dashboards shared with directorate leads: bar charts showing completion rates by team, line charts showing trend over the past six months
- Attendance and absence reporting: line charts for trend, bar charts for comparison by department or reason code
- Finance and budget tracking: bar charts for spend by cost centre, line charts for cumulative spend against a target
- Workforce planning summaries: bar charts for headcount by grade or site, scatter charts for exploring relationships between vacancy rates and absence

The question to ask at this stage is always: what is the one thing I want my audience to understand from this visual? The chart type that most directly answers that question is the right one.

---

*— Break 12:15–12:30 —*

---

### Block 2 — Building & Decluttering Charts in Excel Online
**12:30–13:00**

#### What we cover

- Inserting a chart in Excel Online from a PivotTable or a data range, and the difference in behaviour between the two
- The default Excel chart and everything that is wrong with it: gridlines, borders, redundant legends, uninformative titles, unnecessary data labels
- A decluttering process: removing each element that does not add information, and asking "does removing this make the chart harder to read?" If no, remove it
- Formatting decisions that improve clarity:
  - Choosing a colour palette that is accessible and consistent with Barts Health communications standards
  - Using a single highlight colour to draw attention to the most important bar or data point
  - Adjusting axis labels so they are readable without rotating the chart
  - Removing the chart border and background fill so it integrates cleanly into a slide or report
- Writing chart titles that communicate the finding:
  - Descriptive title (weak): "Mandatory Training Completion by Directorate"
  - Insight-led title (strong): "Three Directorates Below 80% Completion as of October"
  - The insight-led title tells the reader what they need to know before they look at the bars; the descriptive title makes them do the interpretive work themselves
- Brief introduction to Power BI and Microsoft Fabric: what these tools are, how they are used at Barts Health for trust-wide reporting, and how their outputs — dashboards, exported charts — can be referenced or embedded in PowerPoint presentations built in Excel Online
- Hands-on: build and fully format two charts from the Module 1 dataset, applying the decluttering process and writing an insight-led title for each

#### Why this matters

A chart that is built in five minutes and never formatted communicates one thing to a senior audience: that the person who built it did not think carefully about what they were trying to say. That is not a small thing in a healthcare organisation where senior time is limited and reporting credibility matters.

Decluttering is not about making charts look minimalist for aesthetic reasons. It is about removing everything that competes with the signal — every gridline, border, and redundant label that the reader's eye has to move past before it reaches the data. The fewer things there are to look at, the faster and more accurately the finding lands.

The shift from descriptive to insight-led titles is perhaps the single highest-leverage change most people can make to their reporting outputs. It requires no technical skill — only the discipline of asking "what does this chart show?" and writing that as the title, rather than writing a description of the axes.

#### Where you will use this in the data lifecycle

Chart building and formatting sits at the **Visualisation** stage, immediately before the **Communication** stage where the output is shared. In a Barts Health context:

- Any chart included in a monthly report to a clinical director, operations manager, or executive team needs to meet the bar of being immediately interpretable, without the recipient needing to ask what it means
- Charts inserted into PowerPoint slides for board-level reporting need to be formatted consistently and at a quality that reflects the organisation's standards
- Charts embedded in shared SharePoint reports that multiple teams will access should be formatted so that someone encountering them for the first time can understand the finding without context
- When working alongside Power BI dashboards, Excel-built charts should maintain visual consistency in colour and style so that outputs from different tools do not look like they come from different organisations

The narrative framework — Context → Insight → Recommendation — is introduced in the Day 2 recap and practised through Modules 3 and 4. The foundation for it is built here: a chart with an insight-led title is already doing the first part of the work of telling the data story.

---

## Module Conclusion

By the end of Module 2, participants can select a chart type that fits their data and their message, build and format it to a professional standard in Excel Online, and write a title that communicates the finding directly. They have also been introduced to Power BI and Fabric as tools that exist within the Barts Health reporting landscape, giving context for the trust-wide reporting infrastructure their work sits within.

The key principles from this module are:

- **Choose before you build.** Decide what question the chart answers before opening Excel, and let that determine the chart type.
- **Remove before you add.** The default Excel chart needs things taken away, not added. Start by removing everything that does not carry information.
- **The title is the message.** An insight-led title does the interpretive work for the reader. A descriptive title leaves that work to them. Senior audiences do not have time for the latter.
- **Consistency builds credibility.** Formatting choices — colour, label style, axis treatment — should be consistent across all charts in a report. Inconsistency signals that outputs have not been reviewed.

The Context → Insight → Recommendation narrative framework, introduced in the Day 2 recap, gives these individual chart skills a structure to sit within — the framework for turning a well-built chart into a complete, actionable data story.

---

*Module 2 is part of the Barts Health NHS × La Fosse Microsoft 365 Data Skills Training Programme. All datasets used in training are anonymised. Delivered using Excel Online, with reference to Power BI and Microsoft Fabric (Microsoft 365).*
