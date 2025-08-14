# 📊 Zomato Order and Restaurant Analysis – Power BI Dashboard

## 📌 Dashboard Overview
This Power BI project analyzes Zomato's restaurant and order data to generate actionable insights into customer preferences, restaurant performance, pricing strategies, and location-based patterns.

**Dataset:** `ZOMATO`

---

## **KPI Summary**
- **Total Revenue:** ₹15.57 Million  
```dax
-- 🆕 New Measure
Total Revenue =
SUM('ZOMATO'[total_cost])
```
- **Total Orders:** 15,000  
```dax
-- 🆕 New Measure
Total Orders =
COUNTROWS('ZOMATO')
```
- **Average Order Value:** ₹1.04 Thousand  
```dax
-- 🆕 New Measure
Average Order Value =
DIVIDE([Total Revenue], [Total Orders], 0)
```
- **Average Customer Rating:** 3.00  
```dax
-- 🆕 New Measure
Average Customer Rating =
AVERAGE('ZOMATO'[customer_rating])
```
- **Average Delivery Time:** 52.39 minutes  
```dax
-- 🆕 New Measure
Average Delivery Time =
AVERAGE('ZOMATO'[delivery_time])
```
- **Active Restaurants:** 500  
```dax
-- 🆕 New Measure
Active Restaurants =
DISTINCTCOUNT('ZOMATO'[restaurant_id])
```

---

## **Chart 1 – Count of City, First City, and First Area by Restaurant ID**
- **Chart Type:** Column Chart  
- **Dataset:** `ZOMATO`  
- **X-Axis:** Count of City  
- **Y-Axis:** Restaurant ID  
- **Insight:** Shows how restaurants are distributed geographically, highlighting regions with high restaurant density.

---

## **Chart 2 – Count of Order ID, Sum of Delivery Time, and Sum of Total Cost by City**
- **Chart Type:** Clustered Column Chart  
- **Dataset:** `ZOMATO`  
- **Legend:** City  
- **Values:** Count of Order ID, Sum of Delivery Time, Sum of Total Cost  
```dax
-- 🆕 New Measure
Count of Orders =
COUNT('ZOMATO'[order_id])

Sum of Delivery Time =
SUM('ZOMATO'[delivery_time])

Sum of Total Cost =
SUM('ZOMATO'[total_cost])
```
- **Insight:** Compares order volume, delivery time, and revenue per city to identify high-performing and underperforming areas.

---

## **Chart 3 – Sum of Total Cost, Sum of Item Count, Count of Total Ratings, and First Payment Method by City**
- **Chart Type:** Clustered Column Chart  
- **Dataset:** `ZOMATO`  
- **X-Axis:** City  
- **Values:** Sum of Total Cost, Sum of Item Count, Count of Total Ratings  
```dax
-- 🆕 New Measures
Sum of Item Count =
SUM('ZOMATO'[item_count])

Count of Total Ratings =
COUNT('ZOMATO'[total_ratings])
```
- **Tooltip:** Payment Method  
- **Insight:** Helps analyze sales, order size, customer feedback, and preferred payment methods per city.

---

## **Chart 4 – Average Delivery Time and Average Customer Rating by MonthYear**
- **Chart Type:** Combo Chart (Line + Column)  
- **Dataset:** `ZOMATO`  
- **X-Axis:** MonthYear  
- **Column Values:** Avg Delivery Time  
- **Line Values:** Avg Customer Rating  
```dax
-- 🆕 New Column
MonthYear =
FORMAT('ZOMATO'[order_date], "MMM YYYY")
```
- **Insight:** Tracks how delivery speed and customer ratings change over time.

---

## **Chart 5 – Total Orders and Total Revenue by MonthYear**
- **Chart Type:** Combo Chart (Line + Column)  
- **Dataset:** `ZOMATO`  
- **X-Axis:** MonthYear  
- **Column Values:** Total Orders  
- **Line Values:** Total Revenue  
- **Insight:** Highlights monthly sales trends and seasonal order patterns.

---

## **Chart 6 – Total Orders and Total Revenue by City**
- **Chart Type:** Clustered Column Chart  
- **Dataset:** `ZOMATO`  
- **X-Axis:** City  
- **Values:** Total Orders, Total Revenue  
- **Insight:** Compares the business contribution of each city in terms of volume and value.

---

## **Chart 7 – Area Count by City**
- **Chart Type:** Column Chart  
- **Dataset:** `ZOMATO`  
- **X-Axis:** City  
- **Y-Axis:** Area Count  
```dax
-- 🆕 New Measure
Area Count =
DISTINCTCOUNT('ZOMATO'[area])
```
- **Insight:** Shows the number of distinct service areas covered in each city.

---

## **Chart 8 – Average Order Value by Restaurant**
- **Chart Type:** Table Visualization  
- **Dataset:** `ZOMATO`  
- **Values:** Restaurant Name, Order ID, Avg Order Value, Sum of Total Cost  
- **Insight:** Identifies restaurants with the highest average bill size for revenue optimization.

---

## **Chart 9 – Delivery Time and Ratings Summary by City**
- **Chart Type:** Table Visualization  
- **Dataset:** `ZOMATO`  
- **Values:** Sum of Delivery Time, Count of Total Ratings  
- **Insight:** Helps in understanding how delivery time impacts customer engagement in each city.

---

## 📥 Dashboard PDF
[📄 Click here to view the full dashboard (PDF)](https://github.com/sathishkumarj03/zomato-order-and-restaurant-analysis/raw/main/My%20Resume.pdf)  
*(Replace `your-username` with your GitHub username and update file name if changed)*

---

## 👨‍💻 Created by
**Sathish** – Power BI & SQL Developer

