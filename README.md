# HOTEL BOOKING REPORT USING POWER BI

## 📊 Project Overview
This project is a data visualization dashboard built using **Power BI** to analyze hotel booking performance. The dashboard provides insights into key hotel KPIs such as **Total Revenue**, **Occupancy Rate**, **ADR (Average Daily Rate)**, and **RevPAR (Revenue per Available Room)** across multiple hotel branches. 

The goal is to help hotel management teams identify booking patterns, optimize pricing strategies, and improve overall operational performance.

---

## 🎯 Key Objectives
- Monitor business performance across hotel branches
- Track essential KPIs like ADR, RevPAR, and Occupancy Rate
- Identify revenue trends, booking channels, and guest behaviors
- Reduce cancellations and improve room utilization
- Provide actionable insights through dynamic visuals and drillthroughs

---

## 🗂️ Dataset Description
The dataset is a synthetic file created for educational and portfolio purposes with 200+ records. It includes the following fields:

| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| Booking_ID          | Unique booking identifier                        |
| Hotel_Name          | Name of the hotel branch                         |
| Check_In_Date       | Guest check-in date                              |
| Check_Out_Date      | Guest check-out date                             |
| Room_Type           | Type of room booked (Standard, Deluxe, Suite)    |
| Guests              | Number of guests in the booking                  |
| Room_Rate           | Price per night                                  |
| Booking_Channel     | Source of booking (Website, Travel Agent, etc.)  |
| Status              | Booking status (Confirmed, Cancelled, No-show)   |
| Total_Amount        | Total revenue from the booking                   |
| Rooms_Available     | Rooms available during booking period            |

## Data Files 
- <a href = "https://github.com/Bharath-kumar4703/Hotel-Booking-Report-Using-Power-BI/blob/main/Hotel_Booking_Data.csv">Hotel_Booking_Data</a>
- <a href = "https://github.com/Bharath-kumar4703/Hotel-Booking-Report-Using-Power-BI/blob/main/Power%20BI%20Report">Report</a>

---

## 🔧 DAX Measures Used
DAX
Total Revenue = SUM(Hotel_Booking_Data[Total_Amount])

ADR = DIVIDE(SUM(Hotel_Booking_Data[Total_Amount]), COUNTROWS(FILTER(Hotel_Booking_Data, Hotel_Booking_Data[Status] = "Confirmed")))

RevPAR = DIVIDE([Total Revenue], SUM(Hotel_Booking_Data[Rooms_Available]))

Occupancy Rate = DIVIDE(COUNTROWS(FILTER(Hotel_Booking_Data, Hotel_Booking_Data[Status] = "Confirmed")), SUM(Hotel_Booking_Data[Rooms_Available]))

Max Stay Duration = MAX(Hotel_Booking_Data[Staying_Column])

📈 Dashboard Features
•	Trend Analysis: Monthly Revenue & Occupancy Rate
•	Branch Performance: Revenue and bookings by hotel
•	Booking Source: Channel-wise booking distribution
•	Drillthrough Pages: Hotel-specific performance view
•	Cancellation Insight: Track cancellation rates and patterns
•	Stay Duration: Max stay duration by guests
________________________________________
🧠 Skills Demonstrated
•	Power BI Desktop Dashboard Design
•	DAX Calculations and Time Intelligence
•	Data Modeling and Relationships
•	Drillthrough and Interactive Filters
•	Storytelling with Data
________________________________________
🧰 Tools & Technologies
•	Power BI Desktop
•	Microsoft Excel (for data preparation)
•	DAX (Data Analysis Expressions)
________________________________________
🚀 How to Use
1.	Clone this repository or download the files.
2.	Open the .pbix file in Power BI Desktop.
3.	Explore the interactive visuals and analyze hotel booking insights.
4.	Customize or connect to your own dataset if needed.

---


## 📌 Key Insights from the Hotel Booking Report
1. ✅ Total Number of Bookings
A total of 200 hotel bookings were recorded across all branches in the dataset.

2. 👥 Guest Volume
The hotel hosted a total of 483 guests, with an average of ~2.42 guests per booking.

3. 💰 Total Revenue Generated
The hotel earned approximately ₹23,600 from confirmed bookings.

Bookings with Cancelled or No-show status contributed ₹0, leading to potential revenue loss.

4. 📉 Booking Cancellations and No-Shows
33 bookings were either cancelled or marked as no-show, accounting for 16.5% of all bookings.

This represents a significant risk to revenue realization.

5. 🏨 Top Performing Hotel Branch (by bookings)
The branch with the most bookings is likely to be Grand Palace (verify using COUNT of Hotel_Name).

You can highlight this using a bar chart in Power BI.

6. 🛏️ Room Type Popularity
Standard rooms are booked most frequently, followed by Deluxe and Suite rooms.

Useful insight for inventory management and pricing strategy.

7. 🌐 Booking Channels Overview
Majority of bookings come from Travel Agent and Website, indicating strong external partnerships.

You can show this in a donut or bar chart for clear comparison.

8. 🧾 Average Daily Rate (ADR)
ADR = Total Revenue / Total Nights Stayed
(Calculate using Power BI DAX after creating Nights_Stayed column)

This metric helps track pricing efficiency per night.

9. 📅 Peak Stay Durations
Some bookings have stay durations up to 5 days.

The average stay duration is likely around 2–3 nights, indicating most guests are short-term visitors.

10. 🛑 Rooms Not Fully Utilized
Despite 40–100 rooms being available daily, the Occupancy Rate (Bookings / Rooms Available) can be below optimal.

This indicates opportunities to boost promotions or improve booking conversion.





