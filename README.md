# Airtel ChurnQuest: Customer Churn Analysis & Financial Model

A practical, Excel-based analytical framework designed to identify why customers leave, highlight key operational risk points, and quantify the revenue impact on the business.

---

## 🎯 Executive Summary
Retaining high-value subscribers is essential to sustaining growth at Airtel. With an overall **baseline churn rate of 14.07%**, this project goes beyond basic charts to provide a reliable predictive scoring model and a bottom-line financial evaluation—built entirely in standard Excel.

By analyzing customer demographics, usage patterns, plan choices, and support call logs, we identify clear warning signs before customers cancel, allowing retention teams to step in early.

---

## ⚡ Key Business Findings & Risk Thresholds

Customer churn is heavily concentrated around four specific triggers:

* **Customer Support Escalations (4+ Calls) 📞**: Churn stays stable at **10%–13%** for up to 3 support calls, but jumps above **50%** once a customer calls 4 or more times.
* **Daytime Usage "Bill Shock" (220+ Mins) ⚡**: Churn spikes to **over 30%** past 220 daytime minutes and exceeds **55%** above 260 minutes, signaling frustration with daytime billing rates.
* **International Plans 🌍**: International plan subscribers have our highest churn rate at **~40%**, compared to only **11%–14%** for regular subscribers.
* **Voicemail as a Retention Anchor 📼**: Customers using voicemail cancel at roughly half the rate of others (**~7%–8% churn**), making it an effective tool for customer loyalty.

---

## 🛠️ Excel Model Architecture & Methodology

The model starts with the core 20-variable dataset and adds **20 calculated columns** to segment behavior and predict churn risk:

### 1. Standardization & Behavioral Segmentation
To evaluate different metrics fairly (e.g., comparing 400 daytime minutes with 4 service calls), we calculate **Z-scores**:
$$z = \frac{\text{Value} - \text{Mean}}{\text{StdDev}}$$
* **`z_day` / `z_eve` / `z_night` / `z_intl`**: Standardize call volume across different times of day.
* **`Cluster_Segment`**: Automatically groups customers into practical personas (such as *Heavy Daytime Users* or *Heavy International Users*) based on their risk profile.

### 2. Transparent Predictive Model (No ML Required)
Using a calibrated logistic formula, we convert risk factors into clear probabilities without complex external software:
$$P(\text{Churn}) = \frac{1}{1 + e^{-z}}$$
* **`Log_Odds_z`**: Combines baseline risk with weighted scores (e.g., adding `+2.5` for $\ge 4$ support calls; subtracting `-0.8` for voicemail subscribers).
* **`Churn_Prob`**: Converts the score into a clear churn probability from **0% to 100%** using `=1 / (1 + EXP(-Log_Odds_z))`.
* **`Pred_Churn`**: Flags accounts likely to cancel using a **$\ge 0.55$** threshold to minimize false alarms and focus retention spending where it counts.

---

## 📊 Financial Impact & Retention Budgeting

To make a clear business case for customer retention initiatives, the model links churn metrics directly to revenue:

1. **Monthly Charges (`Total_Monthly_Charges`)**: Aggregates all call charges into a single monthly bill per user.
2. **Loss of High-Value Subscribers 💸**: Churned customers have a higher average monthly bill (**$65.53**) than retained customers (**$58.46**), proving that top-tier spenders are most sensitive to bill surprises.
3. **Revenue at Risk**:
   * **Monthly Recurring Revenue (MRR) Lost**: **$39,188.24 / month**
   * **Annual Recurring Revenue (ARR) Lost**: **$470,258.88 / year**
4. **Customer Lifetime Value (CLV)**: At an estimated 75% gross margin over the baseline churn rate, average CLV is **$311.60**.
5. **Target Retention Cost**: With a CLV of $311.60, the business can profitably spend up to **$75 to $100 per at-risk customer** on targeted retention offers.

---

