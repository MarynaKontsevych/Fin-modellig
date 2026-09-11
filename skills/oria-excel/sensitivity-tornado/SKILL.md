---
name: sensitivity-tornado
description: Ranks model assumptions by their impact on a key output and structures a tornado sensitivity analysis.
---

# Sensitivity Tornado

Use this skill when you need to answer: which assumptions actually drive the model result?

## Workflow
1. Choose one decision-relevant output: EBITDA, cash runway, NPV, IRR, equity value, Year-5 revenue, etc.
2. Select 8-15 uncertain material assumptions.
3. Define credible low/high ranges for each assumption.
4. Change one variable at a time, keeping all others at Base.
5. Record low-output and high-output results.
6. Calculate absolute impact range.
7. Rank assumptions from highest to lowest impact.

## Tornado table
Recommended columns:
- Variable
- Base assumption
- Low assumption
- High assumption
- Base output
- Low output
- High output
- Downside vs Base
- Upside vs Base
- Absolute range
- Swing rationale

## Interpretation
The top drivers should receive:
- stronger evidence and validation,
- explicit scenario treatment,
- management attention,
- regular monitoring,
- visibility in client/board outputs.

Low-impact variables usually do not deserve the same modeling complexity.

## Chart
Use a horizontal bar chart centered on Base/zero impact. Plot downside and upside for each driver and order the largest total range at the top.

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
