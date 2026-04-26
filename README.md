# ☕ Mark Coffee Shop Sales Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Tools Used](#tools-used)
- [Data Cleaning](#data-cleaning)
- [Data Analysis](#data-analysis)
- [Dashboard](#dashboard)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Usage Guide](#usage-guide)
- [Dataset Description](#dataset-description)
- [Conclusion](#conclusion)
- [Author](#author)
- [License](#license)

---

## 📌 Project Overview

This project analyzes transactional data from Mark Coffee Shop to uncover sales trends, customer behavior, and product performance. The goal is to generate insights that can help improve business decisions, optimize staffing, and maximize revenue.

---

## 🎯 Objectives

The analysis answers the following key business questions:

- How have sales trended over time?
- Which days of the week are busiest?
- What times of day generate the most sales?
- Which products sell the most and least?
- Which products drive the most revenue?

---

## 🛠 Tools Used

- **Excel** → Data cleaning and preparation
- **SQL** → Data analysis and querying
- **Power BI** → Data visualization and dashboard creation

---

## 🧹 Data Cleaning

The dataset was prepared using Excel and SQL with the following steps:

- ✅ Removed duplicates
- ✅ Handled missing values
- ✅ Ensured correct data types (Date, Time, Numeric fields)
- ✅ Created calculated fields:
  - Revenue = Quantity × Unit Price
  - Day of Week
  - Hour of Transaction

---

## 🔍 Data Analysis (SQL)

Key analyses performed:

- Sales trend over time
- Sales by day of the week
- Sales by hour
- Top-selling products
- Revenue by product category
- Customer purchase patterns
- Seasonal trends

---

## 📊 Dashboard (Power BI)

The interactive dashboard includes:

- 📈 **Line Chart**: Sales over time
- 📊 **Bar Chart**: Sales by product
- 🗓 **Bar Chart**: Sales by day of the week
- ⏰ **Column Chart**: Sales by hour
- 🎛 **Slicers**: Location and product filters for dynamic exploration

---

## 💡 Key Insights

- 📈 Sales are higher on weekends compared to weekdays
- ⏰ Peak sales occur in the morning hours (8 AM – 11 AM)
- ☕ Coffee products are the most popular items
- ⚠️ Some products have low sales, indicating potential inefficiencies
- 💰 A small number of products drive the majority of revenue

---

## 🚀 Recommendations

- ✅ Increase staff during peak morning hours to handle demand
- ✅ Promote products during low-sales periods (afternoon/evening)
- ✅ Focus on high-performing products to maximize revenue
- ✅ Review or improve low-selling items
- ✅ Consider weekend-specific promotions to leverage higher traffic
- ✅ Analyze customer feedback on underperforming products

---

## 📁 Project Structure

```
Mark-Coffee-Shop-Analysis/
├── data/
│   ├── raw/                    # Original unprocessed data
│   └── processed/              # Cleaned and prepared datasets
├── sql/
│   ├── queries.sql             # SQL analysis queries
│   └── data_cleaning.sql       # Data preparation scripts
├── power-bi/
│   ├── dashboard.pbix          # Power BI dashboard file
│   └── visualizations/         # Individual chart exports
├── documentation/
│   ├── data_dictionary.md      # Data field descriptions
│   └── methodology.md          # Analysis approach
├── README.md                   # This file
└── requirements.txt            # Project dependencies
```

---

## 💻 Installation & Setup

### Prerequisites
- Microsoft Excel (2016 or later)
- SQL Server / MySQL / PostgreSQL
- Power BI Desktop
- Git

### Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mattmordi/Mark-Coffee-Shop-Analysis.git
   cd Mark-Coffee-Shop-Analysis
   ```

2. **Download the dataset:**
   - Download the raw data from the `data/raw/` folder
   - Import into your SQL database using the scripts in `sql/data_cleaning.sql`

3. **Clean the data:**
   - Open `data/raw/coffee_shop_data.xlsx` in Excel
   - Follow the cleaning steps outlined in the data_cleaning.sql script

4. **Set up the database:**
   - Run SQL queries from `sql/queries.sql` against your database
   - Export results for Power BI visualization

5. **Open the dashboard:**
   - Open `power-bi/dashboard.pbix` in Power BI Desktop
   - Connect to your processed data source

---

## 🎮 Usage Guide

### Running SQL Queries
```sql
-- Example: View daily sales summary
SELECT DATE(TransactionDate) AS Date, SUM(Revenue) AS DailySales
FROM transactions
GROUP BY DATE(TransactionDate)
ORDER BY Date;
```

### Exploring the Power BI Dashboard
1. Open the `.pbix` file in Power BI Desktop
2. Use the slicers to filter by:
   - Product category
   - Store location
   - Date range
3. Hover over charts for detailed tooltips
4. Export visuals as images for presentations

### Running Python Scripts (Optional)
```bash
python scripts/analysis.py
```

---

## 📊 Dataset Description

| Field | Type | Description |
|-------|------|-------------|
| TransactionID | Integer | Unique transaction identifier |
| TransactionDate | Date | Date of transaction (YYYY-MM-DD) |
| TransactionTime | Time | Time of transaction (HH:MM:SS) |
| Product | String | Name of product sold |
| Category | String | Product category (Coffee, Tea, Pastry, etc.) |
| Quantity | Integer | Number of units sold |
| UnitPrice | Decimal | Price per unit |
| Revenue | Decimal | Total revenue (Quantity × UnitPrice) |
| Location | String | Store location |

**Data Period:** [Specify your date range, e.g., January 2024 - March 2024]  
**Total Records:** [Specify number of transactions]  
**Data Source:** Point of Sale (POS) System

---

## ✅ Conclusion

This project demonstrates a complete, beginner-friendly data analysis workflow — from data cleaning (Excel) to analysis (SQL) and visualization (Power BI) — while focusing on solving real business problems. The insights generated can directly inform strategic decisions to improve coffee shop operations and profitability.

---

## 👤 Author

**Matt Mordi**
- GitHub: [@mattmordi](https://github.com/mattmordi)
- Email: [Your email here]
- LinkedIn: [Your LinkedIn here]

Feel free to reach out with questions, suggestions, or collaboration opportunities!

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

You are free to:
- ✅ Use this project for personal or commercial purposes
- ✅ Modify and distribute the code
- ✅ Use it as a reference for your own projects

**Please attribute** the original work if you use significant portions of this analysis.

---

**Last Updated:** April 26, 2026  
**Status:** ✅ Complete