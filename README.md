# 🛒 Retail Sales Insights Dashboard (Power BI + DAX)

An end-to-end business intelligence project analyzing retail performance across
customers, products, categories, and regions using the Superstore dataset.
This dashboard provides actionable insights on sales, profitability, discount impact,
and customer behavior.

---

## 📌 Project Overview
This project demonstrates a full data analytics workflow:

1. Data cleaning & preprocessing    
2. DAX measure creation for KPIs  
3. Multi-page Power BI dashboard  
4. Business insights & recommendations  

The final dashboard helps answer:
- Which customer segments and regions drive profit?
- Which products or categories are loss-making and why?
- How do discounts impact profitability?
- Which customers contribute most to revenue?
- What geographic areas should the business prioritize?

---

## 🧰 Tech Stack
- **Power BI Desktop**  
- **DAX** (Advanced Measures)  
- **CSV / Excel** for dataset  
- **Power Query** for transformations  

---

## 📂 Project Structure
Retail-Sales-Insights-Superstore/
│── data/
│ └── superstore.csv
│── powerbi/
│ └── Retail_Sales_Dashboard.pbix
└── README.md (this file)


---

## 📊 Dashboard Pages & Features

### **1️⃣ Executive Overview**
- KPIs: Total Sales, Total Profit, Orders, AOV, Profit Margin  
- Monthly Sales & Profit Trend  
- Segment-wise Sales & Profit  
- Slicers: Year, Region, Category  

---

### **2️⃣ Customer Analytics**
- Top 10 Customers by Sales  
- Customer Profitability Table (with conditional formatting)  
- Sales Distribution Histogram  
- Segment-wise Customer Performance  
- Region & Segment slicers  

Key Questions Answered:
- Who are the highest-value customers?
- Which customers have negative or low margin?
- How does customer behavior vary by segment?

---

### **3️⃣ Product & Category Analytics**
- Sales by Category  
- Profit by Sub-Category (sorted to reveal loss-makers)  
- Product-level table with conditional formatting  
- Discount vs Profit scatter plot  
- Drilldown: Category → Sub-category  

Key Insights:
- Identify products causing financial loss  
- Understand discount misuse & its impact on profit  
- Compare category vs sub-category profitability  

---

### **4️⃣ Geography & Regional Performance**
- Filled Map: Sales by State  
- Bubble Map: Profit by State  
- Regional Sales & Profit Comparison  
- State-level Profitability Table  
- Discount vs Profit by Region  

Key Insights:
- Which regions drive most revenue and profit?
- Which states are unprofitable?
- How does discounting vary by region?

---

## 📐 Core DAX Measures

```DAX
Total Sales = SUM('superstore'[Sales])
Total Profit = SUM('superstore'[Profit])
Total Orders = DISTINCTCOUNT('superstore'[Order ID])
Average Order Value (AOV) = DIVIDE([Total Sales], [Total Orders])
Profit Margin % = DIVIDE([Total Profit], [Total Sales])
Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('DateTable'[Date]))
Sales YoY % = DIVIDE([Total Sales] - [Sales LY], [Sales LY])
Loss Product = IF([Total Profit] < 0, "Loss", "Profit")
Average Discount = AVERAGE('superstore'[Discount])
