# Consumer Credit Risk Analytics: Modeling 1.2M Records

This project is a deep dive into high-volume financial data, focusing on identifying loan default risks. Instead of using a perfectly clean "toy" dataset, I worked with 1.2 million real-world records to build a model that prioritizes risk detection over simple accuracy.

## 📌 Why I Built This
Lending institutions lose significant revenue when defaults are missed. My goal was to build a system that can flag risky borrowers at scale. I focused heavily on **Recall** (Sensitivity) because in the credit world, a "False Negative" (missing a defaulter) is far more expensive than a "False Positive" (manual review of a safe borrower).

## 📊 The "Big Data" Strategy
Handling 1.2 million rows requires a smart approach to avoid memory issues and cluttered visuals:
* **Strategic Sampling:** I performed Exploratory Data Analysis (EDA) on a **200,000-row stratified sample**. This allowed me to discover key trends—like the fact that 'Loan Grade' and 'Interest Rate' are the biggest predictors—without crashing the notebook.
* **Full-Scale Modeling:** Once the insights were clear, I trained the final models on the **entire 1.2 million records** to ensure the model captured even the rarest patterns of default.

## 🛠️ Technical Stack
* **Language:** Python (Pandas, NumPy)
* **ML Libraries:** Scikit-Learn, Imbalanced-Learn
* **Key Models:** Weighted Random Forest, Logistic Regression
* **Visualization:** Matplotlib, Seaborn

## 🚀 Key Challenges & Solutions
* **The Imbalance Problem:** Only a small fraction of borrowers actually default. A standard model would just guess "Safe" for everyone. I solved this using **Random Undersampling** and **Class Weighting** (`class_weight='balanced'`).
* **Feature Engineering:** I identified that borrower income and debt-to-income ratios were critical, but only when cross-referenced with the loan term.

## 📈 Results
The final **Weighted Random Forest** model achieved a **Recall of 68.2%**. This means the system successfully identifies nearly 7 out of 10 potential defaults before they happen, providing a significant safety net for the lending process.

---
### 🔗 Live Project
You can view the full interactive notebooks and the 1.2M row dataset on my Kaggle profile:
[View on Kaggle](https://www.kaggle.com/vineethtangedudona)
