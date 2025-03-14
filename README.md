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

 
