# Kickstarting with Excel

## Overview of Project

### Purpose

Louise, a playwright, is interested in using Kickstarter to fund her plays. This analysis was conducted to look at trends in Kickstarter data and ultimately determine factors that influence the likelihood of a campaign succeeding, so that Louise is best prepared to launch a successful campaign. Specifically, campaign **launch date** and **funding goal** are analyzed individually to determine the best time of year and the ideal funding goal to launch a successful theater/play campaign.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To analyze outcomes based on launch date, a pivot table and pivot chart were created using the full Kickstarter dataset. The pivot table was organized and filtered (see Fig. 1 and Fig. 2 below) to show the relevant data.

#### Fig. 1: Outcomes Based on Launch Date - Pivot Table

![Outcomes Based on Launch Date: Pivot Table](https://github.com/amberteets/kickstarter-analysis/blob/main/Analysis_Screenshots/Outcomes_vs_Launch_pivot.png)

#### Fig. 2: Outcomes Based on Launch Date - Pivot Table Field List

![Outcomes Based on Launch Date: Pivot Table Field List](https://github.com/amberteets/kickstarter-analysis/blob/main/Analysis_Screenshots/Outcomes_vs_Launch_pivot_fields.png)

Then, a column was added (see Fig. 3) to indicate the percentage of successful campaigns for each month of the year. Conditional formatting (color scale) was applied to the column to visually indicate the percentage successful for each month.

#### Fig. 3: Outcomes Based on Launch Date - Percent Successful

![Outcomes Based on Launch Date: Percent](https://github.com/amberteets/kickstarter-analysis/blob/main/Analysis_Screenshots/Outcomes_vs_Launch_Date_Percent.png)

The resulting pivot chart (see Fig. 4) reveals that May has the highest number of successful campaigns and December has the least.

#### Fig. 4: Outcomes Based on Launch Date - Pivot Chart

![Outcomes Based on Launch Date: Pivot Chart](https://github.com/amberteets/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

To analyze outcomes based on goals, goal ranges were first established in order to bucket each campaign. Then the `COUNTIFS` function was used to build the following table (blue-shaded cells in the worksheet indicate cells referenced in the `COUNTIFS` formula):

#### Fig. 5: Outcomes Based on Goals - Analysis Table

![Outcomes Based on Goals: Table](https://github.com/amberteets/kickstarter-analysis/blob/main/Analysis_Screenshots/Outcomes_vs_Goal_Full.png)

To calculate the number of successful, failed, and canceled campaigns within each goal range the following formula was applied to cell `E6`, then copied over cells `E6:G17`:

`=COUNTIFS(outcomes, E$5, goal, ">="&$C6, goal, "<"&$D6, subcategory, $D$2)`
* `outcomes` refers to the Outcomes column in the dataset; `goal` refers to the Goal column and `subcategory` to the Subcategory column
* Counts the number of "plays" (`$D$2`) campaigns of each outcome (`E$5`, `F$5`, `G$5`) with goals within the ranges specified in columns `C` and `D`

The resulting line chart (see Fig. 6) depicts the relationship between funding goal and percentage of successful campaigns for Kickstarter campaigns within the "plays" subcategory.

#### Fig. 6: Outcomes Based on Goals - Line Chart

----placeholder

### Challenges and Difficulties Encountered

For an inexperienced Excel user, this analysis may have presented difficulties. To perform the analysis of outcomes based on launch date, it may be necessary (depending on the version of Excel used) to adjust the pivot table fields and group the Years in a specific way to obtain the months of the year as the `Axis (Categories)` values. In addition, when analyzing a large dataset with many conditionals (e.g. specific categories/subcategories, goal, outcome, etc.) it can be easy to overlook or forget to apply a certain filter or conditional statement, leading to incorrect results. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

From 2009 to 2017, the greatest number of successful theater-related Kickstarter campaigns were created during the month of May (111 total successful campaigns), followed by June (100) and July (87). Theater-related campaigns launched in May, June, and July had success rates of 67%, 65%, and 63% respectively, compared to a general success rate of 61% for theater-related campaigns over the time period. This indicates that the best time to launch a successful theater-related Kickstarter campain is early- to mid- summer; specifically, May through July, with May being the ideal launch date.

In the same time period, the month with the least number of successful theater-related Kickstarter campaigns created was December (37 total successful campaigns). Theater-related campaigns launched in December had a success rate of 49%, compared to a general success rate of 61% for theater-related campaigns over the time period. This indicates that theater-related Kickstarter campaigns should not be launched in December in order to increase the likelihood of a successful outcome.

- What can you conclude about the Outcomes based on Goals?

For Kickstarter campaigns within the "plays" subcategory, the likelihood of a successful outcome is inversely correlated with funding goal for goals less than $30,000 and greater than $45,000. However, the likelihood of success increases as goal increases for goals between $30,000 and $45,000. The percentage successful for campaigns with goals between $35,000 to $45,000 is 67%, compared to success rates of 76% for campaigns with goals less than $1000 and 73% for campaigns with goals between $1000 and $5000. This indicates that campaigns within the "plays" subcategory are most likely to be successful if the goal is less than $5000, but still have a relatively high rate of success when the goal is between $35,000 and $45,000. In other words, inexpensive plays are more likely to receive adequate funding from Kickstarter; plays with high production costs are also well-backed.

- What are some limitations of this dataset?

The dataset does not capture certain information or potentially confounding variables that would be relevant to the outcome of a Kickstarter campaign. For instance, it does not include data on the *quality* of campaigns, which is admittedly challenging to quantify or categorize, or the economic conditions at the time and place the campaign was launched that may impact the willingness of backers to fund certain types of campaigns. For example, backers may not support campaigns deemed unnecessary or frivolous during periods of economic recession.

In addition, the 4114 campaigns included in the dataset may not be a representative sample of all Kickstarter campaigns, and may be too small of a sample size to perform meaningful statistical analysis.

- What are some other possible tables and/or graphs that we could create?

To futher explore how to create a successful Kickstarter campain, the duration of campaigns could be analyzed against campaign outcomes to determine how quickly successful campaigns are funded. 

Another possible analysis could be examining the average donation amount across campaign outcomes. A bar chart could depict the average donation to successful, failed, and canceled campaigns. Knowing the average donation received per backer for successful campaigns may enable more targeted marketing efforts to increase awareness of the campaign among potential backers in a target income bracket.
