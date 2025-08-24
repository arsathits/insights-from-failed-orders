# 🧠 Insights from Failed Orders – Data Analysis Project

This project explores the causes and patterns behind failed ride-hailing orders on the Gett platform. The dataset simulates real-world operational data from a corporate transportation service and was provided as a take-home assignment by Stratascratch to assess data science problem-solving and communication skills.

---

## 📌 Objective

To analyze failed ride orders in order to understand:
- When and why failures occur (client cancellations vs. system rejections)
- How driver assignment and ETA impact cancellation behavior
- Temporal trends across the day
- Potential areas for operational improvement

---

## 📂 Data Overview

We used two datasets:

- `data_orders.csv`: includes timestamps, coordinates, ETA estimates, order status, cancellation time, and whether a driver was assigned.
- `data_offers.csv`: maps orders to offers, indicating whether a driver was matched.

A failed order is defined as one that was either cancelled by the client or rejected by the system.

---

## 📊 Analysis & Key Visualizations

### 1. **Failure Type by Driver Assignment**
This visualization breaks down failures by type (client cancellation or system rejection) and whether a driver was assigned.

🔍 **Insight:**  
The majority of failures are **client cancellations before a driver is assigned**, indicating potential issues with estimated wait times or app experience.

---

### 2. **Failed Orders by Hour**
This chart shows the hourly distribution of all failed orders.

🔍 **Insight:**  
Failures spike during **morning (08:00–09:00)** and **evening (21:00–23:00)** peak times, aligning with high-demand periods and potential traffic congestion.

---

### 3. **Failure Categories by Hour**
Orders were further segmented into failure categories by hour of the day.

🔍 **Insight:**  
- **Client cancellations without driver assignment** dominate during late evening hours.
- **System rejections** increase in the morning, likely due to driver unavailability.

---

### 4. **Average ETA by Hour**
This plot shows how the estimated time of arrival (ETA) changes throughout the day.

🔍 **Insight:**  
ETAs are highest during **06:00–09:00**, which may lead to increased user cancellations due to long wait times. Optimizing ETA during these hours could improve completion rates.

---

### 5. **Average Cancellation Time by Hour and Driver Status**
We visualized the average time (in seconds) before cancellation, separated by whether a driver had been assigned.

🔍 **Insight:**  
- Users cancel **faster** when no driver is assigned.
- When a driver is assigned, users tend to wait longer before cancelling — suggesting either hope for arrival or frustration due to delays.

---

## 📌 Key Takeaways

- **Most failures happen before driver assignment**, especially due to user cancellations — indicating opportunity for better ETA estimates or faster matching.
- **System rejections** are more common during **morning rush hours**, likely due to limited driver availability.
- **Evening failures** are largely user-driven and may be addressed through improved communication, incentives, or in-app design.
- **Long ETAs** correlate with cancellations — reducing or better communicating ETA could reduce failure rates.

---

## 🛠️ Tools Used

- Python (Pandas, NumPy)
- Data Visualization: Matplotlib, Seaborn
- Jupyter Notebook
- Geospatial (optional): Folium, H3 (for bonus hex map analysis)

---
