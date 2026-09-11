---
name: sensitivity-tables
description: Builds one- and two-variable sensitivity analysis around a model output such as NPV, IRR, margin, cash runway or valuation.
---

# Sensitivity Tables

Use this skill when a model needs to show how a decision metric changes as one or two material assumptions move.

## Workflow
1. Identify the decision output cell.
2. Identify one or two input cells that actually drive it.
3. Confirm the output is formula-linked to those inputs.
4. Define credible low/base/high or stepped ranges.
5. Build one-variable or two-variable sensitivity grids.
6. Keep the base case centered where practical.
7. Verify the base-case grid result matches the live model output.

## One-variable sensitivity
Sweep one driver across a range and record the resulting output for each input value.

## Two-variable sensitivity
Cross two material drivers, for example:
- WACC × terminal growth
- Price × volume
- Growth × margin
- Churn × acquisition
- DSO × DPO

## Rules
- Label both axes clearly with driver name and unit.
- Use absolute points for rates unless a relative change is specifically intended.
- Keep ranges credible and decision-relevant.
- Do not run a sensitivity table against a hardcoded output.
- Highlight the base case.

## Checks
- Corner/base formula references the live output.
- Center/base case matches the current model output.
- Input orientation is correct.
- No formula errors appear in the grid.

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
