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

-- Querying quantitative aggregations directly from the data warehouse environment
SELECT risk_flag, AVG(amount) AS avg_transaction_amount
FROM 'risk.csv'
GROUP BY risk_flag;

### 2. Quantitative Insights & Visualizing Financial Exposure
The analytical queries revealed a massive divergence in financial exposure between normal operational baselines and flagged high-risk data points:

| Risk Category | Average Transaction Volume ($) | Risk Multiplier |
| :--- | :--- | :--- |
| **Normal** | $29.03 | Baseline (1x) |
| **High Magnitude** | $333.76 | **11.5x Higher Risk Exposure** |

The Python-generated visualization below demonstrates that high-risk or fraudulent flags are heavily concentrated in high-value transactions, proving that risk metrics scale drastically with the transaction magnitude.

![Risk Analysis Chart](risk_analysis)

---

## 📅 Project Roadmap & Phase-wise Progress

### 🟩 Phase 1: Data Ingestion & Quality Control (Completed)
- Successfully loaded, managed, and parsed **0.6 Million rows** of structural data using Python Pandas.
- Handled text formatting anomaly resolution (single-quote cleaning) and outlier detection.

### 🟩 Phase 2: Core Analysis & Interactive Visualization (Completed)
- Mapped total fraudulent exposure worth **$3.82 Million** across 7,200 verified security breaches using Power BI.
- Isolated 'es_travel' as the most critical risk category, driving over $1.53 Million in total fraud loss.
- Executed high-performance SQL aggregations to isolate the high-magnitude risk threshold at $333.76 (an 11.5x multiplier against normal operations).
- Segmented demographics to discover that Customer Age Groups 4, 3, and 2 account for the highest vulnerability frequency.

### 🟨 Phase 3: Risk Triggers & Automated Modeling (In-Progress)
- Mapping correlation between High Credit Utilization (>75%) and 30-day delinquency rates.
- Designing predictive profiling metrics to segment high Debt-to-Income (DTI) customers for automated outreach.

---
### 🔗 Connected Portfolios
* 📁 View my daily learning tracker and foundational Python exercises here: [abhishekyadav-data Master Repository](https://github.com/abhishekyadav-data/abhishekyadav-data)

---
*Developed as part of my Advanced Business Analytics Portfolio | Abhishek Yadav (Delhi University)*


