# 🛍️ Customer Shopping Behavior Analysis


## 📌 Project Overview

This project analyzes how 3,900 retail customers shop, spend, and respond to discounts. The goal was to go beyond surface-level reporting and find the patterns that actually matter for business decisions — things like whether subscriptions drive more spending, whether discounts are working, and where the real revenue is coming from.

I used SQL for structured querying, Python for exploratory data analysis, and Power BI to build a dashboard that makes the insights accessible to both technical and non-technical audiences.

---
# 📊 Power BI Dashboard

![Customer Behavior Dashboard](dashboard.jpg)

## 🔍 Key Findings

- **Subscriptions don't drive bigger baskets** — subscribed customers averaged $59.49 per order vs. $59.87 for non-subscribers. The value of subscriptions is in purchase frequency, not transaction size.

- **Discounts are hurting margin without lifting spend** — promo users spent less on average ($59.28) than non-promo customers ($60.13). Yet Hat, Sneakers, and Coat are being discounted on nearly every other sale (50%, 49.7%, and 49.1% discount rates).

- **The gender revenue gap is a volume problem, not behavioral** — males drove $157,890 vs. $75,191 for females, but average spend per transaction is nearly identical ($59.54 vs. $60.25). The fix is reach, not pricing strategy.

- **80% of customers are already Loyal** (3,116 out of 3,900), yet only 27.6% of repeat buyers hold a subscription — the most valuable customers are the least monetized.

- **Clothing dominates at $104,264 (45% of total revenue)**, Fall is the strongest season ($60,018), and Gloves lead product satisfaction with a 3.86/5 average rating.

---

## 🛠️ Tools & Techniques

### SQL
- Created a `customer_clean` VIEW to standardize column names
- Used **CTEs** for multi-step segmentation logic
- Applied **Window Functions** (`ROW_NUMBER OVER PARTITION BY`) to rank products per category
- Used **Subqueries** to filter against aggregate benchmarks
- Applied **CASE statements** for customer tier classification (New / Returning / Loyal)

### Python
- **Pandas** — data loading, cleaning, and aggregation
- **Matplotlib & Seaborn** — distribution plots, bar charts, correlation heatmaps
- Explored age group distributions, purchase frequency patterns, and seasonal trends

### Power BI
- Built an interactive dashboard with slicers for gender, season, category, and subscription status
- KPIs displayed: total revenue, avg order value, customer segments, top products, discount impact

---



## 💡 Business Recommendations

1. **Re-evaluate the discount strategy** — discounts on Hat, Sneakers, and Coat are near-universal but not increasing spend. Consider restricting promos to first-time or low-frequency buyers only.
2. **Convert loyal customers to subscribers** — with 72.4% of repeat buyers unsubscribed, a targeted subscription push to this segment is the clearest revenue opportunity.
3. **Double down on Clothing and Fall campaigns** — Clothing drives 45% of revenue and Fall is the peak season. Prioritizing inventory and marketing here has the highest ROI.
4. **Investigate gender reach gap** — since spend behavior is equal across genders, closing the volume gap (2,652 male vs. 1,248 female customers) through targeted acquisition could significantly grow revenue.

---

## 🚀 How to Run This Project

1. **SQL** — Import `customer_shopping_behavior_cleaned.csv` into PostgreSQL, then run `sql_analysis.sql`
2. **Python** — Open `customer_behavior.ipynb` in Jupyter Notebook and run all cells
3. **Power BI** — Open `Customer_Behavior.pbix` in Power BI Desktop

---

*Built as part of a data analytics portfolio to demonstrate end-to-end analysis skills across SQL, Python, and business intelligence tools.*
