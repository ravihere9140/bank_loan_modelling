# bank_loan_modelling
# 🏦 Bank Personal Loan Modelling

This project aims to predict whether a bank customer will accept a personal loan offer based on their demographic and financial attributes. Using machine learning models, we analyze the patterns that influence loan acceptance decisions and optimize classification performance.

---

## 📁 Dataset Overview

- **File:** `Bank_Personal_Loan_Modelling.xlsx`
- **Location:** `/content/archive (2).zip`
- **Sheet:** `Data`
- **Total Records:** 5000
- **Target Variable:** `PersonalLoan` (1 = Accepted, 0 = Not Accepted)

### Features Description:

| Feature            | Description                                                |
|--------------------|------------------------------------------------------------|
| ID                 | Customer ID (unique identifier)                            |
| Age                | Customer’s age (in years)                                  |
| Experience         | Work experience (in years)                                 |
| Income             | Annual income (in $000)                                    |
| ZIPCode            | Residential ZIP Code                                       |
| Family             | Family size                                                |
| CCAvg              | Average monthly credit card spend (in $000)                |
| Education          | Education level (1 = Undergrad, 2 = Graduate, 3 = Advanced)|
| Mortgage           | Value of house mortgage (in $000)                          |
| SecuritiesAccount  | 1 if customer has a securities account                     |
| CDAccount          | 1 if customer holds a certificate of deposit account       |
| Online             | 1 if enrolled in online banking                            |
| CreditCard         | 1 if customer has a credit card with the bank              |
| PersonalLoan       | **Target variable** – 1 if accepted loan, 0 otherwise      |

---

## 🎯 Objective

To develop a predictive model using machine learning that helps the bank identify potential customers who are likely to accept personal loan offers.

---

## 🔧 Technologies Used

- Python
- Pandas, NumPy
- scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook / Google Colab

---

## 🚀 Steps Performed

1. Loaded the dataset from within a ZIP archive
2. Cleaned and renamed columns for clarity
3. Explored data patterns using EDA (distributions, correlations, outliers)
4. Preprocessed the data (normalization, encoding if necessary)
5. Trained various ML models:
   - Logistic Regression
   - Decision Tree
   - Random Forest
   - KNN
6. Evaluated models using metrics like:
   - Accuracy
   - Confusion Matrix
   - ROC-AUC Score
7. Identified top features influencing loan decisions

---

## 📦 How to Run

```python
from zipfile import ZipFile
import pandas as pd

with ZipFile('/content/archive (2).zip') as z:
    with z.open('Bank_Personal_Loan_Modelling.xlsx') as f:
        data = pd.read_excel(f, sheet_name='Data')

# Rename columns
data.columns = ["ID", "Age", "Experience", "Income", "ZIPCode", "Family",
                "CCAvg", "Education", "Mortgage", "PersonalLoan", 
                "SecuritiesAccount", "CDAccount", "Online", "CreditCard"]

