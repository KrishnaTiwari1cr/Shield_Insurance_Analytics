# 🛡️ Shield Insurance Analytics Dashboard
### Power BI | Data Analytics | Virtual Internship Project

---

## 📌 Project Overview

This project is a **4-page interactive Power BI dashboard** built for Shield Insurance as part of the **Codebasics Virtual Internship** with AtliQ Technologies. The dashboard analyzes 6 months of insurance business data (Nov 2022 – Apr 2023) covering revenue performance, customer trends, sales channel analysis, and demographic insights.

---

## 🎯 Problem Statement

Shield Insurance needed a comprehensive analytics solution to:
- Track overall revenue and customer performance across months and cities
- Identify top-performing sales channels and policies
- Understand demographic patterns in customer behavior and settlement rates
- Enable dynamic month-by-month comparison with last month (LM) benchmarks

---

## 📊 Dashboard Pages

### 🏠 1. Home Page
A clean landing page with navigation cards linking to all 3 analytics views.

### 📈 2. General View
High-level KPI overview of the business:
- **Total Revenue** with Last Month comparison
- **Total Customers** with Last Month comparison
- **Daily Revenue Growth (DRG)** — Average daily revenue
- **Daily Customer Growth (DCG)** — Average daily customer count
- Revenue & Customer trend by month (toggle between Revenue/Customer view)
- Revenue Split by City (table)
- Customer Split by Age Group (table)
- Customer Segmentation by City × Age Group (matrix with data bars)

### 🛍️ 3. Sales View
Sales channel performance analysis:
- Top Revenue Sales Mode (amount + channel name)
- Top Revenue Policy
- Monthly Customer Trend by Sales Mode (multi-line chart)
- Customer distribution by Sales Mode (donut chart)
- Revenue distribution by Sales Mode (donut chart)

### 👥 4. Age Group Analysis
Demographic deep-dive:
- Average Settlement % by Age Group (bar chart)
- Age Group vs Sales Mode matrix
- Age Group vs Policy Preference matrix
- Total Customers by Age Group (bar chart)
- Performance Breakdown by Age Group over time (multi-line chart)

---

## 🔍 Key Insights

| Insight | Detail |
|---------|--------|
| 💰 Total Revenue | ₹989M across 6 months |
| 👥 Total Customers | 27K+ |
| 🏙️ Top City | Delhi NCR (highest revenue & customers) |
| 📅 Peak Month | March 2023 — customer spike to 7.1K |
| 🛒 Top Sales Channel | Offline-Agent — 55.41% customers, 55.67% revenue (₹551M) |
| 📋 Top Policy | POL2005HEL |
| 👴 Highest Settlement Rate | 65+ age group at 74.33% |
| 👶 Lowest Settlement Rate | 18-24 age group at 37.51% |
| 🎯 Largest Customer Segment | 31-40 age group at 9.9K customers |
| 💡 Growth Opportunity | Digital channels hold only ~29% — significant room to grow |

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| **Power BI Desktop** | Dashboard design, visuals, navigation |
| **DAX** | Measures, KPIs, time intelligence calculations |
| **Power Query** | Data transformation and modeling |
| **Microsoft Power BI Service** | Publishing and sharing |

---

## 📐 Data Model

The data model consists of **5 interconnected tables**:

```
fact_premiums         — Premium transaction data (revenue, sales_mode, policy_id)
dim_customer          — Customer demographics (city, age_group, customer_code)
dim_date              — Date dimension (date, mmm_yy for monthly grouping)
dim_policies          — Policy reference data
fact_settlements      — Settlement data with settlement percentages
```

**Relationships:**
- `fact_premiums` → `dim_customer` (via customer_code)
- `fact_premiums` → `dim_date` (via date)
- `fact_premiums` → `dim_policies` (via policy_id)
- `fact_settlements` → `dim_customer` (via age_group)
---

## 🖼️ Dashboard Screenshots

### Home Page
![Home Page](Screenshots/Home.png)

### General View
![General View](Screenshots/General_View.png)

### Sales View
![Sales View](Screenshots/Sales_View.png)

### Age Group Analysis
![Age Group Analysis](Screenshots/Age_Group_Analysis.png)

---

## 📋 Business Questions Answered

1. How much total revenue and how many customers does Shield Insurance have?
2. Which city contributes the most revenue and customers?
3. Which month had the highest customer acquisition?
4. Which sales channel drives the most revenue?
5. What is the top-performing policy by revenue?
6. How do different age groups prefer to purchase insurance?
7. Which age group has the highest settlement rate?
8. How has daily revenue and customer growth trended month over month?

---

## 🏆 Learnings & Takeaways

- Built a **production-quality dashboard** from scratch with real business data
- Mastered **time intelligence DAX** for month-over-month comparisons
- Learned to handle **edge cases in DAX** (first month, all-months selection)
- Understood **insurance domain KPIs** — DRG, DCG, settlement rates
- Applied **UX principles** to dashboard design — consistent colors, navigation, typography
- Developed a **data storytelling** mindset — not just showing numbers, but showing insights

---
