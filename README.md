# Ford-GoBike-System-Data-Exploration
## by Sultanah Aldossari


## Dataset

> The Ford GoBike system is one of several bike sharing programs in the San Francisco Bay Area. As of January 2018, Bay Wheels had about 10,000 subscribers and launched the first regional and large-scale bicycle sharing system in California and the Western United States. It has provided nearly 500,000 rides since its launch in 2017. This exploration and visualization study primarily focuses on finding the bike usage pattern and customer habit characteristics in Feb 2019.

`About dataset:` 
a dataset include information about bike trips on February and March 2019. The dataset include

• duration_sec: Trip duration in seconds
• start_time: Trip start time and date
• end_time: Trip end time and date
• start_station_id: Trip start station id
• start_station_name: Station name
• start_station_latitude: Start station latitude
• start_station_longitude Start station longitude
• end_station_id: Trip end station ID
• end_station_name: Trip end station name
• end_station_latitude: End Station Latitude
• end_station_longitude: End Station Longitude
• bike_id: Bike ID
• user_type: User type whether a subscriber or a customer -- (“Subscriber” = Member or “Customer” = Casual)
• member_birth_year: User birth year
• member_gender: User gender whether a female or male
• bike_share_for_all_trip


`Data Wrangling Process`

#### Data Gathering: 
Data was provided by Udacity as a csv file.

#### Data Assessing:
At the part, exploring was done to assess data and try to find any quality or tidiness issues that 
will be further cleaned in Cleaning phase
- Drop unwanted columns and columns with missing values 
- Change station name to string type 
- Change birth year from float to int type
- Change gender type to string type 
- Change user_type to string type 
- Change duration(start, end) time to datetime format
- Feature Engineering: days of week, months and hours, member_age, duration_minute

#### Data Cleaning:
- fix multiple fields that are not in the correct dtype, i.e. start_time, end_time should be datetime type, user_type and member_gender should be categorical data type, etc

- add new columns for trip duration in minute, trip start date in yyyy-mm-dd format, trip start hour of the day, day of week and month

- add a new column calculating member's age from 'member_birth_year'

- cast 'dayofweek' to category dtype


## Summary of Findings

> Based on the univariate exploring, I noticed that there were more trips on weekdays(from Monday till Friday) more than on weekends. Peaking hours are around 7-9 AM and 16-18 PM, which means that major propotion of bike usage are for daily commute to work. Also, A large propotion of bike riders are males and few are females. Most bike riders were between 25 and 40 years old.

> Based on bivariate investigation, we discovered different behavior usage between customers and subscribers. Customers are more likely to be casual riders, like tourists or students on vacation. Subscribers, on the other hand, tend to be daily commuters and full-time students who mostly use the system during weekdays, in better weather, and mainly for shorter distances. They tend to rent bikes during the morning and evening of a typical work or school day (8-9am and 5-6pm).


## Key Insights for Presentation

> There are several insights derived from our data:

- On weekdays the number of trips increases unlike on weekends were number of trips decreased sharply. and usually the reason is people on weekdays tend use bikes to go to their work, shops, do some activities. And people on weekends do rest.
- The average age range of FordGo Bikes is between 25 to 35, and then it starts to decrease as age increases. 
- The most bike trips is for young adults [20,30]Y and middle aged [40,50]Y.
- Mostly 90% of bikes trips are made by Subscribers, for Customers there are few bike trips compared to subscribers, which maybe indicates that they use it primarily for leisure purposes.
- Bike riders members are mainly Male members and few are females members, this certainly helps in marketing campaigns as it simplify the targeted segment.
- Willow st Vine st have the highest traffic etart Station.
- Parker ave at McAllister St have the highest traffic end Station.
- In the morning (7-9AM) and afternoon (5-6PM) are the highest bike rides of the day.
- In general, the bike share system is not very popular with customers; usage increases on weekends. The opposite is true for subscribers - on weekdays, usage has been high, but on weekends, usage has declined sharply.
- On weekends, there is a severe decline in volume for subscribers, which suggests that they use their bicycles primarily to commute to work during the week, whereas on weekends, there is a slight increase in volume for customers, which suggests that the use is primarily leisure/touring and relaxing.
- The number of subscribers was higher than the number of casual customers. we can see from the plot  clearly peaks out on typical rush hours when people go to work in the morning and getting off work in the afternoon
- There is a slight age difference between renters of bikes who ride from Monday through Friday and weekend renters, which corresponds to the commute to work patterns observed in the univariable exploration plots above.
- The average duration of subscription usage seems to be more consistent between customers and subscribers.