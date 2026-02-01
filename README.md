# EDA-on-Credit-Card-Fraud-
# Task 10 — Python EDA & Outlier Detection (Credit Card Fraud Analysis)

## 📌 Project Overview
This project performs end-to-end Exploratory Data Analysis (EDA) on a credit card transaction dataset to identify spending patterns, detect outliers, and generate business insights related to fraud risk. The focus is on transforming raw transaction data into a clean, feature-engineered dataset suitable for analytics, dashboards, and predictive modeling.

---

## 🎯 Objective
- Understand transaction behavior and data quality
- Identify and analyze unusual (high-risk) transactions
- Detect and handle outliers using statistical methods
- Generate actionable business insights for fraud prevention

---

## 🛠 Tools & Technologies
- Python
- Jupyter Notebook
- pandas
- numpy
- matplotlib

---

## 📂 Dataset Description
Each row represents a single credit card transaction.  
Key columns include:
- `Time` — Time elapsed since the first transaction
- `V1` to `V28` — Anonymized behavioral features (PCA-transformed)
- `Amount` — Transaction amount
- `Class` — Fraud label (0 = Normal, 1 = Fraud)

---

## 🔍 Steps Performed

### 1. Data Understanding
- Loaded dataset and validated structure
- Checked dataset shape, data types, and missing values
- Previewed sample records

### 2. Exploratory Data Analysis (EDA)
- Generated descriptive statistics
- Analyzed class distribution (fraud vs normal)
- Visualized transaction amount using histograms and boxplots

### 3. Outlier Detection
- Used the IQR (Interquartile Range) method on the `Amount` column
- Created a new feature: `amount_outlier` to flag unusual transactions

### 4. Outlier Handling
- Applied capping strategy instead of removal
- Created a new feature: `Amount_capped` to preserve fraud signals while improving data stability

### 5. Correlation Analysis
- Built a correlation matrix for numeric features
- Identified relationships between transaction behavior and transaction value

---

## 📊 Key Business Insights
- The dataset is highly imbalanced, with very few fraudulent transactions compared to normal ones
- Most transactions are low-value, but a small number of high-value transactions represent higher financial risk
- Fraud is driven by complex transaction behavior patterns rather than transaction amount alone
- High-risk transactions should be prioritized for monitoring and real-time fraud scoring systems

---

## 🏁 Conclusion
This project demonstrates the ability to analyze raw business data, apply statistical techniques for anomaly detection, engineer meaningful features, and translate technical findings into actionable fraud risk insights for business decision-making.

---

## 👤 Author
**Trisha**  
