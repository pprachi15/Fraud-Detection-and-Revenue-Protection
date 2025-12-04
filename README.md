# Fraud Detection and Revenue Protection  
**Applied Business Strategy Challenge – Day 4**

This project explores how financial institutions can reduce fraud losses, protect revenue, and strengthen risk management using a combination of anomaly analysis, modeling, and business strategy. The dataset used is the well-known Kaggle "Credit Card Fraud Detection" dataset with anonymized PCA features.

---

## 📌 Business Problem  
Fraudulent transactions create revenue leakage, increase operational costs, and impact customer experience.  
Financial institutions need tools that help them:

- Detect fraud earlier  
- Prioritize high-risk cases  
- Reduce manual investigation effort  
- Improve customer protection without increasing false positives  

This project simulates how a PM and analyst would partner to diagnose fraud patterns and develop a fraud scoring approach.

---

## 📊 Dataset Overview  
- **Transactions:** 284,807  
- **Fraud cases:** 492 (0.17 percent)  
- **Features:** 30 anonymized PCA components (V1–V28), Amount, and Time  
- **Label:** `Class` (1 = Fraud, 0 = Normal)

---

## 🔎 EDA & Pattern Insights

### 1. **Transaction Distribution**
- Fraud amounts trend lower than normal transactions.  
- Fraud distribution is highly skewed, consistent with micro–fraud patterns.

### 2. **Time-of-Day Patterns**
- Fraud spikes during non-peak hours where fraud is harder to detect manually.

### 3. **Correlation Insights**
- No strong correlations between PCA features and fraud.
- PCA-transformed features require modeling — correlations are not human-readable.

### 4. **Feature Contribution**
- V14, V12, and V10 emerged as the strongest fraud indicators.
- These components align with anomaly-based fraud scoring.

---

## 🤖 Modeling

### 📘 Logistic Regression (baseline)  
- Fast, interpretable, measurable risk scoring.  
- Useful for auditability and compliance.

### 🔥 Model Performance  
- **Accuracy:** 99.92 percent  
- **Precision:** 92.30 percent  
- **Recall:** 82.35 percent  

### 📈 Curves  
- Strong ROC separation  
- Precision-Recall curve highlights rarity of positive cases (preferred metric for fraud)

---

## 🧮 Manual Review Workload Estimate  
A risk-segment rule flags **1,074 transactions** as requiring manual review.  
This is useful for:

- Staffing projections  
- Vendor capacity planning  
- SLA sizing  
- Cost modeling  

---

## 🧭 PM Perspective  
If I were in the shoes of a Technical Program Manager, this work would help me:

- Align teams across Risk, Data, Compliance, and Engineering  
- Define SLAs for fraud detection latency  
- Establish governance with Model Risk Management  
- Build dashboards for real-time fraud spikes  
- Monitor precision/recall drift weekly  
- Prioritize reduction in false positives to protect customer experience  

---

## 🚀 Recommendations  

**1. Deploy ML-based fraud scoring in real-time**  
Add a fraud score to every transaction event.

**2. Introduce adaptive thresholds**  
Adjust for volume spikes, time-of-day, and customer profiles.

**3. Expand feature engineering**  
Integrate merchant category, device fingerprint, and geo-signals.

**4. Build human-in-the-loop escalation**  
Route borderline transactions to specialists.

---

## 📝 Final Summary  
This project demonstrates how machine learning can strengthen fraud prevention, protect revenue, and support PM-level decision-making.

**The analysis provides:**  
- Early detection signals  
- Actionable risk insights  
- PM-level prioritization  
- A clear technical-to-business bridge  

---

## 📣 Part of the 30-Day Applied Business Strategy Challenge  
Each day I solve one real business problem through analytics + PM thinking.

