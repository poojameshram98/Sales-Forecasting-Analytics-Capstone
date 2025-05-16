
# 📊 Sales Forecasting & BI Dashboard for Hardware Distribution

An end-to-end data analytics capstone project simulating real-world business challenges. This project combines SQL-based ETL, interactive dashboards in Power BI, and predictive modeling using Python (XGBoost) to forecast monthly sales for a hardware distribution company.

---

## 📌 Project Overview

This project addresses the need for centralized, accurate, and forward-looking sales intelligence in a simulated business setting. It provides a full analytics pipeline—from raw data extraction to machine learning forecasting—to support business decisions.

---

## 🔧 Tools & Technologies Used

- **SQL (MySQL Workbench)** – Data cleaning, joins, and currency normalization  
- **Power BI** – Data visualization, KPI tracking, return analysis  
- **Python** – XGBoost model development, preprocessing with Pandas & Scikit-learn  
- **Jupyter Notebook** – Code development and documentation  
- **GitHub** – Version control and documentation  
- **Power Query** – ETL inside Power BI  

---

## 🔄 Workflow Overview

```
SQL → Data Cleaning → Feature Engineering (Python) → XGBoost Forecasting → Power BI Dashboard
```

---

## 📊 Step-by-Step Implementation

### 📍 Step 1: Data Collection & Cleaning (SQL)

- Loaded 150,000+ sales records
- Removed:
  - Invalid entries (e.g., -1 or 0 sales)
  - Duplicate transactions
  - Blank or irrelevant regions (e.g., New York, Paris)
- Standardized currencies: USD → INR (1 USD = 85 INR)
- Joined relational tables (customers, products, markets, date)

### 📍 Step 2: Feature Engineering (Python)

- Created features:
  - `month`, `quarter`, `price_after_discount`
  - Lag variables: `lag_1`, `lag_2`
  - `Marketing Efficiency`
- Encoded categorical variables
- Normalized numeric columns

### 📍 Step 3: Predictive Modeling (XGBoost)

- Trained XGBoost regressor to forecast next-month sales
- Metrics:
  - **R² Score:** 0.99
  - **MAE:** 160,997
  - **RMSE:** 184,067
- Key drivers: Quarter, Discount, Customer Segment

### 📍 Step 4: Power BI Dashboard

- Interactive filters for region, time, customer, and product
- Pages include:
  - MoM & YoY Sales Trends
  - Product & Customer Returns
  - Forecast View (XGBoost output)
  - Market & Category-level drilldowns

---

## 📈 Business Impact

| Area               | Outcome                                  |
|--------------------|-------------------------------------------|
| Forecast Accuracy  | 99% (R²) with low RMSE & MAE              |
| Manual Reporting   | Reduced by 30%                            |
| Decision-Making    | Enabled proactive inventory & campaign planning |

---

## 🖼️ Screenshots (See `/dashboard/screenshots/`)

- Year-over-year trends
- Forecast view
- Product performance
- Customer return analysis

---

## 📂 Repository Structure

```
sales-forecasting-analytics-capstone/
├── data/
│   ├── raw/
│   └── cleaned/
├── notebooks/
│   ├── eda_visuals.ipynb
│   └── model_xgboost.ipynb
├── sql_scripts/
│   ├── data_cleaning.sql
│   └── joins_transformations.sql
├── dashboard/
│   ├── PowerBI_Dashboard.pbix
│   └── screenshots/
├── model/
│   ├── xgboost_model.pkl
│   └── metrics.txt
├── README.md
├── requirements.txt
└── LICENSE
```

---

## 🧠 Future Improvements

- Connect Power BI to live SQL for real-time analytics
- Automate forecast updates using APIs or Power Automate
- Expand dashboard to include inventory, marketing ROI, and NPS
- Implement advanced models (Prophet, LSTM)
- Add clustering models for customer segmentation

---


## ✍️ Author

**Pooja Meshram**  
MBA in Data Science, CSTU | Salesforce Certified | Data Analyst  
📧 poojameshram98@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/pooja-meshram-8659a31b7)
