# LoanTap – Credit Risk Modeling Using Logistic Regression

This project involves developing a logistic regression model to assess credit risk for personal loans at LoanTap. The objective is to determine whether a loan applicant is likely to default or repay, based on various demographic, financial, and credit history features.

---

## 📊 Problem Statement

LoanTap, an online lending platform, wants to enhance its underwriting model to screen applicants for personal loans. The task is to predict loan default risk using logistic regression and evaluate the trade-off between maximizing approvals and minimizing defaults.

---

## 📁 Dataset Features

Key variables include:
- `loan_amnt`, `term`, `int_rate`, `installment`
- `emp_length`, `home_ownership`, `annual_inc`, `dti`
- `grade`, `sub_grade`, `loan_status` (Target)
- `pub_rec`, `revol_util`, `total_acc`, `mort_acc`, `pub_rec_bankruptcies`

---

## 🛠️ Tools & Techniques

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn, Statsmodels
- Logistic Regression
- ROC-AUC, Precision-Recall Curve, Confusion Matrix

---

## 🔍 Workflow Summary

1. **EDA**
   - Visualized class imbalance, credit behavior across income and loan grades
   - Analyzed default rates across employment length, home ownership, and purpose
2. **Feature Engineering**
   - Created flags for `pub_rec`, `mort_acc`, and `pub_rec_bankruptcies`
   - Handled outliers and missing values
3. **Scaling**
   - StandardScaler applied for numerical features
4. **Modeling**
   - Logistic Regression using Sklearn & Statsmodels
   - Feature importance extracted from model coefficients
5. **Evaluation**
   - ROC-AUC Curve
   - Precision-Recall Curve
   - Confusion Matrix and classification report

---

## 📌 Key Findings

- Default rates were higher in lower grades (`G`, `F`) and high DTI ranges.
- `annual_inc`, `int_rate`, `emp_length`, and `revol_util` were strong predictors.
- Precision-recall tradeoff highlighted the need for a balanced risk threshold.
- Precision was prioritized to avoid funding high-risk applicants (false positives).

---

## 🧪 Answers to Business Questions

- ✅ **% Fully Paid**: Majority of applicants (~85–90%) had fully paid their loans.
- ✅ **Correlation**: Loan amount and installment were strongly correlated.
- ✅ **Home Ownership**: Most people reported `MORTGAGE`.
- ✅ **Grade A more likely to repay**: ✅ **True**
- ✅ **Top job titles**: `Engineer`, `Manager`
- ✅ **Bank’s focus**: **Precision** (to reduce default risk)
- ✅ **Gap in Precision vs Recall**: Large gap = more rejections of good customers or approval of risky ones.
- ✅ **Highly influential features**: `int_rate`, `dti`, `revol_util`, `grade`
- ✅ **Geography impacts?**: ✅ **Yes**

---

## 📂 Files in this Repository

- `LoanTap_Logistic_Regression.ipynb` – Complete notebook
- `LoanTapData.csv` – Dataset
- `README.md` – Project overview
- Optional: PDF summary or HTML export

---

## 💡 Business Recommendations

- Deploy a precision-optimized threshold to reduce false approvals.
- Use credit utilization and public records to flag high-risk applicants.
- Consider geographic data and job title in future models.
- Regularly retrain models to adapt to market and behavior shifts.

---

## 🤝 Connect

Let’s collaborate or discuss improvements — feel free to connect on [LinkedIn](https://www.linkedin.com/in/varshil-gandhi-08470b200/)

