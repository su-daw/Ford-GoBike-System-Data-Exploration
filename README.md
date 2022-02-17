# Ford-GoBike-System-Data-Exploration
## by Sultanah Aldossari


## Dataset

> The Ford GoBike system is one of several bike sharing programs in the San Francisco Bay Area. As of January 2018, Bay Wheels had about 10,000 subscribers and launched the first regional and large-scale bicycle sharing system in California and the Western United States. It has provided nearly 500,000 rides since its launch in 2017. This exploration and visualization study primarily focuses on finding the bike usage pattern and customer habit characteristics in Feb 2019.

`About dataset:` 
a dataset include information about bike trips on February and March 2019. The dataset include

- duration_sec: Trip duration in seconds
- start_time: Trip start time and date
- end_time: Trip end time and date
- start_station_id: Trip start station id
- start_station_name: Station name
- start_station_latitude: Start station latitude
- start_station_longitude Start station longitude
- end_station_id: Trip end station ID
- end_station_name: Trip end station name
- end_station_latitude: End Station Latitude
- end_station_longitude: End Station Longitude
- bike_id: Bike ID
- user_type: User type whether a subscriber or a customer -- (“Subscriber” = Member or “Customer” = Casual)
- member_birth_year: User birth year
- member_gender: User gender whether a female or male
- bike_share_for_all_trip


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

> There were more trips on work days (Mon-Fri) than on the weekends, peaking around 8-9am and 17-18pm during the day. Males constituted a larger proportion of riders than females, and subscribers were more common than casual riders. Furthermore, Most of the members did not use the bike share for all of their trips, and most were between 25 and 40 years old. Because the data was straight-forward, no transformations were required. There are no unusual expectations for a bike sharing system in a major city. As of now, the data indicates that adults in the average working age range are the primary users of the system, and they use the bikes daily for commuting.

> By analyzing the data for the type of user, we discovered different behavior usage between customers and subscribers. Customers are more likely to be casual riders, like tourists or students on vacation. Subscribers, on the other hand, tend to be daily commuters and full-time students who mostly use the system during weekdays, in better weather, and mainly for shorter distances. They tend to rent bikes during the morning and evening of a typical work or school day (8-9am and 5-6pm). It varies between subscribers and customers in the time it takes to use bikes. Subscribers during weekends use their bicycles largely to commute during the week, whereas on weekends, there is a slight increase in customers, which indicates that they use it primarily for leisure purposes.


## Key Insights for Presentation

> Different usage habit between the two type of members are seen from the exploration. Subscribers use the system heavily on work days i.e. Monday through Friday whereas customers ride a lot on weekends, especially in the afternoon. Many trips concentrated around 8-9am and 17-18pm on work days for subscribers, yet customers tend to use more in the late afternoon around 17pm Monday to Friday. The efficient/short period of usage for subscribers corresponds to their high concentration on rush hours Monday through Friday, indicating the use is primarily for work commute. The more relaxing and flexible pattern of customer use shows that they're taking advantage of the bike sharing system quite differently from the subscribers, heavily over weekends and in the afternoon, for city tour or leisure purpose probably.
