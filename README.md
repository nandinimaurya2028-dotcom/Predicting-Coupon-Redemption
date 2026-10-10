# Coupon Redemption & Customer Behavior (DMW)

## Project Overview
This Data Mining & Warehousing project analyzes customer behavior and predicts coupon redemption using Python, Jupyter Notebook, Weka, and Power BI.

**Objective:** Predict whether a coupon will be redeemed and analyze customer behavior across age groups and campaign types.

- `0` = Not Redeemed
- `1` = Redeemed

## Dataset
**Source:** Kaggle – Predicting Coupon Redemption  
**Training Records:** 78,369  
**CSV Files:** 7

- train.csv
- test.csv
- campaign_data.csv
- campaign_item_mapping.csv
- customer_demographics.csv
- customer_transaction_data.csv
- item_data.csv

## Tools & Technologies
- Python and Jupyter Notebook
- Pandas and Scikit-learn
- Random Forest Algorithm
- Weka
- Power BI

## Project Workflow
1. Loaded and inspected seven CSV files.
2. Checked data quality and missing values.
3. Cleaned and merged relevant datasets using common IDs.
4. Created customer transaction features such as total quantity, sales value, transaction count, and discounts.
5. Prepared categorical data for machine learning.
6. Trained and evaluated a Random Forest model.
7. Created a Power BI dashboard to analyze customer behavior and campaign performance.

## Algorithm Used
**Random Forest** combines multiple decision trees to make predictions.

- Python: 100 trees, balanced class weights, and an 80/20 train-test split.
- Weka: 100 trees and 10-fold cross-validation.

## Power BI Dashboard Insights
- Total Sales Value: 151.80M
- Total Transactions: 60M
- Unique Customers: Approximately 1K
- Coupons Redeemed: 729
- Overall Redemption Rate: 0.93%
- Campaign X Redemption Rate: 1.10%
- Campaign Y Redemption Rate: 0.45%
- Age Group 36–45 has the highest average sales value.

## Model Results
**Python:** Approximately 98% accuracy; redeemed-class recall was 0.12 in the displayed report. The presentation also mentions a refined model with recall of 0.68.

**Weka:**
- Accuracy: 98.95%
- ROC Area: 0.824
- Kappa: 0.0607
- Redeemed-class recall: 0.038 (28 of 729 redeemed cases identified)

The dataset is highly imbalanced, with 77,640 non-redeemed records and 729 redeemed records. Therefore, accuracy alone is not enough to judge model performance; precision, recall, and F1-score are also important.

## How to Run
1. Install Python and Jupyter Notebook.
2. Install the required libraries:

   `pip install pandas scikit-learn matplotlib jupyter`

3. Download the dataset from Kaggle and place the CSV files in the paths expected by the notebook.
4. Open `DMW_Coupon_Redemption.ipynb` and run the cells in order.
5. Open the Power BI `.pbix` file in Power BI Desktop to view the dashboard.

## References
- Kaggle – Predicting Coupon Redemption Dataset
- Breiman (2001) – Random Forests
- Weka Documentation
- Microsoft Power BI Documentation
- Python, Pandas, Scikit-learn, and Jupyter Documentation

## Author
**Nandini Maurya**  
SY B.Sc. – Data Mining & Warehousing Project
