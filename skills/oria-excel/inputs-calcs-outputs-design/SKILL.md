---
name: inputs-calcs-outputs-design
description: Enforces clean separation of Inputs, Calculations, and Outputs in professional Excel financial models.
---

# Inputs / Calculations / Outputs Design

Use this skill when building or restructuring a financial model that must be auditable, maintainable and client-ready.

## Core principle
Separate:
1. **Inputs** — editable assumptions and sourced hardcodes.
2. **Calculations** — formula logic only, no hidden hardcodes.
3. **Outputs** — references to final calculated results, charts and presentation-ready summaries.

## Inputs tab
- Put all material assumptions in one place.
- Use clear labels, units, sources and notes.
- Distinguish manually entered assumptions from derived assumptions.
- Lock non-input cells where practical.
- Use consistent formatting so editable cells are obvious.

## Calculation tabs
- One calculation module per business logic block when possible.
- Never bury assumptions inside formulas.
- Reference Inputs explicitly or via named ranges.
- Break long nested formulas into readable helper rows.
- Keep one consistent formula pattern across a row/period series.
- Separate operating drivers, revenue build, costs, working capital, statements, valuation and sensitivities when complexity requires it.

## Outputs tab
- Use only direct references to calculated results, not new analytical logic.
- Present decision-relevant KPIs, scenario comparison, sensitivity results and charts.
- Make the page printable and understandable without navigating the full workbook.

## Quality checklist
- All material hardcodes are visible and documented.
- No unexplained constants are embedded in calculation formulas.
- Output metrics trace cleanly back to calculations and assumptions.
- Cross-sheet links are readable and stable.
- Model conventions are documented.
- Inputs, formulas and outputs use visibly distinct formatting.

## Typical financial-model architecture
`Cover → Assumptions/Inputs → Data → Revenue/Cost/Working Capital builds → P&L/BS/CF → Scenarios/Sensitivity → Checks → Executive Summary`

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
