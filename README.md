# Consumer-Credit-Risk-Analytics
"An end-to-end analysis and predictive modeling project for consumer loan portfolios."
# 🏦 Strategic Credit Risk & Consumer Loan Analytics

## 📊 Project Overview
This project analyzes a high-volume **Consumer Credit Portfolio** containing over 200,000 historical loan records. The objective is to identify the core drivers of credit risk and build a predictive engine to assist in lending decisions.

**Phase 1** (Current) focuses on Exploratory Data Analysis (EDA) and "Reverse-Engineering" the bank's decision-making logic.

---

## 🔍 Key Business Insights (Phase 1)

### 1. 🛡️ The FICO "Gatekeeper"
The data reveals a near-perfect inverse relationship between credit scores and interest rates. A borrower with a FICO score of **800** pays nearly **half** the interest of someone at **660**. Regardless of income or job history, the FICO score acts as the primary "filter" for loan pricing.

### 2. ⚖️ The Joint Application Truth
Contrary to popular belief, joint applicants are not "safer" borrowers. My analysis found that **Joint Applicants carry double the debt-to-income ratio (32% DTI)** compared to individual borrowers (18% DTI). This suggests that consumers often apply together out of financial necessity rather than credit strength.

### 3. 📈 Strategic Risk Pricing
The platform aggressively prices risk based on **Loan Term** and **Purpose**. 
* **60-Month Loans** carry a significant interest premium over 36-month loans.
* **Small Business Loans** are treated as high-volatility, resulting in higher rates regardless of the borrower's personal credit score.

---

## 🛠️ Data Strategy
* **Data Cleaning:** Removed features with >50% missing values and filtered for "Closed" loans (Fully Paid vs. Charged Off) to ensure a clean target variable for modeling.
* **Feature Engineering:** Identified "Golden Features" (FICO, DTI, Term, Grade) that provide the highest signal for risk prediction.
* **Source:** Analyzed via a large-scale FinTech lending dataset.

---

## 🚀 Next Steps: Phase 2
Having identified the key drivers of risk, the next phase of the project involves building a **Machine Learning Classifier** to predict the likelihood of loan default at the point of application.

---
