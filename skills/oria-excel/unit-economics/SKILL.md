---
name: unit-economics
description: Builds CAC, LTV, LTV/CAC, payback and cohort retention logic for subscription and customer-economics models.
---

# Unit Economics

Use this skill when the model needs customer-level economics instead of only aggregate P&L metrics.

## Core metrics
- CAC
- ARPU / ACV
- Gross margin contribution
- Churn / retention
- Customer lifetime
- LTV
- LTV/CAC
- CAC payback
- Cohort retention and contribution

## Recommended structure
- Assumptions
- Cohorts
- Unit Economics
- LTV-CAC
- Checks

## Core logic
CAC = Sales & Marketing spend / New customers.

Gross profit per customer-period = ARPU × Gross margin %.

Simple payback = CAC / Gross profit per customer-period.

Simple LTV = ARPU × Gross margin % / churn, when this approximation is appropriate.

For stronger analysis, calculate discounted contribution from a cohort retention grid and compare it with the closed-form LTV.

## Cohort model
- Month 0 retention = 100%.
- Each later period rolls prior retention forward using the retention/churn assumption.
- Active customers × ARPU = cohort revenue.
- Cohort revenue × gross margin = contribution.
- Discount contribution when calculating economic LTV.

## Checks
- Retention is non-increasing unless expansion logic explicitly explains otherwise.
- Churn and margin remain between valid bounds.
- CAC, LTV and payback are non-negative.
- Closed-form and cohort-derived LTV are reconciled within a stated tolerance.

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
