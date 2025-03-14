# Project Background
The goal of this project is to analyze a credit card transaction dataset to identify patterns associated with fraudulent activities. Using SQL, we aim to explore the dataset's structure, detect trends, and deliver actionable insights to improve fraud detection systems.

Understanding transaction patterns allows businesses to mitigate financial loss, improve security measures, and optimize operational efficiency. This analysis focuses on fraud detection but provides a framework applicable to other churn-related behaviors, such as customer retention risks.

# Data Structure Overview 
The data set consists of a single table named CreditCard with the following key columns:
| Column | Description | Data Type | 
|---|---|---|
| Time | Seconds since the first recorded transaction | FLOAT |
| V1-V28 | Principal components from PCA (anonymized) | FLOAT |
| Amount | Transaction amount (monetary value) | FLOAT |
| Class | 0 = legitimate transaction, 1 = Fraudulent | INTEGER |

# Executive Summary 
From the SQL-based analysis, we found the following key insights:
- Fraud Occurrence: Only 0.17% of the transactions in the dataset are fraudulent, indicating a severe class imbalance. Special handling (e.g., oversampling or undersampling) may be required for modeling.

- Transaction Amount: Fraudulent transactions have a higher average amount ($122) than legitimate ones ($88). Large transactions are disproportionately more likely to be fraudulent.

- Time of Fraud: Fraudulent activities tend to occur at specific hours, particularly during off-peak times (between 12 AM and 6 AM), suggesting that malicious actors exploit lower monitoring periods.

- Feature Influence: Variables V4, V11, and V17 show the most significant deviations between legitimate and fraudulent transactions, making them key predictors.

- Outliers: Certain transactions have extreme values in PCA components (e.g., V1, V2, V3 exceeding ±10), and these are strongly associated with fraud.

# Recomendations
- Enhanced Monitoring at Off-Peak Hours:
   - Increase fraud detection efforts during late-night when fraudulent transactions spike.
- Threshold-Based Alterting
   - Implement real-time alerts for transactions exceeding 100$ in value, as these are more likely to be fraudulent.
 - Feature-Driven Anomaly Detection:
    - Prioritize features V4, V11, and V17 in future machine learning models to increase prediction accuracy.
- Address Class Imbalance:
    - Use SMOTE or undersampling techniques to balance the dataset when developing machine-learning-based fraud detection models.
- Outlier-Based Monitoring:
    - Flag transactions with extreme PCA values (V1-V3 < -10 or > 10) for manual review.

