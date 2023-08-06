# Cyclistic Case Study

Cyclistic is a bike sharing company located in Chicago. The director of marketing for Cyclistic believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. The marketing analyst team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics.

Data Source [divvy.tripdate](https://divvy-tripdata.s3.amazonaws.com/index.html)
# ASk
Three questions will guide the future marketing program:
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?
 
The first question has been assigned to me to answer: How do annual members and casual riders use Cyclistic bikes
differently?

# Prepare
I will be using Cyclistic historical Data from January 2022 to December 2022. Data has been collected from member usage and stored with the company so it is credible. This data has been made public by Motivate International Inc under this [license](https://ride.divvybikes.com/data-license-agreement)

The data is organized by month so there are 12 individual files to organize. Each file contains column names ride_id, rideable_type, started_at, ended_at, start_station_name, start_station_id, end_station_name, end_station_id, start_lat, start_lng, end_lat, end_lng, and member_casual.
# Process
I will be using SQL in Biqquery to clean and analyze since these datasets would be too large for excel.

First I uploaded the 12 csv files as tables under the divvy_tripdata dataset. I think combined all into one table labeled [divvy_tripdate_combining](https://github.com/imanifriend/portfolio/blob/main/datacombining) This new table contains 5,667,717 rows of data and 13 columns. The ride_id column is our primary key.

[Data Cleaning]

I then began cleaning the data by column.

# Analyze
