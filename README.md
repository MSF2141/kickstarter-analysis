# An Analysis of Kickstarter Campaigns


## **Overview of Project**
An up-and-coming playwright, Louise, started a crowdfunding campaign to help fund her play, *Fever* in the US. Her estimated budget was over $10,000. Louise’s campaign came close to its fundraising goal in a short amount of time. Now, she wants to know how different campaigns fared in relation to their launch dates and their funding goals. 

### Purpose
The purpose of this analysis is to use the Kickstarter dataset and visualize campaign outcomes based on their launch dates and their funding goals. 


## **Analysis and Challenges**
Detail analysis and visualizations can be found here:
[Kickstarter_Challenge](https://github.com/MSF2141/kickstarter-analysis/blob/ff87527236d5482eea37c1c45f67196edc69bc89/Kickstarter_Challenge.zip)

### Analysis of Outcomes Based on Launch Date
Briefly, to analyze campaign outcomes based on their launch dates, the Kickstarter dataset was further processed to make the data more detailed. First, the “Category and Subcategory” column was split into two separate columns, “Parent category” and “Subcategory”. Second, the “Launched_at” and “Deadline” columns were converted from Unix timestamps (i.e., a measure of time in seconds since midnight of January 1, 1970) into a day-month-year format in new columns “Date Created Conversion” and “Date Ended Conversion”, respectively. Third, year was extracted from the “Date Created Conversion” column to a new “Years” column.  

To summarize the data, a pivot table was created from the KickStarter worksheet and filtered based on the “Parent Category” and “Years”. The "Parent Category" was then filtered to show only the data for "Theater" subcategory. For the Columns value the "Outcome" was selected. Column labels were then filtered to show only "Successful," "Failed," and "Canceled" campaigns. For the Rows value the "Date Created Conversion" was selected. The "Row Labels" column was grouped to show only the months of the year. In the Values box, the “Outcome" was selected and it appeared as "Count of outcome."	

To visualize the data, a pivot chart was created from the pivot table. To display campaign outcomes with relation to the launched month, as continuous data over time, a line with markers chart type was selected. 

![Outcomes_vs_Launch](https://github.com/MSF2141/kickstarter-analysis/blob/df7d9ee1ade3c2aa7ec4c6beb252f90852bf5cb7/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
Briefly, to analyze campaign outcomes based on their campaign goals, a summary table was created that contained a “Goal” column with several dollar-amount ranges so campaigns could be filtered based on their goal amount.  A COUNTIF() function was used to collect information from the Kickstarter dataset about the outcome and goal amount for the “Plays” subcategory and to fill the "Number Successful," "Number Failed," and "Number Canceled" campaign columns. Per each goal-amount range, “Total  Projects” was calculated using a SUM() function.  

Percentage of successful, failed, and canceled campaign outcomes was calculated by dividing "Number Successful", "Number Failed", and "Number Canceled" by “Total projects”, respectively. To display data as percentage, the format of  “Percentage successful”, “Percentage failed”, and “Percentage canceled” columns was changed from general to percentage.

To visualize the data as a relationship between the goal-amount ranges and percentage of successful, failed, or canceled campaigns, a line chart was created.
![Outcomes_vs_Goals](https://github.com/MSF2141/kickstarter-analysis/blob/c1ef0c78db6bd53c981d6a32ab45600eeef5841d/Resources/Outcomes_vs_Goals.png)



## **Results**
- What are two conclusions you can draw about the Outcomes based on Launch Date?
The month that launched the most successful Kickstarter campaigns is May, followed by June and July. These months also have similar numner of failed campaigns, which suggest that May is truely the most ideal month to launch a successful campaign.

- What can you conclude about the Outcomes based on Goals?
The most successful campaing goals are within the range of less than $1,000, followed by $1,000-$4,999 and $35,000 and $44,999 range. The third most successful range is substentially higher to the first two most successful ones suggesting that another factor can explain its success.
