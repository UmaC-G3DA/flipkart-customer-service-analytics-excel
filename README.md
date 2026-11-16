# Flipkart Customer Service Analytics (Excel)

## 1. Project Overview

This project analyses Flipkart customer-service call records using Microsoft Excel to evaluate customer satisfaction (CSAT), SLA performance, issue volumes and call-centre allocation.

The project includes data cleaning, exploratory analysis, descriptive statistics, correlation analysis, hypothesis assessments and an interactive dashboard.

## 2. Business Objectives

- Evaluate customer satisfaction across support channels, call centres and states.
- Analyse customer issue patterns and call duration.
- Examine SLA performance across support channels.
- Understand geographical call-centre allocation.
- Analyse customer satisfaction and issue volume during October events.

## 3. Dataset Overview

| Attribute | Details |
|---|---|
| Dataset | Flipkart customer-service call records |
| Records | 30,000 |
| Original Columns | 13 | 
| Final Columns | 17 |
| Period | October 2020 |
| Channels | Call-Center, Chatbot, Email, Web |
| Issue Reasons | Billing Question, Payments, Service Outage |
| Call Centres | Delhi, Mumbai, Kolkata, Chennai |
| Key Measures | CSAT (1–10), call duration (minutes), SLA status |

**Derived columns:** csat_category, call_timestamp_treated, Events, Region.

## 4. Tools & Technical Skills

**Tools:** Microsoft Excel

- **Data cleaning:** Remove Duplicates, filters, `TRIM`, `PROPER`, Find & Replace .
- **Data-quality checks:** `COUNTA`, `COUNTBLANK`, `COUNTIF`, `LEFT`, `MID`, `RIGHT`, `DATE`.
- **Formulas:** Nested `IF`, `OR`.
- **Analysis:** Descriptive Statistics, `CORREL`, PivotTables and PivotCharts.
- **Reporting:** KPIs, slicers, interactive dashboard, hypothesis.

## 5. Data Cleaning & Preparation

- Checked duplicate IDs (none found) and missing values: CSAT 18,786; city and state 132 each; customer name and gender 3 each.
- Standardised text fields and replaced `#N/A` values in city and state with `Unknown`.
- Categorised blank CSAT scores as 'No Response' without imputing original values.
- Grouped CSAT into Dissatisfied (1–4), Moderately Satisfied (5–7) and Highly Satisfied (8–10).
- Derived 'Region' from state and 'Events' from defined October date ranges.

## 6. Hypothesis Analysis

Hypotheses were assessed using PivotTables.

| Hypothesis | Observed Result | Assessment |
|---|---|---|
| H1: Issue reason vs call duration | Average duration remained approximately 25 minutes across issue reasons (24.97–25.14). | Not Supported |
| H2: Channel vs above-SLA share | Above-SLA share varied only slightly across channels (12.4–13.4%). | Not Supported |
| H3: Call centre vs average CSAT | Average CSAT ranged from 5.46 in Kolkata to 5.63 in Chennai. | Partially Supported |
| H4: State vs average CSAT | Tripura recorded the lowest average (4.90) . | Supported |
| H5: Region vs call-centre allocation | Call allocation was not consistently aligned with customer regions; cross-regional allocation was observed. | Partially Supported |
| H6: Channel and issue vs CSAT | Chatbot–Billing Questions recorded the lowest average CSAT (5.45). | Partially Supported |
| H7: Event period vs CSAT | Average CSAT ranged from 5.48 during Navratri/Dussehra to 5.60 during Big Billion Days. | Supported |
| H8: Event periods vs daily volume | Call volume peaked on selected dates during the analysed event periods. | Supported |
| H9: | State-wise issue volume showed the highest call volumes in Uttar Pradesh and Maharashtra. | 

## 7. Key Findings & Recommendations

1. **State and Call-Centre Performance:** Tripura recorded the lowest state-level CSAT (4.90), while Kolkata had the lowest call-centre CSAT (5.46). Conduct targeted service-quality reviews, focusing on these areas.
2. **Channel–Issue Performance:** Chatbot-Billing Questions recorded the lowest CSAT (5.45). Review the relevant channel–issue handling workflows to identify opportunities for improvement.
3. **Regional Call Allocation:** Customer allocation was not consistently aligned with geographic regions. Review regional allocation patterns to identify opportunities for more effective workload distribution.
4. **Event-Period Demand:** Customer issue volume increased around high-demand event periods. Strengthen support readiness through adequate staffing, proactive FAQs and self-service resources.
5. **Call Duration & SLA Performance:** Issue types showed little variation in average call duration, while Above-SLA proportions varied only slightly across channels. These should not be treated as primary improvement priorities based solely on this analysis.

## 8. Project Limitations

- 62.62% of CSAT scores are missing; satisfaction findings represent responding customers only.
- Bot-generated sentiment was excluded.

## 9. Repository Structure

```text

├── FLIPKART_case_study-excel.docx
├── DAF_-_Flipkart_Data_Project_1_-_Sheet_Raw_.csv
├── Flipkart_analysis_UmaC_G3_DA__SQL_Final.xlsx
├── Report_Uma_C_G3_DASQL.docx
└── README.md
```

## 11. Project Outcome

An end-to-end Excel analytics project covering data preparation, exploratory analysis, hypothesis assessment and interactive dashboard reporting to identify customer satisfaction patterns and service-performance improvement areas.
