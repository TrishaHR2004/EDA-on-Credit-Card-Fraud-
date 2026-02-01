EDA Findings — Credit Card Fraud Analysis

1. Dataset Overview:
- Total Transactions: 284,807
- Total Features: 32
- Each row represents a single credit card transaction with behavioral and financial attributes.

2. Data Quality:
- No missing values detected across columns.
- All numeric features are in appropriate formats for statistical analysis and modeling.

3. Class Distribution:
- Normal Transactions (Class = 0): 284,315
- Fraud Transactions (Class = 1): 492
- The dataset is highly imbalanced, reflecting real-world fraud detection scenarios where fraudulent activity is rare but high impact.

4. Distribution Analysis:
- The transaction amount is heavily right-skewed.
- Most customer transactions are low-value, with a small number of high-value transactions forming a long tail.
- High-value transactions represent higher financial risk and require closer monitoring.

5. Outlier Detection:
- Method Used: Interquartile Range (IQR) on the Amount column.
- Approximately 11% of transactions were flagged as statistically unusual.
- An outlier flag feature (amount_outlier) was created to identify high-risk transactions without removing them.

6. Outlier Handling Strategy:
- Instead of deleting outliers, transaction values were capped using upper and lower IQR limits.
- This preserves fraud-related signals while improving data stability for analysis and modeling.
- A new feature (Amount_capped) was created to support downstream analytics.

7. Correlation Insights:
- Strong correlation observed between Amount and the outlier flag, validating the detection logic.
- Moderate correlations found between certain behavioral features (V7, V20) and transaction amount.
- The fraud label (Class) showed weak linear correlation with individual features, indicating that fraud is driven by multi-dimensional behavioral patterns.

8. Business Conclusion:
- Fraud risk cannot be identified using transaction value alone.
- High-risk transactions are better detected through a combination of behavioral patterns and anomaly detection.
- The dataset is suitable for building real-time fraud monitoring systems and predictive risk models.

9. Business Impact:
- Enables prioritization of high-risk transactions for manual review or automated alerts.
- Improves decision-making for fraud prevention teams by highlighting abnormal transaction behavior.
- Supports the development of scalable and data-driven fraud detection strategies.
