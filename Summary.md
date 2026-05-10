# Loan Default Prediction - Project Summary

## Project Goal
The primary objective of this project is to build a machine learning model capable of predicting whether a loan applicant is likely to default or successfully repay their loan based on historical applicant data. This involves cleaning the data, performing exploratory data analysis, extracting meaningful features, and training various classification models to find the best performing one.

## Chosen Model
After evaluating Logistic Regression, Decision Tree, and Random Forest algorithms, **Logistic Regression** was selected as the final model. It outperformed the tree-based models on this specific dataset, likely due to its ability to strongly capture the linear relationship between the most important features (like Credit History) and the target variable.

## Final Accuracy
The final accuracy achieved by the chosen Logistic Regression model on the test dataset (20% holdout) is **82.83%**. 
- **Precision:** 0.79
- **Recall:** 1.00
- **F1-Score:** 0.88

## Insights from Exploratory Data Analysis (EDA)
During the Exploratory Data Analysis phase, several key insights were uncovered:
1. **Credit History is Paramount:** There is a very strong correlation between an applicant's credit history and their loan approval status. Applicants with a positive credit history (`1.0`) are overwhelmingly more likely to have their loans approved compared to those without.
2. **Income Distributions are Skewed:** Both Applicant Income and Loan Amount distributions are heavily right-skewed, indicating a majority of applicants request moderate loan amounts with average incomes, while a few outliers request very large loans or have very high incomes.
3. **Categorical Imbalances:** The dataset contains significantly more male applicants than female applicants, more married applicants than unmarried, and more graduates than non-graduates. These imbalances were handled through appropriate metric evaluation (like F1-Score) to ensure the model wasn't biased toward the majority classes.
