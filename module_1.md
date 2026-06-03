# Module 1 — Data Access, Cleaning & Analysis
### Barts Health NHS × La Fosse — Microsoft 365 Data Skills Training

**Day 1 | 09:00–11:45 | Platform: Excel Online**
**Five 30-minute blocks, with a 15-minute break after Block 3**

---

## Overview

Module 1 lays the foundation for everything that follows in the programme. Before any chart can be built, any insight communicated, or any Copilot prompt written, the data it is based on must be trustworthy. This module is about developing the discipline and practical skills to get from raw, imperfect data — as it actually arrives across NHS systems — to a clean, structured, analysis-ready file.

The skills covered here are not advanced. They are the fundamentals that, when applied consistently, prevent the most common and costly errors in data reporting: wrong totals, missed records, misleading summaries, and conclusions drawn from data that was never checked.

---

## Where Module 1 Sits in the Data Lifecycle

A data lifecycle describes the journey data takes from its origin through to action. In a healthcare administrative context, that journey typically looks like this:

```
Collection → Storage → Access → Cleaning → Analysis → Visualisation → Communication → Action
```

Module 1 covers the **Access → Cleaning → Analysis** stages — the middle of the lifecycle, and the most labour-intensive part for most administrative staff. This is where data moves from being a raw export or shared file into something that can actually be used to answer a question or support a decision.

Getting this stage right is what makes the later stages — visualisation, storytelling, and AI-assisted drafting — reliable. Skip it or rush it, and every downstream output is built on uncertain ground.

---

## Learning Goals

By the end of this module, participants will be able to:

- Access and import data from multiple sources into Excel Online
- Identify and resolve the most common data quality issues: duplicates, blanks, and formatting inconsistencies
- Apply core formulas to interrogate and summarise a dataset
- Understand the structural difference between VLOOKUP and XLOOKUP, and choose the right one for the task
- Build a simple PivotTable to summarise data by category
- Structure a cleaned dataset that is ready to be handed to a visualisation or reporting workflow

---

## Main Areas Covered

- Navigating Excel Online and connecting to data sources (SharePoint, OneDrive, exported CSVs)
- Data cleaning: removing duplicates, fixing formatting, handling blank cells
- Core formulas: SUM, AVERAGE, COUNT, COUNTIF, SUMIF, IF, IFERROR
- VLOOKUP vs XLOOKUP — differences, limitations, and practical application
- Structured tables and named ranges
- Filters, sorting, and PivotTables for summarising data

---

## Block Breakdown

---

### Block 1 — Getting Data into Excel Online
**09:00–09:30**

#### What we cover

- How data flows within Barts Health: the typical journey from source systems (e.g. ESR, Allocate, local trackers) through to SharePoint, OneDrive, and email attachments
- Opening files in Excel Online directly from SharePoint and OneDrive, versus uploading a local file
- Understanding file types: .xlsx, .csv, and what to watch for when opening each
- First-look audit: what to check when you open an unfamiliar dataset before doing anything else
- Hands-on: open a provided anonymised Barts Health dataset, scan it, and note at least five data quality issues

#### Why this matters

Most data problems start before anyone has written a formula. Data arrives from multiple systems, often exported by different teams in different formats, and it lands in Excel looking nothing like a clean spreadsheet. Rows are missing. Column headers have spaces or inconsistent capitalisation. Numbers have been stored as text. Dates are formatted differently in different rows.

If you open a file and go straight to building a formula or a chart, you are working on an assumption that the data is reliable. That assumption is almost always wrong. The discipline of doing a first-look audit — scanning the data before touching it — is one of the highest-value habits a data-literate professional can develop.

#### Where you will use this in the data lifecycle

This skill sits at the **Access** stage. It is relevant every time you receive a new dataset, whether that is a monthly attendance export, a staffing roster, a finance report, or a compliance tracker. The moment you open a file is the moment to assess its quality — not after you have already built a summary table on top of it.

In practice at Barts Health, this applies to: induction compliance reports pulled from the LMS, staffing data exported from Allocate, appointment or referral data from clinical systems, and any shared tracker on SharePoint that multiple people have edited.

---

### Block 2 — Cleaning & Structuring Data
**09:30–10:00**

#### What we cover

- Removing duplicates using Excel Online's built-in tool, and understanding when a duplicate is a genuine error versus an expected repeat
- Finding and handling blank cells: filling with a value, flagging with a formula, or removing the row depending on context
- Fixing formatting inconsistencies: converting text-stored numbers to actual numbers, standardising date formats, correcting inconsistent text entries (e.g. "Full Time" vs "full time" vs "FT")
- Trimming whitespace using the TRIM function to catch invisible formatting issues
- Converting a data range to a structured Excel Table and understanding why this makes everything downstream more reliable
- Hands-on: apply a cleaning checklist to the dataset from Block 1

#### Why this matters

Dirty data produces wrong answers. A COUNTIF formula counting "Full Time" will miss every row that says "full time" or has a trailing space. A SUM formula on a column of numbers will silently ignore any cell where the number is stored as text and return an incorrect total — with no error message, no warning, just a wrong number that looks right.

These are not edge cases. They are the normal state of data that has been entered by multiple people across multiple systems over time. Cleaning is not a preliminary chore to get out of the way — it is the analytical work. It is where you develop an understanding of what the data actually contains, where the gaps are, and what caveats will need to be attached to any conclusions drawn from it.

Structuring data as a formal Excel Table rather than a loose range is equally important. Tables give columns named headers that formulas can reference, they expand automatically when new rows are added, and they make PivotTables and filters more stable and predictable.

#### Where you will use this in the data lifecycle

This is the **Cleaning** stage, and it applies to every dataset before any analysis begins. In a Barts Health context, this is particularly relevant for:

- Compliance trackers that have been edited by multiple ward managers or department leads, resulting in inconsistent entries
- Exported reports from HR or payroll systems where numeric fields are pulled through as text
- Attendance logs where dates have been entered in different formats by different administrators
- Any dataset that has been maintained in a shared Excel file over a period of months, where formatting standards have drifted

A useful rule of thumb: if you did not create the dataset yourself, assume it needs cleaning before you do anything else with it.

---

### Block 3 — Core Formulas for Analysis
**10:00–10:30**

#### What we cover

- **SUM** and **AVERAGE**: calculating totals and means across a column or range, including within a Table structure
- **COUNT** and **COUNTA**: counting numeric entries versus counting any non-empty cell, and why the distinction matters
- **COUNTIF** and **COUNTIFS**: counting rows that meet one or more conditions (e.g. count all staff in a given department who have not completed mandatory training)
- **SUMIF** and **SUMIFS**: summing values based on one or more conditions (e.g. total hours worked by a specific team in a given month)
- **IF**: returning different values based on a logical test, and building simple nested IF logic for categorisation
- **IFERROR**: wrapping a formula to return a clean, readable result when the formula would otherwise produce an error
- Hands-on: build a summary section on the cleaned dataset using at least four of the above formulas

#### Why this matters

Formulas are how you turn a list of records into answers to questions. A spreadsheet full of rows tells you nothing on its own — formulas are what allow you to ask: how many? how much? which category? what proportion? is this above or below a threshold?

COUNTIF and SUMIF in particular are the workhorses of administrative reporting. They allow you to slice a dataset by a condition without restructuring the data, without filtering, and without manual counting. Once you understand their logic, you can answer the most common reporting questions — compliance rates, attendance by team, spend by cost centre — in a single formula.

IFERROR deserves specific attention because it addresses a real problem in shared reports: a formula error displayed to a senior stakeholder looks like carelessness, even if the underlying data is the cause. Wrapping formulas in IFERROR is a small habit that significantly improves the credibility of a report.

#### Where you will use this in the data lifecycle

These formulas sit at the **Analysis** stage. They are the tools you reach for when you need to summarise, count, or interrogate a cleaned dataset. In practice at Barts Health:

- COUNTIF and COUNTIFS: compliance reporting (how many staff have completed induction? how many have not, broken down by directorate?)
- SUMIF and SUMIFS: financial reporting (total spend by department, total hours by grade)
- IF: categorisation (flag records as compliant/non-compliant, above/below target, due/overdue)
- IFERROR: any formula-based summary table that will be shared with a manager or stakeholder

These formulas are also the foundation for everything Copilot will help generate in Module 3 — understanding what a formula does makes it far easier to validate whether what Copilot has written is correct.

---

*— Break 10:30–10:45 —*

---

### Block 4 — VLOOKUP vs XLOOKUP
**10:45–11:15**

#### What we cover

- What a lookup formula is and what problem it solves: joining information from one table to another based on a matching value
- **VLOOKUP**: syntax (`=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])`), how it works, and its key limitations:
  - Can only look to the right — the lookup column must be the leftmost column in the range
  - References columns by number, which breaks silently if columns are inserted or reordered
  - Returns only the first match, with no easy handling of multiple matches
  - Does not handle missing values gracefully without additional IFERROR wrapping
- **XLOOKUP**: syntax (`=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])`), and why it is the modern replacement:
  - Can look in any direction — left, right, or across rows
  - References arrays directly rather than column numbers, so it does not break when the spreadsheet structure changes
  - Has a built-in `if_not_found` argument, removing the need for a separate IFERROR
  - Supports exact match, approximate match, and wildcard matching natively
- Side-by-side demonstration using the same dataset: both formulas solving the same problem, and why XLOOKUP's approach is more robust
- When you might still encounter VLOOKUP: older shared files, templates built by others, and how to read and adapt them
- Hands-on: write an XLOOKUP to pull a value from a reference table into the main dataset, then compare with the VLOOKUP equivalent

#### Why this matters

Lookup formulas are the most commonly used — and most commonly broken — formulas in shared Excel files across any organisation. VLOOKUP has been the default for two decades, and it works until the spreadsheet structure changes. Then it fails silently: no error, just the wrong value returned, because a column was inserted and the column index number now points to a different field.

XLOOKUP solves this. It was introduced in 2019 and is fully available in Excel Online. Understanding the difference is not a technical nicety — it is the difference between a formula that survives being handed to a colleague and one that quietly breaks as soon as the file is edited.

The broader skill being developed here is understanding how data from separate tables is joined together. This is a concept that underpins everything from simple reporting lookups to the way Power BI and other tools combine data sources. Learning it in Excel Online builds the mental model that makes those tools far easier to understand later.

#### Where you will use this in the data lifecycle

Lookups sit at the **Analysis** stage, specifically when combining data from more than one source — which is almost always the case in real reporting work. At Barts Health, typical use cases include:

- Pulling staff names or job titles from an HR reference table into an attendance or compliance tracker, based on a staff ID
- Matching cost centre codes in a spend report to a reference list of directorate names
- Combining data from two separately exported reports — for example, joining a training completion export to a staffing list to calculate compliance rates by team
- Any scenario where data lives in more than one place and needs to be brought together for analysis

XLOOKUP is also relevant when reviewing or inheriting shared files that use VLOOKUP — knowing how to read, adapt, and upgrade those formulas is a practical skill for anyone working with legacy reporting templates.

---

### Block 5 — PivotTables & Summary Structures
**11:15–11:45**

#### What we cover

- What a PivotTable is and what it does: summarising a large dataset dynamically without changing the underlying data
- Building a PivotTable from a structured Excel Table: inserting, choosing row and column fields, selecting values and aggregation type (sum, count, average)
- Grouping data by category, time period, or other field
- Applying filters within a PivotTable to focus on a subset of the data
- Refreshing a PivotTable when the underlying data is updated
- When to use a PivotTable versus a formula-based summary: the trade-offs of flexibility versus portability
- Hands-on: build a PivotTable from the cleaned dataset that summarises a key metric by at least two dimensions (e.g. compliance status by department and grade)

#### Why this matters

PivotTables are one of the most powerful tools available to anyone working with tabular data, and one of the most underused. The reason most people avoid them is that they look complex and feel unfamiliar. In practice, once you understand the logic — rows, columns, values, filters — they become the fastest way to answer a question like "how does this break down by team?" or "what does this look like by month?"

The alternative to a PivotTable is a manual summary table built with COUNTIF and SUMIF formulas, which works well for a fixed structure but becomes unwieldy when you want to slice the data in a different way. PivotTables let you change the breakdown instantly, without rewriting formulas. For exploratory analysis — where you are not yet sure which view of the data is most useful — this flexibility is invaluable.

Understanding when to use each approach is equally important. PivotTables are ideal for exploration and for reports where the data will be refreshed regularly. Formula-based summaries are better when you need a fixed, portable structure that others can read and audit without pivoting experience.

#### Where you will use this in the data lifecycle

PivotTables sit at the boundary between the **Analysis** and **Visualisation** stages. They are the tool you use to find the summary that is worth communicating — before committing to a chart or a slide. In a Barts Health context:

- Summarising induction compliance rates by directorate, grade, and completion status from a raw completion export
- Breaking down staff absence data by team, absence reason, and time period to identify patterns
- Aggregating course attendance records to report total completions per month across multiple programmes
- Building a draft summary that a clinical director or operations manager can interrogate before it is turned into a presentation

PivotTables also form the basis for charts in Module 2 — inserting a chart directly from a PivotTable creates a dynamic visual that updates automatically when the pivot is refreshed, making it far more maintainable than a chart built from a manually typed table.

---

## Module Conclusion

By the end of Module 1, participants have completed the full **Access → Cleaning → Analysis** journey with a real dataset. They have a working, structured Excel file containing cleaned data, formula-based summaries, and a PivotTable — all built in Excel Online, all ready to be turned into a visual in Module 2.

The key habits instilled in this module are:

- **Audit before you act.** Always do a first-look review of any dataset before building anything on top of it.
- **Clean first, analyse second.** The quality of any analysis is bounded by the quality of the data it is based on.
- **Use XLOOKUP, not VLOOKUP.** For any new formula in Excel Online, XLOOKUP is more robust, more readable, and less likely to break.
- **Structure your data as a Table.** This small step makes every formula, filter, PivotTable, and chart more reliable and easier to maintain.
- **Know your tools.** Formulas and PivotTables each have their strengths. Using the right one for the task produces cleaner, more maintainable work.

These are not Module 1 habits. They are career habits — the foundation of working with data confidently and credibly at any level of an organisation.

---

*Module 1 is part of the Barts Health NHS × La Fosse Microsoft 365 Data Skills Training Programme. All datasets used in training are anonymised. Delivered using Excel Online (Microsoft 365).*
