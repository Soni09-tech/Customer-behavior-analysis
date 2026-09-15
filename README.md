# 🛍️ Customer Shopping Behavior Analysis

An end-to-end data analysis project exploring spending patterns, customer segments, and product preferences across **3,900 transactions** — built with **Python**, **PostgreSQL**, and **Power BI**.

---

## 📌 Overview

This project analyzes a retail customer shopping dataset to uncover insights around revenue drivers, customer segmentation, subscription behavior, and product performance. The workflow covers the full data pipeline: cleaning and preparing raw data in Python, loading it into PostgreSQL for SQL-based analysis, and building an interactive Power BI dashboard for reporting.

## 📂 Repository Contents

| File | Description |
|------|-------------|
| `customer_shopping_behavior_analysis.ipynb` | Jupyter notebook with data cleaning, EDA, and analysis in Python |
| `customer_shopping_behavior_data.csv` | Raw/source dataset used for the analysis |
| `Customer_analysis_visualization.pbix` | Power BI dashboard file |
| `Customer Shopping Behavior Analysis Report.pdf` | Written summary report of findings |
| `Customer-Shopping-Behavior-Analysis ppt.pdf` | Slide deck presenting the project and key insights |

## 📊 Dataset at a Glance

- **3,900** total purchases across all product categories
- **18** data columns spanning demographics, purchases, and behavior
- **25** unique items across **4** product categories (Clothing, Accessories, Footwear, Outerwear)
- **37** missing values (limited to `Review Rating`)

**Key features:** customer demographics (Age, Gender, Location, Subscription Status), purchase details (Item Purchased, Category, Purchase Amount, Season, Size, Color), and shopping behavior (Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type).

## 🧹 Data Preparation (Python)

1. **Load & Explore** — Imported the dataset via `pandas`; used `df.info()` and `.describe()` to understand structure and summary statistics.
2. **Clean Missing Data** — Imputed missing `Review Rating` values using the median rating per product category.
3. **Standardize & Engineer** — Renamed columns to `snake_case`; engineered `age_group` and `purchase_frequency_days`; dropped the redundant `promo_code_used` column.
4. **Load to PostgreSQL** — Connected the Python script to PostgreSQL and loaded the cleaned DataFrame for SQL-based analysis.

## 🔑 Key Insights

- **Male customers drive ~2× more revenue** than female customers ($157,890 vs. $75,191), largely explained by males making up 68% of transactions (2,652 of 3,900).
- **Hats are the most discount-dependent product** (50% of purchases made with a discount), followed by Sneakers (49.66%) and Coats (49.07%).
- **Non-subscribers generate far more total revenue** ($170,436 vs. $62,645) than subscribers, though average spend per transaction is nearly identical (~$59.50–$59.90). Subscribers are only 27% of the customer base but show strong repeat-purchase behavior.
- **Customer segments:** 3,116 Loyal customers (core revenue base), 701 Returning customers (candidates for loyalty programs), and 83 New customers (smallest segment, critical for onboarding).
- **Young Adults lead revenue** ($62,143), closely followed by Middle-aged customers ($59,197) — revenue is fairly evenly spread across age groups.
- **Express shipping users spend slightly more on average** ($60.48) than Standard shipping users ($58.46), suggesting a willingness to pay for convenience.
- **Clothing dominates purchase volume**, followed by Accessories, with Footwear and Outerwear trailing but consistent.

## 📈 Power BI Dashboard

An interactive Power BI dashboard presents key metrics — 3.9K customers, average purchase of $59.76, and average rating of 3.75 — with filters for Subscription Status, Gender, Category, and Shipping Type. Revenue by category: Clothing ($100K) > Accessories ($75K) > Footwear ($30K) > Outerwear ($15K).

## ✅ Recommendations

- **Boost Subscriptions** — Promote exclusive subscriber benefits to convert repeat buyers.
- **Loyalty Programs** — Reward returning customers to move them into the Loyal segment.
- **Review Discount Policy** — Balance sales boosts with margin control on discount-heavy products.
- **Targeted Marketing** — Focus on high-revenue age groups and express-shipping users.
- **Product Positioning** — Highlight top-rated and best-selling products in campaigns.

## 🛠️ Tools & Technologies

- **Python** (pandas) — data cleaning and preparation
- **PostgreSQL** — SQL-based data analysis
- **Power BI** — interactive dashboard and reporting

## 🚀 Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/Soni09-tech/Customer-behavior-analysis.git
   ```
2. Open `customer_shopping_behavior_analysis.ipynb` in Jupyter Notebook/Lab to explore the Python data cleaning and analysis steps.
3. Open `Customer_analysis_visualization.pbix` in Power BI Desktop to explore the interactive dashboard.
4. Refer to the PDF report/slide deck for a summarized write-up of the findings.

## 📬 Contact

For questions or further discussion about this analysis, feel free to reach out or open an issue in this repository.
