# Requirements Repository

Central folder to store all incoming User Stories (US) and Business Rules (BR) for future consultation.

## Purpose
- Keep requirement history versioned in the repository.
- Reuse past rules in new test cycles.
- Ensure traceability from requirements to SDD/BDD and automation.

## Folder structure
- `incoming/`: one file per request using the standard template.
- `index.md`: catalog of all requirement packages.
- `TEMPLATE-US-BR.md`: base template to create new requirement packages.

## Naming convention for new files
`REQ-YYYYMMDD-###-short-name.md`

Example:
`REQ-20260524-001-user-onboarding.md`

## Minimal flow
1. Copy `TEMPLATE-US-BR.md` into `incoming/` with a new request name.
2. Fill US, BR, contracts, assumptions, and open questions.
3. Register the new file in `index.md`.
4. Reference this file in Stage 001 template.
