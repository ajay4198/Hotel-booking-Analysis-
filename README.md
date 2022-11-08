# Hotel-booking-Analysis-
Analyzing the data of hotel-booking in the year of 2015-17

## Objective
We are provided with a hotel bookings dataset. 

Out main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.


## Problem Statement:
The hotel industry has a very big role in the world of business and is a very big field that depends upon different factors such as types of hotels, booking cancellations, type of booking data, date, year, month, type of meal, etc. By analyzing past datasets, it is easier to find various flaws, and by correcting the flaws, we can improve the required business strategy to be more effective than the others and, most importantly, to get closer to the interests, wishes, and needs of customers and provide them with satisfying service.
We are working on a hotel dataset that contains booking information for city and resort hotels with their corresponding variables, such as cancelled bookings, arrival data per year, arrival data per month, arrival data per day, types of guests (children, adults, and babies), etc. We have a total of 119390 rows and 32 columns. 
Firstly, we understand the meaning of each column, as it is very important to understand the data first to work effectively on the problems using the provided dataset. 
Secondly, we have done filtering and manipulation in which we did renaming of columns, found missing values in which we found only 5 columns containing null values (i.e., company, country, agent, and children), made changes to null values (we changed null values with zero), found duplicate values (total 31980 null values and 87230 are not null values), and dropped duplicate values, after which we have totaled 87230 rows and 33 columns.
finding through data analysis and visualization, we have performed various problems and reached their conclusions by plotting a bar graph, a pie chart, a count plot, a graphical representation (booking data by the country of origin), a heat map ( correlation between variables), and a, line plot.
## Dataset
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

```
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.
```

- Total number of rows in data: 119390
- Total number of columns: 32

## Data Cleaning and Feature Engineering

### (1) Removing Duplicate rows
All duplicate rows were dropped.

### (2) Handling null values
- Null values in columns `company` and `agent` were replaced by 0.
- Null values in column `country` were replaced by 'others'.
- Null values in column `children` were replaced by the mean of the column.


### (3) Converting columns to appropriate data types

- Changed data type of `children`, `company`, `agent` to str type.
- Changed data type of `reservation_status_date` to date type.

### (4) Removing outliers

- One outlier was found in the `adr` column. Simply dropped it.

### (5) Creating new columns
- Created new column `total_stay` by adding `stays_in_weekend_nights`+`stays_in_week_nights`.
- Created new column `total_people` by adding `adults`+`children`+`babies`.


## Exploratory Data Analysis

Performed EDA and tried answering the following questions:

```
Q-1 which is the most visited country by the visitor 
Q-2 In which month the highest reservations are done?
Q-3 which is the most populor meal ordered by the visitors?
Q-4 In which type of hotel the reservation is highest? (A) City hotel (B) Resort hotel
Q-5 To check the average cancellation booking of the year 2015,2016,2017. (1 is represented as the  canceled booking therefore, 0 represented as the  not-canceled booking)
Q-5 what is the cancellation rate between city and resort hotel?
Q-6 To check if the guest are Repeated or not (if guest is repeated (1) and if guest is not repeated(0))
Q-7 In the following years 2015,2016,2017 when the hotel is mostly booked by the visitors
Q-8 calculatet the ADR per person?
Q-9 find the ADR 
Q-10 check the visitors coming from which segment?
Q-11 check the highest Avrage daily rate months in 2016?



## Conclusion

```
'PRT'(Portugal )has the highest no of visitor (27355) while 'GBR'(Great Britain) has the second highest no of the visitor(10424) and 'FRA'(France)has the third highest no of the visitors(8823)

August is the highest reservation month (11242) meanwhile the lowest reservation month is january(4685)

BB is the most popular meal ordered by the visitor(67907)

City Hotel have the Highest reservation by the visitors as compare to Resort Hotel

The 72.4% booking were not canceled and 27.5% booking have been canceled

The highest cancelation rate was found in City Hotel and Highest booking was also found in City Hotel.

The bare minimum number of the guests were repeated

Most of time the visitors were arrived in the year of 2016 and 2017 in the city hotel.

The maximum of visitors like city Hotels.

The prices for resort hotels were higher and fluctuate more than city hotels.

City hotel: the ADR was more costly during the month of july,august, may, june; Resort Hotel: the ADR was more costly in during the month of july, august, june

Most of the visitor are coming from Online TA in City hotel and Resort hotel

Highest average daily rate month in 2016 is August

And many more conclusions.
```
## Challenges
```
(1) There was a lot of duplicate data.
(2) Data was present in wrong datatype format.
(3) Choosing appropriate visualization techniques to use was difficult.
(4) A lot of null values were there in the dataset.
