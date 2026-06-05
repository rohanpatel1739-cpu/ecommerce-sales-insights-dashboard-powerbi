# 📊 E-Commerce Sales Insights Dashboard

## 📌 Project Overview

The E-Commerce Sales Insights Dashboard is an interactive Business Intelligence solution developed using Power BI to analyze sales performance, profitability, customer behavior, product performance, and regional trends.

This dashboard enables management teams to monitor key business KPIs, identify growth opportunities, evaluate customer segments, and make data-driven decisions.

---

## 🎯 Business Objectives

- Analyze overall sales and profit performance
- Monitor revenue growth trends
- Identify top-performing products
- Evaluate product profitability
- Understand customer segment contribution
- Analyze regional sales distribution
- Track delivery performance
- Support strategic business decisions

---

## 🛠️ Tools & Technologies Used

- Power BI
- Power Query
- DAX
- Data Modeling
- Data Visualization
- Business Intelligence

---

## 📂 Dataset Information

The dataset contains 1,000 e-commerce transactions including:

- Order Details
- Customer Information
- Product Information
- Sales Metrics
- Profit Metrics
- Payment Methods
- Shipping Information
- Delivery Status
- Customer Segments

### Key Columns

- Order ID
- Customer ID
- Order Date
- Product Category
- Product Name
- Quantity Sold
- Sales Amount
- Cost Amount
- Profit Amount
- Region
- Customer Segment
- Payment Method
- Delivery Status

---

## 📈 KPI Measures

### Total Sales

```DAX
Total Sales =
SUM(Fact_Sales[Sales Amount])
```

### Total Profit

```DAX
Total Profit =
SUM(Fact_Sales[Profit Amount])
```

### Total Orders

```DAX
Total Orders =
DISTINCTCOUNT(Fact_Sales[Order ID])
```

### Average Order Value

```DAX
AOV =
DIVIDE([Total Sales],[Total Orders])
```

### Profit Margin %

```DAX
Profit Margin % =
DIVIDE([Total Profit],[Total Sales])
```

### Revenue Growth %

```DAX
Revenue Growth % =
VAR CurrentMonth = [Total Sales]

VAR Previous_Month =
CALCULATE(
    [Total Sales],
    DATEADD('Date Table'[Date],-1,MONTH)
)

RETURN
DIVIDE(
    CurrentMonth-Previous_Month,
    Previous_Month
)
```

---

# 📊 Dashboard Pages

## Page 1 – Executive Overview

### Key Highlights

- Total Sales
- Total Profit
- Total Orders
- Average Order Value
- Profit Margin %
- Revenue Growth %
- Monthly Sales Trend
- Regional Sales Performance
- Category Analysis
- Payment Method Analysis
- Delivery Status Analysis

### Dashboard Preview

![Executive Overview](Images/dashboard_page1.png)

---

## Page 2 – Customer & Product Insights

### Key Highlights

- Top 10 Products by Sales
- Top 10 Products by Profit
- Customer Segment Analysis
- Sales vs Profit Analysis
- Top 10 Customers by Revenue

### Dashboard Preview

![Customer & Product Insights](Images/dashboard_page2.png)

---

# 🔍 Key Business Insights

### Revenue Analysis

- Electronics category contributes the highest revenue.
- Laptop is the highest-selling product.

### Profitability Analysis

- Laptop generates the highest profit contribution.
- High-sales products also show strong profitability.

### Regional Analysis

- West region contributes the highest sales volume.
- Regional sales distribution remains balanced across all regions.

### Customer Analysis

- Home Office and Corporate customers contribute significantly to revenue.
- A small group of customers generates a substantial portion of sales.

### Operational Analysis

- More than 75% of orders are successfully delivered.
- Digital payment methods dominate transaction volume.

---

# 📁 Project Structure

```text
E-Commerce-Sales-Insights-Dashboard/
│
├── Dataset/
│   └── ecommerce_sales_dataset_1000_rows.csv
│
├── Dashboard/
│   └── Ecommerce_Sales_Insights.pbix
│
├── Images/
│   ├── dashboard_page1.png
│   └── dashboard_page2.png
│
├── Reports/
│   └── Project_Report.docx
│
└── README.md
```

---

# 🚀 Outcome

This dashboard provides a comprehensive view of e-commerce business performance by combining sales analysis, profitability metrics, customer insights, and operational KPIs.

The solution demonstrates practical skills in:

- Data Cleaning
- Data Modeling
- DAX Calculations
- Dashboard Design
- Business Intelligence
- Data Storytelling

---

## 👨‍💻 Author

Rohan Patel

Data Analyst | Power BI Enthusiast | Business Intelligence Learner
