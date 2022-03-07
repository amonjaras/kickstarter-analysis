# Kickstarting with Excel

## Overview of Project
This project allowed Louise's play Fever to be successful. Since she is interested in the "theatre" category, the next stage of this project will be to analyze the information in two different sections. Based on the launch date, the outcome will determine when the plays are more successful throughout the year.
Therefore the outcome based on goals will determine the range for the highest probability of success.

### Purpose
The next stage of this project is to analyze different campaigns fared with their launch date and funding goals. They provide better visibility in terms of when is better to perform the campaign and the best goal.

## Analysis and Challenges
### Outcome vs Launch Date

To better analyze through time, it was needed to filter the dates by year using =YEAR() vs Date Created, see Fig1.

<img src="https://github.com/amonjaras/kickstarter-analysis/blob/main/Kickstarter_Challenge/Resources/YEARvsDate_Created.png"/>

###### Fig 1: Use of YEAR() formula


By counting the number of outcomes, "Successful," "Failed," and "Canceled" for the theatre category, we can analyze the outcomes vs launch date by a month.

<img src="https://github.com/amonjaras/kickstarter-analysis/blob/main/Kickstarter_Challenge/Resources/OutcomevsLaunch_build.png"/>

###### Fig 2: Use of Pivot Table


### Outcome Based on Goals

Dividing the goal by ranges and counting the number of goals reached by "Successful," "Failed," and "Canceled," we can analyze the outcomes based on goals. The formula COUNTIFS() was used to organize this information; SUM() was used for the total of projects on every goal range.

###### COUTIFS() formula

> For column B4
```
=COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,">5000",Kickstarter!$D:$D,"<=9999",Kickstarter!$R:$R,"plays")
```

###### Total of Projects Calculation

> For column E4
```
=SUM(B4:D4)
```

###### Percentage Calculation

> For column F4
```
=B4/$E4
```

### Analysis of Outcomes Based on Launch Date
For a play to be successful, it needs to be launched between the month's May and June.
As it can be appreciated in the chart "Theater Outcomes vs Launch Date," May has 111, and June 100 successful theatre plays. Throughout the year, it is noticeable the decrease of successful plays and the increment of failed plays by the month of September and October.
We do not recommend launching a play during the month of January since it has an increase in cancellations. The Figure 3 shows the information explained.

<img src="https://github.com/amonjaras/kickstarter-analysis/blob/main/Kickstarter_Challenge/Resources/Theater_Outcomes_vs_Launch.png"/>

###### Fig 3: Theater Outcomes vs Launch Date


### Analysis of Outcomes Based on Goals
The projects had been grouped based on their goal amount and classified by the number of outcomes "Successful," "Failed," "Canceled."
The results show a play will have more probabilities of being successful when the goal is less than 1000 with a total of Projects less than 200; if the total of projects is around 500, the plays will have probabilities of success.
We need to emphasize that even though there are probabilities of success when the goal is between 35000 and 44999, the total of projects is less than 8; this is not recommendable since there is a high risk of failure.
Having a goal between 20000 and 34999 increases the probability of failure.
The Figure 4 shows the results of the analysis.

<img src="https://github.com/amonjaras/kickstarter-analysis/blob/main/Kickstarter_Challenge/Resources/Outcomes_vs_Goals.png"/>

###### Fig 4: Outcomes Based on Goal


### Challenges and Difficulties Encountered
###### Data Analysis Challenges

1. While analyzing the data, it is not clear if the plays will be for an specific country. Information provided is the count within 19 different countries.

2. It is not clear why the analysis is done with mixed currencies, it is recommendable to generate one more input with the goal in same currency.

###### Data Analysis Difficulties

1. Working on the report using "Atom" interface for Mac and "Commit" all changes to GitHub repository

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. Best time to launch the plays is on May and June, since the number of successful outcomes is greater.

2. Worst time to launch the plays is September to December, since the number of failed outcomes increases. January is also not recommendable due to highest number of cancellations.

- What can you conclude about the Outcomes based on Goals?

The probability of success is higher when the goal is less than 1000. It is not ideal to launch plays with goals between 35000 and 44999, even though the probability of success seems higher, the total of plays is minimum and probability of failure is around 50%.

- What are some limitations of this dataset?

1. For the Outcomes based on Goals, the analysis will be more accurate if the goal was set up with same currency.

2. For Outcomes by Launch Date, the analysis could be complemented by comparing between countries.

- What are some other possible tables and/or graphs that we could create?

Insert a line chart to understand the trend of theatre campaign throughout the years
