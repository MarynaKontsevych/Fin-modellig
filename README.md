# Fin-modellig

Curated finance and financial-modeling skills for Claude/Codex-style agent workflows.

## Purpose
This repository is a practical working library for building professional financial models, FP&A workflows, scenario analysis, sensitivity analysis, unit economics, model audit, and executive outputs.

## Included skills

### Modeling architecture
- `model-architecture-template` — master workbook architecture, tabs, conventions, checks, versioning.
- `inputs-calcs-outputs-design` — strict separation of inputs, calculations, and outputs.
- `assumption-registry-builder` — auditable assumption register with sources, scenarios, owners, sensitivity and sign-off.

### Driver-based modeling
- `revenue-build` — bottom-up driver-based revenue model.
- `unit-economics` — CAC, LTV, LTV/CAC, payback and cohort logic.

### Scenarios and sensitivity
- `scenario-manager` — Base/Bull/Bear scenario switching layer.
- `sensitivity-tables` — one- and two-variable sensitivity analysis.

### QA and client delivery
- `formula-audit-checker` — systematic formula/model quality audit.
- `output-summary-tab` — executive one-page summary for board/client use.

## Sources and licenses
The skills currently copied into `skills/oria-excel/` come from the MIT-licensed repository:
- https://github.com/andreworia/claude-excel-skills

The original MIT license is preserved in `third-party/oria-excel/LICENSE`.

## Recommended repositories not copied here
These are useful references but should be reviewed separately before redistribution or integration:
- https://github.com/m-binimran/finance-pack — FP&A, forecasting, variance analysis, KPI dashboards, budget planning and finance guardrails.
- https://github.com/willpowerju-lgtm/3-statement-ultra-for-finance — advanced three-statement Excel model workflow and QC gates.
- https://github.com/alirezarezvani/claude-skills — broad agent-skill library including a financial analyst skill.
- https://github.com/BillZhenZhang/Financial_Modeling_Skills — investment-banking-style DCF skill.
- https://github.com/andreworia/claude-finance-skills — valuation, corporate finance, IB/PE and financial-modeling agent packs.

## Suggested workflow
`model-architecture-template` → `inputs-calcs-outputs-design` → `assumption-registry-builder` → `revenue-build` / `unit-economics` → `scenario-manager` → `sensitivity-tables` → `formula-audit-checker` → `output-summary-tab`

This repository is intended as a curated working toolkit; source attribution and original licenses should be preserved whenever third-party material is added.
