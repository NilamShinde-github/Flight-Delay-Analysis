Goal Set:

Few days back, when I was talking with my friend I came across that my friend is facing flight delay problems, since he is working in different state and usually come back to see his family on Friday and again travel back on Monday morning for work. He had lots of questions about flights delay issue. Now, this time I am working on big data project and I had to choose dataset for my project. While searching on internet I found very interesting dataset. I have taken “US Flight Data for the month of Jan 2020”. I found this dataset on Kaggle.com. This data has been approved from Bureau of Transportation Statistics, Govt. of the USA and it is open sourced. There are more than 400,000 flights in January 2020, throughout the United States. 

I have chosen this dataset, because I wanted to do analysis on flights cancellation, delay and search the answers of below questions using this dataset:
1.	How many flights cancelled over a month and what were the days of month cancelled the most the flights.
2.	How many flights delayed over a month and what were the days of month most of the flights delayed?
3.	Is there any relation between flight delay and departure time block (flights fly over that period) pick time? (here, I wanted to check busiest time to take off the flights, really causes flight delays?)
•	Check pick time to take off flights over the days of week.
•	Compare it with delayed flights over the days of week.


Data file format:
There are many file formats that I can use to upload the data on Jupyter notebook. 
For example, 
•	Excel 
•	TSV (Tab Separated Values)
•	CSV (Comma Separated Values)
•	XML files (Extensible Markup Language)
•	JESON files (JavaScript Object Notation format), primarily used for transmitting data between a web application and a server.
We can use files as per our experiment needs. I have uploaded CSV files, since I am using python language for data analysis. It is easy to read and manipulate the text from such flat files.
If data found in some format and we want to convert it in different format, then we can do it using different methods. Ex, we can change .csv file into .json using python code and tools.

Explore and understand the data:

This dataset contains all flights in the United States starting from January 1, 2020 till January 31, 2020. There are 21 columns with almost all information about flights including origin airport, destination airport, airline information, departure time and arrival time. I have removed some columns which are not useful for analysis. Removed column names are TAIL_NUM (tail number of airplane), unnamed column, OP_CARRIER (repeated information same as OP_UNIQUE_CARRIER)
The columns I have chosen for my work are discussed below.
a)	DAY_OF_MONTH:
Days starts from 1st January 2020 till 31st January 2020.
b)	DAY_OF_WEEK:
Day of week starts from Monday to Sunday.
c)	OP_UNIQUE_CARRIER:
Unique carrier code is a code names of flights in short form. Here, I changed column name from “OP_UNIQUE_CARRIER” to “Airline_USA” for better understanding (names of flights).
d)	OP_UNIQUE_AIRLINE_ID:
An identification number assigned by US DOT to identify a unique airline (carrier). A unique airline (carrier) is defined as one holding and reporting under the same DOT certificate regardless of its Code, Name, or holding company/corporation.
e)	OP_CARRIER_FL_NUM:
Flight number.
f)	ORIGIN_AIRPORT_ID:
Origin Airport, Airport ID. An identification number assigned by US DOT to identify a unique airport.
g)	ORIGIN_AIRPORT_SEQ_ID:
Origin Airport Sequence ID is an identification number assigned by US DOT to identify a unique airport at a given point of time. Airport name or coordinates can change over time.
h)	ORIGIN: 
Origin Airport name in short form and there are around 360 airport names are in the dataset.
i)	DEST_AIRPORT_ID:
Destination airport identification number.
j)	DEST_AIRPORT_SEQ_ID:
Destination airport sequence id is number assigned by US DOT to identify a unique airport at a given point of time. The airport name or coordinates can change over time.
k)	DEST:
Destination Airport name.
l)	DEP_TIME:
Actual departure time in local time format: hhmm
m)	DEP_DEL15:
Departure Delay. Here, I changed column name as a ‘DEPARTURE_DELAY’ for better understanding.
n)	DEP_TIME_BLK:
Departure time block. The time slot where flights take off from the airport on hourly intervals. 
Example: 
A, B, C and D flights will take off in time slot between 10:00am-10:59am. The ORIGIN_AIRPORT_SEQ_ID could be different for different flights.
o)	ARR_TIME:
Actual arrival time of flight (local time of destination airport in: hhmm format)
p)	ARR_DEL15:
Arrival delay indicator delayed by 15 minutes or more. (if flights delayed then it is 1 = Yes, else 0 = No)
q)	CANCELLED:
Cancelled flight indicator (1= Yes, 0 = No)
r)	DIVERTED:
Diverted Flight Indicator (1 = Yes, 0 = No)
s)	DISTANCE:
Distance between airports in miles.
