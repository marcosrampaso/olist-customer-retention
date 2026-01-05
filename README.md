# Olist Customer Churn Analysis & Business Insights

## 📌 Project Overview
This project performs an in-depth **Exploratory Data Analysis (EDA)** on the **Olist Brazilian E-commerce dataset**, with the goal of understanding **customer behavior, churn patterns, and business-driven retention opportunities**.

Rather than focusing purely on model performance, this analysis is designed to **support strategic decision-making**, translating data insights into actionable business conclusions.

---

## 🧠 Business Problem
Customer churn is one of the most critical challenges in e-commerce. Retaining existing customers is significantly more cost-effective than acquiring new ones, yet many customers make only a **single purchase** and never return.

This project seeks to answer:
- How often do customers repurchase?
- How can churn be defined based on real customer behavior?
- What behavioral patterns differentiate churned vs active customers?
- Are certain product categories structurally prone to churn?

---

## 📊 Dataset
- **Source:** [Olist Brazilian E-commerce Dataset (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **Data includes:**
  - Orders
  - Customers
  - Payments
  - Products
  - Order items

---

## 🔍 Exploratory Data Analysis (EDA)

### Customer Purchase Frequency
- The vast majority of customers make **only one purchase**
- Repeat buyers represent a **very small fraction** of the customer base
- Log-scale visualization highlights extreme imbalance in customer retention

**Key Insight:**  
Low retention is a structural issue and represents a strong opportunity for targeted retention strategies.

---

## 🔄 Churn Definition Strategy

Instead of using an arbitrary threshold, churn is defined using the **empirical distribution of customer recency**.

### Churn Rule
- **Churn = 1:** Customer inactive for more than **315 days**
- **Churn = 0:** Customer placed at least one order within 315 days

📌 The 315-day threshold corresponds to the **70th percentile** of the recency distribution, ensuring a **data-driven and realistic churn definition**.

---

## 🧩 Feature Engineering — RFM Framework

Customer behavior is modeled using the **RFM methodology**:

- **Recency:** Days since last purchase
- **Frequency:** Number of orders
- **Monetary:** Total amount spent

These features provide a compact and interpretable representation of customer engagement.

Visual analyses include:
- RFM scatter plots
- Log-scaled pairplots
- Pairplots segmented by churn status

---

## 📉 Behavioral Findings

### Key Observations
- Churned customers often show **higher monetary values**
- This does **not** indicate loyalty, but rather **high-value, one-time purchases**
- Active customers tend to have more frequent, lower-ticket purchases

📌 **Interpretation:**  
Many churned users are not dissatisfied — they simply purchase products with **long replacement cycles**.

---

## 🛒 Product Category Analysis

By linking churn labels to product categories, we uncover a **category-driven churn pattern**:

### High Churn Categories
- Furniture
- Electronics
- Garden & automotive products

### Low Churn Categories
- Health
- Beauty
- Consumables

📌 **Conclusion:**  
A significant portion of churn is **structural**, driven by product type rather than poor customer experience.

---

## 🧪 Durable Goods Feature
To capture this behavior, a binary feature was engineered:
- **Durable Category = 1:** Customer purchased long-life products
- **Durable Category = 0:** Consumable-focused purchases

While durable goods customers show slightly higher churn, the difference reinforces that **repurchase behavior is product-dependent**.

---

## 📈 Business Insights & Recommendations

- Not all churn should be treated equally — some churn is **expected and structural**
- Retention strategies should prioritize **consumable product customers**
- Durable goods buyers benefit more from:
  - Cross-selling
  - Extended warranties
  - Long-term engagement strategies instead of short-term retention campaigns

---

## 🛠 Technologies Used
- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Jupyter Notebook

---

## 🚀 Next Steps
- Build a churn prediction model using RFM features
- Segment customers by churn risk
- Simulate targeted retention strategies
- Translate insights into a business dashboard

---

## 📎 Author
**Marcos Rampaso**  
Bachelor’s in Computer Science  
Federal Technological University of Paraná  
Aspiring Data Scientist & Machine Learning Engineer
