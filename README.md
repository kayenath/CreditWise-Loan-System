

# 💳 CreditWise Loan Approval Prediction System

## 📌 Overview

CreditWise is a Machine Learning-based Loan Approval Prediction System that helps financial institutions automate preliminary loan approval decisions.

The system analyzes applicant financial, demographic, and credit-related information to predict whether a loan application should be approved or rejected.

This project demonstrates a complete Machine Learning workflow including:

- Data Cleaning
- Missing Value Handling
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Encoding
- Model Training
- Model Evaluation

---

## 🎯 Problem Statement

Manual loan approval processes are often:

- Time-consuming
- Error-prone
- Subject to human bias
- Difficult to scale

This system uses historical applicant data to predict loan approval status, enabling faster and more data-driven decision making.

---

## 📊 Dataset Description

The dataset contains **1000 loan applications** with applicant financial and personal information.

### Features

| Feature | Description |
|-----------|------------|
| Applicant_Income | Applicant monthly income |
| Coapplicant_Income | Co-applicant income |
| Employment_Status | Employment type |
| Age | Applicant age |
| Marital_Status | Marital status |
| Dependents | Number of dependents |
| Credit_Score | Applicant credit score |
| Existing_Loans | Existing active loans |
| DTI_Ratio | Debt-to-Income ratio |
| Savings | Savings amount |
| Collateral_Value | Value of collateral |
| Loan_Amount | Requested loan amount |
| Loan_Term | Loan duration |
| Loan_Purpose | Purpose of loan |
| Property_Area | Property location |
| Education_Level | Educational qualification |
| Gender | Applicant gender |
| Employer_Category | Employer category |
| Loan_Approved | Target variable |

---

## 🛠 Data Preprocessing

### Missing Value Handling

Numerical Features:
- Mean Imputation using `SimpleImputer(strategy='mean')`

Categorical Features:
- Mode Imputation using `SimpleImputer(strategy='most_frequent')`

---

## 📈 Exploratory Data Analysis (EDA)

The following analyses were performed:

### Target Variable Distribution

- Loan Approval Class Distribution
- Approved vs Rejected percentages

### Univariate Analysis

- Gender Distribution
- Income Distribution
- Credit Score Distribution

### Bivariate Analysis

Comparisons against Loan Approval:

- Applicant Income vs Loan Approval
- Credit Score vs Loan Approval
- Dependents vs Loan Approval
- Education Level vs Loan Approval

### Correlation Analysis

- Correlation Matrix
- Heatmap Visualization
- Feature Importance Investigation

---

## ⚙ Feature Engineering

### Removed Features

```python
Applicant_ID
```

Reason:

- Unique identifier
- No predictive value

### Label Encoding

Applied to:

```python
Education_Level
Loan_Approved
```

### One Hot Encoding

Applied to:

```python
Employment_Status
Marital_Status
Loan_Purpose
Property_Area
Gender
Employer_Category
```

Using:

```python
OneHotEncoder(drop='first')
```

Final Dataset Shape:

```text
1000 Rows × 28 Features
```

---

## 🔍 Correlation with Loan Approval

Top Positive Correlations:

| Feature | Correlation |
|----------|------------|
| Credit_Score | 0.451 |
| Applicant_Income | 0.120 |
| Employer_Category_MNC | 0.069 |

Top Negative Correlations:

| Feature | Correlation |
|----------|------------|
| DTI_Ratio | -0.445 |
| Loan_Amount | -0.126 |
| Loan_Term | -0.087 |

### Key Insights

✅ Higher Credit Scores increase approval chances.

✅ Higher Applicant Income increases approval chances.

✅ Higher Debt-To-Income Ratio decreases approval chances.

✅ Larger Loan Amounts are less likely to be approved.

---

## 🔄 Train-Test Split

```python
test_size = 0.2
random_state = 42
```

Training Set:

```text
800 Samples
```

Testing Set:

```text
200 Samples
```

---

## 📏 Feature Scaling

Standardization performed using:

```python
StandardScaler()
```

---

## 🤖 Machine Learning Models

### 1️⃣ Logistic Regression

#### Results

```text
Precision Score : 0.7833

Recall Score    : 0.7705

Accuracy Score  : 0.8650

F1 Score        : 0.7769
```

Confusion Matrix

```text
[[126 13]
 [14 47]]
```

---

### 2️⃣ Gaussian Naive Bayes

#### Results

```text
Precision Score : 0.8036

Recall Score    : 0.7377

Accuracy Score  : 0.8650

F1 Score        : 0.7692
```

Confusion Matrix

```text
[[128 11]
 [16 45]]
```

---

### 3️⃣ K-Nearest Neighbors (KNN)

Parameters:

```python
n_neighbors = 5
```

#### Results

```text
Precision Score : 0.6275

Recall Score    : 0.5246

Accuracy Score  : 0.7600

F1 Score        : 0.5714
```

Confusion Matrix

```text
[[120 19]
 [29 32]]
```

---

## 🏆 Model Comparison

| Model | Accuracy | Precision | Recall | F1 Score |
|---------|------------|------------|------------|------------|
| Logistic Regression | 86.5% | 78.3% | 77.0% | 77.7% |
| Gaussian Naive Bayes | 86.5% | 80.4% | 73.8% | 76.9% |
| KNN | 76.0% | 62.7% | 52.5% | 57.1% |

### Best Performing Model

🏆 **Logistic Regression**

Reasons:

- Highest balanced performance
- Strong F1 Score
- Good Recall
- Interpretable model

---

## 📦 Libraries Used

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

## 🚀 Future Enhancements

- Hyperparameter Tuning
- Random Forest Classifier
- XGBoost Classifier
- Feature Selection Techniques
- Cross Validation
- Streamlit Web Application
- Loan Approval API Deployment

---

## 📷 EDA Visualizations

- Pie Chart
- Bar Chart
- Histograms
- Boxplots
- Correlation Heatmap

---

## 🧠 Learning Outcomes

This project demonstrates:

- Data Cleaning
- Missing Value Handling
- Feature Engineering
- Encoding Techniques
- Standardization
- EDA Techniques
- Classification Algorithms
- Model Evaluation Metrics

---

## 👨‍💻 Author

**Kayenath**

Layer-1 Technical Support Engineer | Aspiring Data Scientist & AI Engineer

GitHub:
https://github.com/kayenath

