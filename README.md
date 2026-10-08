# Airtel ChurnQuest: Customer Churn Analysis & Financial Model

A practical, Excel-based analytical framework designed to identify why customers leave, highlight key operational risk points, and quantify the revenue impact on the business.

---

## Executive Summary

Retaining high-value subscribers is essential to sustaining growth at Airtel. With an overall baseline churn rate of **14.07%**, this project goes beyond basic charts to provide a reliable predictive scoring model and a bottom-line financial evaluation—built entirely in standard Excel.

By analyzing customer demographics, usage patterns, plan choices, and support call logs, we identify clear warning signs before customers cancel, allowing retention teams to step in early.

---

## Key Metrics Summary

* **Total Subscriber Base:** 3,333 active accounts analyzed
* **Total Churn Count:** 469 canceled accounts
* **Overall Baseline Churn Rate:** **14.07%**
* **Average Monthly Charges:** **$59.45**
* **Average Daytime Minutes:** **179.8 minutes**
* **Support Escalation Rate:** ~18% requiring multiple calls

---

## Repository Structure
```
├── Dashboard/                      # Visual report snapshots & charts
├── Excel_Dataset/                  # Raw and intermediate data tables
├── Airtel_Communications_.xlsx     # Core Excel model with calculated columns & scoring
└── README.md                       # Project Documentation & Methodology
```
---

## Categorized Deep Insights

### 1. Customer Support Escalations (4+ Calls)
* Churn stays stable at **10%–13%** for up to 3 support calls, but jumps above **50%** once a customer calls 4 or more times. Frequent service calls are the strongest warning signal.

### 2. Daytime Usage "Bill Shock" (220+ Mins)
* Churn spikes to **over 30%** past 220 daytime minutes and exceeds **55%** above 260 minutes, signaling customer frustration with high daytime billing rates.

### 3. International Plan Vulnerability
* International plan subscribers have our highest churn rate at **~40%**, compared to only **11%–14%** for regular domestic subscribers.

### 4. Voicemail as a Retention Anchor
* Customers using voicemail features cancel at roughly half the rate of non-users (**~7%–8% churn**), proving it acts as an effective stabilizer for customer loyalty.

### 5. High-Value Revenue Sensitivity
* Churned customers have a higher average monthly bill (**$65.53**) than retained customers (**$58.46**), proving that top-tier spenders are most sensitive to pricing pressures.

---

## Strategic Recommendations for Retention Leadership

1. **Early Intervention on Support Escalations:**
   * Automatically flag accounts that reach 3 support calls and route them to a specialized retention specialist before a 4th call triggers cancellation.
2. **Targeted International Plan Review:**
   * Re-evaluate pricing tiers and bundle options for international plan holders to reduce the **~40%** churn rate.
3. **Proactive Tiered Plan Adjustments ("Bill Shock" Mitigation):**
   * Introduce automated text alerts or flexible bucket upgrades for heavy daytime users exceeding 220+ minutes before they encounter unexpected charges.
4. **Feature Bundling (Voicemail & Loyalty Perks):**
   * Bundle voicemail or similar engagement features into standard baseline plans to leverage their retention-boosting effect across the broader subscriber base.
