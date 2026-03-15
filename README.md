# FinTech-Analytics-Dashboard-Project
Overview

This project presents an interactive FinTech Transaction Analytics Dashboard built using Google Looker Studio with data prepared in Google Spreadsheets.
The dashboard analyzes digital payment transactions to monitor key business metrics, merchant performance, payment behavior, and geographic transaction distribution.


Tools & Technologies

Google Looker Studio
Google Spreadsheets


The dataset contains the following attributes:

transaction_id
customer_id
merchant_name
merchant_category
transaction_amount
payment_method
transaction_date
city
device_type
transaction_status

Steps to Build the Dashboard

Imported the dataset into Google Spreadsheets and validated column data types.
Connected the dataset to Google Looker Studio.
Created KPI scorecards to monitor core metrics:
Total Transactions
Total Revenue
Average Transaction Value
Transaction Success Rate
Unique Customers
Active Merchants

Built visualizations for transaction analysis:

Transaction volume trend over time
Revenue by merchant category
Payment method distribution
Top merchants by revenue
Transaction success vs failure rate
Transaction distribution by city

Added interactive filters for better exploration:

City
Payment Method
Merchant Category
Device Type
Date Range
Designed the dashboard layout including KPIs, charts, filters, and a key insights section.

Important Calculations

Total Transactions
COUNT(transaction_id)

Total Revenue
SUM(transaction_amount)

Average Transaction Value
AVG(transaction_amount)

Transaction Success Rate
SUM(CASE WHEN transaction_status = "Success" THEN 1 ELSE 0 END)
/ COUNT(transaction_id)

Unique Customers
COUNT_DISTINCT(customer_id)

Active Merchants
COUNT_DISTINCT(merchant_name)


Dashboard Features

KPI monitoring for transaction performance
Time-series analysis of transaction trends
Merchant category revenue comparison
Payment method usage insights
Identification of top revenue-generating merchants
Geographic transaction visualization
Interactive filters for deeper analysis

Key Insights

UPI is the most frequently used payment method.
Shopping category generates the highest transaction revenue.
Transaction success rate is above 94%.
Metro cities contribute the majority of digital payment transactions.

Project Structure
FinTech-Transaction-Dashboard
│
├── data
│   └── fintech_transactions_dataset.csv
│
├── dashboard
│   └── dashboard.pdf
│
└── README.md

Dashboard Preview
https://lookerstudio.google.com/reporting/2ea1ea1f-12ed-4d7a-b92a-6a1ac635f0cf


