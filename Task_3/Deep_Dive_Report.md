# Deep-Dive Report: Cohort Analysis (Customer Retention & Lifetime Value)
**ApexPlanet Software Pvt. Ltd. — Data Analytics Internship, Task 3**

---

## Why Cohort Analysis

Of the three deep-dive options (cohort, funnel, segmentation), cohort analysis was chosen because the dataset is order-level with customer IDs and dates — exactly the structure needed to group customers by their first-purchase month and track behavior over time. A funnel needs step-by-step event data we don't have; segmentation was already partially covered in Task 2's age/gender/category cuts.

---

## Method

1. Each customer's **cohort** = the calendar month of their first order
2. **Cohort Index** = number of months between that first order and any later order
3. Built a retention matrix (% of each cohort still ordering N months later) and a cumulative revenue matrix per cohort

See `cohort_analysis.py` for the full implementation and `charts/cohort_01` through `cohort_04` for visuals.

---

## Findings

### 1. Repeat purchases are rare
Only **52 of 947 customers (5.5%)** placed more than one order in the dataset's ~13-month window. The retention heatmap (`cohort_01_retention_heatmap.png`) shows month-0 at 100% (by definition) and almost everything after that in the low single digits — there's no cohort that shows a sustained, healthy retention curve.

### 2. Repeat customers still punch above their weight
Even at 5.5% of the customer base, repeat customers generated **11.6% of total revenue** (₹1.62 Cr of ₹13.94 Cr). Their average lifetime spend (₹3,11,035) is **2.3× higher** than one-time customers (₹1,37,682) — see `cohort_03_onetime_vs_repeat.png`.

### 3. Almost all repeat customers ordered exactly twice
`cohort_04_orders_per_customer.png` shows the order-count distribution is heavily concentrated at 1 and 2 — there's no customer with 3+ orders in this dataset. This points to a business that hasn't yet built a habitual repeat-purchase pattern.

### 4. Top repeat customers are high-value, not high-frequency
The top 10 repeat customers by lifetime value (table in `cohort_analysis.py` output) are all 2-order customers whose value comes from large individual orders (₹4.7L–₹8.7L total), not purchase frequency.

---

## Caveat — be upfront about sample size

This dataset has only 52 repeat customers across 13 cohort months — once split into a monthly retention grid, most cells have 0–2 customers. The retention percentages in the heatmap are **directionally correct but statistically thin**; treat them as a starting hypothesis ("this business doesn't retain customers well") rather than a precise measurement. A real production analysis would want a longer observation window and more repeat-customer volume before making retention-budget decisions off these numbers.

---

## Business Implication

The data argues for **acquisition-focused** strategy in the near term (since most revenue comes from one-time buyers), paired with a **targeted retention pilot** aimed at the customer profile that already shows 2x order behavior — since converting even a small share of one-time buyers into repeats would have an outsized revenue effect given the 2.3× LTV gap.

---

## Files
- `cohort_analysis.ipynb` — full analysis code
- `customer_ltv_summary.csv` — per-customer order count, total spend, customer type
- `charts/cohort_01_retention_heatmap.png`
- `charts/cohort_02_cumulative_ltv.png`
- `charts/cohort_03_onetime_vs_repeat.png`
- `charts/cohort_04_orders_per_customer.png`
