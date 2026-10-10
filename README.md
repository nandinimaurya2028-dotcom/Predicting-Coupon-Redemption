# Predicting-Coupon-Redemption

A Data Mining & Warehousing project to analyze customer behavior and predict coupon redemption using Python/Jupyter, Scikit-learn, Weka, and Power BI.
Objective
Predict whether a coupon will be redeemed and analyze redemption patterns by customer demographics and campaign type.
`redemption\_status = 0`: Not redeemed
`redemption\_status = 1`: Redeemed
Dataset
Source: Kaggle — Predicting Coupon Redemption  
Training data: 78,369 records  
CSV files (7): `train.csv`, `test.csv`, `campaign\_data.csv`, `customer\_demographics.csv`, `customer\_transaction\_data.csv`, `item\_data.csv`, `coupon\_item\_mapping.csv`.
Workflow
Load and inspect all seven CSVs.
Check data quality and missing values, then clean relevant data.
Merge relevant data using shared IDs such as `customer\_id` and `campaign\_id`.
Create customer transaction features: total quantity, total sales value, transaction count, and discount totals.
Encode categorical features for modelling.
Train and evaluate a Random Forest model in Python using an 80/20 split; evaluate separately in Weka with 10-fold cross-validation.
Explore trends and campaign performance in a Power BI dashboard.
Algorithm
Random Forest combines predictions from multiple decision trees.
Python: 100 trees, `random\_state=42`, `class\_weight="balanced"`, 80/20 train-test split.
Weka: 100 trees and 10-fold cross-validation.
Dashboard Findings
Total sales value: 151.80M
Total transactions: 60M
Unique customers: ~1K
Coupons redeemed: 729
Overall redemption rate: 0.93%
Campaign X redemption rate: 1.10%
Campaign Y redemption rate: 0.45%
Age group 36–45 has the highest average sales value.
Model Results and Limitation
Python: ~98% accuracy; redeemed-class recall shown as 0.12. The presentation also mentions a refined model with recall 0.68.
Weka: 98.95% accuracy, ROC Area 0.824, Kappa 0.0607, redeemed-class recall 0.038 (28 of 729 redeemed cases identified).
The data is highly imbalanced: 77,640 not redeemed vs 729 redeemed. Therefore, accuracy alone is not enough; precision, recall, and F1-score also matter. These results do not prove that the project increased redemption or revenue.
Run the Project
Install Python and Jupyter.
Install packages:
```bash
   pip install pandas scikit-learn matplotlib jupyter
   ```
Download the seven CSV files from Kaggle and place them where the notebook expects them.
Open `DMW\_Coupon\_Redemption.ipynb` and run cells in order.
Open `DMW\_PROJECT.pbix` in Power BI Desktop to view the dashboard.
References
Kaggle Predicting Coupon Redemption dataset; Breiman (2001), “Random Forests”; Weka documentation; Microsoft Power BI documentation; Python, Pandas, Scikit-learn, and Jupyter documentation.
Author: Nandini Maurya 
