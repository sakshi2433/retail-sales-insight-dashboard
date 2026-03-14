# Retail Sales Insight Dashboard

A multi-page Power BI dashboard built on the Superstore dataset, analysing 9,000+ retail transactions across sales, profit, customer segments, and regional performance. Designed to answer the questions a retail business manager would actually ask.

---

## Dashboard pages

| Page | What it shows |
|---|---|
| **Overview** | Total sales, profit, orders, and YoY growth at a glance |
| **Product Performance** | Top/bottom products, category profitability, discount impact |
| **Customer Segments** | Segment-wise revenue, order frequency, and value distribution |
| **Regional Analysis** | State and region-level sales and profit breakdown |
| **Trends** | Monthly and quarterly sales trends with seasonality |

---

## DAX measures built

15+ custom DAX measures including:

- `YoY Sales Growth %` — year-over-year comparison using `SAMEPERIODLASTYEAR`
- `Profit Margin %` — dynamic margin calculation per filter context
- `Discount Impact` — quantifies revenue lost to discounting
- `Customer LTV` — estimated lifetime value per customer segment
- `MoM Growth` — month-over-month delta using `DATEADD`
- `Running Total Sales` — cumulative sales using `DATESYTD`

---

## Key insights uncovered

- The **Technology** category had the highest revenue but Tables sub-category was consistently loss-making due to deep discounting
- **Corporate segment** customers had higher average order values than Consumer, but Consumer had 2x the volume
- The **South region** underperformed on profit margin despite moderate sales — driven by high discount rates
- Seasonal peaks in **November–December** contributed ~28% of annual revenue

---

## Project structure

```
retail-sales-insight-dashboard/
├── dashboard/
│   └── RetailInsights.pbix        # Power BI file
├── data/
│   └── superstore.xlsx            # Source dataset
├── screenshots/
│   ├── overview.png
│   ├── product_performance.png
│   └── regional_analysis.png
└── README.md
```

---

## How to open

1. Download and install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Clone this repo and open `dashboard/RetailInsights.pbix`
3. Data is embedded — no additional setup needed

---

## Dataset

[Superstore Sales Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final) — a widely-used retail analytics dataset with orders, customers, products, and regional data.

---

## Tech stack

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-yellow?style=flat)
![Excel](https://img.shields.io/badge/Excel-Data%20Source-217346?style=flat&logo=microsoft-excel&logoColor=white)

---

> **Author:** Sakshi · [GitHub](https://github.com/sakshi2433) · [Email](mailto:sakshi240905@gmail.com)
