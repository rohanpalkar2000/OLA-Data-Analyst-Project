# OLA-Data-Analyst-Project

#### **Project Overview**
This project involves analyzing booking data from OLA rides in Mumbai over a period of one month. The analysis covers metrics such as booking statuses, ride distances, cancellation reasons, payment methods, customer and driver ratings, and revenue generation. Insights are visualized using **Power BI** and queried through **SQL**.


#### **Project Objectives**
1. Perform detailed data analysis to uncover trends in booking statuses, ride volumes, cancellations, and revenue generation.
2. Create visualizations for business insights, including ride volume trends, revenue breakdown, and customer behavior.
3. Use SQL to extract specific insights for further analysis and reporting.


#### **Dataset Description**
The dataset comprises 100,000 records with the following key columns:
1. **Date** and **Time** of booking.
2. **Booking ID**, **Booking Status**, and **Customer ID**.
3. **Vehicle Type**: Includes Auto, Prime Plus, Prime Sedan, Mini, Bike, eBike, Prime SUV.
4. **Pickup** and **Drop Locations**: Based on 50 dummy areas.
5. **Ride Metrics**:
   - VTAT (Vehicle Time to Arrival)
   - CTAT (Customer Time to Arrival)
   - Ride Distance
6. **Cancellation Data**:
   - Reasons for cancellations by drivers and customers.
7. **Ratings**:
   - Customer and Driver Ratings.
8. **Payment Methods**: Cash, UPI, Credit Card, Debit Card.
9. **Revenue Metrics**:
   - Booking Value and Cancellation Rates.

#### **Analysis Performed**
1. **SQL Analysis**:
   - Retrieve successful bookings.
   - Analyze average ride distance per vehicle type.
   - Identify top 5 customers by booking value and ride count.
   - Summarize cancellation reasons for drivers and customers.
   - Calculate total booking value of successful rides.

2. **Power BI Analysis**:
   - Visualize booking status breakdown.
   - Identify top 5 vehicle types by ride distance.
   - Evaluate customer and driver ratings.
   - Analyze revenue by payment methods.
   - Ride distance distribution across days.

#### **Key Insights**
- **Booking Status Breakdown**: 
  - 61.9% success rate, with a 24.94% cancellation rate.
- **Revenue Analysis**: 
  - Majority of revenue comes from cash and UPI payments.
- **Ride Volumes**: 
  - Higher volumes observed on weekends and specific match days.
- **Top Customers**: 
  - Identified top 5 contributors to booking value.
- **Cancellations**:
  - Major reasons include changes in plans (customers) and personal issues (drivers).

#### **Steps to Replicate**
1. **Data Preparation**:
   - Use the structured dataset to create a relational database.
   - Upload data to Power BI for visualization.

2. **SQL Queries**:
   - Use provided SQL scripts for querying insights.

3. **Power BI Dashboard**:
   - Recreate the dashboard using given visuals and measures.

#### **Files**
- **SQL Scripts**: Queries for analysis and reporting.
- **Power BI Dashboard**: Includes visuals for detailed insights.


## **ScreenShot**
![Overall](https://github.com/user-attachments/assets/a7612931-615a-4363-aa79-164ccd33f965)
![Vehicle Type](https://github.com/user-attachments/assets/35580d10-649d-4492-8eca-5eaf7f29f100)
![Revenue](https://github.com/user-attachments/assets/b3ba5f2f-4f9d-4f61-8c8f-341f31c59243)
![Cancellation](https://github.com/user-attachments/assets/0d188012-1919-4372-a6fe-fea891e9d777)
![Ratings](https://github.com/user-attachments/assets/fb746328-ca3f-4d9b-93ae-2fb4163372c2)
