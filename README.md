# An Analysis of Kickstarter Campaigns

## Overview of Project
  
  
### Purpose

The purpose of this is project to analyze data from Kickstarter campaigns, to uncover trends in the successes and failures of campaigns. This project is going to be focused on finding patterns in the successes and failures in the **Theatre** Category and **Plays** subcategory, with the specific goals of analysing the following:

* Outcomes based on Launch Date (Focus on the **Theatre** category)
* Outcomes based on Goals (Focus on the **Plays** subcategory)
  

## Initial Familiarization with Data
  

### Visualization of Outcomes by Category

#### Explanation

I created a pivotchart of the data that groups the data by **Category** and then displaying their **Outcomes**. Using a stacked column visualization of this data was a great way to get a broad view of each type of Kickstarter campaign and their outcomes.

![parent_category_outcomes](/resources/parent_category_outcomes.png)

#### Brief Discussion

It's interesting to see **Theatre** taking the lead in volume of campaigns started. Also upon first look, it looks that **Music** seems to have the most successful distribution of **Outcomes**.
  
  ---
  
### Visualization of Outcomes by Subcategory

#### Explanation

Continuing with the stacked column visualization, let's take a more detailed look at the data sorted by **Subcategory** instead of Category, with each of their **Outcomes**.

![subcategory_outcomes](/resources/subcategory_outcomes.png)

#### Brief Discussion

It seems that **Plays** take the lead in **Subcategory** volume of campaigns. If you look through this chart, you can see that a few subcategories have seemingly 100% successful **Outcomes**. That data could be interesting to explore at another time...
  
  ---
  
## Analysis and Challenges

*For the following analyses, I only want the outcomes of **Successful**, **Failed**, and **Canceled** to be considered.*
  
### Analysis of Outcomes Based on Launch Date ("Theatre" Category)

#### Explanation

I filtered the information to only include campaigns from the **Theatre** category. Using the **Date Launched** column, I separated the outcomes into the months in which they launched and added the information to a line chart.

![theatre_outcomes_vs_launch](/resources/theatre_outcomes_vs_launch.png)

#### Brief Discussion

This visualization shows that when considering launch date, the highest count of Theatre campaigns with succcessful outcomes belongs to the group with launch dates in the month of May - with more than double the amount of failed outcomes of the same group. It also shows that Theatre based campaigns launched in the month of December will yield almost an equal amount of successful and failed campaigns.
  
  ---
  
### Analysis of Outcomes Based on Goals ("Plays" Subcategory)

#### Explanation

I filtered the information to only include campaigns from the **Plays** subcategory. For this analysis, I divided this data sample into groupings determined by ranges of campaign **Goal** amounts. Each was further divided by there campaign outcomes. After converting the outcomes counts to percentages in their respective goal amount groups, I used a line chart to visualize this data.

![play_outcomes_vs_goals](/resources/play_outcomes_vs_goals.png)

#### Brief Discussion

This chart shows that play campaigns with goal amounts that are less than $5000 have a much higher chance of succeeding than failing. Once the goal amount starts to rise, the chance of succeeding declines. This chart shows that there were more successful outcomes than failures with goal amounts between $35,000 and $45,000. Higher than that, and the odds for success plummet. Not impossible at higher goal amounts but the history doesn't show that it is a safe bet.
  
  ---
  
## Challenges and Difficulties Encountered

There was one small, subtle, and analysis-ruining mistake I caused for myself. Using the COUNTIFS() function for the **Outcomes of Plays Subcategory Based on Goals** was simple and intuitive, but... if you point to the wrong column for the function, you surprisingly get a very incorrect analysis. It was a mistake that made me scratch my head for half an hour as I tried to find where things were going wrong. It was slightly humbling to realize that the reason was due to a wrong column reference, and I needed that humility. 
  
  
  
## Results
  
  
### Conclusion of Outcomes Based on Launch Date ("Theatre" Category)

* May is a month with the highest count of successful theatre campaign outcomes when launched from this month, more than double the failed outcomes launched the same month. May is a safe month to use as a launch point. 

* Theatre based campaigns launched in the month of December will yield almost an equal amount of successful and failed campaigns. December isn't a safe month to launch a campaign from.
  
  
  
### Conclusion of Outcomes Based on Goals ("Plays" Subcategory)

Play campaigns with goals less than $5000, have a much healthier chance of success. More than 70% of the outcomes of this goal range were successful. 
  
  
### Limitations of this Data Set

* The analyses performed in this project were limited to a data set of Kickstarter campaigns with launch dates between **2009-05-17** and **2017-03-15**
* The data set used covered 21 countries. While this data set could be great for some areas which provided more to the overall data set, it may be misleading to people launching campaigns in countries that this data doesn't fully capture.
* The story being told by this data set could be made so much clearer if we also knew how much each campaign spent on marketing.
* It would be helpful to know if the campaigns are being launched by an established company/group or not. 
* In the **Outcomes of Plays Subcategory Based on Goals**, it seems as if there is a high success rate for plays that have goal amounts of $35,000 to $45,000 (above 66%). This is likely misleading, as there is only 9 campaigns in that range that are being analyzed.
  
  
  
### Other Possible Tables/Graphs for Consideration

* It would be fantastic to analyse the relationship the **Staff Pick** TRUE/FALSE data point has with the outcome of campaigns. It would be worth analysing the staff picked campaigns which failed. It could really paint a picture of what not to do.
* Similar to the goal amounts in the **Outcomes of Plays Subcategory Based on Goals**, it might be enlightening to see how the **Length of Campaign** impacts the outcome of the campaigns.


## References

* All data used: [Kickstarter Data](/Kickstarter_challenge.xlsx).
