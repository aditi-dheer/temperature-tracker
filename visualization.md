# 📊 Visualizing Temperature Data

## Overview

This dashboard visualizes **real-time temperature updates** for New York City using **Streamlit** and **Plotly**. It retrieves temperature data stored in a MongoDB collection and displays the data in a time-series line chart, updated every 10 seconds. The chart shows temperature fluctuations over time and provides an interactive way to track changes in the weather.

---

## 📈 Visualization

The visualization is powered by **Streamlit**, **Plotly**, and **MongoDB**. The dashboard provides a real-time view of the last 10 temperature readings and updates every 10 seconds to simulate real-time data trends.

---

## 🛠️ How It Works

1. **Data Ingestion**  
   The script continuously calls the `ingest_data()` function to insert mock temperature data into the MongoDB collection.

2. **Data Retrieval**  
   It retrieves the most recent 10 temperature records from the MongoDB collection using a query that sorts by the `_id` field in descending order.

3. **Data Processing**  
   The data is loaded into a **Pandas DataFrame**, and the timestamp field is converted to a datetime format for proper plotting.

4. **Plot Creation**  
   A **Plotly line chart** is created, showing temperature over time, with markers indicating the individual data points.

5. **Real-time Updates**  
   The chart is updated every 10 seconds, providing a near-real-time view of the temperature data.

---

## View Dashboard

[View the live dashboard here](https://aditi-dheer-temperature-dashboard-visualization-98ddjs.streamlit.app/)

## 🧑‍💻 Code

The visualization is generated by the `visualization.py` script. This script does the following:
- Sets up the Streamlit app with a real-time update loop.
- Fetches the latest data from MongoDB and generates a Plotly chart.
- Displays the chart in the Streamlit interface with continuous updates every 10 seconds.
