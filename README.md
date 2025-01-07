
# Data preparation and customer analytics Experimentation and uplift testing Analytics

## Table of Contents
1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Step-by-Step Explanation](#step-by-step-explanation)
4. [Data Description](#data-description)
5. [Libraries Used](#libraries-used)
6. [Visualizations and Insights](#visualizations-and-insights)
7. [Recommendations](#recommendations)
8. [Support and Resources](#support-and-resources)
9. [License](#license)

---

## Introduction

In this project, we aim to analyze and segment customer purchase behavior to better understand the key drivers of sales. The analysis will also uncover customer preferences, helping businesses optimize their product offerings and marketing strategies.

---

## Project Overview

The primary objective of this project is to clean, merge, and analyze transaction and customer data to identify the following:

- Missing values, duplicates, and outliers in the datasets.
- Customer segmentation based on demographics like `LIFESTAGE` and `PREMIUM_CUSTOMER`.
- Sales trends over time and analysis of sales drivers.
- Identification of customer preferences based on packet size.

---

## Step-by-Step Explanation

### 1. Data Loading
We begin by loading two datasets:
- `QVI_transaction_data.csv`: Contains customer transaction details.
- `QVI_purchase_behaviour.csv`: Contains customer demographics and purchase behavior.

### 2. Exploring the Data
We explore the datasets to check for:
- Missing values and perform necessary imputation.
- Inspect the first few rows of each dataset to understand its structure.

### 3. Checking for Duplicates
We identify any duplicate rows in both datasets and remove them if necessary to ensure data integrity.

### 4. **Handling Outliers**
We visualize the total sales distribution using a boxplot and use Z-scores to filter out extreme outliers in the sales data.

### 5. Merging Data
We merge the transaction data with customer data on the `LYLTY_CARD_NBR` field to enrich the transaction data with customer demographics.

### 6. Customer Segmentation
We segment customers by `LIFESTAGE` and `PREMIUM_CUSTOMER` to analyze their total sales contributions. A bar plot visualizes the sales distribution across customer segments.

### 7. Analyzing Sales Drivers
We explore the trend of total sales over time by grouping the transaction data by month. A line plot is used to visualize the sales trend.

### 8. Analyzing Packet Size Trends
We analyze the relationship between product quantity (`PROD_QTY`) and total sales to identify preferred packet sizes.

### 9. Insights and Recommendations
Based on the data analysis and visualizations, we provide actionable insights into customer behavior and sales drivers.

---

## Data Description

- QVI_transaction_data.csv: Contains transaction information such as total sales (`TOT_SALES`), product quantity (`PROD_QTY`), and transaction date (`DATE`).
- QVI_purchase_behaviour.csv: Contains customer demographics and purchase behavior, including `LIFESTAGE`, `PREMIUM_CUSTOMER`, and `LYLTY_CARD_NBR` (loyalty card number).

---

## Libraries Used

This project makes use of the following Python libraries:

- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations and handling of arrays.
- `matplotlib`: For visualizing the data using charts and graphs.
- `seaborn`: For advanced data visualization with a higher-level interface.
- `scipy`: For statistical functions, including Z-score to detect outliers.

---

## Visualizations and Insights

### Sales Trend Over Time

![Sales Trend](./sales_trend.png)

Insight: The total sales have seen steady growth in recent months, with certain peaks that may be linked to promotional activities.

### Customer Segmentation by Lifestage

![Customer Segments](./customer_segments.png)

Insight: Premium customers in the 'OLDER FAMILIES' lifestage contribute significantly to total sales, suggesting a potential target group for marketing campaigns.

### Sales by Packet Size

![Packet Size Sales](./packet_size_sales.png)

Insight: The most popular packet size is 3, which indicates a consumer preference for smaller portion sizes. This could inform future packaging strategies.

---

## Recommendations

- Targeting Premium Customers: Focus on the 'OLDER FAMILIES' demographic for premium offers and personalized marketing campaigns.
- Optimizing Product Packaging: Given the preference for smaller packet sizes, consider offering more 3-pack options to cater to customer needs.
- Sales Promotions: Use insights from the sales trend analysis to plan promotions around peak sales periods.

---

## Support and Resources

If you have any questions or need support regarding this project, please reach out via the Issues section on this repository.

For further learning, you can explore the following resources:

- [Pandas Documentation](https://pandas.pydata.org/pandas-docs/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Seaborn Documentation](https://seaborn.pydata.org/)

