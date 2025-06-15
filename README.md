# Superstore-Sales-Analysis-and-Forecasting-PowerBI-Dashboard
# Superstore Sales Analysis and Forecasting

![cashier-and-customer-with-grocery-trolley-and-basket-at-supermarket-checkout-counter-illustration-vector](https://github.com/user-attachments/assets/6548ccd1-cacb-404f-a152-5f9a80c0f5f0)

## Introduction

In the modern business environment, leveraging data for decision-making is more critical than ever. The Superstore Sales Analysis and Forecasting project harnesses data analytics to identify trends, patterns, and valuable insights within a sales dataset. Through advanced analytics and visualization, this project helps stakeholders understand past sales performance and predict future sales trends.

## Process

### Data Preparation

1. **Data Cleaning:** Initial tasks involved addressing data quality by removing null values, eliminating unnecessary columns, handling duplicates, and adjusting data types.

### Data Modeling

2. **Calculated Measures and Tables:** We used DAX (Data Analysis Expressions) in Power BI to enhance the dataset's analytical capabilities.

   ```dax
   # Created time-series table of sales for forecasting.
   TimeSeriesTable = 
   SUMMARIZE(
     SuperStore_Sales_Dataset,
     SuperStore_Sales_Dataset[Order Date],
     "Total Sales", SUM(SuperStore_Sales_Dataset[Sales])
   )  

   # Calculate a measure to determine the number of days it took for delivery.
   DaysToDeliver = 
   DATEDIFF(
     SuperStore_Sales_Dataset[Order Date],
     SuperStore_Sales_Dataset[Ship Date],
     DAY
   )
   ```

### Data Analysis

3. **Visualization:** After modeling, we conducted in-depth analysis in Power BI using various visualization techniques such as matrices to identify sales trends by region, category, and other factors.

### Dashboard Creation

4. **Interactive Dashboard:** We developed a dynamic dashboard in Power BI featuring bookmarks for easy navigation between charts and visualizations, offering a comprehensive view of the data.

### Sales Forecasting

5. **Forecasting:** We used Power BI's advanced forecasting feature to predict sales for the next 10 days, providing insights into future trends.

## Dashboard

The dashboard features a range of visualizations to explore historical sales data, including:

- Monthly and yearly sales trends
- Sales comparison across categories and sub-categories
- Geographical distribution of sales
- Insights into top payment modes, segments, shipping modes, and more

![Dashboard Screenshot](https://github.com/AakankshaLanghani/Super-Store-Sales-and-Forecast-Dashboard-PowerBI/blob/main/Super%20Store%20Sales%20Dashboard.jpg)


## Sales Forecasting
![Dashboard Screenshot](https://github.com/AakankshaLanghani/Super-Store-Sales-and-Forecast-Dashboard-PowerBI/blob/main/Sales%20Forcast%20for%2015%20days.png)
### Forecasting Report

The forecasting page focuses on predicting sales for the upcoming 10 days using historical data and advanced forecasting techniques in Power BI.

## Key Insights

From the dashboard and forecasting report, the following insights are highlighted:

- **Monthly Peaks:** Sales spikes are observed in February, August, and October.
- **Parallel Growth:** Sales in 2020 exceeded 2019 figures, with consistent trends.
- **Geographic Leaders:** California and New York are the top sales regions.
- **Region Impact:** The West region is the largest contributor to sales.
- **Payment Preference:** Cash On Delivery (COD) is the most preferred payment method.
- **Consumer Segment:** The consumer segment generates the highest sales.
- **Top Category:** Office Supplies is the leading sales category.
- **Preferred Shipping:** Standard Class is the most popular shipping choice.
- **Sub-Category Stars:** Phones and chairs are top-selling sub-categories.

## Tech Stack

This project utilizes the following technologies:

- **Power BI Desktop:** For design, visualization, and interactive reporting.
- **DAX (Data Analysis Expressions):** For creating calculations and measures.
- **Advanced Analytics:** For forecasting future sales trends.
- **Power Query:** For cleaning and transforming raw data.

## Files Information

### Data

- **SuperStore Processed Data:** Contains cleaned and processed data.
- **Sales TimeSeries:** Includes a time-series table created using DAX for forecasting.

### Results

- **Dashboard:** Features interactive dashboard and forecasting report.

## Data Source

The Superstore Sales Data used in this project can be accessed here: https://drive.google.com/drive/folders/1t_r26xUjm5ZyEFFOF3AD1BmOvUgQaxd1

## License

This project is licensed under the MIT License. You are free to use, modify, and distribute the code and visuals, provided that the original license terms are maintained.

Enjoy exploring the Power BI Sales Insights and Forecasting Dashboard!
