# Sales Data Analysis — Superstore Dataset
### Synent Technologies | Data Science Internship | Task 5

---

## Problem Statement

Retail businesses often struggle to understand where they are actually making money versus where they are losing it. High sales numbers can hide poor profitability, and without a structured analysis it is difficult to know which products, regions, or customer types are driving real business value.

This project analyzes four years of transactional data from a US-based superstore to answer the following questions:

- Which product categories and sub-categories are most and least profitable?
- How does revenue trend across months and years — are there seasonal patterns?
- Which regions are performing well and which are underperforming on profit margin?
- What is the impact of discounting on profitability?
- Which customer segments offer the best long-term value?

The goal is to move beyond surface-level numbers and surface actionable insights that a business can actually use.

---

## Dataset

**Name:** Superstore Sales Dataset  
**Source:** [Kaggle — Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)  
**File:** `superstore.csv`  
**Records:** ~9,994 orders  
**Time Period:** 2014 to 2017  

**Key columns used in this analysis:**

| Column | Description |
|--------|-------------|
| Order Date | Date the order was placed |
| Sales | Revenue from the order |
| Profit | Profit earned from the order |
| Discount | Discount applied (0 to 1 scale) |
| Category | Product category (Furniture, Office Supplies, Technology) |
| Sub-Category | Product sub-category (e.g. Phones, Tables, Binders) |
| Region | Geographic region (West, East, Central, South) |
| Segment | Customer segment (Consumer, Corporate, Home Office) |

---

## Approach

### Step 1 — Data Cleaning and Preprocessing
- Loaded the dataset using Pandas and checked its shape and data types
- Converted `Order Date` and `Ship Date` columns to datetime format
- Extracted `Year`, `Month`, and `Month_Name` as new columns for time-based analysis
- Checked for null values (none found) and duplicate records (none found)
- Added a derived `Profit_Margin` column: `(Profit / Sales) * 100`

### Step 2 — Exploratory Data Analysis
- Computed summary statistics for Sales, Profit, Discount, and Quantity
- Grouped data by Category, Sub-Category, Region, and Segment to compare performance
- Analyzed monthly and yearly revenue trends to identify seasonality
- Calculated correlation between Discount and Profit to measure discount impact
- Identified top 10 sub-categories by revenue and flagged loss-making ones

### Step 3 — Visualization
- Line chart: Monthly revenue trends across all four years
- Bar chart: Top 10 sub-categories by total sales
- Bar chart: Sales vs Profit comparison by Region
- Bar chart: Category-wise revenue and profit margin
- Scatter plot: Discount vs Profit to visualize the negative relationship
- Heatmap: Correlation matrix across numerical columns

### Step 4 — Insight Extraction
- Translated all visual and statistical findings into 10 plain-language business insights
- Each insight includes a specific, data-backed recommendation
- Summarized into a business insights report

---

## Key Findings

- Q4 (October to December) drives approximately 35% of annual revenue every year
- Technology is the most profitable category with a margin of around 17%
- The Tables sub-category runs at a -8.6% profit margin — the only loss-making sub-category
- Discounts above 40% almost always result in a net loss (correlation r ≈ -0.22)
- The West region leads in both revenue and profit; Central region has the weakest margin at ~8%
- Corporate customers generate higher order values and better margins than Consumer customers

---

## Results

- Identified 10 business insights across revenue trends, product performance, regional gaps, and discount impact
- Produced a business insights report with 5 prioritized recommendations
- Estimated potential profit recovery of $17,000–$20,000 annually by capping Tables discounts at 20%

---

## Tools and Libraries

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Files in this Repository

```
synent-task5-salesanalysis-pulkit/
│
├── superstore.csv                  # Dataset
├── sales_analysis.ipynb            # Main Jupyter notebook
├── business_insights_report.docx  # Final report
├── outputs/
│   ├── monthly_revenue.png
│   ├── top_products.png
│   ├── region_profit.png
│   └── discount_vs_profit.png
└── README.md
```

---

## Author

**Pulkit Mehrotra**  
Data Analyst | Python | SQL | Power BI  
📧 pulkitmehrotra246@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/pulkit-mehrotra05)  
🐙 [GitHub](https://github.com/Pulkit-2github)  
🌐 [Portfolio](https://pulkit-mehrotra-portfolio.netlify.app)

---

*Submitted as part of the Synent Technologies Data Science Internship Program — Task 5: Sales Data Analysis*
