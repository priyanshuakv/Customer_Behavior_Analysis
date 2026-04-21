# Customer Behavior Analytics: End-to-End ETL & SQL Pipeline

![Dashboard](/Images/Project_image1.png)

## Project Overview: From Data Noise to Strategic Clarity

In the modern retail landscape, data is abundant, but actionable insight is rare. **This project began with a common corporate challenge**: a raw, messy dataset of customer transactions that held the secrets to the company's growth, yet remained "unreadable" in its original state. *We were faced with a classic fragmented data problem missing customer reviews that skewed performance metrics*, inconsistent naming conventions that slowed down technical workflows, and a lack of clear segmentation that left the marketing team guessing who their most loyal customers actually were.

**The mission was clear** : 
Transform this "noise" into a high-performance analytical engine. We didn't just want to see what was bought; we wanted to understand the who and the why. **By engineering a custom ETL pipeline, we solved the problem of data decay by accurately imputing missing values and standardizing the architecture for professional grade SQL environments**. This allowed us to bridge the gap between raw CSV files and executive-level decision making. Through this project, we moved from asking **"What happened?"** to answering critical strategic questions: **Which demographic is driving our revenue?** Are our discount strategies actually fostering loyalty or just eating our margins? The result is a seamless transition from Python based engineering to deep SQL analysis, culminating in a visual dashboard that turns complex numbers into a clear story of business opportunity.


## Introduction 
This project demonstrates a complete data pipeline that transforms raw retail transaction data into actionable business intelligence. **Using Python (Pandas) for data engineering and PostgreSQL for deep dive analytical querying, the project identifies key drivers of revenue, customer loyalty segments, and product performance**.

The final output includes a structured SQL database and a Power BI Dashboard providing a 360-degree view of customer behavior.

## 🛠️ Tech Stack

- **Language:** Python 3.x
- **Libraries:** Pandas, NumPy, SQLAlchemy, Psycopg2
- **Database:** PostgreSQL (pgAdmin 4)
- **Visualization:** Power BI 
- **Environment:** Jupyter Notebook / VS Code

## 🚀 Data Pipeline (ETL Process)
1. **Cleaning & Imputation,
Handled Missing Values:** Implemented Grouped Median Imputation for `review_rating` based on product categories to maintain distribution accuracy.

- **Standardization:** Normalized all headers to snake_case for seamless SQL integration.

2. **Feature Engineering
Demographic Binning:** Segmented customers into `age_group` (Young Adult to Senior) using quantile-based binning.

- **Metric Conversion:** Transformed qualitative `purchase_frequency` strings into numerical day_intervals to enable mathematical modeling.

- **Redundancy Removal:** Performed correlation checks and dropped redundant features like `promo_code_used` to ensure a lean dataset.

3. **Database Integration**
Established a production-ready pipeline using SQLAlchemy to export the cleaned data from a Python environment directly into a PostgreSQL schema.

**🔍 SQL Analysis & Business Insights
The following business questions were addressed using advanced SQL techniques (CTEs, Window Functions, and Case Logic):**

- **Customer Segmentation:** Classified users into New, Returning, and Loyal tiers based on historical purchase counts.

- **Revenue Drivers:** Analyzed revenue contribution by gender and age group.

- **Discount Strategy:** Identified which products have the highest discount-to-purchase ratio.

- **Top Performers:** Ranked the top 3 most purchased items within every category using ROW_NUMBER().

- **Subscription Impact:** Compared spending habits and total revenue between subscribers and non-subscribers.

- **📈 Dashboard Highlights
Revenue Overview:** Real-time tracking of total sales and average order value.

- **Demographic Deep-dive:** Interactive filters for age groups and gender.

- **roduct Leaderboard:** Visual ranking of top-rated and most-purchased items.

- **Shipping Analysis:** Cost vs. Speed efficiency comparison.

## Key Findings


- **📈 1. Customer Segmentation & Loyalty
The "Loyal" Powerhouse:** By segmenting customers based on previous purchases `(SQL Q7)`, we discovered that Loyal Customers **(10+ purchases)** have a significantly higher Average Spend compared to New customers.

- **Subscription Value:** Subscribed customers don't just spend more per transaction; they represent a more stable revenue stream. Our analysis `(SQL Q5)` showed that while subscribers are a smaller group, their Total Revenue contribution is growing, justifying the cost of the subscription program.

- **💰 2. Revenue & Demographic Drivers
Gender-Based Revenue:** The analysis `(SQL Q1)` revealed which gender demographic is currently driving the majority of sales, allowing the marketing team to tailor **"Hero Product"** advertisements accordingly.

- **Age Group Contribution:** Using the age_group feature we engineered in Pandas, we found that the `[Insert Age Group, e.g., Adult/Senior] segment contributes the highest total revenue (SQL Q10)`, identifying a prime target for high-ticket item promotions.

- **📦 3. Operational & Shipping Efficiency
The Shipping Paradox:** Comparing Standard vs. Express shipping `(SQL Q4)`, we found that customers using Express shipping do not necessarily have a higher average purchase amount. This suggests that the **"need for speed"** is consistent across all price points, and the business should ensure Express margins are protected.

- **🏷️ 4. Discount Sensitivity
High-Discount Products:** We identified the Top 5 products `(SQL Q6)` that are most frequently bought with a discount. This highlights products that customers may be waiting to buy on sale, suggesting these items have high price sensitivity.

- **Strategic Spending:** By identifying customers who spend above average despite using a discount `(SQL Q2)`, we've mapped out a **"Premium Bargain Hunter"** segment—customers who buy high-value items only when incentivized.

- **⭐ 5. Product Performance
Top-Tier Categories:** Our SQL window functions `(SQL Q8)` identified the Top 3 products in every category. This allows the inventory team to prioritize stock for these **"Category Leaders"** to prevent stockouts during peak seasons.

- **Quality Benchmarks:** By rounding and averaging review ratings `(SQL Q3)`, we identified products with the highest customer satisfaction, which can be used as **"Social Proof"** in digital marketing campaigns.

## 🎯 Conclusion
This project successfully transformed a fragmented retail dataset into a structured analytical pipeline. **By integrating Python (ETL), PostgreSQL (Analysis), and Power BI (Visualization),** we moved from raw data to actionable business intelligence.

## Key Results:
- **Data Integrity:** Resolved missing values and standardized schemas for production-ready SQL workflows.

- **Customer Insights:** Developed a segmentation model (New vs. Loyal) and identified high-revenue demographics.

- **Strategic Value:** Quantified the impact of discounts and shipping types on total spend, providing a roadmap for margin optimization.

- **Final Impact:** The project delivers a scalable framework that allows stakeholders to monitor KPIs and make data-driven decisions through an automated, centralized reporting system.
