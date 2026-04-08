# SaaS Customer Churn Analysis: Identifying a Sudden Churn Event

## Business Context

A B2B SaaS company is experiencing churn and wants to understand **who is leaving, when it’s happening, and what to do about it**.

---

## Key Insight

Churn was not driven by plan type, acquisition cost, or a specific customer segment.
Instead, it **spiked sharply in March and June 2025**, suggesting a likely external or internal event rather than a gradual trend.

---

## Why I Chose This Dataset

Originally, I did an analysis of two different datasets. The first dataset seemed promising at first with 2,800 rows, contained behavioral signals including login recency, weekly usage hours, support tickets, and payment failures alongside a binary churn indicator and tenure in months. The key limitations in this dataset included no satisfaction scores, no churn reason, and no plan history. The churn rate was 57% which requires context on the measurement period before drawing conclusions. This dataset was strongest for analyzing behavioral patterns that predict churn, particularly the rare columns like payment failures and usage hours that most churn datasets don't have.

The second dataset (the one I chose) was a SaaS business metric dataset with 3 different files: Customers with 1,000 rows, then Revenue and Subscriptions both with 988 rows because the latter two only contain customers that have a churned date. This dataset had some unique columns as well including acquisition cost and revenue data. The limitations here were no information about the plan journey, no support ticket data, no satisfaction scores, and two sheets only containing churned customers. This dataset was strongest for understanding when customers were leaving and if it were tied to acquisition cost or the plans. Since dataset 2 offered richer financial context that better served the business question, I went with that one.


---

##  Process
I started in Excel to understand how the datasets were structured.

- Noticed a mismatch in row counts (1,000 customers vs 988 revenue records)
- Identified that missing records were active customers with no churn date
- Used XLOOKUP to merge datasets into a complete working file
- Removed redundant data (Subscriptions sheet)
  
After cleaning:

- 832 active customers
- 168 churned customers
- Churn rate: **16.8%**
  
I then analyzed churn across:

- Plan type
- Acquisition cost
- Customer tenure

---

## Key Findings

**1. No clear at-risk customer profile**
Plan type and acquisition cost showed no meaningful relationship to churn

**2. Churn is driven by timing, not segmentation**
Churn tripled in March 2025 and spiked again in June

**3. Tenure differences are misleading without time context**
Shorter tenure among churned users reflects the timing of the spike, not behavior

---

## Recommendations

1. **Investigate March–June 2025** — Cross-reference marketing campaign data, 
support ticket history, and the development changelog to identify any product, 
campaign, or operational changes that coincided with the churn spike.

2. **Extend the dataset to present day** — Confirm whether churn has stabilized 
or is still accelerating. If still elevated, immediate intervention is needed 
before the customer base erodes further.

3. **Implement month 4 proactive Customer Success outreach** — A check-in call 
or automated health survey to identify disengaging customers before they reach 
the churn window.

4. **Deploy a one-question exit survey** — Even a 10% response rate from 
recently churned customers would provide direct evidence of the root cause 
that no amount of internal data analysis can replace.

---

## What I Would Do Differently With More Data

I would compare what services and features were used by both churned customers 
and customers who stayed active through the spike periods. I would also calculate 
the difference in behavior between customers who churned within 6 months and 
those who were active longer. This would help investigate whether there is a gap 
between what customers expected from the product and what they experienced.

---

## Tools Used

- Microsoft Excel
- [SQLiteOnline](https://sqliteonline.com)
- [Tableau Public](https://public.tableau.com)
- Microsoft PowerPoint

---

## Files

- [SQL Queries](https://github.com/CrystalMBrown/Data-Analytics-Portfolio/blob/main/SaaS%20Business%20Metrics%3A%20SQL)
- [Presentation Slides](https://github.com/CrystalMBrown/Data-Analytics-Portfolio/blob/main/Saas%20customer%20Churn%20Analysis.pdf)
  
---

## Visualizations

[View Dashboard on Tableau Public](https://public.tableau.com/app/profile/crystal.brown8544/viz/SAASCUSTOMERCHURN/SAASCUSTOMERCHURN)

---

*Thank you for reviewing my portfolio. I welcome feedback and am actively 
seeking my next opportunity. Please feel free to connect with me.*
