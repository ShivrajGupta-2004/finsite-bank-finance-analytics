# 💳 Finsite Bank Finance Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

> An interactive Power BI dashboard that transforms raw banking transaction data into actionable financial intelligence — tracking KPIs, customer behavior, regional performance, and year-over-year growth across thousands of daily transactions.

---

## 📌 Table of Contents

- [Problem Statement](#-problem-statement)
- [Solution](#-solution)
- [Dashboard Preview](#-dashboard-preview)
- [Key Features](#-key-features)
- [Dashboard Insights](#-dashboard-insights)
- [Project Workflow](#-project-workflow)
- [Data Model](#-data-model)
- [Tools & Technologies](#-tools--technologies)
- [Business Value](#-business-value)
- [Author](#-author)

---

## 🔍 Problem Statement

Financial institutions process thousands of transactions daily across multiple customer segments, regions, and transaction types. Without a centralized system, management teams struggle to answer critical questions like:

- Are transaction volumes and revenue **growing year-over-year**?
- Which **customer segments** (Retail, Premium, SME, Corporate, Wealth) drive the most revenue?
- Which **states** generate the highest transaction value?
- What is the ratio of **successful vs. failed vs. pending** transactions?
- How much **fee and tax revenue** is being collected across transaction types?

Manual reporting across disconnected sources led to slow decision-making and missed business opportunities.

---

## 💡 Solution

Built a fully interactive **Finance Analytics Dashboard in Power BI** that serves as a single source of truth for financial performance monitoring.

The dashboard enables stakeholders to:
- Monitor real-time KPIs at a glance
- Dynamically filter by **Year**, **Occupation**, **Category**, and **Business Metrics**
- Drill through from summary visuals down to individual transaction records
- Export detailed transaction data for offline analysis

---

## 📊 Dashboard Preview

> **Dashboard 1 — Financial Overview**

![Dashboard Overview](Dashboard%20Image/image1.png)

> **Dashboard 2 — Transaction Trends & Status Analysis**

![Transaction Trends](Dashboard%20Image/image2.png)

> **Dashboard 3 — Customer & Regional Performance**

![Customer & Regional](Dashboard%20Image/image3.png)

> **Dashboard 4 — Detailed Transaction Drill-Through**

![Drill Through](Dashboard%20Image/mage4.png)

---

## ✨ Key Features

### 📈 Financial KPIs
| KPI | Description |
|-----|-------------|
| **Total Transaction Amount** | Aggregate value of all processed transactions |
| **Total Transactions** | Count of all transaction records |
| **Average Transaction Value** | Mean amount per transaction |
| **Total Fees Collected** | Sum of all fees charged across transaction types |
| **Total Tax Generated** | Total tax revenue from transactions |
| **YoY Growth** | Year-over-Year comparison for all key metrics |

### 🎛️ Interactive Capabilities
- Dynamic slicers: Year, Occupation, Category, Business Metrics
- Cross-filtering between all visuals
- Drill-through to transaction-level records
- Exportable transaction data grid

---

## 📉 Dashboard Insights

### 1. Monthly Transaction Trends *(Line / Area Chart)*
Tracks total transaction amounts across all 12 months to identify seasonal spikes, dips, and growth trajectories.

### 2. Transaction Status Breakdown *(Donut Chart)*
Visualizes the split between **Success**, **Failed**, and **Pending** transactions — a key operational efficiency indicator.

### 3. Customer Segment Revenue *(Horizontal Bar Chart)*
Ranks contribution from **Retail**, **Premium**, **SME**, **Corporate**, and **Wealth** segments to identify the most valuable customer groups.

### 4. State-wise Performance *(Horizontal Bar Chart)*
Compares transaction amounts across all states to pinpoint top-performing and underperforming regions.

### 5. Transaction Type Profitability *(Matrix / Heatmap Table)*
Provides a multi-metric view (Amount, Fees, Tax, Count) across all 10 transaction types:

| Transaction Types | | |
|---|---|---|
| Bill Payment | Card Payment | Deposit |
| Fee Charge | Interest Credit | Investment |
| Loan EMI | Refund | Transfer |
| Withdrawal | | |

### 6. Gender-based Analysis *(Donut Chart)*
Analyzes transaction volume and value split by **Male** vs. **Female** customers for demographic insights.

### 7. Detailed Transaction Records *(Dashboard 2)*
A drill-through grid view providing row-level transaction details for audit, investigation, or export.

---

## 🔄 Project Workflow

```
1. Data Collection       →  Sourced structured transaction data (CSV/Excel)
                             covering customer segments, states, transaction types,
                             fees, taxes, and statuses across multiple years.

2. Data Cleaning         →  Used Power Query to handle null values, normalize
                             date formats, remove duplicate transaction IDs,
                             and standardize category and region labels.

3. Data Modeling         →  Designed a Star Schema with:
                             - Fact Table: Transactions (amount, fees, tax, status)
                             - Dimension Tables: Customer, Date, Geography, Category

4. DAX Measures          →  Created 15+ DAX measures including:
                             - YoY % Change, Running Totals, Avg Transaction Value,
                               Dynamic Measure Selector, Fee & Tax Aggregations.

5. Time Intelligence     →  Implemented SAMEPERIODLASTYEAR, TOTALYTD, and
                             DATEADD functions for period-over-period analysis.

6. Dashboard Development →  Built 2 dashboard pages with linked visuals,
                             cross-filters, slicers, and drill-through actions.

7. Business Insights     →  Validated visuals against business requirements
                             and generated stakeholder-ready insights.
```

---

## 🗂️ Data Model

```
                    ┌─────────────┐
                    │  DIM_Date   │
                    └──────┬──────┘
                           │
┌──────────────┐    ┌──────┴──────┐    ┌─────────────────┐
│ DIM_Customer ├────┤  FACT_Trans ├────┤  DIM_Category   │
└──────────────┘    └──────┬──────┘    └─────────────────┘
                           │
                    ┌──────┴──────┐
                    │ DIM_Region  │
                    └─────────────┘
```

**Star Schema** — single fact table joined to 4 dimension tables for optimized query performance and clean DAX measure logic.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Dashboard development & visualization |
| **Power Query (M)** | Data ingestion, cleaning & transformation |
| **DAX** | KPI measures, time intelligence & dynamic calculations |
| **Data Modeling** | Star schema design & relationship management |
| **Microsoft Excel / CSV** | Source data files |

---

## 💼 Business Value

| Stakeholder | Benefit |
|-------------|---------|
| **C-Suite / Management** | Real-time KPI monitoring and YoY performance tracking |
| **Regional Managers** | State-wise revenue comparison to prioritize resources |
| **Product Teams** | Transaction type profitability to optimize offerings |
| **Risk & Operations** | Failed/pending transaction rate to improve success rates |
| **Marketing** | Customer segment and demographic analysis for targeting |

> The dashboard replaced hours of manual Excel reporting with a self-service analytics tool, enabling faster and more confident data-driven decisions.

---

## 👨‍💻 Author

**Shivraj Gupta**

*Aspiring Data Analyst passionate about transforming raw data into meaningful business insights using Power BI, SQL, Excel, and Python.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shivrajgupta2004)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ShivrajGupta2004)

---

<p align="center">⭐ If you found this project useful, consider giving it a star on GitHub!</p>
