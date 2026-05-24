# Commit Convention Quick Reference

This file provides copy-and-paste commit message examples based on iuricode/padroes-de-commits.

## Standard format

`<type>: <short description>`

Examples:
- `docs: update QA pipeline guide`
- `feat: add requirement repository`
- `fix: correct stage 005 approval checklist`

## Recommended types

- `feat`: new feature
- `fix`: bug fix
- `docs`: documentation only changes
- `test`: test-related changes
- `build`: dependencies/build setup
- `perf`: performance improvements
- `style`: formatting and linting
- `refactor`: internal restructuring without behavior changes
- `chore`: maintenance and config
- `ci`: CI pipeline changes
- `raw`: config/data/parameter changes
- `cleanup`: dead code cleanup
- `remove`: file/feature removal

## Copy-and-paste by stage

### Stage 001 - Intake
- `docs: fill stage 001 intake specification`
- `raw: add requirement package for new request`

### Stage 002 - Planning
- `docs: fill stage 002 planning test plan`

### Stage 003 - Risk Analysis
- `docs: fill stage 003 risk analysis matrix`

### Stage 004 - SDD + BDD
- `docs: model stage 004 sdd bdd gherkin scenarios`

### Stage 005 - Approval Gate
- `docs: register stage 005 approval evidence`
- `chore: update approval gate decision status`

### Stage 006 - Automation
- `test: add playwright scenarios for approved sdd bdd ids`
- `feat: implement approved automation flow`
- `fix: correct failing scenario mapping`

## Suggested commit bodies and footers

Body example:

`Implements approved scenarios for checkout boundary validation.`

`Keeps traceability with SDD-BDD IDs in test titles and evidence.`

Footer example:

`Refs: REQ-20260524-001`

`Reviewed-by: QA Team`

## Practical command examples

- `git commit -m "docs: fill stage 001 intake specification"`
- `git commit -m "docs: model stage 004 sdd bdd gherkin scenarios"`
- `git commit -m "test: add playwright scenarios for approved sdd bdd ids"`
