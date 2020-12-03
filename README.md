# Kickstarting with Excel

## Overview of Project

### Purpose

Louise is interested in using Kickstarter to fund plays. This analysis was conducted to look at trends in Kickstarter data and ultimately determine factors that influence the likelihood of a campaign succeeding, so that Louise is best prepared to launch a successful campaign. Specifically, campaign **launch date** and **funding goal** are analyzed individually to determine the best time of year and the ideal funding goal to launch a successful theater/play campaign.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To analyze outcomes based on launch date, a pivot table and pivot chart were created using the full Kickstarter dataset. The pivot table was organized and filtered (see images below) to show the relevant data.

----placeholder for pictures-----

### Analysis of Outcomes Based on Goals

To analyze outcomes based on goals, goal ranges were first established in order to bucket each campaign. Then the `COUNTIFS` function was used to build the following table:

----placeholder for pictures-----

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

From 2009 to 2017, the greatest number of successful theater-related Kickstarter campaigns were created during the month of May (111 total successful campaigns), followed by June (100) and July (87). Theater-related campaigns launched in May, June, and July had success rates of 67%, 65%, and 63% respectively, compared to a general success rate of 61% for theater-related campaigns over the time period. This indicates that the best time to launch a successful theater-related Kickstarter campain is early- to mid- summer; specifically, May through July, with May being the ideal launch date.

In the same time period, the month with the least number of successful theater-related Kickstarter campaigns created was December (37 total successful campaigns). Theater-related campaigns launched in December had a success rate of 49%, compared to a general success rate of 61% for theater-related campaigns over the time period. This indicates that theater-related Kickstarter campaigns should not be launched in December in order to increase the likelihood of a successful outcome.

- What can you conclude about the Outcomes based on Goals?

The

- What are some limitations of this dataset?

The dataset does not capture certain information or potentially confounding variables that would be relevant to the outcome of a Kickstarter campaign. For instance, it does not include data on the *quality* of campaigns, which is admittedly challenging to quantify or categorize, or the economic conditions at the time and place the campaign was launched that may impact the willingness of backers to fund certain types of campaigns. For example, backers may not support campaigns deemed unnecessary or frivolous during periods of economic recession.

In addition, the 4114 campaigns included in the dataset may not be a representative sample of all Kickstarter campaigns, and may be too small of a sample size to perform meaningful statistical analysis.

- What are some other possible tables and/or graphs that we could create?

To futher explore how to create a successful Kickstarter campain, the duration of campaigns could be analyzed against campaign outcomes to determine how quickly successful campaigns are funded. 

Another possible analysis could be examining the average donation amount across campaign outcomes. A bar chart could depict the average donation to successful, failed, and canceled campaigns. Knowing the average donation received per backer for successful campaigns may enable more targeted marketing efforts to increase awareness of the campaign among potential backers in a target income bracket.
