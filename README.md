# 📊 Scalable Consumer Behavior & Delinquency Analysis (0.6M+ Records)
> **Status:** 🛠️ Active Development / In-Progress

## 🖼️ Executive Dashboard Preview
![Financial Fraud Matrix](./Screenshot%202026-05-16%20214932.png)

## 📌 Business Problem & Objective
In retail lending, identifying at-risk customer segments early is crucial to safeguarding asset quality. This project focuses on analyzing a massive dataset of **600,000+ consumer records** to identify key variables driving payment delinquency, perform predictive profiling, and build an interactive monitoring system.

To overcome the performance bottlenecks of traditional relational database transactional engines handling 0.6M+ rows, the data architecture utilizes a hybrid approach: fast file parsing via **Python (Pandas)** and modern in-memory data warehousing via **SQL (DuckDB Engine)**.

---

## 🛠️ Tech Stack & Architecture
- **Data Wrangling & Processing:** Python 3 (Pandas, Matplotlib)
- **Database Querying & Analytics Engine:** SQL (DuckDB Architecture)
- **Data Visualization & Dashboarding:** Power BI for executive storytelling, anomaly detection, and risk tracking.

---

## 🚀 Technical Implementation & SQL Insights

### 1. High-Performance SQL Querying
Instead of traditional slow row-by-row transactional processing, the raw data was connected directly to an analytical SQL engine to run rapid group aggregations across the 600,000+ records in under 5 seconds.

```sql
-- Querying quantitative aggregations directly from the data warehouse environment
SELECT risk_flag, AVG(amount) AS avg_transaction_amount
FROM 'risk.csv'
GROUP BY risk_flag;

