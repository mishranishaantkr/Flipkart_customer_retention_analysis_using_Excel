# 📊 Flipkart Customer Service Analysis & Retention Insights

> **Data Analysis Milestone Project** — Analyzing 30,000 customer call records to uncover service quality issues impacting retention across Flipkart's 4 call center cities.

**Author:** Nishant Kumar Mishra &nbsp;|&nbsp; **Period:** March 2026

---

## 📌 Project Overview

Flipkart, one of India's leading e-commerce platforms, has observed a **decline in customer retention rates**. This project analyzes customer call center data using **Microsoft Excel** to identify key performance indicators, underlying trends, and specific issues within customer service operations contributing to this decline.

The analysis spans data cleaning, exploratory data analysis (EDA), hypothesis testing, pivot-based summarization, and interactive dashboard creation — all within Excel.

### 🔢 At a Glance

| Metric | Value |
|--------|-------|
| Total Customers Analyzed | 30,000 |
| Negative Sentiment Rate | 51.7% |
| Call Center Cities | 4 (Chennai, Delhi, Mumbai, Kolkata) |
| Average CSAT Score | 5.57 |
| Peak CSAT Month | May (5.84) |
| Lowest CSAT Month | June (5.31) |

---

## 🎯 Project Objectives

- Identify key metrics that assess customer service performance
- Formulate and test hypotheses linking service quality to customer retention
- Perform structured EDA to uncover actionable insights
- Build interactive dashboards for stakeholder presentation
- Provide data-driven recommendations to improve retention

---

## 🗂️ Repository Structure

```
flipkart-customer-retention-analysis/
│
├── 📄 README.md
│
├── 📁 Data/
│   ├── flipkart_raw_dataset.csv                              # Original raw customer call data
│   ├── cleaned_customer_data.xlsx                            # Cleaned dataset (base)
│   └── cleaned_data_with_csat_sentiment.xlsx                 # Cleaned data with CSAT + sentiment
│
├── 📊 Milestone_01_Flipkart_customer_retention_analysis.xlsx # Main analysis workbook
│
├── 📑 Data_Cleaning_and_Processing_Steps.pdf                 # Step-by-step data cleaning documentation
│
└── 📋 Flipkart_Customer_Service_Analysis_nishant_mishra_01.pptx  # Final presentation
```

---

## 📒 Main Excel Workbook — Sheet Index

The primary workbook contains **15 sheets** organized in the following workflow order:

| # | Sheet Name | Description |
|---|------------|-------------|
| 1 | `Milestone_01_Flipkart` | Project overview, metric tree diagram, defined KPIs, and documented hypotheses |
| 2 | `Flipkart_raw_dataset` | Raw imported customer call data as-is from the source CSV |
| 3 | `cleaned_customer_data_overall` | Cleaned dataset — missing values handled, duplicates removed, formats standardized |
| 4 | `cleaned_data_with_csat` | Cleaned dataset enriched with CSAT scores and sentiment classifications |
| 5 | `Customer_satisfaction_analysis` | Hypothesis analysis focused on customer satisfaction drivers Sentiment |
| 6 | `Service_quality_analysis_hypo` | Hypothesis analysis focused on Effect of response time on customer retention |
| 7 | `_Service_quality_analysis_hypo` | Hypothesis analysis focused on Effect of sentiment/training on CSAT scores and retention |
| 8 | `Operational_factor_analysis_hyp` | Hypothesis analysis focused on Effect of call duration efficiency on CSAT and retention |
| 9 | `Insights_charts_of_overall_data` | Charts and visualizations derived from the overall cleaned dataset |
| 10 | `Insight_charts_of_datawith_csat` | Charts and visualizations derived from the CSAT-enriched dataset |
| 11 | `Pivot_table_and_slices_` | Pivot tables with slicers on overall cleaned data (by call center, sentiment, etc.) |
| 12 | `Pivot_table_On_data_with_csat` | Pivot tables with slicers on CSAT dataset (by agent, channel, location, etc.) |
| 13 | `Final_Insights_collections_stat` | Aggregated descriptive statistics and final insight summaries |
| 14 | `Dashboard_flipkart_Dynamic` | 🟢 **Interactive Dynamic Dashboard** — slicer-enabled, explorable KPIs |
| 15 | `Dashboard_flipkart_Static` | 📌 **Static Dashboard** — snapshot of key metrics for presentation use |

---

## 🔄 Data Processing Flow

Follow this exact order when reviewing or reproducing the analysis:

```
RAW CSV
   ↓
[Sheet] Flipkart_raw_dataset              → Import raw data into Excel
   ↓
[PDF]   Data_Cleaning_Steps.pdf           → Reference for all cleaning decisions
   ↓
[Sheet] cleaned_customer_data_overall     → Cleaned base dataset
   ↓
[Sheet] cleaned_data_with_csat            → Add CSAT scores + Sentiment labels
   ↓
[Sheets] Hypothesis Analysis              → Service quality, Satisfaction, Operational factors
   ↓
[Sheets] Insight Charts                   → Visual EDA on both datasets
   ↓
[Sheets] Pivot Tables + Slicers           → Aggregated summaries and drill-downs
   ↓
[Sheet] Final_Insights_collections_stat   → Descriptive statistics & consolidated insights
   ↓
[Sheets] Dashboards (Dynamic + Static)    → Stakeholder-ready presentations
   ↓
[PPTX]  Final Presentation                → Findings, recommendations, conclusions
```

---

## 🧪 Hypotheses Tested

| # | Hypothesis | Key Columns | Finding |
|---|------------|-------------|---------|
| H | Reducing average response time improves customer retention | `response_time`, `csat_score` | Above-SLA responses scored higher CSAT (5.60) than Within-SLA (5.52) — speed alone doesn't drive satisfaction |
| H | Addressing negative sentiment via training increases CSAT and retention | `sentiment`, `csat_score`, `call_center` | 51.7% negative sentiment driven by billing issues; gender-neutral — systemic problem, not demographic |
| H | Reducing call duration through efficient processes improves CSAT | `call_duration`, `csat_score`, `channel` | Chatbot (lowest duration) has lowest CSAT (5.46) — efficiency without quality worsens satisfaction |

---

## 📊 Key Findings

### 1. Sentiment Crisis
- **51.7%** of customers (15,526) express **negative sentiment** — the largest group
- Only **21.6%** are positive (6,471 customers)
- Both female (7,900) and male (7,624) show identical dissatisfaction patterns → systemic issue, not demographic

### 2. Billing is the Root Cause

| Issue Type | Total Customers | Negative Sentiment | Avg CSAT |
|------------|----------------|--------------------|----------|
| Billing Question | 8,030 | 6,934 | 5.53 |
| Payments | 1,584 | 1,406 | 5.63 |
| Service Outage | 1,600 | 1,370 | 5.51 |

Billing Questions generate **4.9× more** negative cases than other issue types combined.

### 3. Response Time Analysis

| Response Category | Negative Customers | Avg CSAT |
|-------------------|-------------------|----------|
| Within SLA | 9,710 | 5.52 |
| Below SLA | 3,842 | 5.57 |
| Above SLA | 1,974 | 5.60 |

Customers with **Above-SLA** response time are *more* satisfied — current SLA targets may be set too rushed.

### 4. Channel Performance

| Channel | Negative Customers | Avg CSAT |
|---------|-------------------|----------|
| Call-Center | 5,028 | 5.61 |
| Chatbot | 3,884 | **5.46** ← Lowest |
| Email | 3,582 | 5.49 |
| Web | 3,032 | 5.61 |

**Chatbot** has the lowest CSAT despite moderate volume — automation quality needs urgent improvement.

### 5. Call Center City Performance

| City | Customers | Avg CSAT |
|------|-----------|----------|
| Chennai | 963 | **5.63** ← Best |
| Delhi | 4,651 | 5.57 |
| Mumbai | 3,782 | 5.53 |
| Kolkata | 1,818 | **5.46** ← Lowest |

Kolkata underperforms despite moderate volume — a quality-over-quantity issue.

### 6. Seasonal CSAT Pattern

| Month | Avg CSAT |
|-------|----------|
| Jan | 5.54 |
| Feb | 5.62 |
| Mar | 5.66 |
| Apr | 5.78 |
| **May** | **5.84** ← Peak |
| **Jun** | **5.31** ← Sharp Drop |
| Jul–Nov | 5.49–5.64 |
| Dec | 5.38 |

CSAT climbs Jan → May, then **drops sharply in June** — possible operational overload or policy change.

---

## 💡 Recommendations

| Priority | Action | Business Impact |
|----------|--------|-----------------|
| 🔴HIGH | **Fix Billing Processes** — Dedicated billing team, self-service portal, real-time invoice transparency | Directly addresses 6,934 negative cases |
| 🔴HIGH | **Revamp Chatbot Quality** — Improved NLP models, auto-escalation to human agents on negative sentiment | Lifts lowest CSAT channel from 5.46 |
| 🟡 MED | **Improve Kolkata Center** — Quality audits, targeted upskilling, KPIs benchmarked to Chennai's 5.63 | Baseline quality parity across centers |
| 🟡 MED | **Redesign SLA Targets** — Shift from speed-first to quality-first response design | Better resolution quality, less churn |
| 🟢LOW | **Seasonal Surge Planning** — June operational playbooks: extra staffing, proactive billing reminders | Prevent predictable annual June dip |
| 🟢LOW | **Gender-Neutral Programs** — Universal customer-centric fixes (both genders equally dissatisfied) | Inclusive, scalable retention strategy |

---

## 🏁 Conclusion

Flipkart's customer service data reveals a **systemic dissatisfaction problem** concentrated around:

1. **Billing issues** — the #1 driver of negative sentiment (6,934 cases)
2. **Chatbot failures** — lowest CSAT channel (5.46) despite automation investment
3. **Regional inconsistencies** — Kolkata underperforming vs Chennai benchmark
4. **Seasonal risk** — predictable June CSAT dip requiring proactive planning

Implementing the prioritized recommendations will improve CSAT scores, reduce churn, and strengthen Flipkart's competitive position in India's e-commerce market.

---

## 🛠️ Tools & Techniques Used

| Tool / Technique | Purpose |
|-----------------|---------|
| Microsoft Excel | Primary analysis environment |
| Data Cleaning | Null handling, deduplication, format standardization |
| Descriptive Statistics | Mean, Median, Std Dev of all KPIs |
| Correlation Analysis | Response time vs CSAT, Channel vs Sentiment |
| Pivot Tables + Slicers | Dynamic aggregation and drill-down exploration |
| Charts & Graphs | Bar charts, pie charts, line trends |
| Interactive Dashboards | Dynamic KPI exploration with slicers |

---

## 📂 File Reference

| File | Type | Description |
|------|------|-------------|
| `flipkart_raw_dataset.csv` | CSV | Source data — 30,000 customer call records |
| `cleaned_customer_data.xlsx` | XLSX | Base cleaned dataset |
| `cleaned_data_with_csat_sentiment.xlsx` | XLSX | Cleaned data with CSAT scores and sentiment labels |
| `Milestone_01_Flipkart_customer_retention_analysis.xlsx` | XLSX | **Main workbook** — 15 sheets of analysis, pivots, charts, dashboards |
| `Data_Cleaning_and_Processing_Steps.pdf` | PDF | Sequential documentation of all data cleaning decisions |
| `Flipkart_Customer_Service_Analysis_nishant_mishra_01.pptx` | PPTX | Final 9-slide presentation with findings and recommendations |

---

## 🚀 How to Use This Repository

1. Read `Data_Cleaning_and_Processing_Steps.pdf` to understand the data preparation methodology
2. Open the **Main Excel Workbook** and navigate sheets in the Sheet Index order listed above
3. Use the **Dynamic Dashboard** (`Dashboard_flipkart_Dynamic`) with slicers to explore KPIs interactively
4. Review `Final_Insights_collections_stat` for consolidated static findings
5. Open the **PPTX** for the executive narrative and recommendations

---

## 👤 Author

**Nishant Kumar Mishra**  
Data Analyst | Excel | Business Intelligence | EDA ( Exploratory Data Analysis ) 


---

*This project is submitted as part of an Academic Milestone Project within a time frame. Data used is for educational purposes only.*
