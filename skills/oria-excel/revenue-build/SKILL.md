---
name: revenue-build
description: Builds a bottom-up driver-based revenue forecast using customers/units, acquisition, churn, ARPU/price, scenarios and checks.
---

# Revenue Build

Use this skill when revenue must be modeled from operating drivers instead of a single top-down growth percentage.

## Typical drivers
- Starting customers or units
- New customer additions
- Marketing spend and CAC, or funnel conversion
- Churn / retention
- ARPU / average price
- Product mix or volume × price
- Base/Bull/Bear multipliers

## Core roll-forward
For each period:
- Beginning customers/units
- New additions
- Churn/losses
- Ending customers/units
- Revenue = ending or average active base × ARPU, or volume × price

For subscription models, add ARR/MRR and retention metrics where relevant.

## Recommended workbook structure
- Cover
- Drivers
- Revenue Build
- Summary
- Sensitivity
- Checks

## Modeling rules
- Keep all constants on Drivers/Inputs.
- Use one consistent formula across the time series.
- Use absolute references for driver cells.
- Never mix hidden hardcodes into forecast formulas.
- Distinguish source facts, assumptions and formulas.

## Scenario layer
Use a visible scenario selector and Base/Bull/Bear assumptions for the drivers that matter most. Do not hide scenarios inside Excel's built-in Scenario Manager when auditability matters.

## Checks
- Ending = Beginning + Adds - Churn
- Current beginning = prior ending
- Revenue and customers never go negative
- Churn remains within a valid range
- Growth stays within a defined sanity band

## Deliverables
- Driver table
- Period-by-period revenue build
- Annual/quarterly summary
- Scenario comparison
- Sensitivity view
- Model checks

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
