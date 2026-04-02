# SaaS Customer Churn Analysis

Since starting self directed learning over a year ago, I had the opportunity 
to work in a Junior Data Analyst capacity in healthcare at the end of a year 
long Customer Experience Analyst contract. A lot of my background has been in 
B2C and I wanted to apply those skills in a SaaS context, so SaaS churn was 
the perfect business problem to solve. Churn is a common issue amongst businesses and 
being able to understand why is the difference between improving CX/business 
reputation and losing millions.

This dataset stood out to me because of the ability to do more with the 
available columns. I knew I would be able to calculate and fill in tenure, 
blanks (active status), remove redundant columns and combine multiple excel 
sheets (XLOOKUP). These are skills that you wouldn't get to see in action 
from my resume alone. I have experience with sales, marketing, and operations. 
I have always loved being able to contribute to the customer experience and I 
am really excited about being able to do that in the most impactful way. 
I prioritize the quality of the output by making these kinds of decisions 
before any analysis begins.

In this portfolio, I chose and addressed the business question as if from 
The Head of Customer Success: *"Who is churning, when it's happening, and 
what we should do about it?"*

---

## Dataset Selection

Originally, I did an analysis of two different datasets. The first dataset 
seemed promising at first with 2,800 rows, contained behavioral signals 
including login recency, weekly usage hours, support tickets, and payment 
failures alongside a binary churn indicator and tenure in months. The key 
limitations in this dataset included no satisfaction scores, no churn reason, 
and no plan history. The churn rate was 57% which requires context on the 
measurement period before drawing conclusions. This dataset was strongest for 
analyzing behavioral patterns that predict churn, particularly the rare columns 
like payment failures and usage hours that most churn datasets don't have.

The second dataset (the one I chose) was a SaaS business metric dataset with 
3 different files: Customers with 1,000 rows, then Revenue and Subscriptions 
both with 988 rows because the latter two only contain customers that have a 
churned date. This dataset had some unique columns as well including acquisition 
cost and revenue data. The limitations here were no information about the plan 
journey, no support ticket data, no satisfaction scores, and two sheets only 
containing churned customers. This dataset was strongest for understanding when 
customers were leaving and if it were tied to acquisition cost or the plans. 
Since dataset 2 offered richer financial context that better served the business 
question, I went with that one.

---

## Process

I chose to approach dataset 2 in Excel first. I wanted to understand how the 
columns were constructed and to calculate the churn percentages. While exploring 
in Excel I noticed the Revenue and Subscriptions sheets only contained 988 rows 
compared to 1,000 in Customers. Comparing customer_id across files revealed the 
12 missing rows were active customers which I confirmed by blank churn_date 
entries in the Customers sheet. I resolved this by joining the Customer and 
Revenue files using XLOOKUP on customer_id, creating one complete working 
dataset. The Subscriptions sheet was omitted entirely as it contained no new 
information beyond what was already in Revenue.

I used filters to identify 832 active customers and 168 churned customers — 
a churn rate of 16.8%. I then investigated plan type, acquisition cost, and 
tenure as potential churn predictors.

---

## Key Findings

None of the variables investigated identified a specific at-risk customer 
profile. Instead the data points to a timing event in March 2025 as the 
primary driver.

Active customers average nearly twice the tenure of churned customers — 
8-9 months compared to 5-6 months. However, this comparison is influenced 
by dataset timing rather than customer behavior alone. In March 2025 churn 
tripled suddenly and never recovered, spiking again in June 2025. Acquisition 
cost and plan type show no meaningful relationship to churn. The evidence 
points to an external event or internal change in March 2025 as the likely driver.

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
- [Presentation Slides]
---

## Visualizations

[View Dashboard on Tableau Public](https://public.tableau.com/app/profile/crystal.brown8544/viz/SAASCUSTOMERCHURN/SAASCUSTOMERCHURN)

---

*Thank you for reviewing my portfolio. I welcome feedback and am actively 
seeking my next opportunity. Please feel free to connect with me.*
