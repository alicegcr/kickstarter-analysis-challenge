# Kickstarting with Excel

## Overview of Project

--- 

### Purpose
- About the data 
* It is a datasets of plays from 2009 to 2017 included information from 21 countries.
* The columns has information about the id plays, the plays's name, the play's blurb, 

- This project want to answer the next question:

* How different campaigns fared in relations to the plays launch dates and their funding goals?

- To answer the main question:
* converted the launch date from timestamps to regular dates 
* applied a condionational formatting to the coutcomes column so I could visualize better the data 
* converted the goal column from currency to general numbers 
* divided the Category and Subcategory column in two differents columns, one for Parent Category and other for Subcategory 
* created a columns for the year launch date 

---
## Analysis and Challenges


### Analysis of Outcomes Based on Launch Date

- to find the results on this analysis:
* created a Pivot table on a new sheet 
* named the sheet Theater Outcomes by Launched Dates 
* Filteres by Parent Category and Year
* Outcomes as columns and Data Launched Convertion as rows 
* Counts of Outcomes on Values 
* filtered the Parent Category by Theater 

- results:
![Theater_Outcomes_vs_Launch](Resources/Theater_Outcomes_vs_Launch.png)

* It is a descriptive data that shows thhe month that had the most successful numbers was May and the month that had the most failed plays was October comparing the numbers total plays on the month. 


### Analysis of Outcomes Based on Goals

- to find the results on this analysis:
* on the dataset Kickstarter I filtered the subcategory by plays and the outcomes by successful, failed and caceled
* created a new sheet with the filtered information 
* created the Outcomes Based on Goals 
* created a column for the Goal Range, one for the Number of Successful, one for the Number of Failed, one for the Number of Canceled, one for Total of Projects, then a percentage column  for each of the outcomes 
* to find the numbers of the outcomes I used the CountIFs funtion

```=COUNTIFS('Plays subcategory data'!$D$2:$D$1067;"<1000";'Plays subcategory data'!$F$2:$F$1067;"=successful")```

* to find the numbers of the outcomes between ranges I used the CountIfs function:

```=COUNTIFS('Plays subcategory data'!$D$2:$D$1067;">=1000";'Plays subcategory data'!$D$2:$D$1067; "<=4999";'Plays subcategory data'!$F$2:$F$1067;"=successful")```

- results:
![Outcomes_vs_Goals](Resources/Outcomes_vs_Goals.png)

* On this analysis I could viasualize the why the number of failed plays was high, most of the plays that failed they had a higher funding goal, and they could not reached it. 


### Challenges and Difficulties Encountered

* I found difficulties finding the best formula to find the information between tha goals range, since I was using the CountIfs function, I had to watched some videos on youtube and also read some articles to find the best way to fit the goal range in the formula.
* Other challenge that I was strugle within it, the details, especially when I was filtering and doing charts.


---
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. May was the month that most had successful outcomes theater on the year 
2. october was the montg that most had failed outcomes theater on the year

- What can you conclude about the Outcomes based on Goals?

The greater the funding goal, the more significant the difference between Failed and Successful Outcomes, so there is more chance that the play will not reach the Funding Goal

- What are some limitations of this dataset?

One of the dataset limitations that I found is the Low quality of data, for example, I  wanted to know the customer side, reasons of choosen to go to a play ans other way, know more about the customer experience. 


- What are some other possible tables and/or graphs that we could create?

I would do a chart with the result of the Outcomes based on the Launched dates and the Goals Range 
