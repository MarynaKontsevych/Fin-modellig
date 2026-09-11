---
name: output-summary-tab
description: Designs a one-page executive summary tab for a financial model with KPIs, decision narrative, scenario/sensitivity summary and key assumptions.
---

# Output Summary Tab

Use this skill when a completed model needs a client-, board- or management-facing front page.

## Goal
The summary must answer the decision question without forcing the reader to navigate calculation tabs.

## Recommended layout
- Title/metadata strip
- 4-6 KPI tiles
- Main conclusion / management narrative
- Scenario or sensitivity summary
- Key assumption log
- Version/date/confidentiality footer

## KPI selection
Choose only decision-relevant metrics. Depending on the model this may include revenue, gross margin, EBITDA, cash runway, working capital, enterprise/equity value, IRR, payback, ROIC, CAC/LTV or covenant headroom.

## Narrative
Lead with the conclusion, then 2-4 quantified supporting observations and the decision implication. Clearly separate confirmed facts from assumptions/hypotheses.

## Assumptions
Show the most material assumptions and reference the actual Inputs/Assumptions cells rather than copying static values.

## Rules
- Do not introduce new calculation logic on the summary tab.
- Trace every number back to a model output or input.
- Keep the page printable in landscape on one page where practical.
- Remove unnecessary gridlines and working-model clutter.
- Include scenario/sensitivity range when the decision depends heavily on uncertain drivers.

## Screenshot test
A reader seeing only this tab should understand:
1. what the model says,
2. why,
3. which assumptions matter,
4. what could change the answer,
5. what decision/action follows.

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
