# SaaS Customer Churn Analysis: Identifying a Sudden Churn Event

## At a Glance

- Churn increased **3x starting March 2025**.
- Not driven by plan type or acquisition cost.
- Indicates **a timing-based event, not a customer segment issue**.
- Recommendation: investigate product, support, and marketing changes during that period.

---

I transitioned from Customer Experience into data analytics and wanted to apply that background to a SaaS environment. 
Churn is something most businesses deal with, but understanding why it’s happening is what determines whether a company improves its customer experience or slowly loses revenue and trust over time.

---

## Business Context

I approached this analysis from the perspective of a Head of Customer Success:

- **Who is churning?**
- **When churn is occurring?**
- **What actions should be taken to reduce it?**

---
## Executive Summary

Churn was **not driven by customer segmentation factors** such as plan type or acquisition cost.

Instead, churn **spiked sharply in March 2025 and again in June 2025**, indicating **a systemic event rather than gradual customer dissatisfaction**.

This suggests a **breakdown in customer experience or product delivery**, not a mismatch in customer targeting.

Without identifying and addressing the root cause of this event, retention efforts risk being ineffective and misdirected.

---
## Business Impact

- Churn increased from a stable baseline in 2024 to **3x higher levels in peak months**.
- This type of spike represents a **significant risk to recurring revenue and customer lifetime value**.
- Because the issue is not tied to customer profile, scaling acquisition or adjusting pricing will not resolve the problem.

  This should be treated as a high priority retention incident, not a routine fluctuation
  
---

## Why I Chose This Dataset

I initially explored two datasets.

The first dataset (2,800 rows) included behavioral signals like login recency, weekly usage hours, support tickets, and payment failures. It was strong for identifying behavioral patterns, especially with less common fields like usage hours and failed payments. However, it lacked key context such as satisfaction scores, churn reasons, and plan history. The reported churn rate (57%) also lacked a clear time window, making it difficult to interpret reliably.

The second dataset (which I selected) included SaaS business metrics across three files: Customers (1,000 rows), Revenue, and Subscriptions (both 988 rows, limited to churned users). It introduced financial context through acquisition cost and revenue data, but lacked behavioral and customer experience indicators.

I chose the second dataset because it better supported the business question of when churn is happening and whether it’s tied to customer or financial factors, even with its limitations.

---

##  Process
I began in Excel to understand how the data was structured and to validate key assumptions.

- Identified a mismatch between Customers (1,000 rows) and Revenue (988 rows).
- Confirmed missing records were active customers (no churn date).
- Merged datasets using XLOOKUP on customer_id.
- Removed the Subscriptions sheet as it added no new information.

After cleaning:

- 832 active customers
- 168 churned customers
- Churn rate: 16.8%

From there, I analyzed churn across:

- Plan type
- Acquisition cost
- Customer tenure
- Time (monthly churn trends)

---

## Key Findings

**1. No clear at-risk customer profile**

Plan type and acquisition cost showed no meaningful relationship to churn.


**2. Churn is driven by timing, not segmentation**

Churn tripled in March 2025 and spiked again in June.


**3. Tenure differences are misleading without time context**

Shorter tenure among churned users reflects the timing of the spike, not behavior.

---

## What This Means

The data points to a **specific event or change around March 2025** as the primary driver of churn.

Because churn is not tied to plan type or acquisition cost adjusting pricing or targeting is unlikely to fix the issue.
The root cause is more likely tied to product, experience, or operational changes.

This analysis identifies where the problem is. The next step is *confirming what caused it*.

---

## Recommendations

**1. Investigate March-June 2025**
  
I would start by cross-referencing:

- Product releases and feature changes
- Support ticket volume and sentiment
- Marketing campaigns or messaging shifts

The goal is to identify what changed during this period.

**2. Extend the dataset to present day**

Determine whether churn has stabilized or is still elevated.
If it’s ongoing, this becomes a more urgent retention issue.

**3. Proactive outreach at Month 4**

Introduce a Customer Success check-in (call or automated survey) before customers reach the observed churn window.

**4. Capture direct feedback from churned customers**

A simple one-question exit survey (“Why did you leave?”) can provide insights that internal data alone cannot.

---

## If I Were Embedded on This Team

My first priority would be figuring out what actually caused the March spike.

In the first 1–2 weeks, I would:

- Compare churn cohorts before and after March 2025.
- Review support trends for sudden increases or pattern changes.
- Audit product releases or incidents during that window.

The goal would be to isolate the root cause quickly and prevent further loss.

---

## What I Would Do Differently With More Data

With additional data, I would:

- Compare feature usage between churned and retained customers
- Analyze behavior differences between short-term and long-term users
- Investigate whether there’s a gap between what customers expected and what they experienced

---

## Final Note

This project reflects how I approach problems: starting with the business question, understanding the data deeply, and focusing on decisions that actually impact the customer experience.

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
