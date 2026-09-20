# Credit Card Analytics Dashboard

A two-page Power BI dashboard that analyses a year of credit card activity (2023) to show where revenue comes from and which customer segments drive it.

## Data

- **Source:** PostgreSQL database (`ccdb`), loaded into Power BI with Power Query
- **Size:** 10,293 customers, weekly activity from January to December 2023
- **Tables:**
  - `cc_detail`: card category, fees, credit limit, transaction amount and count, interest earned, spend type, usage channel, delinquency flag
  - `cust_detail`: age, gender, income, education, job, state, dependents, satisfaction score
- **Relationship:** one-to-one on `client_num`

## Data Model and DAX

- **Revenue** = annual fees + interest earned + total transaction amount
- **Age_Group** and **Income_Group**: calculated columns that group customers into age bands and low, medium and high income
- **Current_Week_Revenue**, **Previous_Week_Revenue** and **wow_revenue**: measures for week-over-week revenue change

## Dashboard Pages

1. **Transaction Report:** revenue, interest, transaction amount and count, quarterly trends, and revenue by card category, spend type, usage channel, education and job
2. **Customer Report:** revenue by income group, age group, state, job, education and dependents, weekly revenue by gender, and average satisfaction score

Both pages include a week slicer and filters for gender, income group and card category.

## Key Findings

- Total revenue is about 56.5M, made up of 45.5M in transactions, 8.0M in interest and about 3.0M in annual fees
- Blue cards generate about 83% of revenue, while Platinum contributes only about 2%
- Swipe transactions account for 63% of revenue, chip 31% and online 6%
- Customers aged 40 to 50 generate the most revenue (about 44%)
- Revenue dipped slightly in Q2, then rose to end Q4 about 4% above Q1
- About 6% of accounts (624) are flagged as delinquent

## Tools

Power BI, DAX, Power Query, PostgreSQL

## Note

The report connects to a local PostgreSQL database (`localhost`), so the data cannot be refreshed on another machine. The report opens normally and shows the data already loaded into it.

## Author

Muhammad Umer Mehmood
[LinkedIn](https://linkedin.com/in/muhammad-umer-mehmood) | [Portfolio](https://muhammadumermehmood.github.io)
