# LoanClassification

A custom-built **Decision Tree Classifier** implemented from scratch in Python to predict **loan status** (approved or not) based on customer data. This project demonstrates full-cycle machine learning — from preprocessing a real-world dataset, encoding features, and model training, to evaluation and comparison against scikit-learn’s `DecisionTreeClassifier`.

---

## 📊 Problem Statement

The goal is to classify whether a loan should be approved based on features like income, education level, loan intent, home ownership status, previous defaults, etc.

This is a **binary classification** task:
- **0** → Loan Denied  
- **1** → Loan Approved

---

## 🧰 Technologies Used

- Python 3
- NumPy
- Pandas
- Scikit-learn (for benchmarking)
- Matplotlib / Seaborn (optional for visualization)

---

## 📁 Dataset

The dataset (`loan_data.csv`) contains anonymized information on individuals applying for loans.  
Features include:
- `person_income`
- `person_age`
- `person_gender`
- `person_education`
- `person_home_ownership`
- `loan_intent`
- `loan_amnt`
- `loan_int_rate`
- `previous_loan_defaults_on_file`
- `loan_status` (target)

---

## 🧹 Data Preprocessing

1. **Missing Value Handling:**  
   → Checked and confirmed no null values.

2. **Feature Encoding:**  
   - Binary encoding for `gender` and `previous_loan_defaults_on_file`
   - Ordinal encoding for `education`
   - One-hot encoding for `home_ownership` and `loan_intent`

3. **Scaling:**  
   → No scaling needed, as Decision Trees are not affected by feature scales.

---

## 🌲 Custom Decision Tree Classifier

Implemented from scratch with support for:
- Splitting by **Information Gain (Entropy)** or **Gini Impurity**
- Depth control and minimum sample split
- Recursive binary tree building
- Pure node detection
- Evaluation: Accuracy, Precision, Recall, F1 Score

---

## 🔬 Evaluation & Comparison

| Metric        | Custom Decision Tree | Sklearn DecisionTreeClassifier |
|---------------|----------------------|--------------------------------|
| Accuracy      | ✅                    | ✅                              |
| Precision     | ✅ (better)           | —                              |
| Recall        | ✅ (better)           | —                              |
| F1 Score      | ✅ (better)           | —                              |

✅ Our custom model slightly outperforms the sklearn implementation on this dataset.

---

