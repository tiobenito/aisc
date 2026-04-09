# Expense Report Summary

**Generated:** 2026-04-21
**Source:** messy-expenses.csv (38 rows raw, 36 rows cleaned)

---

## Overview

| Metric | Value |
|--------|-------|
| Total Expenses | $6,185.19 |
| Date Range | 2026-04-08 to 2026-04-20 |
| Total Entries | 36 (after cleanup) |
| Categories | 7 |
| Unique Vendors | 19 |

---

## Spend by Category

| Category | Total | % of Total | # Entries |
|----------|-------|------------|-----------|
| Travel | $2,384.75 | 38.6% | 15 |
| Meals | $1,399.10 | 22.6% | 10 |
| Software | $700.67 | 11.3% | 3 |
| Training | $899.00 | 14.5% | 1 |
| Office | $246.52 | 4.0% | 3 |
| Client Relations | $125.00 | 2.0% | 1 |
| Phone | $85.00 | 1.4% | 1 |

**Note:** Travel + Meals account for 61.2% of total spend.

---

## Top Vendors

| Vendor | Total | # Transactions |
|--------|-------|----------------|
| Delta Airlines | $2,490.00 | 2 |
| United Airlines | $1,056.00 | 2 |
| TechCrunch Disrupt | $899.00 | 1 |
| Nobu | $520.00 | 1 |
| Marriott | $578.00 | 2 |
| HubSpot | $450.00 | 1 |

---

## Anomalies & Flags

- **2 duplicate entries removed** -- Starbucks breakfast on 04/09 appeared twice (rows 5 & 7), United Airlines flight on 04/16 appeared twice (rows 27 & 30)
- **3 missing dates** -- inferred from surrounding context (taxi, parking, and one other)
- **4 missing categories** -- assigned based on description (gift basket -> Client Relations, taxi -> Travel, working lunch -> Meals, parking -> Travel)
- **1 vendor typo corrected** -- "Starbacks" -> "Starbucks"
- **Large single expenses** -- Delta flights ($1,245 each), TechCrunch Disrupt ($899), Nobu dinner ($520). These may warrant manager approval depending on policy.
- **Inconsistent vendor casing** -- "uber", "UBER", "Uber" all normalized to "Uber"

---

## Cleanup Summary

| Issue | Count | Action |
|-------|-------|--------|
| Date formats standardized | 38 | All converted to YYYY-MM-DD |
| Categories normalized | 12 | Mapped to 7 canonical categories |
| Duplicates removed | 2 | Kept first occurrence, flagged in notes |
| Missing dates inferred | 3 | Estimated from surrounding entries |
| Missing categories assigned | 4 | Inferred from description |
| Amount formatting fixed | 4 | Stripped "$" and commas, consistent decimals |
| Vendor names corrected | 4 | Typos fixed, casing standardized |

**Raw rows:** 38 | **Cleaned rows:** 36 | **Issues fixed:** 27
