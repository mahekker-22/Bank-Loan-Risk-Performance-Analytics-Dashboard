# Bank Loan Risk & Performance Analytics Dashboard

## Project Overview
This repository houses a comprehensive **Power BI Business Intelligence solution** focused on retail loan portfolio performance, credit risk identification, and lending operations tracking. Using an extensive dataset (`Financial_loan_data.xlsx`), this project establishes critical banking Key Performance Indicators (KPIs), isolates risk vectors, and builds a robust framework for monitoring bank asset health.

Instead of navigating static reports, users can download the `.pbix` file inside the `dashboard/` folder to explore full cross-filtering functionality, dynamic tooltips, and custom DAX measures.

---
<img width="1912" height="978" alt="image" src="https://github.com/user-attachments/assets/fd0de96f-5349-425a-81c6-16c521cdc3aa" />

## 📋 Project Disclaimers & Attribution
* **Portfolio Purpose Only:** Developed strictly as a non-commercial portfolio piece to showcase data modeling, business intelligence, and DAX proficiency in Power BI.
* **Data Transparency:** All transaction volumes, values, and demographics are synthetic or masked for simulation purposes. They do not represent real-time financial or operational metrics of any live enterprise.
* **Trademark Attribution:** Any brand assets or banking visuals used are properties of their respective owners. They are included solely for UI design aesthetics to replicate a realistic corporate environment. No affiliation, sponsorship, or endorsement is implied; all rights belong to the respective trademark owners.

---

## 📊 Executive Portfolio Performance (KPI Summary)

The underlying core data model aggregates information across **38,576 loan applications**, monitoring a total disbursed principal of **\$435.76M**.

### 🛠️ Core Portfolio Metrics
* **Total Loan Applications:** 38,576
* **Total Funded Capital:** \$435,757,075
* **Total Capital Repaid:** \$473,070,933
* **Portfolio Blended Interest Rate:** 12.05%
* **Portfolio Average Debt-to-Income (DTI):** 13.33%

### 🎯 Credit Quality Segmentation (Good vs. Bad Loans)
The dashboard separates asset quality based on the operational repayment state into a **Good Loan vs. Bad Loan KPI Framework**:

| Loan Operational Status | Application Count | Share (%) | Funded Amount | Received Amount | Net Financial Impact |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **Fully Paid** | 32,145 | 83.33% | \$351.36M | \$399.07M | Strong positive yield |
| **Current** | 1,098 | 2.85% | \$18.86M | \$18.68M | Active interest-bearing |
| **Charged Off (Default)** | 5,333 | 13.82% | \$65.54M | \$55.32M | **\$10.22M Write-off Loss** |

> **Key Risk Takeaway:** The portfolio shows strong basic health with an **86.18% Good Loan Ratio**. However, a **13.82% Default (Charged-Off) Rate** indicates the need for targeted credit policy adjustments, particularly on higher-tier risk bands.

---

## 🔍 Analytical Deep Dives & Segments

### 1. Month-over-Month (MoM) Growth
Lending activities show a sharp upward scaling trend towards the final quarter of the year, pointing to cyclical credit demands:
* **December Applications Peak:** 5,381 applications (A **+25.58% MoM surge** compared to November’s 4,285 applications).
* **December Funding Peak:** \$62.76M disbursed (A **+25.20% MoM surge** compared to November’s \$50.13M).

### 2. Loan Term Risk Variance
* **36-Month Term:** 28,231 applications | \$273.04M Funded | Blended Int. Rate: **11.07%**
* **60-Month Term:** 10,345 applications | \$162.71M Funded | Blended Int. Rate: **14.72%**
* *Insight:* 60-month loans fetch a higher interest premium (+3.65% yield) but correlate heavily with structural payment vulnerabilities.

### 3. Allocation by Purpose
* **Debt Consolidation** represents **53.5%** of all loans issued (\$232.48M funded across 18,214 applications).
* Other leading segments include **Credit Card Clearances** (\$58.87M funded) and **Home Improvements** (\$36.13M funded).

### 4. Regional Demographics
* **California (CA)** leads structural credit exposure with 6,894 applications (\$80.48M funded).
* **New York (NY)** (\$43.34M) and **Florida (FL)** (\$29.74M) follow as key operational states.

---

## 🛠️ Tech Stack & Technical Implementation
* **Power BI Desktop:** Star-schema data modeling, dynamic dashboard composition, and multi-page interactive UI layout.
* **Advanced Power Query (M Language):** Extracted, cleaned, and structured raw CSV sheets; formatted dates (`ISSUE_DATE`, `LAST_PAYMENT_DATE`), standardized structural string records (`EMP_LENGTH`), and handled currency data parsing.
* **DAX (Data Analysis Expressions):** Engineered optimized dynamic metrics including Running Totals, Month-over-Month % variances, conditional grouping flags, and weighted average portfolio yields.

