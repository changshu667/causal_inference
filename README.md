# Customer Churn Analysis

This project is about finding factors that cause customers to churn. The customer churn analysis contributes to the business domain the most is a severe problem for all kinds of organizations that causes major expenses. The causal question at hand to answer is whether a choice of a particular phone plan (e.g., a phone plan with unlimited internet access), lead to a lower probability of churn?

## Motivation

Companies usually increase the customer base by acquiring new customers as well as retaining old ones. In many cases, it is a more cost-efficient way to retain a current customer than to acquire a new one. Therefore, customer retention is a key issue for companies and we aim to investigate it using causal inference tools. 

## Ideal Experiment

We would have two identical copies of each study participant. We would separate them into two groups: one group enrolled in a regular phone plan and the other group enrolled in an upgraded phone plan. Upgraded phone plans could include streaming TV access, free international calls, or, as mentioned above, unlimited internet access, etc. Then we would investigate whether there is a statistically significant difference in churn rates between these two groups.

## Project Design

We will define treatment and control groups: treatment as the upgraded phone plan users, and control as the regular plan users. We then will use propensity score matching to assure that there is no significant difference in the chosen variables (in other words, treatment and control groups are well balanced), except the one indicating phone plan (the treatment variable). After matching the groups, we will use logistic regression to predict the churn rate and analyze the coefficient for the phone plan holding the regular plan users as the baseline.

## Expected Model Result

As discussed in the question above, we aim to have the regression table coefficients after applying a logistic regression and holding the regular plan users as a baseline. 

If the coefficient for the odds ratio for the phone plan is less than one, the upgraded plan users are less likely to churn compared to customers with a regular plan.

Results if hypothesis is true:

Churn rates are lower among upgraded plan users in comparison with regular plan users.	

Results if hypothesis is false:

Churn rates are higher for upgraded plan users in comparison with regular plan clients, or there is no difference between them in terms of churning out of telephone services


## Final Variable Required

For both regular and upgraded plans users, we need the following variables:

Demographic variables including age, gender, location, etc. from a representative sample of a population that have a service contract with a tele company. We believe it is important to have information about location since it may impact the available services (for example, rural areas may have fewer services available and therefore lower satisfaction rates influencing customers to churn).

Information about the types of services each customer has, contract type, number of months using a service. If service is provided on a monthly basis, we want to have a population that used a service longer than a month so see whether they extended the contract to the next month.

Information of customers’ level of satisfaction: customers’ level of satisfaction is directly related to whether customers will churn or not. 

Outcome variable: churn or not. We want a population that has all the information we want above but also their churn status is being recorded.

## Data Source

The data is obtained from IBM Cognos Analytics sample data sets on Telco customer churn. The datasets contain demographic information about clients like gender, age group, dependents, and paying information like monthly charges, types of services each customer has, etc. The churn column indicates whether or not the customer left within the last month.

Extral Datasource:
2018: ACS 5-Year Estimates Subject Tables
Survey/Program: American Community Survey
Link: https://data.census.gov/cedsci/table?g=0400000US06&tid=ACSST1Y2018.S1902&t=Income%20and%20Earnings%3AIncome%20and%20Poverty&vintage=2018&hidePreview=false&layer=VT_2018_040_00_PY_D1&cid=S1901_C01_001E
