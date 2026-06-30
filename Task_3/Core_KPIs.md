# Core KPIs — ApexPlanet Sales Analytics
**Task 3: Deep-Dive Analysis & Interactive Dashboarding**

Five KPIs were selected to give complete coverage of revenue, customer behavior, and operational volume — each with a clear formula, current value, and business rationale.

---

### 1. Total Revenue
**Formula:** `SUM(Total_Sales)`
**Current value:** ₹13,93,99,439.65 (≈ ₹13.94 Cr)
**Business rationale:** The core top-line growth metric. Every other KPI exists to explain *why* this number moves.

---

### 2. Average Order Value (AOV)
**Formula:** `Total Revenue ÷ Total Orders`
**Current value:** ₹1,39,399.44
**Business rationale:** Tracks pricing and upsell effectiveness. A rising AOV with flat order count means customers are buying more per visit — a healthier growth lever than discounting for volume.

---

### 3. Repeat Purchase Rate
**Formula:** `(Customers with >1 order ÷ Total unique customers) × 100`
**Current value:** 5.5% (52 of 947 customers)
**Business rationale:** Directly measures retention and loyalty. This is the KPI the cohort deep-dive is built around — a low rate here signals the business is acquisition-dependent rather than retention-driven, which changes where marketing spend should go.

---

### 4. Customer Lifetime Value (CLV) — Repeat Segment
**Formula:** `AVG(Total_Sales) for customers with >1 order`
**Current value:** ₹3,11,034.64 average per repeat customer (vs. ₹1,37,682.28 for one-time customers — 2.3× higher)
**Business rationale:** Quantifies exactly how much more valuable a retained customer is. This is the number that justifies investment in retention campaigns: even a small shift of one-time buyers into the repeat segment has an outsized revenue effect.

---

### 5. Revenue Concentration by Category
**Formula:** `SUM(Total_Sales) GROUP BY Category`, expressed as % of Total Revenue
**Current value:** Electronics ≈ 36% of total revenue (highest of 5 categories)
**Business rationale:** Flags dependency risk. If over a third of revenue rides on one category, that category's supply chain, pricing, and competitive position deserve closer monitoring than the others.

---

## Summary Table

| KPI | Formula | Current Value |
|---|---|---|
| Total Revenue | SUM(Total_Sales) | ₹13.94 Cr |
| Average Order Value | Total Revenue ÷ Orders | ₹1,39,399 |
| Repeat Purchase Rate | Repeat Customers ÷ Total Customers | 5.5% |
| CLV (Repeat Segment) | AVG(Total_Sales) for repeat customers | ₹3,11,035 |
| Revenue Concentration | Top category's % of total revenue | 36% (Electronics) |
