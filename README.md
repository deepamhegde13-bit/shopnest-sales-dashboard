# 📊 ShopNest Sales & Operations Dashboard (Power BI)

## 📌 Project Overview

This project presents an interactive Power BI dashboard developed using the ShopNest e-commerce dataset. The dashboard analyzes sales performance, customer behavior, delivery performance, payment preferences, product ratings, and regional sales trends to support business decision-making.

---
## 🖼️ Dashboard Preview

### Executive Dashboard

![Executive Dashboard](Images/Executive_Dashboard.png)

---

### Order-Level Drill-Through Analysis

![Drill Through](Images/Drill_Through.png)

## 🎯 Business Objective

The objective of this project is to help business stakeholders:

- Monitor sales performance
- Identify top-performing product categories
- Analyze delayed vs on-time deliveries
- Understand customer payment preferences
- Evaluate regional sales performance
- Track sales trends over time
- Analyze customer ratings

---

## 📂 Dataset

The dashboard uses multiple related datasets including:

- Customers
- Orders
- Order Items
- Order Payments
- Product Categories
- Products
- Sellers
- Customer Reviews
- Geolocation

---

## 📅 Dataset Source and Reporting Period

### Dataset Source
This project uses the **Brazilian E-Commerce Public Dataset by Olist**, publicly available on Kaggle.

Source: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

The dataset contains related CSV files covering orders, customers, products, sellers, payments, customer reviews, and geolocation information for Brazilian e-commerce transactions.

### Reporting Period
The order purchase timestamps in the dataset range from September 2016 to October 2018. The dashboard includes yearly and quarterly sales trend analysis across this period.

### Data Preparation
The CSV files are organised in the repository's `Dataset` folder and loaded into Power BI Desktop. Power Query is used to connect to the source files and prepare the data for analysis.

---

## 🛠️ Tools & Technologies

- Power BI Desktop
- Power Query
- DAX
- Data Modeling
- DAX Measures

---

## 🔄 How to Open and Refresh the Dashboard

### Requirements
- Power BI Desktop installed on Windows.
- The repository's `Dataset` folder containing the required CSV files.
- The `ShopNest Sales & Operations Dashboard.pbix` file.

### Open the Dashboard
1. Download or clone this repository to your computer.
2. Open `ShopNest Sales & Operations Dashboard.pbix` using Power BI Desktop.
3. If Power BI prompts you to locate a data source, update the file paths to match the location of the downloaded repository and its `Dataset` folder.

### Refresh the Data
1. Confirm that the required CSV files are available in the `Dataset` folder.
2. In Power BI Desktop, open **Transform data → Data source settings** if the existing file paths need to be updated.
3. Update the source paths to the local CSV files, as required.
4. Select **Close & Apply** if you made changes in Power Query.
5. Select **Home → Refresh** to reload the data.
6. Review the report pages and visuals for any errors after refreshing.

**Note:** The PBIX file uses nine CSV data sources stored in the repository's `Dataset` folder. The source paths were updated and tested in Power BI Desktop, and the report loaded successfully with its existing visuals intact. If you download or clone the repository to a different location, check the data source paths and update them to point to the local `Dataset` folder before refreshing.

---

## 📊 Dashboard Metrics and Visual Definitions

### Sales Analysis
- **Top 10 Products:** Ranks product categories using the sum of the `price` field.
- **Sales by Quarter:** Shows quarterly sales trends across the reporting period.
- **Total Sales by Year:** Compares annual sales totals for 2016, 2017, and 2018.
- **Regional Sales:** Compares sales across Brazilian states.

Total Sales / Item-Price Value: Calculated as the sum of the price field in the Order_Items table (SUM(Order_Items[price])). This represents the total value of order items before freight charges; it should not be interpreted as net profit.

### Order and Delivery Analysis
- **Delayed Orders:** Displays delayed-order counts by product category. The visual shows a total of 6,535.
- **Late & On-Time Orders:** Compares monthly delayed and on-time order counts. The displayed totals are 6,535 delayed orders and 89,941 on-time orders.
- The dataset contains 99,441 distinct orders before report-level filtering: 6,535 classified as delayed (Orders delivered after the estimated delivery date), 89,941 as on time (Orders delivered on or before the estimated delivery date), and 2,965 with missing delivery dates (Orders for which the actual customer delivery date is unavailable).

**Business interpretation**: Most orders with available delivery dates were classified as on time. Orders with missing delivery dates are reported separately rather than automatically classified as delayed or on time, helping avoid misleading delivery-performance conclusions.

### Payment Type Analysis
The payment-type pie chart compares the distribution of payment records across payment methods. The `Frequent_Payment_Type` DAX measure uses `COUNT(Order_payments[payment_type])` to count non-blank payment-type entries.

The dashboard shows the following distribution:
- **Credit card:** 73.92%
- **Boleto:** 19.04%
- **Voucher:** 5.56%
- **Debit card:** 1.47%
- **Not defined:** 0%

**Business interpretation**: Credit card is the most frequently recorded payment type in the dataset, followed by boleto. This distribution describes payment records, not necessarily the percentage of unique orders or the share of total payment value.

### Product Rating Analysis
- **Lowest Rating Products:** Compares products or categories with lower displayed rating values.
- **Highest Rating Products:** Compares products or categories with higher displayed rating values.

**Interpretation note:** The values above are taken from the dashboard visuals. Their exact calculation methods depend on the Power BI measures, fields, relationships, and filters used in the report.

---

## 📊 Dashboard Features
- Interactive Filters
- Drill-through Navigation

### Executive Dashboard

- Top 10 Product Categories by Item-Price Value
- Delayed Orders Analysis
- On-Time vs Delayed Orders
- Regional Sales Performance
- Frequently Used Payment Methods
- Highest Rated Products
- Lowest Rated Products
- Quarterly Sales Trend
- Yearly Sales Trend

### Drill-Through Analysis

Detailed order-level analysis including:

- Order Status
- Product Category
- Order Date
- Delivery Performance

---

## 📈 Key Business Insights

- **Product Performance**: Product categories show different item-price totals, helping identify higher-performing categories.
- **Payment Preferences**: Credit card was the most frequently recorded payment type, accounting for 73.92% of payment-type records.
- **Delivery Performance**: The dashboard identifies product categories with higher delayed-order counts, highlighting areas for further logistics investigation.
- **Sales Trends**: Total item-price value increased from 2016 to 2018.
- **Product Ratings**: Ratings vary across products and categories, helping identify areas for potential customer-experience improvement.
- **Regional Performance**: São Paulo recorded the highest sales total among the Brazilian states shown in the dashboard.

---

## 📁 Repository Structure

```
shopnest-sales-dashboard/
│
├── README.md
├── ShopNest Sales & Operations Dashboard.pbix
├── Dataset/
│   ├── Customers.csv
│   ├── Geolocation.csv
│   ├── Order_items.csv
│   ├── Order_payments.csv
│   ├── Order_reviews.csv
|   ├── Orders.csv
│   ├── product_category_name_translation.csv
|   ├── Products.csv
│   └── Sellers.csv
└── Images/
    ├── Executive_Dashboard.png
    └── Drill_Through.png
```

---

## 🚀 Skills Demonstrated

- Data Cleaning
- Data Transformation
- Data Modeling
- DAX Calculations
- Dashboard Design
- Business Analysis
- KPI Reporting
- Data Visualization

---

## 👩‍💻 Author

**Deepa Hegde**

📧 deepamhegde13@gmail.com

💼 https://www.linkedin.com/in/deepamhegde
