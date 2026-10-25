# Superstore Sales Analysis Dashboard | Power BI

## 📌 Project Overview
This project focuses on analyzing Superstore sales data using Microsoft Power BI to understand sales performance, profitability, customer behavior, regional performance, and shipping efficiency.

The project involves data cleaning, data modeling, DAX calculations, and interactive visualizations to convert raw data into meaningful business insights that support data-driven decision-making.

## 🎯 Project Objectives
- Analyze overall sales, profit, quantity, and order performance.
- Identify top-performing product categories, sub-categories, and products.
- Compare sales and profitability across different regions and customer segments.
- Analyze monthly sales trends and Year-over-Year (YoY) sales growth.
- Evaluate the relationship between discounts and profitability.
- Identify products generating negative profits.
- Analyze customer purchasing behavior and repeat customers.
- Compare average shipping time across different shipping modes.

## 🛠️ Tools & Technologies
- **Microsoft Power BI Desktop** – Dashboard development and data visualization
- **Power Query** – Data cleaning and transformation
- **DAX (Data Analysis Expressions)** – Measures and business calculations
- **Data Modeling** – Relationships between Orders, People, Returns, and Calendar tables

## 🧹 Data Cleaning & Preparation
- Checked data quality and column data types.
- Reviewed duplicate records.
- Prepared the People and Returns tables by correcting headers and handling null entries.
- Created a Calendar table for time-based analysis.
- Established relationships between the relevant tables.

## 📊 Key Analysis Performed
1. **KPI Analysis:** Total Sales, Total Profit, Total Quantity, Average Discount, and Total Orders.
2. **Category & Sub-Category Analysis:** Compared sales and profit across product categories and sub-categories.
3. **Regional Analysis:** Identified regions with the highest sales and profit.
4. **Monthly Sales Trends:** Analyzed sales performance over time.
5. **YoY Sales Growth:** Compared current-year sales with previous-year sales.
6. **Top 10 Products:** Identified the top products based on sales.
7. **Top 10 Customers:** Analyzed customers contributing the most sales.
8. **Profit Margin Analysis:** Compared profitability across categories and sub-categories.
9. **Discount Impact Analysis:** Examined profit patterns across discount ranges.
10. **Loss-Making Products:** Identified products with negative total profit.
11. **Customer Segment Analysis:** Compared sales, profit, profit margin, and average order value across segments.
12. **Shipping Analysis:** Compared average shipping days across shipping modes.
13. **Repeat Customer Analysis:** Identified customers with multiple orders.

## 🧮 Important DAX Measures

### Total Sales
```dax
Total Sales = SUM(Orders[Sales])
```

### Total Profit
```dax
Total Profit = SUM(Orders[Profit])
```

### Total Orders
```dax
Total Orders = DISTINCTCOUNT(Orders[Order ID])
```

### Profit Margin %
```dax
Profit Margin % =
DIVIDE([Total Profit], [Total Sales], 0)
```

### Previous Year Sales
```dax
Previous Year Sales =
CALCULATE(
    [Total Sales],
    SAMEPERIODLASTYEAR(Calendar[Date])
)
```

### YoY Growth %
```dax
YoY Growth % =
DIVIDE(
    [Total Sales] - [Previous Year Sales],
    [Previous Year Sales],
    0
)
```

### Average Shipping Days
```dax
Average Shipping Days =
AVERAGEX(
    Orders,
    DATEDIFF(
        Orders[Order Date],
        Orders[Ship Date],
        DAY
    )
)
```

## 💡 Key Business Insights
- Technology was the highest-performing category in terms of sales and total profit.
- The West region recorded the highest sales and profit, while the Central region had the lowest profit.
- Copiers generated the highest total profit among sub-categories.
- The 0.6–0.8 discount range showed the lowest total profit in the analysis.
- Products with negative total profit were identified for further investigation.
- Standard Class had the highest average shipping duration among the shipping modes analyzed.

*Note: These insights are based on the analysis performed in this project. Discount patterns indicate an association with profitability and do not, by themselves, establish causation.*

## 📈 Dashboard Features
- KPI cards for key business metrics.
- Product, category, customer, and regional analysis.
- Time-based sales analysis and YoY growth.
- Profitability and discount analysis.
- Shipping and repeat customer analysis.
- Interactive filtering and visual exploration.

## 📁 Project Files
- Power BI project file (`.pbix`)
- Dataset file, if permitted to share
- `README.md` – Project documentation

## 🚀 How to Use
1. Clone or download this repository.
2. Open the `.pbix` file using Power BI Desktop.
3. Refresh the data source if required.
4. Explore the report pages and interact with the available filters.

## 👩‍💻 Skills Demonstrated
Power BI, Power Query, DAX, Data Cleaning, Data Modeling, Data Visualization, KPI Reporting, Time Intelligence, Business Analysis, and Data-Driven Decision-Making.

---

**Project Type:** Data Analytics | Business Intelligence  
**Tool:** Microsoft Power BI Desktop
