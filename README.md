# Ford GoBike / bike-sharing system - San Francisco Bay area
## by Michael Hasterok


## Dataset

- The data is provided by udacity and includes data from the 'Ford GoBike / bike-sharing system - San Francisco Bay area' in the period February 2019.
- The name of the origiinal file is '201902-fordgobike-tripdata.csv' and has 183412 entries/rows with 16 columns.
- Each entry contains an index and the following 16 entries:
    duration_sec, start_time, end_time, start_station_id,
    start_station_name, start_station_latitude, start_station_longitude, end_station_id,
    end_station_name, end_station_latitude, end_station_longitude, bike_id, user_type,
    member_birth_year, member_gender, bike_share_for_all_trip
- I used jupyter notebook as a basis. So I read the .csv file and converted it into a pandas df.
- The results and plotted graphics were created on this basis.

## Summary of Findings

- Duration has a very long-tailed distribution, with a lot of durations on the low last end, and few on the high end. When plotted on a log-scale, the duration looks like normal dirstributed, with a peak of around 10 minuts
- most common Start Station: Market St at 10th St. and most common End Station: San Francisco Caltrain Station 2 (Townsend St at 4th St)
- The largest amount of users are subscriber 89 %, the rest are customer 11 %
- The distribution of customer age is left tailed, the largest customer group is at age between 25 and 35 years. Average age is 34.
- Almost 3/4 % of customers are male, round about 1/5 % are female, 2 % ohter and 5 % are not specified.
- at the weekend the number of users is much lower
- The distribution of day hour is bimodal with two peaks at 8 and 17 a clock.

> **correlations between numeric data of interest**
- Ther is a linear correlation of 0.34 between start station and end station.
- The realationships betwee (member_age, weekday, hour, duration_min, bike_id, start_station_id, end_station_id) are close to zero.

> **duration vs. age**
- A concentration of data is visible in the range of ages between 25 and 35 years and duration of 10 minutes.
> **duration vs. categorical (weekday, hour, gender, user type)**
- At weekend day the trip durations are a little longer than at Monday till Friday.
- At the times of day with the most frequent use (8 a.m. and 5 p.m.), the travel times are least spread.
- Customer drive longer than subscriber.

> **age vs. categorical (weekday, hour, gender, user type)**
- At weekend days the member age is a little younger.
- When comparing age to hour, one value in particular stands out, 4 a clock. Here the users are older than average and the spread is greatest.
- Male user are slightly older on average than Female user.
- There are few more older subscribers than there are customers.


## Key Insights for Presentation

> Main threads:
- What does the duration of the bike rental tell us?
- Who are the users and what differences do they have?

> Changes in design of polished plots from exploration step.
- Pie chart 'The user type distribution.': added title, changed color, used data without not specified users
- Pie chart 'The gender distribution.': added title, changed color, used data without not specified users
- Histogram 'Number of users by age.': changed color, limit the x-axis, changed binsize
- Histogram 'Distribution of duration.': changed color, limit the x-axis, changed x-label, addedd title
- Bar plot 'User per weekday.' and 'User per hour.': changed color, added title
- Bar plot 'duration / weekday per (user_type & gender)': changed color, removed x-label, changed y-label, set confidence interval, ci=None, , used data without not specified users

