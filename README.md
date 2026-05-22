# Fraud Detection Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Model](https://img.shields.io/badge/Model-Random%20Forest-green)
![Dataset](https://img.shields.io/badge/Dataset-Synthetic-orange)
![Dashboard](https://img.shields.io/badge/Dashboard-Interactive-navy)

A fraud detection analysis using a Random Forest classifier on synthetic 
banking transaction data. Includes exploratory data analysis, model training, 
feature importance analysis, and an interactive dashboard.

Built as a portfolio project demonstrating data science and AI governance 
capability applied to financial crime detection.

---

## Live Dashboard

[View Interactive Dashboard](https://brandonmuch.github.io/fraud-detection-analysis/fraud_detection_dashboard.html)

---

## Project Overview

- **Dataset:** 1,000 synthetic banking transactions (5% fraud rate)
- **Model:** Random Forest Classifier
- **Accuracy:** 100% on synthetic data
- **ROC AUC Score:** 1.0000
- **Fraud Recall:** 100% (zero missed fraud cases)
- **False Positives:** 0 (zero legitimate customers wrongly flagged)

---

## Dataset Features

| Feature | Description |
|---------|-------------|
| transaction_id | Unique transaction reference |
| amount | Transaction value in euros |
| merchant_category | Type of merchant |
| hour_of_day | Hour the transaction occurred |
| day_of_week | Day the transaction occurred |
| customer_age | Age of the account holder |
| account_age_days | How long the account has been open |
| num_transactions_last_24h | Transaction frequency in last 24 hours |
| distance_from_home_km | Distance from customer home location |
| is_fraud | Target variable (0 = legitimate, 1 = fraud) |

---

## Key Findings

**Top fraud indicators by feature importance:**

1. Account age (0.3294) — new accounts are highest risk
2. Distance from home (0.2860) — transactions far from home location
3. Transaction frequency in 24 hours (0.1172) — fraudsters move fast
4. Customer age (0.0989) — correlated with new account patterns
5. Transaction amount (0.0968) — unusually high or suspiciously low amounts

**Fraud patterns identified:**

- Fraudulent transactions have a median value of 1,603 euros vs 35 euros for legitimate
- Highest fraud rates occur between midnight and 5am and after 10pm
- Travel, online retail, and electronics show the highest fraud rates by merchant category
- Card testing pattern detected: fraudsters make tiny transactions (under 1 euro) before large ones

---

## AI Governance Commentary

This project raises real governance considerations relevant to EU AI Act compliance:

**High Risk classification** — under Article 6 and Annex III, AI systems used in financial services that make or influence decisions affecting individuals are classified as High Risk. A fraud detection model deployed by a bank would require a conformity assessment, human oversight mechanism, and registration with the EU AI database.

**Feature risk: customer age** — customer age appearing as a top four feature would require scrutiny in a governance review. The model must be tested to confirm age is not acting as a proxy for discrimination against younger customers.

**Human oversight requirement** — under the EU AI Act, High Risk AI systems must include meaningful human oversight. A real deployment would require all fraud flags to be reviewed by a qualified analyst before any customer account action is taken.

---

## File Contents

- `fraud_detection_analysis.ipynb` — full analysis notebook
- `fraud_transactions.csv` — synthetic dataset
- `fraud_detection_dashboard.html` — interactive dashboard
- `README.md` — project documentation

---

## Disclaimer

This project uses synthetic data generated for portfolio purposes. All 
transactions, customer profiles, and fraud patterns are hypothetical. 
Perfect model accuracy reflects the clarity of synthetic fraud patterns 
and does not represent real world fraud detection performance, which 
typically achieves 85 to 95% accuracy on noisy transaction data.

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

---

## References

- [EU AI Act, EUR-Lex 2024/1689](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32024R1689)
- [NIST AI Risk Management Framework](https://www.nist.gov/artificial-intelligence)
- [Scikit-learn Random Forest Documentation](https://scikit-learn.org/stable/modules/ensemble.html#forest)
```
