---
name: assumption-registry-builder
description: Builds an auditable assumption register with base/bull/bear values, sources, owners, monitoring flags and sensitivity ranking.
---

# Assumption Registry Builder

Use this skill when a model needs formal assumption governance for client handover, board review, recurring FP&A use, valuation or capital-allocation decisions.

## Register structure
Recommended columns:
- ID
- Assumption name
- Category
- Base value
- Unit
- Source / rationale
- Bull value
- Bear value
- Sensitivity rank
- Impact on key output
- Monitoring flag
- Owner
- Last verified date
- Notes
- Optional sign-off and change-vs-prior fields

## Rules
- Link Base Value to the actual model input cell instead of duplicating a static number.
- Every material assumption needs a source or explicit rationale.
- Separate sourced facts from management assumptions and analyst assumptions.
- Pull Bull/Bear from the scenario layer where available.
- Rank assumptions by impact on a chosen key output using sensitivity/tornado results.
- Mark high-impact uncertain assumptions for active monitoring.
- Track who owns each assumption and when it was last verified.

## Sensitivity ranking
Use absolute change in the decision metric between low and high assumption values. Sort largest impact first. A numeric rank can be converted into High/Medium/Low tiers.

## Monitoring protocol
For each actively monitored assumption record:
- owner,
- review frequency,
- data source,
- next review date,
- trigger threshold that forces a forecast/scenario refresh.

## Sign-off
For decision-use models, include reviewer/sign-off fields and flag material assumptions that remain unapproved.

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
