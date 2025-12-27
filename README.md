# Unit Economics Analysis

This repository contains a complete analysis of key unit economics metrics for a subscription-based or transactional business. The goal is to evaluate customer profitability by calculating Customer Acquisition Cost (CAC), Average Revenue Per User (ARPU), Gross Margin, Customer Lifetime Value (LTV), and the critical LTV/CAC ratio.

The analysis is performed using real-world-style sample data and is fully reproducible.

## Key Metrics Calculated (2023 Data)

| Metric                  | Value       | Notes                                                                 |
|-------------------------|-------------|-----------------------------------------------------------------------|
| Customer Acquisition Cost (CAC) | $1,570.79  | Marketing spend + Sales & Marketing payroll + allocated office expenses |
| Average Revenue Per User (ARPU) | $327.28    | Total revenue / Unique customers                                      |
| Cost of Goods Sold (COGS)       | $151,960   | All payroll + operational office expenses                             |
| Gross Margin                    | 37.00%     | (Revenue - COGS) / Revenue                                            |
| Average Customer Lifespan       | ~8.1 months| Based on historical churn data                                        |
| Customer Lifetime Value (LTV)   | $97.95     | ARPU × Lifespan × Gross Margin                                        |
| LTV / CAC Ratio                 | 0.09       | Significantly below healthy benchmark              |

## Data Sources

Data was originally sourced from Google Sheets and exported to CSV for version control and reproducibility:

- **Customer Lifespan**: Start and churn dates for 100 customers
- **Marketing Spendings**: Daily ad spend across channels (Google Ads, Facebook, LinkedIn, etc.)
- **Payroll**: Monthly salaries by department (Sales, Marketing, Engineering, etc.)
- **Expenses**: Monthly office and operational costs
- **Receipt History**: Transaction-level revenue data with new/existing customer flags (Q1 2023)

The original data is pulled from Google Sheets (via export to XLSX). Here are the original Google Sheet IDs and descriptions:

* Customer Lifespan (`customer_lifespan.csv`): Contains customer IDs, start dates, and churn dates.

  Sheet ID: `1by8tPHwOnq3uKYK2E7sA9VBUYoPM4p1Rnrm_Ss9cyHI`.

* Marketing Spendings (`marketing_spendings.csv`): Daily spend by channel (e.g., Google Ads, Facebook Ads).

  Sheet ID: `1AZOIThOV4P-0eYDge53ZwumVkfkHoYPWxst3k3Bv87c`.

* Payroll (`payroll.csv`): Monthly payroll by department, employee, and position.

  Sheet ID: `1MY6j_um6X6O9Md9OTr3Z80g8l7qQd6lQ8HbyjY8n8g4`.

* Expenses (`expenses.csv`): Monthly operational expenses.

  Sheet ID: `1dR2tnv6zOIoM3S4v64X9f5Z1iH9b2B6eK3x6h4Y1k8w`.

* Receipt History (`receipt_history.csv`): Daily receipts with customer IDs, amounts, and new customer flags.

  Sheet ID: `1qayqML1zCKdmtzutkcy9LWvE6xFRm6TGBEVkHHJKIuE`.

To regenerate CSVs from Google Sheets:

Use the export URL format: `https://docs.google.com/spreadsheets/d/{SHEET_ID}/export?format=csv`.
Replace `{SHEET_ID}` with the IDs above.

**Methodology**

* `CAC`: Sum of marketing spend, Sales & Marketing payroll, and allocated office expenses / Number of new customers in 2023.
* `ARPU`: Total revenue from receipts / Total unique customers.
* `COGS`: All payroll + office expenses (conservative assumption for a service/SaaS-like business).
* `Gross Margin`: Standard formula.
* `LTV`: ARPU × Average lifespan (in months) × Gross Margin.

**Key Insights & Conclusions**

- The LTV/CAC ratio of 0.09 is critically low. A healthy business typically aims for 3:1 or higher.
- Customer acquisition is currently not sustainable — the business spends ~$1,571 to acquire a customer worth only ~$98 over their lifetime.

**Recommendations:**
- Optimize or reduce marketing spend (analyze channel ROI).
- Improve customer retention to extend average lifespan.
- Increase pricing or ARPU through upselling/cross-selling.
- Reduce operational costs to improve gross margin.

This analysis serves as a foundation for deeper cohort analysis, channel attribution, or predictive modeling.

