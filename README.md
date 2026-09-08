# V-Mart Sales Data Analysis 📊

## 📌 Project Overview

**V-Mart Sales Data Analysis** is an interactive **Power BI business intelligence project** built to analyze sales performance, profitability, product performance, customer activity, promotions, discounts, and sales trends.

The project transforms transactional sales data into an interactive dashboard that helps identify high-performing products, low-performing products, sales trends, promotion performance, and differences between selected time periods.

The dashboard is designed as a portfolio project to demonstrate practical skills in **Power BI, Power Query, DAX, data modeling, data visualization, and business analysis**.

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Analyze overall sales and profit performance.
- Track total quantity sold and order volume.
- Identify the top-performing products.
- Identify the bottom-performing products.
- Analyze sales trends over time.
- Compare sales, profit, and quantity between different date ranges.
- Analyze average discounts across promotion categories.
- Understand sales distribution across cities.
- Provide detailed transaction-level analysis.
- Build an interactive dashboard using slicers and Power BI visuals.

---

## 🗂️ Dataset

The project uses an Excel-based sales dataset containing four logical components:

| Dataset / Table | Description |
|---|---|
| **Dim Customers** | Customer master data including customer name, city, state, pincode, email, and phone information |
| **Dim Product** | Product master data including product name, product line, and price |
| **Dim Promotion** | Promotion information including promotion name, advertising type, coupon code, and price reduction type |
| **Sheet3** | Transaction-level sales data containing date, customer, promotion, product, units sold, and sales/discount fields |

### Dataset Statistics

- **3,510** sales transactions
- **50** customers
- **30** products
- **5** defined promotions
- Transaction period: **January 2020 – January 2024**
- **7,125** total units sold in the source transaction data

---

## 🛠️ Tools & Technologies

- **Power BI** — Dashboard development and visualization
- **Power Query** — Data cleaning and transformation
- **DAX** — Measures and analytical calculations
- **Microsoft Excel** — Source dataset
- **Data Modeling** — Relationships between customer, product, promotion, and transaction data

---

## 🔄 Data Preparation & Transformation

The project follows a typical Power BI data-analysis workflow:

1. Imported the Excel dataset into Power BI.
2. Reviewed customer, product, promotion, and transaction tables.
3. Prepared the transactional data for analysis.
4. Connected transaction records with customer, product, and promotion information.
5. Created calculated analytical fields/measures for sales, profit, quantity, discounts, and orders.
6. Built interactive visuals and slicers.
7. Added comparative analysis using date-range filters.
8. Created a detailed transaction-level table for drill-down analysis.

---

## 🧩 Data Model

The dataset is organized around a transactional sales table supported by dimension tables:

```text
                 ┌──────────────────┐
                 │   Dim Customers  │
                 └────────┬─────────┘
                          │
                          │ Customer ID
                          ▼
┌──────────────────┐   ┌──────────────────┐   ┌──────────────────┐
│   Dim Product    │──▶│    Sales Data    │◀──│  Dim Promotion   │
└──────────────────┘   │     Sheet3       │   └──────────────────┘
                       └──────────────────┘
```

This structure allows the dashboard to analyze transactions from multiple business perspectives.

---

# 📊 Dashboard Features

## 1. Overview Dashboard

The overview page provides a high-level view of business performance.

### Key visualizations include:

- Profit vs. Net Sales scatter analysis
- Number of orders
- Average discount by promotion category
- City-wise units sold map
- Sales trend by period

The dashboard allows users to quickly understand overall performance and identify patterns in sales and profitability.

<img width="851" height="458" alt="Screenshot 2026-09-09 002052" src="https://github.com/user-attachments/assets/ca09c514-ed9f-440a-b0d0-1c7ef7c806d4" />


---

## 2. Top / Bottom 5 Product Analysis

This page focuses on product-level performance.

### Top 5 Products by Sales

The dashboard highlights:

1. Apple iPhone 14 — **₹22.5M**
2. Apple MacBook Air — **₹20.8M**
3. Sony Bravia 55" TV — **₹20.5M**
4. Samsung Galaxy S21 — **₹16.1M**
5. HP Pavilion Laptop — **₹15.5M**

### Bottom 5 Products by Sales

The dashboard identifies the lowest-performing products, including:

- Tupperware Lunch Box
- L'Oreal Shampoo
- Nivea Body Lotion
- Dove Soap Pack
- Colgate Toothpaste

The same page also provides **Top 5 and Bottom 5 analysis by quantity sold and profit**.

---

## 3. Sales, Profit & Quantity Comparison

The comparison page allows users to select two different date ranges and compare:

- **Total Sales**
- **Total Profit**
- **Total Quantity Sold**

This makes it easier to evaluate how business performance changed between two selected periods.

---

## 4. Interactive Date Comparison

Two independent date filters allow users to choose different periods for comparison.

This functionality can be used for analysis such as:

- Period-over-period performance
- Before vs. after promotion analysis
- Year/date-range comparison
- Sales performance comparison

---

## 5. Edit Interactions

The dashboard uses Power BI's **Edit Interactions** functionality to control how visuals respond to user selections.

This improves the usability of the dashboard and allows users to interact with specific visuals without affecting unrelated analysis.

---

## 6. Detailed Transaction Table

A dedicated table view provides transaction-level details.

Available fields include:

- Customer ID
- Product ID
- Promotion ID
- Date
- Discount Percentage
- Discount Value
- Net Sales
- Price Per Unit
- Profit
- Total Sales
- Units Sold

Interactive slicers allow users to filter the table by:

- Date
- Customer Name
- Product Name
- Promotion ID

---

# 📈 Key Business Insights

Based on the dashboard, several useful observations can be made:

### 🏆 Product Performance

**Apple iPhone 14** is the strongest product by sales, generating approximately **₹22.5M** in the dashboard's Top 5 analysis.

Apple MacBook Air and Sony Bravia 55" TV also show strong sales performance.

### 📉 Low-Performing Products

Products such as **Tupperware Lunch Box, L'Oreal Shampoo, Nivea Body Lotion, Dove Soap Pack, and Colgate Toothpaste** appear among the bottom-performing products by sales.

### 💰 Sales & Profit Relationship

The dashboard uses a **Profit vs. Net Sales** visualization to examine the relationship between sales value and profitability across transactions.

### 🎯 Promotion & Discount Analysis

The dashboard compares average discounts across promotion categories. **Clearance Sale** shows the highest average discount among the promotion categories displayed.

### 🌍 Geographical Analysis

The city-level map visual provides a geographical view of units sold, helping identify locations with relatively higher sales activity.

### 📅 Time-Series Analysis

The sales trend visual makes it possible to identify fluctuations in sales across the transaction period and investigate changes over time.

---

# 📸 Dashboard Preview

Add your Power BI dashboard screenshots to the repository and place them inside a folder named `images`.

Recommended structure:

```text
images/
├── overview.png
├── top-bottom-analysis.png
├── comparison.png
├── edit-interactions.png
└── table-view.png
```

Then you can display them in this README using:

```markdown
![Overview Dashboard](images/overview.png)
```

---

# 📁 Project Structure

```text
Amazon-Sales-Data-Analysis/
│
├── README.md
│
├── data/
│   └── Store+Data.xlsx
│
├── powerbi/
│   └── Amazon-Sales-Data-Analysis.pbix
│
└── images/
    ├── overview.png
    ├── top-bottom-analysis.png
    ├── comparison.png
    ├── edit-interactions.png
    └── table-view.png
```

> **Note:** Update the filenames above to match the actual files you upload to GitHub.

---

# 💡 Business Questions Answered

This dashboard helps answer questions such as:

- What are the highest-selling products?
- Which products have the lowest sales?
- Which products sell the highest quantity?
- Which products contribute most to profit?
- How are sales changing over time?
- Which cities have higher sales activity?
- Which promotion categories provide higher discounts?
- How does one selected period perform compared with another?
- What are the detailed sales transactions behind the summary metrics?

---

# 🚀 Skills Demonstrated

This project demonstrates practical experience in:

- **Power BI Dashboard Development**
- **Power Query**
- **DAX**
- **Data Cleaning & Transformation**
- **Data Modeling**
- **Data Visualization**
- **KPI Analysis**
- **Time-Series Analysis**
- **Product Performance Analysis**
- **Sales & Profit Analysis**
- **Promotion & Discount Analysis**
- **Geographical Analysis**
- **Interactive Filtering**
- **Business Intelligence**

---

# 🔮 Future Improvements

Possible improvements for a future version include:

- Add year-over-year growth analysis.
- Add monthly and yearly KPI cards.
- Add customer segmentation.
- Add customer retention analysis.
- Add promotion ROI analysis.
- Add profit-margin analysis by product.
- Add drill-through pages for product and customer analysis.
- Add a dedicated executive summary page.
- Improve mobile/responsive dashboard layout.

---

## 👨‍💻 Author

**Sundram**

**Data Analyst | Power BI | SQL | Excel | Python**

---

## ⭐ Project Purpose

This project was created as a **Data Analyst portfolio project** to demonstrate the complete process of converting raw business data into an interactive Power BI dashboard and extracting meaningful insights for decision-making.
