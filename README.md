# CreditWise Loan System

## 📌 Project Overview
CreditWise Loan System is a supervised machine learning project that predicts whether a loan application should be approved or not based on applicant financial, demographic, and credit-related information.

The objective is to assist financial institutions in making data-driven loan approval decisions.

---

## 📊 Dataset Overview
- Total Records: 1000
- Features: 20 (before preprocessing)
- Target Variable: `Loan_Approved`
- Numerical Features: Income, Credit Score, DTI Ratio, Loan Amount, etc.
- Categorical Features: Employment Status, Marital Status, Property Area, etc.

⚠ The dataset file (`loan_approval_data.csv`) is excluded from this repository using `.gitignore`.

---

## 🛠 Project Workflow

### 1️⃣ Data Cleaning
- Handled missing values using:
  - Mean imputation for numerical columns
  - Most frequent value imputation for categorical columns
- Removed `Applicant_ID` column (not useful for prediction)

---

### 2️⃣ Exploratory Data Analysis (EDA)
Performed:
- Class distribution analysis (Loan Approved vs Not Approved)
- Income distribution analysis
- Boxplots for outlier detection
- Correlation heatmap
- Feature-wise relationship analysis

Key Observations:
- Credit Score has strong positive correlation with loan approval.
- DTI Ratio has strong negative correlation with loan approval.

---

### 3️⃣ Feature Engineering
Created new features:
- `DTI_Ratio_sq`
- `Credit_Score_sq`

Removed original `DTI_Ratio` and `Credit_Score` in engineered version.

---

### 4️⃣ Encoding
- Label Encoding:
  - Education_Level
  - Loan_Approved (Target)

- One-Hot Encoding:
  - Employment_Status
  - Marital_Status
  - Loan_Purpose
  - Property_Area
  - Gender
  - Employer_Category

---

### 5️⃣ Train-Test Split
- 80% Training Data
- 20% Testing Data
- `random_state = 42`

---

### 6️⃣ Feature Scaling
- StandardScaler used to normalize numerical values.

---

## 🤖 Models Implemented

### 🔹 Logistic Regression
After Feature Engineering:
- Accuracy: 87.5%
- Precision: 0.79
- Recall: 0.80
- F1 Score: 0.79

Confusion Matrix:
[[126 13]
 [12  49]]

---

### 🔹 K-Nearest Neighbors (KNN)
- Accuracy: 75.5%
- Precision: 0.62
- Recall: 0.50
- F1 Score: 0.55

---

### 🔹 Naive Bayes
- Accuracy: 86.5%
- Precision: 0.78
- Recall: 0.77
- F1 Score: 0.77

---

## 🏆 Best Model
Logistic Regression performed best with highest accuracy (87.5%) and balanced precision-recall performance.

---

## 📈 Key Insights
- Higher Credit Score significantly increases approval chances.
- Higher DTI Ratio reduces approval probability.
- Loan Amount negatively correlates with approval.
- Income has moderate positive impact.

---

## 🚀 Future Improvements
- Hyperparameter tuning (GridSearchCV)
- Cross-validation
- Model deployment using Flask or Streamlit
- Advanced models (Random Forest, XGBoost)

---

## 🧰 Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 👨‍💻 Author
Ravish