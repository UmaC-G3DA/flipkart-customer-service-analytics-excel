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

1. **Billing Calls:** Billing Questions accounted for 21,410 calls (71.4%). Average call duration was approximately 25 minutes across issue types. Review recurring billing queries, communication and self-service content to address avoidable contacts.
2. **SLA Performance:** 62.5% of calls were within SLA, 24.8% below SLA and 12.7% above SLA. Since above-SLA shares were similar across channels, investigate broader operational factors rather than focusing on one channel.
3. **Survey Coverage:** CSAT was available for 11,214 calls. Its correlation with call duration was −0.007. Improve survey coverage and avoid using handling time alone as a measure of service quality.
4. **Customer Experience:** Chatbot–Billing Questions recorded the lowest channel–issue CSAT (5.45). Kolkata had the lowest call-centre average (5.46), while Tripura had the lowest state average (4.90). Review these areas while considering the small differences and sample size.
5. **Call Routing & Event Readiness:** Regional allocation was not consistently aligned with customer geography. Review routing and centre capacity, and prepare support capacity, FAQs and self-service resources for major event periods.

## 8. Project Limitations

- 62.62% of CSAT scores are missing; satisfaction findings represent responding customers only.
- Bot-generated sentiment was excluded.

## 9. Repository Structure

```text
.
├── FLIPKART_case_study-excel.docx
├── DAF_-_Flipkart_Data_Project_1_-_Sheet_Raw_.csv
├── Flipkart_analysis_UmaC_G3_DA__SQL_Final.xlsx
├── Report_Uma_C_G3_DASQL.docx
└── README.md
```

## 11. Project Outcome

An end-to-end Excel analytics project covering data preparation, exploratory analysis, hypothesis assessment and interactive dashboard reporting. The project identifies customer-service patterns and operational areas for further investigation while recognising the limitations of the available data in assessing customer retention.
