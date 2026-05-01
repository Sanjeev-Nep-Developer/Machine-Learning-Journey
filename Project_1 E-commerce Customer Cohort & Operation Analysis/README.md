# 📊 E-Commerce Logistics & Customer Behavior Intelligence System

---

## 🧭 Executive Summary

This project analyzes large-scale e-commerce transaction data to understand how **logistics performance and customer behavior directly impact revenue and retention**.

Using **RFM (Recency, Frequency, Monetary) segmentation**, time-series analysis, and delivery performance evaluation, the project transforms raw transactional data into **actionable business intelligence**.

The final outcome highlights:
- Customer value segmentation
- Revenue evolution over time
- Operational bottlenecks in delivery performance
- Retention vs acquisition dynamics

---

## 🎯 Business Objective

The core objective of this analysis is to answer:

- Who are the most valuable customers over time?
- How does delivery performance affect customer satisfaction?
- Is the business improving in customer retention or only acquisition?
- Which customer segments drive long-term revenue?

---

## ⚙️ Technical Approach

### 1. Data Engineering & Preparation
- Merged multi-table e-commerce dataset (orders, customers, payments)
- Standardized datetime features using `pd.to_datetime`
- Engineered key behavioral features

---

### 2. RFM Customer Segmentation

Built a custom **RFM scoring system**:

- **Recency** → Time since last purchase  
- **Frequency** → Number of orders per customer  
- **Monetary** → Total spending per customer  

Applied:
- `pd.qcut()` for quantile-based scoring
- `rank(method="first")` to handle duplicate values and tie issues

This ensured stable and statistically consistent customer segmentation.

---

### 3. Customer Segments Defined

Customers were categorized into:

- 🟣 **Champions** → High value, frequent, and recent buyers  
- 🔵 **Loyal Customers** → Frequent buyers with consistent engagement  
- 🟡 **Potential Customers** → Recently active users with growth potential  
- 🔴 **Others** → Low engagement or inactive users  

---

### 4. Time-Series Revenue Analysis

- Extracted yearly trends using `order_purchase_timestamp`
- Analyzed revenue contribution per segment over time
- Visualized customer evolution using grouped aggregation

---

## 📈 Key Business Insights

### 🚚 1. Logistics Bottleneck Effect
Business growth increased sharply over time, but delivery fulfillment began hitting operational limits during peak demand periods.

---

### ⭐ 2. Customer Satisfaction Sensitivity
Delivery timing is the strongest driver of customer satisfaction:
- Early deliveries → high ratings (4–5 stars)
- Delayed deliveries → sharp drop in ratings (<2 stars)

---

### 📊 3. Customer Value Shift Over Time
- Early stage: dominated by low-value “Others” customers  
- Later stage: increase in “Loyal” and “Champion” segments  
- Indicates improving retention and customer quality over time  

---

### 🔁 4. Retention Opportunity Gap
A large base of “Potential” customers suggests strong acquisition performance but weak conversion into long-term loyal users.

---

## 📂 Project Structure
analysis.ipynb → End-to-end data analysis pipeline
final_insights.md → Executive summary of business insights
README.md → Project documentation

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn  
- **Techniques:** RFM Analysis, Time-Series Aggregation, Quantile Binning  

---

## 🧠 Key Learnings

- Real-world datasets require careful handling of skewed distributions
- Business segmentation is not fixed — it is defined by strategy
- Visualization choice directly impacts insight clarity
- Data preprocessing is as important as modeling

---

## ▶️ How to Explore

1. Start with `analysis.ipynb` to understand the full workflow  
2. Refer to `final_insights.md` for executive-level conclusions  

---