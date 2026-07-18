# [Pawan Guru] — Data Analyst Internship Portfolio

**ApexPlanet Software Pvt. Ltd. · FY 2025 · Data Analytics Internship**

> End-to-end analytics project: 1,000 sales orders, 5 tasks, one statistically proven business insight.

🌐 **[View Live Portfolio →](https://[YourUsername].github.io/[YourName]-DataAnalyst-Internship-Portfolio)**

---

## The Number That Matters

> **2.26×** — the Customer Lifetime Value multiplier for repeat customers vs one-time buyers.
> Confirmed via Welch t-test: t = 6.62, p < 0.0001.

This internship started with a raw Excel dataset. It ended with a formally validated, statistically significant business recommendation: invest in customer retention, because the data proves it pays 2.26× more than acquiring new customers.

---

## Project at a Glance

| Metric | Value |
|---|---|
| Dataset | 1,000 orders · 947 unique customers · 5 categories · 8 cities |
| Total Revenue Analysed | ₹13.94 Crore |
| Statistical Tests Run | 4 (3 × Welch t-test, 1 × Chi-squared) |
| Visualisations Produced | 18+ charts |
| Deliverables | Python scripts, notebooks, Excel workbooks, PPTX decks, HTML dashboard |
| Timeline | 5 tasks over 60 days |

---

## Repository Structure

```
[YourName]-DataAnalyst-Internship-Portfolio/
│
├── README.md                         ← You are here
├── index.html                        ← GitHub Pages portfolio site
│
├── Task1_Data_Wrangling/
│   ├── data_cleaning.py
│   ├── ApexPlanet_Cleaned_Dataset.xlsx
│   └── ApexPlanet_Cleaned_Dataset.csv
│
├── Task2_EDA/
│   ├── part1_univariate_analysis.py
│   ├── part2_sql_business_questions.py
│   ├── part3_corrected.ipynb         ← multivariate analysis notebook
│   ├── SQL_Query_Results.xlsx
│   ├── EDA_Report.md
│   └── charts/                       ← 18 PNG visualisations
│
├── Task3_Dashboard/
│   ├── cohort_analysis.py
│   ├── dashboard.html                ← fully interactive (open in any browser)
│   ├── customer_ltv_summary.csv
│   ├── Core_KPIs.md
│   ├── Deep_Dive_Report.md
│   ├── Power_BI_Setup_Guide.md
│   └── charts/
│
├── Task4_Storytelling/
│   ├── hypothesis_testing.py
│   ├── Task4_Final_Presentation.pptx
│   ├── Hypothesis_Testing_Summary.md
│   └── charts/
│
└── Task5_Portfolio/
    └── (this repository itself)
```

---

## The Five Tasks

### Task 1 · Data Immersion & Wrangling (10 days)
Loaded and profiled a 1,000-row sales dataset. Found and resolved 5 data quality issues: 20 missing Age values, 13 missing City values, 8 duplicate Order IDs, a string-typed date column, and Age stored as float. Added 7 engineered features (Age_Group, Order_Quarter, Revenue_Tier, etc.). Output: a professional 4-sheet Excel workbook with a Data Dictionary, Quality Assessment report, cleaned data, and summary statistics.

**Key files:** `data_cleaning.py`, `ApexPlanet_Cleaned_Dataset.xlsx`

---

### Task 2 · Exploratory Data Analysis & Business Intelligence (14 days)
Produced 18 visualisations across univariate (histograms, bar charts, pie charts), bivariate (scatter plots, box plots), and multivariate (correlation heatmap, pair plot, grouped bars) analysis. Wrote 7 SQL queries using a normalised 3-table SQLite schema — demonstrating filtering, aggregation, and multi-table JOINs. Key SQL finding: top-5 products (Laptop, Mobile) alone drive ~36% of total revenue.

**Key files:** `part2_sql_business_questions.py`, `SQL_Query_Results.xlsx`, `EDA_Report.md`

---

### Task 3 · Deep-Dive Analysis & Interactive Dashboard (12 days)
Selected **cohort analysis** as the deep-dive method. Grouped 947 customers by their first-purchase month and tracked repeat behaviour. Found that only 5.5% of customers ever returned for a second order — but those who did spent 2.26× more in lifetime value. Built a fully interactive HTML dashboard using Chart.js (category filtering, live KPI updates, hover tooltips). Also produced a step-by-step Power BI setup guide with DAX measures ready to paste.

**Key files:** `dashboard.html`, `cohort_analysis.py`, `customer_ltv_summary.csv`

---

### Task 4 · Data Storytelling & Statistical Validation (16 days)
Formulated 4 business hypotheses and tested them with formal statistical methods:

| Hypothesis | Test | p-value | Result |
|---|---|---|---|
| Gender predicts AOV | Welch t-test | 0.495 | ❌ Not significant |
| Electronics has higher AOV | Welch t-test | 0.207 | ❌ Not significant |
| Revenue tier depends on gender | Chi-squared | 0.986 | ❌ Not significant |
| **Repeat customers have higher LTV** | **Welch t-test** | **< 0.0001** | **✅ SIGNIFICANT** |

Built a 12-slide professional stakeholder presentation synthesising all findings from Tasks 1–4 into a cohesive business narrative.

**Key files:** `Task4_Final_Presentation.pptx`, `hypothesis_testing.py`, `Hypothesis_Testing_Summary.md`

---

### Task 5 · Capstone Integration & Portfolio (8 days)
Consolidated all deliverables into this master repository and live portfolio site. Built a GitHub Pages site with sticky navigation, animated evidence strip of real filenames, stats bar, task cards, findings grid, and skills catalogue.

---

## Key Technical Skills Demonstrated

| Category | Skills |
|---|---|
| **Languages** | Python 3.12, SQL, JavaScript, HTML/CSS |
| **Libraries** | Pandas, NumPy, Matplotlib, Seaborn, SciPy, OpenPyXL |
| **Statistical Methods** | Welch t-test, Chi-squared test, correlation analysis, 95% confidence intervals |
| **Analytics** | Cohort analysis, EDA, feature engineering, KPI definition |
| **Tools** | Jupyter Notebook, Power BI + DAX, Excel, PowerPoint, Chart.js, Git |

---

## Key Learnings

1. **Data quality is never free** — 5 issues found even in a "clean" dataset; systematic profiling before any analysis is non-negotiable.
2. **Statistical significance ≠ business significance** — Electronics dominates revenue (36.4%), but not because it has a statistically higher per-order price (H2 rejected). Volume matters more than AOV for this category.
3. **Small samples need honest labelling** — with only 52 repeat customers, cohort retention percentages are directionally correct but statistically thin. I flagged this rather than overselling the charts.
4. **The most actionable finding is often the simplest** — not a complex ML model, but one t-test: retain customers, because they're worth 2.26× more, and that's proven at p < 0.0001.

---


---

*ApexPlanet Data Analytics Internship · FY 2025 · 1,000 orders · 5 tasks · 4 hypothesis tests · 18+ charts*
