# Corporate Budget Variance Analysis (Excel)

An end-to-end FP&A (Financial Planning & Analysis) project built entirely in Excel, consolidating three real transactional datasets to analyze budget performance across departments, quarters, and fiscal years.

<img width="797" height="415" alt="image" src="https://github.com/user-attachments/assets/05236ad5-574c-4420-a17e-d02c0ee4fabf" />



📊 [View the Excel file](Corporate_Budget_Variance_Analysis.xlsx)

## Project Overview

This project simulates a real-world corporate finance analyst workflow: pulling data from multiple systems (budget planning, general ledger, expense management), reconciling them into a single source of truth, and surfacing actionable insights for leadership.

**Business context:** A mid-size company wants to understand whether departments are spending in line with their approved budgets, and where the biggest planning gaps exist.

## Data Sources

| Source | Description | Volume |
|---|---|---|
| **Budget Forecast** | Quarterly budget, forecast, and target figures by department (FY2024-FY2025) | 48 records |
| **General Ledger** | Transactional revenue and expense entries across 6 departments, multi-currency | 2,000 records |
| **Expense Claims** | Employee reimbursement requests by category and approval status | 1,000 records |

## Tools & Techniques

- **Data validation:** Pre-analysis quality checks for blanks, duplicates, and cross-table consistency
- **VLOOKUP:** Currency conversion (5 currencies → USD) applied across two separate tables
- **SUMIFS:** Multi-criteria aggregation of ledger transactions by department, year, and quarter
- **INDEX + MATCH:** Multi-key lookups (via concatenated key) to join Budget and Actuals into a single variance table
- **PivotTables & PivotCharts:** Four interactive views (by department, by quarter, ranked by variance, by expense category)
- **Slicers:** Cross-filtering by Department, Fiscal Year, and Quarter across all connected visuals
- **Conditional formatting:** Visual variance scaling for quick pattern recognition

## Key Insights

**1. Departments consistently underspend against budget**

- **Business Question:** Are departments spending in line with their approved budgets?
- **Finding:** Across all 6 departments and both fiscal years, actual spend was consistently lower than budgeted, ranging from -22% to -88% variance in realized quarters.
- **Insight:** This may indicate over-conservative budgeting, delayed spending execution, or gaps between the budgeting process and the general ledger's expense categories.

**2. Actual spend is stable regardless of budget fluctuation**

- **Business Question:** Does actual spending track budget changes over time?
- **Finding:** While quarterly budgets varied significantly (~$330K to ~$580K company-wide), actual spend stayed relatively flat (~$110K-$130K per quarter).
- **Insight:** This decoupling suggests the budgeting process may not be grounded in realistic operational spend patterns.

**3. Operations Q4 2024 shows the largest single variance**

- **Business Question:** Which department/quarter combination represents the biggest planning gap?
- **Finding:** Operations Q4 2024 had the largest variance at -$129,846, followed by Marketing Q3 2024 (-$117,922).
- **Insight:** These instances warrant prioritized investigation with the respective department heads.

**4. Travel is the leading expense claim category**

- **Business Question:** Where is employee expense spend concentrated?
- **Finding:** Travel represents the largest share of total reimbursed amount among all expense claim categories.
- **Insight:** Travel policy and vendor negotiation may offer the highest-leverage cost-control opportunity.
