# Loan Default Prediction

![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Classification-blue.svg)
![Python](https://img.shields.io/badge/Python-3.8+-yellow.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)

## 📌 Project Overview
This project aims to build a robust machine learning classification model to predict whether a loan applicant is likely to default or successfully repay their loan based on historical applicant data. By automating the risk assessment process, financial institutions can make more informed, data-driven lending decisions.

## 📊 Dataset Details
The model was trained on a historical loan prediction dataset (`loan_data.csv`). The dataset contains the following features used for prediction:

* **Demographics:** `Gender`, `Married`, `Dependents`, `Education`
* **Financials:** `ApplicantIncome`, `CoapplicantIncome`, `LoanAmount`, `Loan_Amount_Term`
* **Background:** `Self_Employed`, `Credit_History`, `Property_Area`
* **Target Variable:** `Loan_Status` (1 for Approved/Repaid, 0 for Rejected/Default)

## 🛠️ Project Lifecycle / Phases

### 1. Data Preprocessing
- Removed irrelevant identifiers (e.g., `Loan_ID`).
- Handled missing values using statistical imputation (mode for categorical, median for numerical).
- Encoded categorical variables using `LabelEncoder`.
- Scaled numerical features using `StandardScaler` to ensure all features contribute equally to the distance calculations.

### 2. Exploratory Data Analysis (EDA)
Uncovered key insights such as:
- **Credit History** is the most significant indicator for loan approval.
- Income distributions are heavily right-skewed, requiring careful handling by the models.
- Categorical imbalances were identified (e.g., more male applicants than female).

### 3. Model Building
The data was split into an **80-20 Train-Test split**. The following algorithms were evaluated:
1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Random Forest Classifier**

### 4. Model Comparison & Results
Based on testing, **Logistic Regression** proved to be the best performing model for this specific dataset. 

**Final Model Performance:**
- **Accuracy:** 82.83%
- **Precision:** 79.2%
- **Recall:** 100.0%
- **F1-Score:** 88.4%

Because the linear relationship between Credit History and Loan Status is extremely strong, Logistic Regression outperformed the more complex tree-based models, providing highly interpretable and accurate results.

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/sahithi-manda/Loan-Default-Prediction.git
   cd Loan-Default-Prediction
   ```

2. **Install the required libraries:**
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
   ```

3. **Run the Jupyter Notebook:**
   ```bash
   jupyter notebook Loan_Default_Prediction.ipynb
   ```

## 📁 Repository Structure
- `loan_data.csv`: The dataset used for training and testing.
- `Loan_Default_Prediction.ipynb`: The complete Python source code in a Jupyter Notebook format containing all phases of the project.
- `Summary.md`: A 1-page high-level summary of the project goal, chosen model, and EDA insights.
- `README.md`: This detailed documentation file.

---
*This project was completed as part of an AI/ML Internship.*
