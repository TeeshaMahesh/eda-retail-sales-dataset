# Retail Sales EDA – Understanding Customer & Sales Patterns

## About This Project
This repository contains an exploratory data analysis (EDA) built on a retail transactions dataset. The aim was simple: dig into real sales data, clean it up, and figure out what it's actually telling us about customers, products, and revenue — then turn that into recommendations a retail business could act on.

Built as part of a Data Science Internship submission (Task 1 – EDA).

---

## The Dataset
- **Where it's from:** [Kaggle – Retail Sales Dataset](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset)
- **Size:** 1,000 transactions
- **Columns:** Transaction ID, Date, Customer ID, Gender, Age, Product Category, Quantity, Price per Unit, Total Amount
- **Categories:** Beauty, Clothing, Electronics

---

## Stack
| Tool | Purpose |
|---|---|
| Python | Core language |
| Pandas / NumPy | Cleaning & data wrangling |
| Matplotlib / Seaborn | Charts & visual analysis |
| Jupyter Notebook | Where it all comes together |

---

## Cleaning the Data
Before drawing any conclusions, the raw data went through:
- Duplicate transaction removal
- A full missing-values check across every column
- Converting the `Date` field into an actual datetime type
- Building two new helper columns — `Month` and `Age Group` — to make trend and demographic analysis easier
- A boxplot pass on `Total Amount` to flag anything that looked like a data error (nothing did — high values were genuine big-ticket Electronics sales)

---

## What Came Out of the Analysis
- **Electronics edges out the competition** as the top revenue category (~157K), with Clothing right behind (~156K) and Beauty a bit lower (~144K)
- **Gender split is nearly 50/50** — 51.1% of revenue from Female customers, 48.9% from Male
- **Age isn't a factor** — customers are spread evenly from their 20s to their 60s, no single group stands out
- **May was the strongest month** (~53K in sales); **September was the weakest** (~24K) — a dip worth investigating seasonally
- **Price drives sales, not quantity or age** — Price per Unit correlates strongly with Total Amount (0.85), while Quantity (0.37) and Age (-0.06) barely move the needle

---

## Charts Included
All available under `/screenshots`:
- Bar chart — category-wise total sales
- Line chart — sales trend across months
- Histogram — customer age spread
- Heatmap — correlation between numeric variables
- Scatter plot — price vs. transaction value
- Pie chart — gender-wise revenue split
- Boxplot — outlier check on transaction amounts

---

## So What Should the Business Do?
1. Put more weight behind Electronics — it's the strongest earner by both total revenue and average transaction size
2. Don't over-segment marketing by age or gender — the data doesn't support it
3. Target the slow months (like September) with promotions to flatten out the yearly sales curve
4. Push for higher price-per-unit sales (bundles, premium options) rather than just more units — that's what actually grows revenue here

---

## Folder Layout
retail-sales-eda-analysis/


├── EDA_Retail_Sales.ipynb     → full notebook: code, charts, commentary

├── retail_sales_dataset.csv   → cleaned data

├── EDA_Report.pdf             → write-up of the full analysis

├── screenshots/                → exported chart images

└── README.md                   → you're reading it
