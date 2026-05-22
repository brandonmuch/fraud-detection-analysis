# Fraud Detection Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Model](https://img.shields.io/badge/Model-Random%20Forest-green)
![Dataset](https://img.shields.io/badge/Dataset-Synthetic-orange)

A fraud detection analysis using a Random Forest classifier on synthetic 
banking transaction data. Built as a portfolio project covering exploratory 
data analysis, model training, feature importance, and an interactive dashboard.

---

## Live Dashboard

[View Interactive Dashboard](https://brandonmuch.github.io/fraud-detection-analysis/fraud_detection_dashboard.html)

---

## What This Project Does

Takes a dataset of 1,000 synthetic banking transactions and trains a 
classifier to distinguish fraudulent transactions from legitimate ones. 
The analysis identifies which transaction features most strongly predict 
fraud, and presents findings through an interactive browser-based dashboard.

---

## Dataset Features

| Feature | Description |
|---------|-------------|
| transaction_id | Unique transaction reference |
| amount | Transaction value in euros |
| merchant_category | Type of merchant |
| hour_of_day | Hour the transaction occurred |
| day_of_week | Day of the week |
| customer_age | Age of the account holder |
| account_age_days | How long the account has been open |
| num_transactions_last_24h | Number of transactions in the last 24 hours |
| distance_from_home_km | Distance from customer home location |
| is_fraud | Target variable (0 = legitimate, 1 = fraud) |

The dataset was generated synthetically using realistic fraud patterns 
including card testing behaviour (very small transactions before large ones), 
late night activity, new account risk, and high transaction frequency.

---

## Results

**Model:** Random Forest Classifier
**Dataset split:** 80% training, 20% test
**Accuracy:** 100% on synthetic data
**ROC AUC Score:** 1.0000
**Fraud caught:** 10 out of 10 (zero missed)
**False positives:** 0

**Top fraud indicators by feature importance:**

1. Account age in days (0.3294)
2. Distance from home in km (0.2860)
3. Number of transactions in last 24 hours (0.1172)
4. Customer age (0.0989)
5. Transaction amount (0.0968)

**Fraud patterns found in the data:**

- Median fraud transaction: 1,603 euros vs 35 euros for legitimate
- Highest fraud rates between midnight and 5am
- Travel, online retail, and electronics show the highest fraud rates by category
- Card testing pattern present: very small transactions preceding large ones

---

## AI Governance Note

A fraud detection model deployed in a real bank would be classified as 
High Risk under Article 6 and Annex III of the EU AI Act, requiring a 
conformity assessment, human oversight mechanism, and EU database registration.

Customer age appearing as a top feature would require scrutiny in a 
governance review to confirm it is not acting as a proxy for 
discrimination against younger customers.

---

## File Contents

- `fraud_detection_analysis.ipynb` — full analysis notebook
- `fraud_transactions.csv` — synthetic dataset
- `fraud_detection_dashboard.html` — interactive dashboard
- `README.md`

---

## Disclaimer

Synthetic data only. Perfect accuracy reflects how clearly defined the 
fraud patterns are in generated data. Real fraud detection on noisy 
transaction data typically achieves 85 to 95% accuracy.

---

## Author

**Brandon Muchenje**
AI Governance and GRC Analyst
BCom in Law (Cum Laude) | IBM Data Science | IAPP AIGP Training
[LinkedIn](https://www.linkedin.com/in/brandon-m-muchenje) |
[GitHub](https://github.com/brandonmuch)

---

## Related Projects

- [EU AI Act Risk Classification Tool](https://github.com/brandonmuch/eu-ai-act-classifier)
- [Model Risk Register, AI in Financial Services](https://github.com/brandonmuch/model-risk-register-ai-banking)
```
