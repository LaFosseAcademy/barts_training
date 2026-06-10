# Module 1 — Data Access, Cleaning & Analysis
### Barts Health NHS × La Fosse — Microsoft 365 Data Skills Training

**Day 1 | 09:00–11:45 | Platform: Excel Online**
**Five 30-minute blocks, with a 15-minute break after Block 3**

---

## Pre-Session Setup

- Load Slidee: barts_module_1


## Training

- `Slide 1`

### Personal Intro

Good morning everyone, good to be with you all today. 

My name's Emile and I'm a Senior Trainer for LaFosse. My role at LaFosse is as a technical trainer, whether that's building websites, deploying software onto servers in the cloud or exploring databases and the data they contain. 

Susana and Simon from my team have been working on a plan for some bespoke training for you which we've put together which will revovle around the data lifecycle. 

From when an email lands in your inbox with an attatchment about attendance record, to understanding that data and getting the relevant insights out of it. 

### Training Overview

- `Slide 2`

You may already be familiar with the training and how it'll be structured but in case you're not. 

We'll be spending 2 mornings together. 

On the slide, you'll see the group we're in and also the corresponding second session. 

Additionally the 4 modules we'll be looking at, each one building on what we cover in the previous training. 

- `Slide 3`

So:
- Module 1
  - This is laying the foundation for everything that follows. Before any chart can be built or insight communicated, before we take a look at automating some of the processes with AI we need to make sure the data is trustworthy. 
  - This module is going to focus on the practical skills to get raw information or imperfect data as it may arrive across different systems into a clean and structured file. 

- Module 2
  - Module 2 is designed to convert that spreadsheet into something more meaningful. We'll discuss selecting the right visual form for the message we're trying to communicate and then stripping away any noise which obscures that message. This is what we'll cover over the course of this morning, then we'll pick up again for Module 3 and 4.

- Module 3 & 4
  - I wont delve too deeply into those modules right now but they can be summarised by taking the learnings we hopefully achieve this morning and then making that process more efficient using CoPilot. We'll then conclude with a little example which takes us all the way through the process. 

### How to follow the training

It's my recommendation that during the training you ask questions as we go along. You can make notes if you wish but I've developed a cheatsheet for each module we go through which summarises the main takeaways. 

I'll distribute those at the end of the training. 

We'll also be recording the training so you'll have access to revisit this session at a later date if there's anything specific you want to recap.

### The Training

Ok, let's get into it then! 

#### The Data Lifecycle

When we discuss data, often we're inadvetently referring to the Data Lifecycle.

- `Slide 4`

I hope you can see but it describes the journey data takes from it's origin through to action. 

We start with:
- Collection
  - Where we gather raw data from different source systems
- Storage
  - Where that data exists, which could be SharePoint, OneDrive or downloaded directly onto your computers
- Access
  - Essentially opening the data or spreadsheet
  - This is the phase where we'll be starting our training today
- Cleaning
  - Fixing errors, blanks and any formatting requirements 
- Analysis
  - Actually defining different functions in Excel and creating LookUps or Pivot Tables
- Visualisation
  - Relatively straight forward but creating charts or illustrations about our data
  - This is hopefully the endpoint of where we'll get to today
- Communication
  - Creating slides, reports... essentially distribtuing the insights more widely
- Action
  - Then what do we actually do with that insights we have

Those last two parts we'll tackle more comprehensively in Modules 3 and 4. 


## Block 1 - Getting Data into Excel Online

So before we get started we need some data. 

You should have been invited to a SharePoint, I'll share the link on Teams as well just incase the invite has got lost. 

- *LINK*: https://lafosseassociatesltd.sharepoint.com/sites/BartsHealthxLaFosse

If you click into *Documents* on the left hand side you'll see a series of mock spreadsheets we'll be working from. 

The whole point of SharePoint is to share files, conversations across a team which is fine but for the purpose of the training what I've done is created some folders for the different groups we'll have recieving this training. 

Can I ask you all to:

1. click into *<insert hopistal currently located>* and then in the top right hand side, you'll see a green *Create or upload* button. 

2. Could create a folder and name that folder your first and last name. 

So for me, I'll go into *Trainers* and just create a folder called *Emile Sherrott*

### The problem 

Most of the problems we have with data start before we've even opened a file. Data arrives from multiple different systems and exported to a place like SharePoint in multiple formats from different teams.

In the mock data I think we have a good example of this. In SharePoint you'll notice two files. 

- 0923 BSc Student allocations (LSBU-Barts Health)
- student allocations

Before we open these up and potentially edit them, can I ask you to select both of these files from the Documents window. 

Then on the toolbar at the top click on Copy To, once you've done that just navigate to where you created the folder with your name and copy to that location. 

Again this isn't something that we'd normally need to do but I'm just making sure we're not all potentially editing the same file directly. 

### Accessing Data

So once you've done that, just navigate in SharePoint to your named folder and let's open up both the two files we copied over. 

The first file: 0923 BSc Student allocations (LSBU-Barts Health)

You likely to be better equipped in reading this spreadsheet better than myself but it looks like a student placement allocation spreadsheet to allocate London South Bank University students into clinical placements. 

Based on the worksheet title:
- **0923 BSc** likely a student cohort who started September 2023
- **PL7** a placement number
- **5 Jan- 22 Feb 26** - a placement period

Then some information about how long they'd be expected to spend on their placements. 

The column headings I hope are fairly self explanitory

- **Trust**
- **First name**
- **Surname**
- **Student email**
- **Placement Dates**
- Under **5 Jan- 22Feb 26** looks like the Allocated ward/department
- **LL** I believe to be the Link Lecturer 

I appreciate it may sound very obvious but having an initial understanding of the data, what it contains is always the first thing we need to do. 

Without that insight we can't start to identify any issues with the health of the data and then try to resolve them before we go any further.

- `Slide 4`

If we think back to the data life cycle, this is the **Access** stage. When we open a file we understand it and assess it's quality.

## Block 2 - Cleaning & Structuring Data

If we go back to the spreadsheet we can see there's a few anomalies with the data. 

- On row 21: We're missing data about the **Trust**, **Placement Dates** then the **Allocated ward and department** info.

- Between rows 36 and 39 we're missing data on the **Allocated ward and department**

- Row 40 we're missing trust information with a few other things

- Then generally throughout the spreadsheet it looks like there's varying ways information has been inputted. 
  - row 10 the trust is Barts-contin
  - row 11 it's Barts-ext degree
  - 12 it's just BSc
  - 20 it's *from 0922* with a lower case *f*
  - rows 30 & 31 it's *From 0922* with an upper case *F*
  - row 35 the trust name is *Other*
 
 You'll have an understanding about the insights you want to collect from these types of reports but we can easily indentify that if we wanted to understand how many students were doing their placements in the Community. 

 We've got the 4 between rows 36 and 39. We could guess Kendall Martinez on row 35 is part of the community placement or that Quinn Gonzalez is as well but they would just be assumptions.

 With 35 students, 4 of which don't have the data regarding their placement location, that represents just over 11% of the entries. 

 ### Cleaning Data

 #### White Space

 Generally speaking when we clean data the first thing we do is observe the issues with the data and where they are, which we have done.

 - There's multiple casings
 - Missing values
 - Hard to interprete values

If there's any user input, maybe someone arrives at the training center at checks in one an iPad or a similar device they may accidentally input their name with a leading or trailing whitespace. 

If I'm writing a simple query to see how many students are in a community placement I can write a simple function in an empty cell. 

- *Click into cell K42 and type*: "Number of students in community"
- *Click into cell L42 and type*

```xlsx
=COUNTIF(L36:L39,"Community")
```

So `COUNTIF` is the function and we have two arguments which are seperated by a comma. 

1. The range of cells we're assessing
2. The condition we're checking

As we can see we get back 4. 

If I introduce a trailing white space to one of the cells with "Community", then we get 3 instead.

- *Add a trailing space into a cell with "Community"*
- *Show change*

So if there's any pieces of data which are typed in manually by a human it's always good to trim any leading or trailing white space. 

There's a few ways to clean it, eventually we'll get CoPilot AI to do this for us but I'll write a new function.

- *Click into cell S6*

```xlsx
=TRIM(CLEAN(L6))
```

This is just nesting two functions together.

1. First, we clean the cell which removes any hidden formatting codes
2. Then we TRIM which removes any leading or trailing whitespace

All I'll do next is drag down or "Auto Fill" for every entry in this column.

That's are cleaned data. 

If I highlight all of it and then copy it, I can do to the original column *L6* and do a "Paste Special" which essentially let's me choose if I want to paste the formulas, values or the styling with formatting. 

I'll choose "Values Only" and it'll overwrite our original values with the clean ones. 

Then we'll just delete the data we created in column S.

Hopefully we can see our **countif** function is now correctly showing 4. 

#### Standardise Casing

We noticed in our **Trust** column that the casing wasn't accurate on Row 20 and then Row 30 and 31. 

Now that we've removed any problematic white space, generally this is what we'd do next. 

It's a very similar process. 

- *In cell S6 write:*

```xlsx
=PROPER(A6)
```

- *Then Auto Fill*

I'll copy the values and do another Special Paste into the original row. Then we can delete *column S* again. 

As well as the *PROPER* function which will capitalise the first character of each new letter we can also use:
- *LOWER()* which is useful for emails
- *UPPER()* which you may use with PostCodes

Most functions in excel actually aren't case sensetive but for data presentation and professionalism, it's not a step to miss out. 


#### Standardised Values

Another thing I noticed was in the trust section we had values like: `0923 BSc Barts-Contin` on row 10. 

If there was an insight and the organisation just considered anything beginning with `0923 BSc Barts` to be the same cohort, it'd be difficult to extract this information from the data as it stands. 

- *Write in cell S6*:

```xlsx
=IF()
```

If is another built in function which returns a boolean value, essentially either **True or False** based on a condition

So if I add:

```xlsx
=IF(COUNTIF(A6,"0923 BSc*"))
```

This basically checks if the value in the cell A6 starts with "0923 BSc" regardless of what follows. 

We can see in the little pop up it's telling me the arguments the function needs, with our condition, we can provide a value to add if the condition is True or False. 

In my use case I essentially want a new column of the students original cohort, regardless of if it's a **continued placement** or they've perhaps **extended their degree**

The second argument is just going to be text wrapped in double quotes.

```xlsx
=IF(COUNTIF(A6,"0923 BSc*"),"0923 BSc Barts")
```

Then if the condition returns False, I want to leave it as the original value. 

```xlsx
=IF(COUNTIF(A6,"0923 BSc*"),"0923 BSc Barts",A6)
```

- *Then auto fill the other rows*

If we wanted to we could use Column S as our base data for a new column to replace the "From 0922" Values but I'll leave this for now. 

I'm not going to overwrite the original data, in a couple of weeks if someone asks, *"how many students have extended their degree"*, we want to be able to answer them. 

So I'm going to leave this as a new column which will persist. 

- *In cell S5 type:* "Original cohort"

#### Fill or Infer missing values

That'll be our clean data for the time being. As we saw it's quite manual, this is fine, we'll be using CoPilot this time next session to achieve those results which better efficiency. 

What's more important is the process of getting to a stage where we can extract information with confidence that a trailing white space for instance won't cause errors. 

The last thing I want to talk about is the missing entries. Unfortunately, there's not a silver bullet to address these but generally we have three options:

1. **Populate missing values**
  - This is seeing if there's another trusted source of data and adding in that information. 

  - **Quinn Martin** from row 32 we can see is missing quite a few pieces of information:
    - Trust
    - Placement Dates
    - Where their placement is

  - If I open our second spreadsheet *student allocations*, on row 31, it looks like Quinn is based in A&E at the Royal London Hospital, so I can lift that information and add it to be first spreadsheet.

  - *In `0923 BSc Student allocatons (LSBU-Barts Health)` in cell L32 add:* `A&E RLH`

  We want go through all of these due to time restrictions but if you're not guessing, this is fine. 

2. The second way we can fill in values to to **Derive them**
  - This is essentially using logic to fill in missing data.
  - In cell K32, we can see Quinn is missing this data as well.
  - As I said you'll know these spreadsheets better than myself but it looks like all the Placement dates are the same, so what I'll do is make the assumption and lift the date from other values in the spreadsheet.

  - *Copy `5 Jan-22 Feb '26` from another cell into K32*

3. Our final option with missing data is **Leave it blank**

  - I can't from the data I have access to, reasonbly infer the original cohort Quinn was on. 
  - An absence of data is better than incorrect data.
  - Generally speaking at this point you can flag for a review if it's important to fill out those values. 

So: Populate when you know, derive when there's an agreed approach to derive, leave blank if you have neither. 

#### Remove duplicates

After this we could remove duplicates if they existed but following that our data would be ready to be assess. 


## Block 3 - Core Formulas for Analysis

So now that we've got clean data I want to take a look through a few more formulas. 

We've seen so far the **COUNTIF** and **IF** functions and I don't want to pause on this topic for too long. 

The main reason being is because I wouldn't expect anyone to know to different arguments and values off the top of their head. Generally, and this is a good use for AI and Google, if there's something you want to do, give it a Google and see if there's a function which can achieve it. This is probably more time efficient than you remembering all of these.

More generally though, formulas are how we turn a series of records into insights. A spreadsheet full of rows doesn't really tell us anything on its own. 

With formulas we can ask:
- how many?
- how much?
- which category?
- what proportion?

`COUNTIF` and `SUMIF` in particular are the workhoreses of administrative reporting. 

We've seen that they allow us to slice a dataset by a condition without restructuring the data, without filtering and without manual counting. 

If you haven't seen this already, you can answer the most common reporting questions with a single formula. 

Another forumla which is probably remembering is `IFERROR`, the main reason is because if a formula displays an error, often to a senior stakeholder, that reads as carelessness, even if the underlying issue is the data that was shared with you by that stakeholder. 

We can wrap formulas in a `IFERROR`, which is a small habit but improves the credibility of a report significantly. 

To show case these I want to use a new spreadsheet: `L&D learner tracker FG`, if we can go through the same process of copying it into our personal folder. 

- *Copy file into trainer folder*

I recommend that before we start defining any formulas we create a new sheet at the bottom. 

A generic name could be **Dashboard** and what we're doing is having a seperation of concerns. 

- Raw data in a file
- Dashboard or analysis in another

Generally just keeps our files a little more organised. 

There's no right name but anything which is descriptive of what it is. 

Before I demo a few formulas I'll want to know what insights I'm interested in. 

- I want to know how many students there are
- How many have: 'passed', 'failed' are in 'progress', or 'not completed'

So I'll add this header information to my Dashboard. 

- *In dashboard sheet*
  - *In A1 add*: Number of learners
  - *In A2 add*: Pass
  - *In A3 add*: Fail
  - *In A4 add*: In progress
  - *In A5 add*: Not completed

For the number of students, we want to target, or count the number of non-empty cells in the name column of the 'Learner tracker' sheet. 

That's fine, we can use the `COUNTA` formula. We pass in one argument, the range of information we want to count and it'll tell you how many values are present, ignoring empty cells. 

The only thing I'll need to specify ontop of this is a reference to the sheet.

- *In B1 add*: `=COUNTA('Learner tracker'!B5:B210)`

Because 'Learner tracker' has a space in the middle I'll wrap it within single quotes. 

I'll use a `CONTIF` for the other segments. 

- *In B2 add*: `=COUNTIF('Learner tracker'!L:L,A2)`

I could, instead of adding in A2, typed "Pass" inside double quotes, with a lot of these interlinking formulas, it's a trade of between what's readable for the person writing the formula and what's easy. 

I'd always preference readability and maintainability though. 

This does allow me to 'fill down' against our other outcomes. 

- *Auto fill down*

Another set of information we may be interested in is the number of students based at each site and the passrate. 

I'll repeat a similar process, giving a section header to give the data meaning

- *In cell A8 add*: 'Site'
  - *In cell A9 add*: 'RLH'
  - *In cell A10 add*: 'NUH'
  - *In cell A11 add*: 'WXH'
  - *In cell A12 add*: 'SBH'
  - *In cell A13 add*: 'MEH'
  - *In cell A14 add*: 'CW'
  - *In cell A15 add*: 'GSS'

Then to find the number of students, our workhorse of analysis, `COUNTIF`

- *In cell B8 add*: 'Number of students'
- *In cell B9 add*: `=COUNTIF('Learner tracker'!G:G,A9)`

Then I'll 'fill down' the other sites as well. 

A good thing to do at this point would be to check our work. I've manually gone through and looked for different sites.

- *In cell A16 add*: 'Total'
- *In cell B16 add*: `=SUM(B9:B15)`

Now we can do some more interesting analysis. 

- *In cell C8 add*: 'Pass'

We're not just counting one thing now but many, so I'll use the `COUNTIFS` formula which let's us pass in a set of conditions. 

- *In cell C9 add*: `=COUNTIFS('Learner tracker'!G:G,A9,'Learner tracker'!L:L,"Pass")`

So we have 2 conditions, that for each row in coloumn G in the Learner tracker sheet has the value 'RLH' and also in row L has the value "Pass"

- *auto fill down remaining values*

Finally for this section, just the ability to find the percentage of those passed based on site. 

- *In cell D8 add*: '% Passed'
- *In cell D9 add*: `=C9/B9`

- *auto fill down remaining values*

Now I'll just format this as a percentage

<img src="../trainer_images/1.png">

We've got lots of formatting options.
- I'll choose **Number**
- Then **percentage**

This type of calculation could cause an error. Hypothetically if we had oversight of a new hospital and initially had 0 students there, any number divided by 0 would cause an error. 

Let me demo this quickly.

- *On row 15 create a row underneath*
  - *Add to new A16*: 'New Hosptial*
  - *Auto fill down cell B16, C16, D16*

We've correctly found that there's currently no students at 'New Hosptial' and therefore there's differently no students who've passed. That's fine, the 'Learner tracker' will be updated in due course but the problem is we've not got an error.

What we ought to do is wrap our formulas with the `IFERROR`

- *In cell D9, add*: `=IFERROR(C9/B9,"No students attending: "&A9)`

What we're saying is, if the first argument produces an error, instead of displaying that error, pass the second argument instead. 

I've combined some text and the cell value just with an ampersand. 

- *Auto fill down*


## Break

Let's take a little break now, let's come back in 15 minutes and we'll look at combining data from several files. 

## Block 4 - VLOOKUP vs XLOOKUP

Let's turn our attention to **Look Ups**, you'll most likely have heard about these in relation to a **VLOOKUP** and an **XLOOKUP**. 

Generally, a look up is a process that searches for a specific piece of information in one part of your data and pulls back a corresponding value for the same row or column.

"Find this value in one place, and bring back related information from somewhere else". 

So in our spreadsheets, as we saw at the very beginning we have data relating to students inside the files:

- 0923 BSc Student allocations (LSBU-Barts Health)
- student allocations

When you data which can potentially all fit together but it does span several folders, think **LOOKUP**. 

If you don't already, let's reopen those two files from our personal folders. 

### Difference between VLOOK and XLOOKUP

You may have used **VLOOKUPs** before, they work but they're a bit more limited in regards to what they can do:

If I refer to them as **'breaking silently'**, what I mean by that is they don't handle changes to a spreadsheet really well. If we change things around, reorder a column or have duplicates of data they can return incorrect values without giving an error.

In these situations an error is probably favourable because at least you know something's gone wrong, rather than having incorrect information. 

  - Can only look to the right — the lookup column must be the leftmost column in the range
  - References columns by number, which breaks silently if columns are inserted or reordered
  - Returns only the first match, with no easy handling of multiple matches
  - Does not handle missing values gracefully without additional IFERROR wrapping


**XLOOKUPS** on the other hand:
  - Can look in any direction — left, right, or across rows
  - References arrays directly rather than column numbers, so it does not break when the spreadsheet structure changes
  - Has a built-in `if_not_found` argument, removing the need for a separate IFERROR

What this basically means is that they're far more dynamic and don't break as quickly. 

Let's actually create one. 

So in `0923 BSc Student allocations (LSBU-Barts Health)` we have placement details from early January until late February.

Then in `student allocations` we have similar data between early May and early June. 

What I want to do is basically see their placement progression, from one area to another and track their progress. 

In `student allocations` I'm going to create a new sheet called **tracker**

- *Create new sheet called 'tracker'*
    - *Intentionally omit the final closing parenthesies*

- *In cell A1 type*: `=XLOOKUP(`

We can see the syntax is the first argument is the **lookup_value**

This ought to be a unique value based on the dataset. In our data an **email** would be a good value as two students may share the same name or location.

I'm going to go into `student allocations -> Sheet1` and just copy the student email addresses. 

- *Copy student email address into new 'tracker' sheet, starting from A2*
- *Add to cell A1*: 'Student Emails'

Let's define a **LOOKUP** again, we know how to reference data in a seperate sheet so I'll add that. 

- *In cell B2 add*: `=XLOOKUP(A2,)`

This is what we're using to search for in seperate spreadsheets or files. 

The next argument to the formula is the **lookup_array**. This is asking, where shall I look for to find this email value you passed in as the **lookup_value**. 

- *In cell B2 add*: `=XLOOKUP(A2,Sheet1!E:E,)`

Then we can see the third argument is the **return_array**, that's simply asking us which row of corresponding information should we return

- *In cell B2 add*: `=XLOOKUP(A2,Sheet1!E:E,Sheet1!C:C)`

The other three arguments are:
1. **if_not_found**
2. **match_mode**
3. **search_mode**

**if_not_found** is straight forward, what value to give if not information isn't present in that look up. 

i.e. If the email address found in Sheet1 doesn't have a corresponding email in Sheet1 column E, what should I return. 

I'll just add: 'Not found'

- *In cell B2 add*: `=XLOOKUP(A2,Sheet1!E:E,Sheet1!C:C,"Not found",)`


The **match_mode** argument takes a number to represent how we identify a match. 

We're using an email to search other spreadsheets so we want an exact match which is 0. 0 is also the default value which is fine, but if we had scores asigned to each student and a table which had the tiers of scoring, i.e. 

- 0 was a Fail
- 40 was a Pass
- 70 a Distinction

We could use -1 to search the score column and find a match for a students score or a the next smaller score to know what band their in. 

That sounds more complicated than it is, so I'll show you a quick example at the end. 

If we pass **1** in instead, it does the same thing but searches for the next highest number.

Then finally **2** takes a substring, so we can search for text which contains part of the value. 

I'll leave mine as the default **0** and just add another comma. 

- *In cell B2 add*: `=XLOOKUP(A2,Sheet1!E:E,Sheet1!C:C,"Not found",,)`


Finally, we have the **search_mode**, I won't go into this in too much detail but it asks us whether we want to search:
- top to bottom
- bottom to top
  - this is useful if we had exams where students were allowed to resit
  - if each resit got added to the bottom of a spreadsheet we'd want to search **last-to-first** to take their latest score.
- the **binary search** options are for when there's millions of rows and we're assisting excel to do it's job faster to tell the formula where to begin it's search
  - not something often used

I can add in a 1 or another comma if I wish but I want these formulas to be as readable as possible so actually I'm going to delete those last two commas and just assume the default values

- *In cell B2 remove*: `=XLOOKUP(A2,Sheet1!E:E,Sheet1!C:C,"Not found")`

- *In cell B1 add*: 'First Name'
- *Auto fill down corresponding values*

### Challenge

I'd like you to spend 10 minutes adding two more look ups from **Sheet1**:
- One for the student last name
- Another for the student clinical area

### Solution

- **Last Name** - `=XLOOKUP(A2,Sheet1!E:E,Sheet1!D:D,"Not found")`
- **04 May - 07 June Clinical Area** - `=XLOOKUP(A2,Sheet1!E:E,Sheet1!B:B,"Not found")`

### Seperate files

Let's finish with a look up on a seperate file all-together. 

The syntax is exactly the same, we just need to change the **lookup_array** syntax, which was our second value.

All we do is pass the file name in square brackets before targetting a sheet.

- *In cell E1 add*: '05 Jan - 22 Feb Clinical Area'

- *In cell E2 add*: `=XLOOKUP(A2,)`

Then same as before, single quotes and a square bracket, where we put our filename in.

- *In cell E2 add*: `'[0923 BSc Student allocations (LSBU-Barts Health)-.xlsx]Sheet1'!J:J,)`

Then the same syntax to reference the column inform we want to bring in.

- *In cell E2 add*: 
```xlsx
=XLOOKUP(
    A2,
    '[0923 BSc Student allocations (LSBU-Barts Health)-.xlsx]Sheet1'!J:J,
    '[0923 BSc Student allocations (LSBU-Barts Health)-.xlsx]Sheet1'!L:L,
    "Not found"
)
```

You may have to click a little pop-up to trust external spreadsheets but it should be able to pull infrmation and consolidate information from several sources. 

### Different match mode

The final thing I'll show you that match mode we saw earlier.

If we had data from assessments in a file we could use an XLOOKUP in a similar way but for ease I'll add my own mock data.

- *In cell F1 add*: 'Score'

Then I'll generate a random score for each of the students. 

- *In cell F2 add*: `=RANDBETWEEN(0,100)`
  - *Auto fill down*

Again I'll just create a small table which breaks down results and a grade they align to.

- *In cell M1 add*: 'Score'
  - *In cell M2 add*: '0'
  - *In cell M3 add*: '40'
  - *In cell M4 add*: '70'
- *In cell N1 add*: 'Grade'
  - *In cell N2 add*: 'Fail'
  - *In cell N3 add*: 'Pass'
  - *In cell N4 add*: 'Distinction'

- *In cell G2 add*: `=XLOOKUP(F2)`

Our lookup value isn't now the email, but the score

- *In cell G2 add*: `=XLOOKUP(F2, $M$2:$M$4)`

Our lookup array is now those values between M2 and M4

Notice I've used dollar symbols as well. When I go to **'auto fill down'**, I want want to increment the values from this range, by passing dollar symbols, excel will understand these to be absolute values instead. 

- *In cell G2 add*: `=XLOOKUP(F2, $M$2:$M$4, $N$2:$N$4)`

Then our return value is between N2 and N4

I'll add an argument for when a value is not found and then a **match mode**, most of our learners won't have scored exactly a 0, 40 or 70 and we want to categarise them by grade so if I add a **-1** it'll check if there's a match, then look for the next smallest value in the **lookup_array** we gave.

- - *In cell G2 add*: `=XLOOKUP(F2, $M$2:$M$4, $N$2:$N$4,"Not found",-1)`


## Block 5 - Pivot Tables and Summary Structures

We'll finish this module looking at Pivot Tables.

PivotTables are one of the most powerful tools available to anyone working with tabular data, and also one of the most underused. 

The reason most people avoid them is that they look complex and feel unfamiliar. Once you understand the logic — rows, columns, values, filters — they become the fastest way to answer a question like "how does this break down by team?" or "what does this look like by month?"

The alternative to a PivotTable is a manual summary table built with COUNTIF formulas, like we saw earlier, which works well for a fixed structure but again, there's a lot of manual input and if the data changes, formulas may break. 

PivotTables let you change the breakdown really easily, without rewriting formulas. 

If you're initially trying to gain an insight - where you are not yet sure which view of the data is most useful — the flexibility is invaluable.

This doesn't mean, you'll never write a a excel formula again. 

- PivotTables are ideal for exploration and for reports where the data will be refreshed regularly. 
- Formula-based summaries are better when you need a fixed, portable structure that others can read who may not understand how to use PivotTables.

PivotTables sit at the boundary between the **Analysis** and **Visualisation** stages. They are the tool you use to find the summary that is worth communicating — before then going to create a chart or diagram.

### Getting Started

We'll be using the `Apprentice KPI tables April 2026` file.

The reason I chose this is because the data is firstly **tabular** but it's:
- repetitive
- and categorical

A good test you can do by yourself is to say to yourself:

- *Can I ask, "how many", or "how much" or "what's the average" based on a category.*

With our data I can easily ask questions like:
- *how many data analysts are there?*
- *how many are based at the Royal London Hospital?*
- *how many are married?*

To create a **PivotTable** we need to click on any cell within the data. 

Then on the top window then click **Insert**. Following that you should see a drop down option for **PivotTable**, then we'll need to selet **From Table/Range**

It'll ask for a **Source**, the default one should be fine, as we started the process from within the data set we care about. So I'll click on the green tick. 

Finally just a choice of where to create the table and I'll select **New sheet**


### PivotTable Fields

Hopefully you can see something similar to myself, a new sheet and a window called PivotTable Fields. 

We have all the columns from the previous table and then we can see:
- Filters
- Rows
- Columns
- Values

Those fields help up answer questions like: *"How do I want to group my data, and what do I want to calculate?"*

#### Rows

If I drag **Site** into the **Rows** section what we're doing is group the information by the individual values from in that column on the previous table. 

We can add more fields to the **Rows**. If I drag **Division** underneath **Rows**, you can see that we're initially grouping by **Site**, then within each **Site**, what we've done is group all the **Divisions** which appear within each parent group. 

So pretty quickly you can see that:
- the site **GCS** has only one division represented
- the **RLH** has much more


I'll remove that field but we can layer these groups however we want. 
- *Remove Division from Rows*


#### Values

Values on the other hand are what you want to:
- count
- sum
- average etc..

If I drag **Names** into **Values**, Excel automatically counts the number of names related to each row or group. 

- *Drag Names into Values**

Count is the default but I can change that. 

If I hover over the *Cont of Names* you'll see a drop down menu and then if I click into *Value Field Settings* we'll see options for:
- Count
- Average
- Max
- Min
- Product etc..

If I drag the field **age** into values, it'll add a new column and we can then change the field instead of **count** or **sum** into **average** and then see the average age of students based on each site. 

Again, all these depends on the field we're grouping by, or what we've added to rows. 

If we were to group by **Site** and then **Staff Group**

- *Add field "Staff Group" to rows, underneath Site*

Then we'd be seeing the **Average of age** column would be showing the average ages of people within each Staff Group. 

#### Columns

Let's take a look at columns. 

I'll remove everything but our **Site** row and **Count of Name** in Values. 

- *remove all fields, aside from 'site' in rows and 'count of name' in Values*

If I then drag **Ethnicity** into Columns, it'll split to group which we've got, **rows** into the ethnicities based in each group. 

- *Add Ethnicity to Columns*

We can add a further column and similar to our first, within each column we've got, so:
- Asian
- Black
- Mixed
- etc..

Then the Pivot Table will add columns for the other values in the data. 

- *Add Gender to Columns underneath Ethnicity**

So now we're seeing the breakdown of gender for each ethnicity. 

With all of these things it's best to have fairly shallow data. 

Having 1 to 2 rows which combine well together, maybe a:
- row to group data by *city*, then another row for *site* works quite well. If we were to go much deeper, the readability of the data becomes quite hard and it'll prevent you from telling the core story of your data.

- a similar thing in relation to columns and values as well

So just as a recap:
- rows - group the data 
- values - calculate 
- columns - split the groups

#### Filters

Filters limit the data being shown 

Let me place **Apprenticeship Status** into Filters

- *Place 'Apprenticeship Status' into Filters.

We'll see a new section above our pivot table, if we click on the drop down we can then select to only return information on completed apprentices. 

We can also apply a filter onto a specific row or group by clicking on the drop down arrow as well. 

Using PivotTables can feel quite complicated and I'm sure some people will be more comfortable than others but it's important to play around with the data.

See the different ways you can present it and have your approach how to get meaningful insights. 

### Challenge

I'd like to give you an opportunity to do that right now. 

What I want is for you to have a go and basically create a PivotTable which will show, from those who've **withdrawn** or **paused** their training, how many of them had any form of **caring responsibilities** or those who didnt. 


### Solution

We could have:

- rows
  - Caring Responsibility 

- values
  - Cont of Name

- filter
  - Apprenticeship Status and only see information about Paused and Withdrawn students

We could then from this point if we wish make a calculation about what percentage each of these represent from all students or study trends over time. 
