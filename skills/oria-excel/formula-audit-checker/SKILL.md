---
name: formula-audit-checker
description: Runs a systematic audit of financial-model formulas, hardcodes, circular references, broken names, sign conventions, lookup errors and sensitivity integrity.
---

# Formula Audit Checker

Use this skill before a model goes to a client, board, investment committee, lender or other decision-maker.

## Audit sequence
1. Save a versioned working copy.
2. Scan for Excel errors: `#REF!`, `#DIV/0!`, `#VALUE!`, `#NAME?`, unexpected `#N/A`.
3. Find circular references and confirm whether any are genuinely intentional.
4. Trace precedents for major outputs such as Revenue, EBITDA, FCF, cash, valuation and IRR.
5. Trace dependents for key calculation outputs.
6. Hunt for hardcoded assumptions buried inside formulas.
7. Review lookup formulas and error handling.
8. Check named ranges for broken or stale references.
9. Verify sign conventions across P&L, working capital and cash flow.
10. Verify sensitivity-table input cells actually feed the live model.
11. Flag formulas that are unnecessarily long, nested or opaque.
12. Record every issue in an audit log.

## Hardcode rule
Material assumptions should live in Inputs/Assumptions, not inside calculation formulas. Constants that are structural rather than assumptions should still be documented when they are not self-evident.

## Audit log
Recommended fields:
- Finding ID
- Tab
- Cell
- Issue type
- Severity
- Description
- Status
- Fixed by
- Date fixed

Issue types can include: hardcoded value, circular reference, formula error, lookup/error-handling problem, sign inconsistency, broken named range, sensitivity error, formula complexity.

## Severity
- Critical: model currently produces or can readily produce a wrong decision output.
- Major: error emerges under certain conditions or materially weakens reliability.
- Minor: convention/documentation problem without current material output impact.

## Pass logic
Fail if Critical or unresolved Major findings remain. Conditional pass when only low-risk issues remain. Record the basis for any accepted exception.

## Source
Adapted from `andreworia/claude-excel-skills`, MIT License. Copyright (c) 2026 Oria.
