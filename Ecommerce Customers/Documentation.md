# 📘 Project Documentation - Ecommerce Spending Prediction

This project aims to predict the **yearly amount spent by e-commerce customers** based on their profile and usage data.  
The purpose is to understand which features most influence spending behavior and build a simple predictive model using **Linear Regression**.


## Dataset Description

The dataset contains customer information, including:

| Column | Description |
|---------|--------------|
| Avg. Session Length | Average time spent per session |
| Time on App | Average minutes spent on the mobile app |
| Time on Website | Average minutes spent on the website |
| Length of Membership | Years since the customer joined |
| Yearly Amount Spent | Target variable to predict |


## Data Preprocessing

- Dropped irrelevant columns: `Email`, `Address`, and `Avatar`.
- Scaled numerical features using `StandardScaler` for consistent feature scaling.
- Split the dataset into **training (75%)** and **testing (25%)** subsets.


## Model Training

Used **Linear Regression** from Scikit-learn.

```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)



###Model Evaluation

---Mean_Squared_Error , Mean_Absolute_Error , R²_score

## Model Evaluation

| Metric | Train | Test |
|---------|--------|--------|
| R² Score | 98.39% | 98.51% |
| MSE | 99.35 | 96.39 |

The results show excellent generalization performance, indicating no signs of overfitting.


## Visualization

Two main visualizations were created:
1. **Actual vs Predicted Plot** – shows how close predictions are to real values.
2. **Residual Plot** – confirms even error distribution, proving a balanced model.


---
**Note:** This project was created for self-improvement to strengthen my understanding of machine learning fundamentals, particularly Linear Regression.
