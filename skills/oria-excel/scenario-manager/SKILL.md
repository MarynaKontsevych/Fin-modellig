---
name: scenario-manager
description: Builds a visible, auditable Base/Bull/Bear scenario layer with a selector, active assumption links, side-by-side outputs and validation checks.
---

# Scenario Manager

Use this skill when a financial model needs clean Base/Bull/Bear switching without hiding assumptions in Excel's built-in Scenario Manager.

## Structure
- `Scenario Inputs`: one row per driver, columns for Base, Bull, Bear and Active.
- `Selector`: one visible control cell choosing the active case.
- `Model links`: model assumptions reference the Active column.
- `Outputs`: compare Base/Bull/Bear side by side.
- `Checks`: verify selector, completeness and case integrity.

## Formula patterns
Use a selector value 1/2/3 and formulas such as:
`=CHOOSE(selector, Base, Bull, Bear)`
or
`=INDEX(Base:Bear, selector)`.

## Rules
- Never retype the active case value into the model.
- Keep scenario-controlled assumptions visible and traceable.
- Keep case values on-sheet so reviewers can audit them.
- Where possible, show all three outputs side by side, not only the currently selected case.

## Checks
- Selector is valid.
- No scenario driver is blank.
- Active value matches the selected case.
- Directional sanity: Bull should not accidentally produce a worse headline output than Base unless model economics genuinely imply it.

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
