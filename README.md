# 🚗 Car Insurance Policy & Claims Analysis

---

## 📌 Project Overview

This is an end-to-end **SQL data analysis project** on **58,592 car insurance policies** aimed at solving real business problems faced by insurance companies — identifying high-risk customer segments, evaluating the impact of vehicle safety features on claim rates, and supporting data-driven decisions in underwriting and premium pricing.

---

## 🗂️ Dataset

| Detail | Info |
|---|---|
| **Source** | Kaggle — Car Insurance Claim Prediction |
| **Files** | `car_insurance.csv` (train), `test.csv` |
| **Size** | 58,592 rows · 44 columns |
| **Target Column** | `is_claim` → 1 = Claim Filed, 0 = No Claim |
| **Link** | https://www.kaggle.com/datasets/ifteshanajnin/carinsuranceclaimprediction-classification |

---

## 🛠️ Tools Used

- **SQL Server Management Studio (SSMS)**
- SQL Server (Local Instance)

---

## 📁 Repository Structure

```
📁 Car-Insurance-SQL-Analysis
   ├── 📄 README.md                     ← You are here
   ├── 📄 car_insurance_analysis.sql    ← All 15 queries with comments
   ├── 📄 car_insurance.csv             ← Training dataset
   └── 📄 test.csv                      ← Test dataset
```

---

## ❓ Business Problems Solved

| # | Business Question | SQL Concept Used |
|---|---|---|
| 1 | What is the overall claim rate across the portfolio? | Aggregation |
| 2 | Which fuel type carries the highest claim risk? | GROUP BY |
| 3 | Which car segment is the riskiest? | GROUP BY |
| 4 | Does transmission type affect claim rate? | GROUP BY |
| 5 | Which policyholder age group files the most claims? | CASE WHEN |
| 6 | Do older vehicles have higher claim rates? | CASE WHEN |
| 7 | Do long-tenure customers file fewer claims? | CASE WHEN |
| 8 | Does NCAP safety rating reduce claim frequency? | GROUP BY |
| 9 | Do more airbags mean fewer claims? | GROUP BY |
| 10 | Urban vs Rural — where do most claims originate? | CASE WHEN |
| 11 | Which area clusters have the highest claim rates? | HAVING |
| 12 | Does a higher safety feature score reduce claims? | Derived Column |
| 13 | What does the highest-risk customer profile look like? | WHERE Filters |
| 14 | Rank all car segments by claim rate | RANK() Window Function |
| 15 | What is the cumulative claim exposure by region? | SUM() OVER Window Function |

---

## 🧠 SQL Concepts Demonstrated

- **Aggregate Functions** — `COUNT()`, `SUM()`, `ROUND()`
- **CASE WHEN** — Customer segmentation by age, car age, tenure, density
- **Conditional Aggregation** — `SUM(CASE WHEN is_claim = 1 ...)`
- **Window Functions** — `RANK() OVER`, `SUM() OVER` for rankings and running totals
- **HAVING Clause** — Filtering groups with insufficient data
- **GROUP BY / ORDER BY** — Multi-dimensional claim analysis
- **Derived Calculations** — Safety feature scoring across 7 columns

---

## 💡 Key Business Insights

> *(Fill these in after running the queries in SSMS)*

- 📊 Overall claim rate across 58K policies = **X%**
- ⛽ **[Fuel type]** had the highest claim rate among fuel types
- 🚘 **[Segment]** was the riskiest car segment in the portfolio
- 👤 **Young policyholders** with older cars showed significantly higher claim rates
- 🛡️ Higher NCAP safety ratings correlated with **[lower/higher]** claim frequency
- 🏙️ **Metro/Urban** areas showed higher claim rates than rural zones
- 📍 Area cluster **[X]** had the highest regional claim rate

---

## ▶️ How to Run This Project

1. Download the dataset from the Kaggle link above
2. Open **SQL Server Management Studio (SSMS)**
3. Create the database:
```sql
CREATE DATABASE car_insurance_db;
USE car_insurance_db;
```
4. Import `car_insurance.csv` via **Tasks → Import Flat File**
5. Open `car_insurance_analysis.sql`
6. Run each query section by section

---
