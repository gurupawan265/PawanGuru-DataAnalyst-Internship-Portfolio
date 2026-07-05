# Hypothesis Testing Summary
**ApexPlanet Data Analytics Internship — Task 4**
**Statistical significance level: α = 0.05 · All t-tests use Welch's method (unequal variances)**

---

## Overview

Four business hypotheses were formulated from the EDA and cohort findings in Tasks 2–3, then tested using formal statistical methods. Three were disproved; one was confirmed with extremely strong evidence.

---

## H1 — Gender vs Average Order Value

**Test:** Independent two-sample t-test (Welch's, two-tailed)
**H₀:** Mean order value is equal for Male and Female customers
**H₁:** Mean order value differs between genders

| Metric | Value |
|---|---|
| Male mean AOV | ₹1,41,807 (n=511) |
| Female mean AOV | ₹1,36,883 (n=489) |
| t-statistic | 0.683 |
| p-value | 0.495 |
| 95% CI on difference | approximately −₹10K to +₹20K |
| **Result** | **Fail to reject H₀ — not significant** |

**Business conclusion:** Gender does not predict spending. Avoid gender-based pricing strategies or gender-targeted campaign budget allocation based on AOV — the data does not support it.

---

## H2 — Electronics Average Order Value vs Other Categories

**Test:** Independent one-sample t-test (Welch's, one-tailed, right-side)
**H₀:** Electronics AOV = AOV of other categories
**H₁:** Electronics has a higher AOV than other categories

| Metric | Value |
|---|---|
| Electronics mean AOV | ₹1,43,442 (n=354) |
| Other categories mean AOV | ₹1,37,184 (n=646) |
| t-statistic | 0.818 |
| p-value | 0.207 |
| **Result** | **Fail to reject H₀ — not significant** |

**Business conclusion:** Electronics leads in revenue through order volume (354 orders, 36.4% revenue share), not because it commands a meaningfully higher per-order price. Supply chain and stock protection matter more than Electronics-specific premium pricing.

---

## H3 — Revenue Tier Independence from Gender

**Test:** Pearson Chi-squared test of independence
**H₀:** Revenue tier (Low / Medium / High) is independent of Gender
**H₁:** Revenue tier distribution differs by Gender

| Metric | Value |
|---|---|
| chi2 statistic | 0.028 |
| Degrees of freedom | 2 |
| p-value | 0.986 |
| **Result** | **Fail to reject H₀ — not significant** |

**Observed counts:**

|  | High_Revenue | Low_Revenue | Medium_Revenue |
|---|---|---|---|
| Female | 165 | 162 | 162 |
| Male | 175 | 168 | 168 |

**Business conclusion:** Revenue tiers distribute almost perfectly equally across genders (p=0.986 — near-perfect independence). Gender-based tier targeting will not improve segmentation.

---

## H4 — Repeat vs One-Time Customer Lifetime Value ✅ KEY FINDING

**Test:** Independent one-tailed t-test (Welch's), one-tailed (repeat > one-time)
**H₀:** Mean lifetime value of repeat customers = one-time customers
**H₁:** Repeat customers have a higher mean lifetime value

| Metric | Value |
|---|---|
| Repeat customer mean LTV | ₹3,11,035 (n=52) |
| One-time customer mean LTV | ₹1,37,682 (n=895) |
| LTV ratio | **2.26×** |
| LTV difference | **₹1,73,353 more per repeat customer** |
| t-statistic | **6.622** |
| p-value | **9.02 × 10⁻⁹ (< 0.0001)** |
| **Result** | **✅ REJECT H₀ — HIGHLY SIGNIFICANT** |

**Business conclusion:** With p < 0.0001 and t = 6.62, this is the strongest statistical finding in the entire analysis. Repeat customers are demonstrably and substantially more valuable. A retention investment targeting the 895 one-time buyers is the single highest-ROI action available. Even converting 10% of them to repeat buyers adds approximately ₹1.5 Crore in incremental revenue at near-zero acquisition cost.

---

## Summary Table

| ID | Test | p-value | Significant? | Business Action |
|---|---|---|---|---|
| H1 | t-test, gender vs AOV | 0.495 | ❌ No | Gender irrelevant for pricing |
| H2 | t-test, Electronics AOV | 0.207 | ❌ No | Volume, not price, drives dominance |
| H3 | χ²-test, tier vs gender | 0.986 | ❌ No | No gender-tier targeting benefit |
| H4 | t-test, repeat vs one-time LTV | <0.0001 | **✅ Yes** | **Build a retention programme** |

---

## Descriptive Statistics Reference

| Variable | Mean | Std Dev | Skew | 95% CI (where applicable) |
|---|---|---|---|---|
| Age | 41.35 | 13.68 | 0.04 | — |
| Quantity | 5.44 | 2.84 | 0.06 | — |
| Unit_Price | ₹25,487 | ₹14,179 | -0.03 | — |
| Total_Sales (AOV) | ₹1,39,399 | ₹1,14,100 | 0.99 | ₹1,32,319 – ₹1,46,480 |
