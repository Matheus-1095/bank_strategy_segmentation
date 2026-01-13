# 🏦 Bank Client Segmentation (K-Means Clustering)

This repository contains an end-to-end **Customer Segmentation** project using a credit card customer dataset.  
The goal is to group customers into meaningful behavioral segments using **K-Means clustering**, enabling **targeted business actions** such as revenue growth, churn reduction, and risk mitigation.

---

## 📌 Business Problem
Banks often apply generic campaigns and credit policies to all customers, leading to:
- low campaign conversion rates
- inefficient marketing spend
- higher default risk for vulnerable customers
- missed upsell opportunities for high-value customers

This project solves that by creating **data-driven customer clusters** that can be activated in CRM and credit strategy decisions.

---

## 🎯 Project Objectives
✅ Build customer clusters using **unsupervised learning (K-Means)**  
✅ Identify different spending and payment behaviors  
✅ Profile clusters to make them **explainable and actionable**  
✅ Propose strategies to generate business value through:
- **Revenue increase**
- **Cost reduction**
- **Risk / loss reduction**

---

## 📊 Dataset Overview
The dataset contains **8,950 customers** and the following features:

- `BALANCE`, `BALANCE_FREQUENCY`
- `PURCHASES`, `ONEOFF_PURCHASES`, `INSTALLMENTS_PURCHASES`
- `PURCHASES_FREQUENCY`, `ONEOFF_PURCHASES_FREQUENCY`, `PURCHASES_INSTALLMENTS_FREQUENCY`
- `CASH_ADVANCE`, `CASH_ADVANCE_FREQUENCY`, `CASH_ADVANCE_TRX`
- `PURCHASES_TRX`
- `CREDIT_LIMIT`
- `PAYMENTS`, `MINIMUM_PAYMENTS`, `PRC_FULL_PAYMENT`
- `TENURE`

The `CUST_ID` column is used only for identification and exporting the final segmentation output.

---

## 🧠 Methodology
### 1) Data Preprocessing
- Missing value handling (median imputation)
- Feature scaling with `StandardScaler`

### 2) Model Training
- K-Means clustering (8 clusters)

### 3) Cluster Evaluation
- Elbow Method (WCSS)
- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Index

### 4) Cluster Interpretation
- Cluster profiling using mean values per feature
- Feature importance by z-score per cluster (interpretability)
- PCA projection for 2D visualization (exploratory)

---

## ✅ Key Output
The final deliverable is a customer segmentation table:

- `CUST_ID`
- `cluster_id`

This output can be integrated into:
- CRM campaigns (push / email / WhatsApp)
- credit policy decisions (limit control, risk rules)
- retention playbooks

---

## 💰 Business Application (Monetization Strategies)
Each cluster can be linked to a strategy based on customer behavior:

### 📈 Strategy 1 — Revenue Growth (Upsell + Interchange)
Target clusters: **high spenders / high engagement**
- premium card upgrade
- partner cashback campaigns
- cross-sell insurance and investments

**KPIs:** spend uplift, conversion rate, retention

---

### 📉 Strategy 2 — Risk Reduction (Loss Prevention)
Target clusters: **cash advance heavy users / low full payment**
- replace cash advance with structured loan products
- early warning nudges + renegotiation
- controlled credit policy adjustments

**KPIs:** cash advance reduction, payment improvement, delinquency reduction

---

### 🔁 Strategy 3 — Activation & Engagement
Target clusters: **low usage customers**
- first purchase incentives
- category-specific cashback offers
- loyalty and frequency campaigns

**KPIs:** transaction growth, engagement uplift

---

## 📌 Expected Value (Indicative)
This segmentation enables measurable value through:
- **profit increase** via targeted upsell/cross-sell
- **loss reduction** by protecting vulnerable credit profiles
- **cost reduction** by avoiding low-propensity campaigns

A realistic expected impact for a portfolio of 8,950 customers can range from:
- **Conservative:** ~$30K/year  
- **Moderate:** ~$100K/year  
- **Optimistic:** ~$250K/year+

Final results should be validated through **A/B testing** in production.

---

## 🛠️ Tech Stack
- Python
- Pandas / NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

