<h1>Hotel-Booking-Analysis</h1><br>
The project contains the real world data record of hotel bookings of a city and a resort hotel containing details like bookings, cancellations, guest details etc. from 2015 to 2017. In this project we are going to analyze Hotel Booking Data in order to find out valuable insights and give suggestions to increase revenue of hotels.<br>

Programming Language : Python

Libraries used : Pandas, Numpy, Matplotlib, Seaborn

NoteBook : Google Colab

Dataset Source : Provided by Almabetter themself.

<h2>Objective</h2><br>
We are provided with a hotel bookings dataset.

The main purpose of this study is to perform EDA on the given dataset and draw useful conclusions about the trends in hotel bookings and how factors that control hotel bookings influence each other.

<h2>Dataset</h2><br>
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

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
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for Yes)
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
  
Total number of rows in data: 119390<br>
Total number of columns: 32

<h2>Data Cleaning and Feature Engineering</h2><br>
(1) Handling null values
Null values in columns company and agent were replaced by 0.
Null values in column country were replaced by 'others'.
Null values in column children were replaced by the mean of the column.

(2) Removing Duplicate rows
All duplicate rows were dropped.

(3) Converting columns to appropriate data types
Changed data type of children, company, agent to int type.

(4) Renaming the columns
The adr column was renamed for better understanding to average_daily_rate

(4) Removing outliers
One outlier was found in the average_daily_rate column. Dropping them.

(5) Creating new columns
Creating new column Total_stay by adding stays_in_weekend_nights+stays_in_week_nights.
Creating new column Total_members by adding adults+children+babies.

<h2>Exploratory Data Analysis</h2><br>
Performed EDA and tried answering the following questions:

 Q1) Which hotel has more no of bookings and What is the  percentage of bookings in each hotel ?<br>
 Q2) Hotel Wise Bookings based on Month and year also What is the trend of bookings within a month ?<br>
 Q3) Which meal type is the  most preffered meal of customers ?<br>
 Q4) Country Wise - Number of Bookings ?<br>
 Q5) Which agent is making maximum Bookings ?<br>
 Q6) Which room type is in most demand and which room type generates the  highest average daily rate?<br>
 Q8) How long do people stay at the hotels?<br>
 Q9) What is preferred stay length in each hotel based on weekday nights and weekend nights ?<br>
 Q10) Which Booking is preffered with the deposite type?<br>
 Q11) Cancellation rates in both the hotels also arival year and  lead time?<br>
 Q12) What is the Average daily rate month wise also which are the most busy months??<br>
 Q13) What is the Average daily rate with respect to per person?<br>
 Q14) Is thier any Special request given by the customer to hotels?<br>
 Q15) Which channel is mostly used for the booking of hotels? <br>
 Q16) Chances that its customer will return for another stay?<br>
 Q17) Which types of customers mostly make bookings?<br>
 Q18) How many customers are most likely to require a parking space?<br>
 
Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:
1) Bar Plot.
2) Scatter Plot.
3) Pie Chart.
4) Line Plot.
5) Heatmap.
6) Box Plot

<h2>Analysis:</h2><br>
Performed analysis and made following conclusions:

 1.) 61% bookings are for City hotel and 39% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel. <br>
 2.) July- August are the most busier and profitable months for both of hotels.  <br>
 3.) Most popular meal type is BB(Bed and Breakfast).<br>
 4.) Most of the guests came from european countries, with highest number of guests from Portugal.<br>
 5.) Agent no. 9 has made most no. of bookings.<br>
 6.) Most demanded room type is A, but better average daily rate generating rooms H, G and C. Hotels should increase the no. of room types A and H to maximise revenue.<br>
 7.) Most common stay length is less than 4 days and generally people prefer City hotel for short stay, but for long stays, Resort Hotel is preferred.<br>
 8.) Guests use different channels for making bookings out of which most preferred way is TA/TO.<br> 
 9.) Overall average daily rate of City hotel is slightly higher than Resort hotel and no. of bookings of City hotel is also higher than Resort hotel. Hence, City hotel is makes more revenue.<br>
 10.) Cancelation rate is higher in city hotel. With lead time more than 100 there is more possibility of cancellation.<br>
 11.) Both hotels have very small percentage that customer will repeat.<br>
 12.) Arrivals in hotels increases at weekends and also the average daily rate tends to go up as month ends. <br>
 13.) Moslty bookings are done by couples(bookings have two adults.)<br>
 
<h2>Conclusion</h2><br>
(1) 61% bookings are for City hotel and 39% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel. Also the overall average daily rate of City hotel is slightly higher than Resort hotel.<br>
(2) Mostly guests stay for less than 5 days in hotel and for longer stays Resort hotel is preferred.<br>
(3) Most of the guests came from european countries, with most of guests coming from Portugal.<br>
(4) It's clearly seen that the most people preferred room is Type A, . Also, the average daily rate of type A rooms seems to be less. But, those whose average daily rate is higher i.e.(Type C,G,F,H) it's seen that preference is also less, hotel need to improve on this.<br>
(5) Retention rate of both the hotel is very low need to think on that too.<br>
(6) We should also target months between May to Aug. Those are peak month for Hotel revenue generation. <br>
(7) Within a month, average daily rate gradually increases as month ends, with small sudden rise on weekends.<br>
(8) Couples are the most common guests for hotels, hence hotels can plan services according to couples needs to increase revenue.<br>
(9) For customers, generally the longer stays (more than 15 days) can result in better deals in terms of low average daily rate.<br>
(10) November, December, January and February are the months which has least bookings so in this periods you can get rooms with less average daily rate.<br>
And many more conclusion

<h2>Challenges</h2><br>
(1) Lot of null values were present in the dataset.<br>
(2) Data type of some Data was in wrong format.<br>
(3) Lot of duplicate data.<br>
(4) Which visualization techniques to use was a challenge?<br>
