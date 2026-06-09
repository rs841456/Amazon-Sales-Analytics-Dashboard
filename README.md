# 📊 Amazon Sales Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)
![Records](https://img.shields.io/badge/Records-3203-blue?style=for-the-badge)

---

## 📌 Project Overview

This project is an **end-to-end Amazon Sales Analytics Dashboard** built using **Microsoft Excel** for data cleaning and preprocessing, and **Power BI** for interactive visualization. The dashboard analyzes **3,203 sales records** from **2011 to 2014** across the United States, covering **17 product categories** with a total revenue of **$725,457**.

---

## 🎯 Objectives

- Analyze Amazon sales data to identify key revenue and profit trends
- Understand product category-wise performance across 4 years
- Identify top-performing states and regions in the United States
- Track order volume and profitability at product level
- Enable data-driven decision-making through interactive Power BI visuals

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Microsoft Excel** | Data cleaning, formatting, and preprocessing |
| **Power BI Desktop** | Interactive dashboard creation and visualization |
| **Power Query** | Data transformation and modeling |
| **DAX (Data Analysis Expressions)** | Custom KPI measures and calculated columns |

---

## 📁 Project Structure

```
Amazon-Sales-Analytics-Dashboard/
│
├── Amazon_2_Raw.xlsx               # Raw dataset (3203 records)
├── Amazon_3_Final.xlsx             # Cleaned and processed data
├── AmozonSalesDashboard.pbix       # Power BI dashboard file
└── README.md
```

---

## 📂 Dataset Description

| Column | Description |
|--------|-------------|
| `Order ID` | Unique identifier for each order |
| `Order Date` | Date when the order was placed |
| `Ship Date` | Date when the order was shipped |
| `EmailID` | Customer email address |
| `Geography` | Country, City, and State of the customer |
| `Category` | Product category (17 categories) |
| `Product Name` | Name of the product sold |
| `Sales` | Revenue generated from the order |
| `Quantity` | Number of units ordered |
| `Profit` | Profit earned from the order |

**Dataset Size:** 3,203 rows × 10 columns  
**Time Period:** January 2011 – December 2014  
**Region:** United States

---

## 📊 Dashboard Features

### 🔢 Key Performance Indicators (KPIs)
- **Total Sales Revenue** — $725,457
- **Total Profit** — $108,418
- **Total Orders** — 3,203
- **Profit Margin** — ~14.9%
- **Average Order Value** — ~$226

### 📈 Visualizations
- **Yearly Sales Trend** — Revenue growth from 2011 to 2014
- **Sales by Category** — Bar chart across 17 product categories
- **Top Products by Sales** — Best-selling individual products
- **State-wise Sales Map** — Geographic distribution across US states
- **Profit vs Sales Analysis** — Scatter chart to identify profitable categories
- **Monthly Order Trend** — Seasonal demand patterns

### 🔍 Interactive Filters (Slicers)
- Date / Year Range
- Product Category
- State / Region
- Customer

---

## 🧹 Data Cleaning Steps (Excel)

1. **Removed duplicate records** from the raw dataset
2. **Handled missing/null values** across all columns
3. **Standardized date formats** for Order Date and Ship Date
4. **Split Geography column** into Country, City, and State
5. **Corrected data types** — Sales, Quantity, Profit as numeric
6. **Removed irrelevant whitespace** from Product Name and Category columns
7. **Verified negative profit values** for loss-making orders

---

## 📐 DAX Measures Used

```dax
Total Sales = SUM(Amazon[Sales])

Total Profit = SUM(Amazon[Profit])

Total Orders = COUNT(Amazon[Order ID])

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)

YoY Sales Growth = 
    DIVIDE(
        [Total Sales] - CALCULATE([Total Sales], PREVIOUSYEAR('Date'[Date])),
        CALCULATE([Total Sales], PREVIOUSYEAR('Date'[Date])),
        0
    )
```

---

## 💡 Key Insights

- 🏆 **California** was the top-performing state with **$457,688** in sales (63% of total revenue)
- 🥈 **Washington** ranked second with **$138,641** in sales
- 📦 **Phones, Chairs, and Tables** were the highest revenue-generating categories
- 📉 Some orders in **Binders, Accessories, and Furniture** had **negative profit**, indicating discounting issues
- 📅 Sales consistently grew **year-over-year from 2011 to 2014**
- 💰 Overall **profit margin was ~14.9%** across all categories and regions

---

## 🚀 How to Use

1. Clone or download this repository
2. Open `Amazon_2_Raw.xlsx` to see the original raw data
3. Open `Amazon_3_Final.xlsx` to review the cleaned/processed data
4. Open `AmozonSalesDashboard.pbix` in **Power BI Desktop**
5. Refresh the data source if needed (update the file path to your local machine)
6. Use the slicers on the dashboard to filter data interactively

> **Note:** Power BI Desktop (free) is required to open the `.pbix` file.  
> Download it from [Microsoft's official site](https://powerbi.microsoft.com/desktop).

---

## 👤 Author

**Rajan Kumar**
📧 rs8595984@gmail.com  
💻 [GitHub Profile](https://github.com/rs841456)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

⭐ **If you found this project helpful, please give it a star!**
