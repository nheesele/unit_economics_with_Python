# Unit Economics Analysis

![](https://github.com/nheesele/unit_economics_with_Python/blob/main/Business-IT-Services-1024x536.jpg)
>source: [techstreamit](https://techstreamit.com.au/wp-content/uploads/2025/09/Business-IT-Services-1024x536.jpg)

This repository contains the unit economics analysis of Streamline Pro, a Software as a Service (SaaS) platform by TechStream Solutions. Streamline Pro provides comprehensive project management and collaboration tools for businesses of all sizes. Understanding the unit economics of the product helps the company:

* Assess the profitability of acquiring and retaining customers.
* Evaluate the efficiency of marketing and sales strategies.
* Make informed decisions about scaling operations and optimizing resource allocation.

The analysis focuses on the month of **March 2023**.

The analysis calculates key business metrics such as:
* Customer Acquisition Cost (CAC)
* Average Revenue Per User (ARPU)
* Cost of Goods Sold (COGS)
* Gross Margin
* Customer Lifetime Value (LTV)
* LTV/CAC ratio.
These metrics help evaluate the profitability and sustainability of customer acquisition and retention strategies.

## Key Metrics Calculated

| Metric                          | Value       | 
|----------------------------------|-------------|
| Customer Acquisition Cost (CAC) | $1,570.79  | 
| Average Revenue Per User (ARPU) | $327.28    | 
| Cost of Goods Sold (COGS)       | $151,960   |
| Gross Margin                    | 37.00%     | 
| Average Customer Lifespan       | ~8.1 months|
| Customer Lifetime Value (LTV)   | $97.95     | 
| LTV / CAC Ratio                 | 0.09       |

## Data Sources

The data used for this analysis is stored in the shared
 [Google Drive folder](https://drive.google.com/drive/folders/1qhOW9Y2orRXuzbX-kXEmuJ7TMQiRs2Uv).

Here are the original Google Sheet IDs and descriptions:

* **Customer Lifespan**: Contains customer IDs, start dates, and churn dates.

  Sheet ID: `1by8tPHwOnq3uKYK2E7sA9VBUYoPM4p1Rnrm_Ss9cyHI`.

* **Marketing Spendings**: Daily spend by channel (e.g., Google Ads, Facebook Ads).

  Sheet ID: `1AZOIThOV4P-0eYDge53ZwumVkfkHoYPWxst3k3Bv87c`.

* **Payroll**: Monthly payroll by department, employee, and position.

  Sheet ID: `1MY6j_um6X6O9Md9OTr3Z80g8l7qQd6lQ8HbyjY8n8g4`.

* **Expenses**: Monthly operational expenses.

  Sheet ID: `1dR2tnv6zOIoM3S4v64X9f5Z1iH9b2B6eK3x6h4Y1k8w`.

* **Receipt History**: Daily receipts with customer IDs, amounts, and new customer flags.

  Sheet ID: `1qayqML1zCKdmtzutkcy9LWvE6xFRm6TGBEVkHHJKIuE`.

To regenerate xlsxs from Google Sheets:

Use the export URL format: `https://docs.google.com/spreadsheets/d/{SHEET_ID}/export?format=xlsx`.
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

**Google Colab**
You can assess the related Google Colab link below to explore the code and data:
[Unit Economics with Python](https://colab.research.google.com/drive/1rRUwo3pIbZA3ZOnOjhlHU4MunLAWa6hH?usp=sharing)

