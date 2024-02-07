# **Case Study: : How does a bike-share navigate speedy success?**

![image](https://github.com/GSD228/Data-analytics/assets/149749647/b2daeb65-49ca-4822-b9f0-f59f7221724c)


## Scenario 

You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of
marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your
team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team
will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve
your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

## About Cyclistic 

In 2016, Cyclistic launched a successful bike-sharing offering. Since then, the program has grown to a fleet of **5,824** bicycles that are geotracked and locked into a network of **692** stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime. 

Until now, Cyclistic’s marketing strategy relied on building general awareness and appealing to broad consumer segments. One approach that helped make these things possible was the flexibility of its pricing plans: single-ride passes, full-day passes, and annual memberships. Customers who purchase single-ride or full-day passes are referred to as casual riders. Customers who purchase annual memberships are Cyclistic members.

## The Stakeholders 

> 1. **Lily Moreno:** The director of marketing and my manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program. 
> 2. **Cyclistic marketing analytics team:** A team of data analysts who are responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy. 
> 3. **Cyclistic executive team:** A notoriously detail-oriented team which will decide whether to approve the recommended marketing program.

## The Business Task

The goal of this case study is to provide clear insights for designing marketing strategies aimed at converting casual riders into annual members. Towards this goal, I asked the following questions:

> 1. How do annual members and casual riders use Cyclistic bikes differently?
> 2. Why would casual riders buy Cyclistic annual memberships?
> 3. How can Cyclistic use digital media to influence casual riders to become members? 

## Preparing the Data 

This case study uses Cyclistic's historical trip data (previous 6 months) to analyze and identify trends. The data has been made available by Motivate International Inc. under and open license. The data can be dowloaded [here.](https://divvy-tripdata.s3.amazonaws.com/index.html)

This data is reliable, original, comprehensive and current as it is internally collected and stored safely by Cyclistic from June 2020 to present month. Personally identifiable information  such as credit card numbers has been removed because of data-privacy issues.

The data selected for use covers 6 months from November 2022 to April 2023. Each month has a separate dataset. The datasets are organized in tabular format and have 13 columns. Combined, the datasets have 1585555 rows. The **member_casual** column will allow me to group, aggregate and compare trends between casual riders and member riders. 

## Processing the Data from Dirty to Clean

### Tools
To process the data from dirty to clean, I chose to use **SQL.** because, it is relatively fast and thus useful in dealing with huge dasets.

### Cleaning the data

After reading in and combining the 6 datasets into a single dataframe, the first step in data cleaning was to identify spelling mistakes and duplicates,if any. 

Next, i removed blank cells (null values) and seperated out hour,days,month from the timestamp and put together in a single table.

### Transforming the data

I created the **diff_mins** column by getting the difference between the ended_at and started_at columns in minutes.

Additionally, I created four more columns **day**,**month**,**starting_time** and **ending_time**. These contain the day of the week, month, starting and ending time in which the bike was hired respectively. 

Upon getting the summary to ensure data was ready for analysis, I discovered that there were negative integers on the **diff_mins** column. I therefore removed the rows with negative values and values exceeding 1440 minutes (1 day) to examine them further. 

Finally, I got the summary of the data and concluded the data was ready for analysis. 

## Analyze Data to Answer Questions

In this step, I analyzed the cleaned data to find out how annual members and casual riders use Cyclistic bikes differently.

First,I extracted **no_of_rides** and **average_duration** as bike,hour,day and month wise from the dataset.

Then, analysed the extracted data in spreadsheet using pivot tables on various categories.

![bike_share_analysis - Pivot Table 1](https://github.com/GSD228/Data-analytics/assets/149749647/36afe4c2-fb13-44a5-aa75-bbc4f82f32cf)

Finally, I uploaded these data in tableau for visualization.

## Sharing Insights Through Visualization 

In this step, I've created captivating visualizations using **Tableau** to communicate the results of my analysis. Feel free to checkout my visualizations and insights [here.](https://docs.google.com/presentation/d/1POJvKukLZIi01EyL__qKeCHKIPrxzsmoBueLVLKxbBo/edit?usp=sharing)

## Key takeaways

> 1. Annual membership holders are found to be regular school/office goers, whereas casual riders can be categorized into two segments based on purpose as regular work and recreational purposes.

> 2. From the analysis, it is evident that casual riders take long duration rides than members. Therefore, Offers can be made based on duration of rides.

> 3. Advertisements can be made focussing non-member regular riders, especially targetting college students who takes ride without annual membership.
