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


## Block 1

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

## Block 2

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