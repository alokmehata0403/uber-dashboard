# uber-dashboard
📌 Project Overview
This repository contains an end-to-end business intelligence (BI) solution that analyzes key ride-hailing metrics. The interactive dashboard evaluates transactional ride data to generate actionable insights across demand patterns, fleet utilization, pickup/drop-off route efficiency, and revenue streams.

Key objectives include:

Ride Demand & Peak Time Analysis: Identifying high-volume pickup locations and peak hours to optimize driver distribution.

Revenue & Fare Tracking: Analyzing gross booking values, average fare per trip, commission cuts, and breakdown by payment methods (UPI, Cards, Cash, Uber Wallet).

Cancellation Diagnostics: Evaluating driver-initiated vs. customer-initiated cancellations to reduce supply-demand gaps.

Vehicle Tier Performance: Comparing metrics across ride categories (Auto, Go Mini, Go Sedan, Premier, UberXL).

💾 Data Source & Dataset Info
The data used in this project is sourced from publicly available/simulated ride-hailing transactional logs:

Primary Dataset Source: Kaggle - Uber Request Data / Uber City Rides Dataset (or synthetic ride-hailing data generated to mirror real-world ride-share operational logs).

Dataset Volume: ~120,000+ transactional ride records.

Key Fields Included: Booking_ID, Booking_Date, Booking_Time, Booking_Status (Success, Cancelled by Driver, Cancelled by Customer), Vehicle_Type, Pickup_Location, Drop_Location, V_TAT (Vehicle Arrival Time), C_TAT (Customer Wait Time), Booking_Value, Payment_Method, Customer_Rating, Driver_Rating.

🛠️ Data Architecture & Modeling
The project leverages a structured star-schema data model built with DAX calculations and relational schema layouts:

Fact Table: Core ride booking records including timestamps, pickup/drop coordinates, trip distance, fare breakdown, and booking status (Completed, Cancelled).

Dimension Tables: Date/time hierarchies, vehicle category mappings, pickup/drop-off location tables, and driver/customer details.

Custom DAX Measures: Advanced calculations for completion rates, customer/driver cancellation percentages, average trip durations (CTAT), pickup lead times (VTAT), and rolling revenue growth.

📊 Dashboard Key Features & Pages
The Power BI report (.pbix) is structured across targeted report pages:

1. Executive Operations & Revenue Summary
High-level KPI cards highlighting Total Bookings, Completed Trips, Gross Revenue, Average Fare, and Overall Cancellation Rate.

Dynamic trend lines showing daily, weekly, and monthly ride volume growth.

2. Fleet & Vehicle Tier Breakdown
Vehicle performance visualizer comparing booking volume, success rate, and average trip distance across vehicle categories (Go Sedan, Auto, UberXL, etc.).

Revenue share breakdown by payment types.

3. Supply, Demand & Cancellation Analytics
Hourly heatmap identifying peak demand hours and driver availability bottlenecks.

Cancellation breakdown visuals highlighting top customer reasons (e.g., driver not moving, wrong address) and driver reasons (e.g., capacity, car issues).

4. Customer & Driver Ratings Analysis
Rating distribution matrix tracking driver satisfaction ratings vs. customer feedback scores.

🛠️ Built With
Power BI / DAX: Interactive dashboard development, data modeling, and custom measures.

Power Query (M): Data cleaning, null handling, data type transformations, and custom column logic.

![Dashboard Preview](https://github.com/alokmehata0403/uber-dashboard/blob/main/uber.png.png)
