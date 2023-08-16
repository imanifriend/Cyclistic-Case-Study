# Cyclistic Case Study

Cyclistic is a bike sharing company located in Chicago. The director of marketing for Cyclistic believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. The marketing analyst team needs to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics.

Data Source [divvy.tripdate](https://divvy-tripdata.s3.amazonaws.com/index.html)
# Ask
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

[Data Cleaning](https://github.com/imanifriend/portfolio/commit/ddc892d0d03f8b96b2426ab0f76f9bf744308196)

I then began cleaning the data by column.

Ride_id was checked first to confirm that all the ride ids were the same length. Rideable_type was then checked to confirm that the spelling is the same and only three options showed (electric, classic, and docked). Docked shows bikes not in use so this will be removed as neither memeber has touched these. Member_casusal was then checked to confirm spelling and that there was only two member types. Start_station and end_station were also checked and confirmed to not have any errors. Next null values were removed from all columns.

# Analyze

[Data analysis](https://github.com/imanifriend/Cyclistic-Case-Study/blob/main/analysis)

Next I moved on to analyzing the data for each member type. Queries were for e performed to show the start_lat, end_lat, start_lng, and end_lng for each memeber type and grouped to show the number of trips between these. Quereies were also done for the station_name to show the areas members and casusal riders are likely to start and end at. The same was done for ridable_type to show the total number of rides for each bike type between members and casual users. 

# Share

Visualizations were created using Tableau public.

Below shows total trips by member and by the bike type. Both members and casusal riders tend to use the classic bikes over the electric. Members tend to choose the classic at a higher margin. This also confirms what is known, that members are using the bikes more than casual riders. 

![Total trips by member and bike type](https://github.com/imanifriend/Cyclistic-Case-Study/assets/141570594/a058ea69-d03d-4857-ab40-72b241d5f141)

Below marks the start and stop latitude and longitude for each member type. A large cluster is shown for casusal riders around tourist areas while members tend to use around suburban/ neightborhood areas.
![Sheet 2](https://github.com/imanifriend/Cyclistic-Case-Study/assets/141570594/f1a99cbe-8545-41d8-b43a-3b1900596397)

![Sheet 2 (1)](https://github.com/imanifriend/Cyclistic-Case-Study/assets/141570594/4a9561e9-2a06-47da-8854-2c426f46ad1d)


