# Module 2 — Data Visualisation & Storytelling
### Barts Health NHS × La Fosse — Microsoft 365 Data Skills Training

**Day 1 | 11:45–13:00 | Platform: Excel Online, Power BI (overview), Microsoft Fabric (overview)**
**Two 30-minute blocks, with a 15-minute break between them**

---

## Pre-Session Setup

- Load Slidee: barts_module_1_2

## Training 

- `Slide 4`

### Training Overview

We're now moving into Module 2.

This is where data stops being a spreadsheet and starts becoming a message. 

The analytical work we've done so far, cleaning, joining is all about producing numbers that are correct. 

Now we need to try and make those numbers useful. 

That involves selecting the right visual form, stripping away the noise that obsecures the point we're trying to convey and framing the finding we made that prompts a decision rather than just an observation. 

The skills here aren't necessarily technical, building charts in Excel takes minutes. 

The harder and more valuable skill is knowing which chart to build, formatting it so the right thing stands out. Then how to frame it so your audience understands it immediately. 

If we think back to our Data Lifecycle, this module will cover **Visualisation** and the beginning of the **Communication** stage.

### The Training

## Block 1 - Choosing the Right Chart 

Let's get onto charts, there's many which we can choose from but if there's 3 I want you to really focus on it'll be:

1. Bar Charts
2. Line Charts
3. Scatter Charts

### Bar Charts

Whether vertical or horizontal, **bar charts** are great for comparing values across distinct categories.
- which team
- which month
- which site

### Pie Charts

**Pie charts** are good for showing how a whole divides into parts, but really when there's a few categories and the proportional relationship is the main emphasis of the message

### Scatter Charts

**Scatter Charts** on the other hand for exploring whether two variables are related.

Like: *"Does higher absence correlate with lower scores or overall completion of a course."*

### Issues

Again the main purpose of choosing the right chart is to clearly convey a message to be acted upon. 

**Pie charts** with more than four or five segments, where the proportions become impossible to compare visually loose meaning. 

If we have **Bar charts** that don't start at zero can unitendidly exaggerate or understate differences between categories. 

**Line charts**, if they're used for categorical data implies a continuous trend where none exists. 

### Why it matters

Which chart you choose isn't an aesthetic decision, I want you to consider it an analytical one. 

The wrong chart type can make a meaningful pattern invisible. Or equally make a trivial difference look significant.

A habit we should all adopt is asking *"what question am I answering, and what visual form answers it most directly"*

### Bad Charts

I've got some bad charts and hopefully we'll see where the meaning has gotten lost or obscured. 

- `Slide 5`

On the screen we have a breakdown of the number of students in each **Division**

**ASK**
- Any thoughts?

**ANSWER**
- Too many segments or divisions
- Difficult to see the meaning of the chart
  - Makes us ask further questions

One thing we've not done with this dataset is clean it, which we should do. 

The largest segment of the chart is actually N/A.

For anyone viewing this chart fundamentally will need to ask several follow up questions which the creator would need to guide the viewer through. 

- `Slide 6`

Ok... another chart. This one shows the gender split of apprentices.

**ASK**
- Thoughts?

**ASK**
- With only three categories I think a pie chart would better serve the data
- Also at a glance you'd believe there were many many more, maybe 5 times as many males than females. 
  - That's because the graph starts at 700. 
  - In reality there's:
    - 708 *Females*
    - 753 *Males*
    - 739 who selected *Other*
  - The meaning of the visualisation changes quite dramatically 

- `Slide 7`

This is a better representation of the data and the message we're trying to convey. 

I've changed the scale on the y-axis and the title as well to tell the viewer what I want them to observe. 

Less questions to ask and more meaning. 

I've made one more improvement to my opinion and turn this into a pie chart. 

- `Slide 8`

The main improvement with this chart to my opinion is that we've removed uncessary data for the point I'm trying to convey. 

What I want the viewer to understand is that according to the data the gender balance is fairly even.

It's not important that the viewer knows theres:
- 708 *Females*
- 753 *Males*
- 739 who selected *Other*

This graph really quickly just shows the even distribution and the message lands straight away. 

I've got the numbers to back that up if people are curious but the graph is to convey a message for an action. 

The question to always ask yourself is when creating the chart is, *what is the one thing I want my audience to understand from this visual?* 

Then find the chart type that most directly answers that question. 

If you can write a single sentence beginning: *"This chart shows that..."*, then your chart is focused. 

If that sentence contains multiple *"ands"*, consider splitting that message into multple charts. 



## Block 2 - Building & Decluttering Charts in Excel Online

Let's actually build some charts together. 

As I've said a few times, we need to be considered when creating charts. The presentation of a chart is a reflection on the consideration we've taken regarding the underlying data. 

So although it may not seem that way, the presentation of our charts will correlate to whether the actions which ought to be taken off the back of them are or are not. 

We want our charts to be free of cluter. Again, not for aesthetic reasons - it's about removing everything that competes with the message.

- Gridlines
- Borders
- Redundant labels

Anything the readers eye has to move past before it reaches the data. The fewer things there are to look at the faster and more accurately the findings land. 

Part of this is also shifting from descriptive to insight-led titles. It requires no technical skill - only the discipline of asking *"what does this chart show?"* and writing that as the title, instead of the conventional description of the axes. 