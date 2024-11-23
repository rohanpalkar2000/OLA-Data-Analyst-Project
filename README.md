# OLA-Data-Analyst-Project

### **Project Overview**
This project involves analyzing booking data from OLA rides in Mumbai over a period of one month. The analysis covers metrics such as booking statuses, ride distances, cancellation reasons, payment methods, customer and driver ratings, and revenue generation. Insights are visualized using **Power BI** and queried through **SQL**.

---

### **Project Objectives**
1. Perform detailed data analysis to uncover trends in booking statuses, ride volumes, cancellations, and revenue generation.
2. Create visualizations for business insights, including ride volume trends, revenue breakdown, and customer behavior.
3. Use SQL to extract specific insights for further analysis and reporting.

---

### **Dataset Description**
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

---

### **Analysis Performed**
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

---

### **Key Insights**
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

---

### **Steps to Replicate**
1. **Data Preparation**:
   - Use the structured dataset to create a relational database.
   - Upload data to Power BI for visualization.

2. **SQL Queries**:
   - Use provided SQL scripts for querying insights.

3. **Power BI Dashboard**:
   - Recreate the dashboard using given visuals and measures.

---

### **Dataset Description**
The dataset contains the following key columns:
- **Booking_Status**: Status of each booking (e.g., Success, Cancelled).
- **Vehicle_Type**: Type of vehicle (e.g., Prime Sedan, Mini).
- **Ride_Distance**: Distance covered in each ride.
- **Customer_ID**: Unique identifier for customers.
- **Booking_ID**: Unique identifier for bookings.
- **Driver_Ratings**: Ratings provided by customers for drivers.
- **Cancelled_Rides_by_Driver**: Reasons for cancellation by drivers.



### **SQL Query List**

1. **Retrieve All Successful Bookings**  
   **Query**:  
   ```sql
   SELECT * FROM bookings WHERE Booking_Status = 'Success';
   ```  
   **Description**: This query retrieves all records where the booking status is marked as "Success."  
   **Use Case**: Analyze completed rides for revenue generation and customer satisfaction metrics.

2. **Find the Average Ride Distance for Each Vehicle Type**  
   **Query**:  
   ```sql
   SELECT Vehicle_Type, AVG(Ride_Distance) as avg_distance FROM bookings GROUP BY Vehicle_Type;
   ```  
   **Description**: Calculates the average distance covered by each type of vehicle.  
   **Use Case**: Identify vehicle types suitable for long-distance trips.

3. **Get the Total Number of Cancelled Rides by Customers**  
   **Query**:  
   ```sql
   SELECT COUNT(*) FROM bookings WHERE Booking_Status = 'cancelled by Customer';
   ```  
   **Description**: Counts the total number of bookings cancelled by customers.  
   **Use Case**: Understand cancellation patterns to improve customer experience.

4. **List the Top 5 Customers Who Booked the Highest Number of Rides**  
   **Query**:  
   ```sql
   SELECT Customer_ID, COUNT(Booking_ID) as total_rides FROM bookings GROUP BY Customer_ID ORDER BY total_rides DESC LIMIT 5;
   ```  
   **Description**: Retrieves the top 5 customers based on the number of rides booked.  
   **Use Case**: Reward loyal customers and create targeted marketing strategies.

5. **Get the Number of Rides Cancelled by Drivers Due to Personal and Car-Related Issues**  
   **Query**:  
   ```sql
   SELECT COUNT(*) FROM bookings WHERE cancelled_Rides_by_Driver = 'Personal & Car related issue';
   ```  
   **Description**: Counts rides cancelled by drivers citing personal or car-related issues.  
   **Use Case**: Address operational inefficiencies and driver-related challenges.

6. **Find the Maximum and Minimum Driver Ratings for Prime Sedan Bookings**  
   **Query**:  
   ```sql
   SELECT MAX(Driver_Ratings) as max_rating, MIN(Driver_Ratings) as min_rating FROM bookings WHERE Vehicle_Type = 'Prime Sedan';
   ```  
   **Description**: Identifies the range of driver ratings for Prime Sedan rides.  
   **Use Case**: Monitor driver performance and maintain quality standards.

---

### **Files**
- **SQL Scripts**: Queries for analysis and reporting.
- **Power BI Dashboard**: Includes visuals for detailed insights.

---

## **ScreenShot**
![Overall](https://github.com/user-attachments/assets/e680d397-d6be-485e-a7dd-af9604978f33)
![Vehicle Type](https://github.com/user-attachments/assets/a2a5fbfb-ed90-46af-b104-d8f949af3e50)
![Revenue](https://github.com/user-attachments/assets/3ccabcbf-eab4-449c-b5fb-61804a34cd95)
![Cancellation](https://github.com/user-attachments/assets/41ee6565-135a-45fe-9563-c57c2179b771)
![Ratings](https://github.com/user-attachments/assets/91bec62d-4d1f-4b06-b70f-fbb6fd749630)



