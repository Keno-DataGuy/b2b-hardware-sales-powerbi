# b2b-hardware-sales-powerbi


A one-page **Power BI** report that tells the 2017 sales-pipeline story for a fictitious B2B computer-hardware retailer.

![Dashboard Screenshot](/b2b_hardware_dashboard.png)

---
## Contents
1. [Project Context](#project-context)  
2. [Dataset](#dataset)  
3. [Data Prep & Model](#data-prep--model)  
4. [Report Layout](#report-layout)  
5. [Key Findings](#key-findings)  
6. [Recommended Actions](#recommended-actions)  

---

## Project Context
The company logged **8 800+ opportunities** in five CSV files. After cleaning and modelling, the dashboard surfaces headline KPIs, time trends, regional and product performance, pipeline shape and agent effectiveness—all in under a second refresh time.

---

## Dataset
| File | Rows | Purpose |
|------|------|---------|
| `sales_pipeline.csv` | 8.8 k | Fact table – one row per opportunity |
| `sales_teams.csv` | 90 | Agent & region lookup |
| `products.csv` | 11 | SKU details |
| `accounts.csv` | 800 | Customer firmographics |
| `data_dictionary.csv` | n/a | Field definitions |

---

## Data Prep & Model
* **Power Query**: fixed dates, standardised currencies.  
* **Star schema**: `sales_pipeline` in the centre, linked 1 : * to sales agents, products and accounts.  
* **DAX**: created reusable measures including total won/lost $, win rate %, stage counts. Also created new calculated columns to fix the values field.

 ---

## Report Layout
* **Header**: title + subtitle in brand purple.  
* **KPI strip**: value won/lost, counts, win rate.  
* **Middle row**:
  * Quarterly win-percentage column chart.  
  * Regional bars for dollars won and win %.  
  * Scrollable product bar chart.  
* **Bottom row**:
  * Donut of pipeline stages.  
  * High-loss agents bar + sortable table.  
* Collapsible slicers for year, quarter and region.

---

## Key Findings
* **Win rate** averages **63 %**, sliding from 82 % in Q1 to 60 % in Q4.  
* **West office** leads with **US $3.6 Trillion won** at **64 %** win rate.  
* Five agents account for **> 40 % of total losses**.  
* **23 % of deals** sit idle in Prospecting or Engaging stages.

---

## Recommended Actions
Replicate West’s playbook across regions, coach high-loss agents, re-evaluate under-performing products, and enforce stage-gate SLAs to move stalled deals.


