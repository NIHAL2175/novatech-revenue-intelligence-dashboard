# 🚀 Novatech Revenue Intelligence Dashboard


Welcome to the Master Guide for **Milestone Project 1** in **AWS AI & ML Scholars Program (August 2026 Cohort)**!

---

## 📌 Executive Project Summary

* **Project Title**: Revenue Intelligence Dashboard for NovaTech Solutions
* **Your Role**: Business Intelligence Analyst at NovaTech Solutions
* **Primary Stakeholder**: **Sarah Chen**, Vice President of Revenue Operations
* **Company Profile**: NovaTech Solutions (Mid-market B2B Enterprise SaaS Company)
* **Core Business Problem**: Critical revenue, customer, and pipeline data is currently fractured across three disconnected platforms (CRM system, Marketing automation platform, and Customer Support ticketing portal). Every Monday morning, analysts waste hours manually compiling spreadsheets. Sarah Chen has commissioned you to unify these systems into a single, interactive Amazon QuickSight dashboard and configure an AI-powered Quick Topic to allow leadership to query the end-to-end customer journey in natural language.

---

## 📂 Project Datasets & Schema Inventory


```
                               ┌──────────────────────────────────────────────┐
                               │               NOVATECH DATASETS              │
                               └──────────────────────┬───────────────────────┘
                                                      │
         ┌────────────────────────────────────────────┼────────────────────────────────────────────┐
         ▼                                            ▼                                            ▼
┌───────────────────────────────┐            ┌───────────────────────────────┐            ┌───────────────────────────────┐
│     1. crm_deals.csv          │            │ 2. marketing_campaigns.csv    │            │     3. support_tickets.csv    │
├───────────────────────────────┤            ├───────────────────────────────┤            ├───────────────────────────────┤
│ • 500 Records, 9 Columns      │            │ • 300 Records, 8 Columns      │            │ • 1,200 Records, 7 Columns    │
│ • Deal ID, Account ID/Name    │            │ • Campaign ID, Channel        │            │ • Ticket ID, Account ID       │
│ • Deal Amount ($), Stage      │            │ • Spend ($), Impressions      │            │ • Ticket Status, Priority     │
│ • Close Date, Win/Loss Label  │            │ • Leads Generated, Clicks     │            │ • Escalation Flag, CSAT Score │
│ • Sales Rep, Segment          │            │ • Conversion Rate, Date       │            │ • Resolution Time (Hours)     │
└───────────────────────────────┘            └───────────────────────────────┘            └───────────────────────────────┘
```

---

## 🏗️ Technical Architecture & Workflow Stages

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        End-to-End Project Implementation Plan                          │
└───────────────────────────────────────────┬────────────────────────────────────────────┘
                                            │
    ┌───────────────────────────────────────┴───────────────────────────────────────┐
    ▼                                                                               ▼
┌───────────────────────────────┐                               ┌───────────────────────────────┐
│ STAGE 1: DATA VERIFICATION    │                               │ STAGE 2: ETL & TRANSFORMATION │
├───────────────────────────────┤                               ├───────────────────────────────┤
│ • Query pre-indexed KBs in Q  │                               │ • Correct Data Types (Dates)  │
│ • Check row counts & nulls    │ ───► [DATA INTEGRATION] ─────►│ • Calculated Fields (ROI, Days│
│ • Compile Verification Log    │                               │ • Unified 3-Way SPICE Join    │
│   (6+ entries across 3 KBs)   │                               │ • Justify Anchor & Join Types │
└───────────────┬───────────────┘                               └───────────────┬───────────────┘
                │                                                               │
                └───────────────────────────────┬───────────────────────────────┘
                                                ▼
                                ┌───────────────────────────────┐
                                │ STAGE 3: 3-SHEET DASHBOARD    │
                                ├───────────────────────────────┤
                                │ 1. Marketing Funnel           │
                                │ 2. Sales Pipeline             │
                                │ 3. Customer Health (Unified)  │
                                │ • KPIs, Filters, Cross-Visual │
                                │ • Cross-Sheet Navigation Link │
                                └───────────────┬───────────────┘
                                                ▼
                                ┌───────────────────────────────┐
                                │ STAGE 4: AI Q TOPIC & CHAT    │
                                ├───────────────────────────────┤
                                │ • Baseline Q Evaluation       │
                                │ • Configure Topic & Synonyms  │
                                │ • Post-Topic Accuracy Boost   │
                                │ • Q Exploration Log (5+ Qs)   │
                                └───────────────┬───────────────┘
                                                ▼
                                ┌───────────────────────────────┐
                                │ STAGE 5: EXECUTIVE REPORT     │
                                ├───────────────────────────────┤
                                │ • 3-5 Quantified Annotations  │
                                │ • 1-3 Page Report for VP Sarah│
                                │ • PDF Export & Final Package  │
                                └───────────────────────────────┘
```

---

## 📑 Required Submission Deliverables Checklist

| # | Deliverable Artifact | Description & Rubric Requirement | Working Template Link |
| :---: | :--- | :--- | :--- |
| **1** | **Verification Log** | At least 6 entries documenting data quality checks across all 3 indexed knowledge bases (Question, Q Response, Expected Answer from Data Dictionary, Pass/Fail). | [`Verification Log`](./01.%20Verification%20Log/01_Verification_Log.md) |
| **2** | **Data Transformation Screenshots** | Screenshots showing data type corrections, at least 2 calculated field formulas, and the unified dataset join diagram/configuration. | [`Data Transformation`](./02.%20Data%20Transformation%20Screenshots/02_Data_Prep_Plan_and_Calculations.md) |
| **3** | **Dashboard PDF Export** | High-resolution PDF export covering all 3 published sheets (`Marketing Funnel`, `Sales Pipeline`, `Customer Health`). | [`Dashboard PDF Export`](./03.%20Dashboard%20PDF%20Export/03_Dashboard_Design_Brief.md) |
| **4** | **Before / After Topic Screenshots** | Baseline Quick Chat responses (2–3 questions before Topic config) vs. Post-Topic responses showing measurable accuracy improvement. | [`Before/After Shots`](./04.%20Before-After%20Topic%20Screenshots/04_Before_After_Topic_Screenshots.md) |
| **5** | **Q Exploration Log** | At least 5 entries spanning CRM, Marketing, and Support domains + at least 1 cross-dataset question, verified against dashboard visuals. | [`Q Exploration Log`](./05.%20Q%20Exploration%20Log/05_Q_Exploration_Log.md) |
| **6** | **Executive Summary** | Auto-generated summary text from the published QuickSight dashboard. | [`Executive Summary`](./06.%20Dashboard%20Executive%20Summary%20Text/06_Dashboard_Executive_Summary.md) |
| **7** | **Annotated Dashboard Screenshots** | 3–5 text annotations embedded directly on dashboard sheets containing: Quantified Finding + Business Implication + Recommended Action. | [`Annotated Dashboard`](./07.%20Annotated%20Dashboard%20Screenshots/annotated_sheet1_marketing.png) |
| **8** | **Written Executive Report** | 1–3 page non-technical business report addressed to VP Sarah Chen covering Data Strategy, Design Rationale, Topic Configuration Impact, Key Insights, and AI vs. Dashboard Comparison. | [`Written Report for VP`](./08.%20Written%20Report%20for%20VP/08_Executive_Report_SarahChen.md) |

---

## 🎯 Official Udacity Rubric Evaluation Criteria

### 1. Data Preparation & Quality
* **Verification Log**: 6+ entries covering all 3 KBs with fact-checkable questions (row counts, date ranges, null counts) and correct Pass/Fail assessments.
* **Transformations & SPICE**: Data types corrected (e.g. string to date), 2+ calculated fields with business logic, and all 4 datasets saved to SPICE.
* **Unified Dataset**: CRM, Marketing, and Support datasets joined on shared key with identified anchor table and justified join types.

### 2. Dashboard Design & Interactivity
* **3 Multi-Page Sheets**: `Marketing Funnel`, `Sales Pipeline`, and `Customer Health`.
* **Visual Standards**: Each sheet contains KPI summary cards and appropriate chart types; `Customer Health` features a visual from the unified dataset.
* **Interactivity**: Filter controls on at least 2 sheets, one-click cross-visual filtering on at least 2 visuals, and cross-sheet navigation configured.
* **Publication**: Dashboard published and exported as a complete 3-page PDF.

### 3. AI-Powered Analysis & Communication
* **Topic Configuration**: Baseline Q screenshots (2–3 questions) compared against improved Post-Topic screenshots.
* **Q Exploration Log**: 5+ entries across all 3 domains + 1 cross-dataset question with verified dashboard checks.
* **Annotations**: 3–5 text callouts with exact figures, business impact, and concrete recommendations.
* **Executive Report**: 1–3 page professional report for VP Sarah Chen with clear explanations, no raw SQL/code formulas, and strategic alignment.

---

<div align="center">

## 👨‍💻 Author

# NIHAL N

### DevOps | Cloud | Kubernetes | AWS 

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Nihal%20N-blue?logo=linkedin)](https://www.linkedin.com/in/nihal-n-cse/)

**If you found this repository useful, consider giving it a ⭐**

</div>

---
