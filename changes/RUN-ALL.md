# RUN ALL - Pipeline Orchestrator

Use this file as the single operational checklist to execute all stages in sequence.

## Requirement Intake First
Before Stage 001, create or update a requirement package in `../requirements/incoming/` and register it in `../requirements/index.md`.

## Stage Order
1. 001-intake-specification
2. 002-planning-test-plan
3. 003-risk-analysis
4. 004-sdd-bdd-gherkin-modeling
5. 005-approval-gate
6. 006-automation-playwright-js

## Fill-in Templates
1. `001-intake-specification/TEMPLATE.md`
2. `002-planning-test-plan/TEMPLATE.md`
3. `003-risk-analysis/TEMPLATE.md`
4. `004-sdd-bdd-gherkin-modeling/TEMPLATE.md`
5. `005-approval-gate/TEMPLATE.md`
6. `006-automation-playwright-js/TEMPLATE.md`

## Suggested commits by stage

| Stage | Suggested commit message |
|---|---|
| Requirement intake | `🗃️ raw: add requirement package for new request` |
| 001 | `📚 docs: fill stage 001 intake specification` |
| 002 | `📚 docs: fill stage 002 planning test plan` |
| 003 | `📚 docs: fill stage 003 risk analysis matrix` |
| 004 | `📚 docs: model stage 004 sdd bdd gherkin scenarios` |
| 005 | `📚 docs: register stage 005 approval evidence` |
| 006 | `🧪 test: add playwright scenarios for approved sdd bdd ids` |

Detailed reference:

- `../docs/commit-convention.md`

## Global Execution Checklist
- [ ] Requirement package created or updated in requirements/incoming
- [ ] Requirement package registered in requirements/index.md
- [ ] Stage 001 completed
- [ ] Stage 002 completed
- [ ] Stage 003 completed
- [ ] Stage 004 completed
- [ ] Stage 005 completed and approved
- [ ] Stage 006 unlocked and executed

## Gate Policy
Do not run Stage 006 until stages 001-005 are complete and approved.
