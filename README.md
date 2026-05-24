# Base-QA

Base-QA is an opinionated starter kit to accelerate software quality projects with a strong focus on governance, traceability, and predictable delivery.

The repository follows a **Zero-Code First** approach: before any automation starts, the team must produce and approve planning, risk, and test modeling artifacts.

## Purpose

- Standardize the QA pipeline from discovery to automation.
- Ensure automated tests are derived from clear specifications.
- Reduce rework caused by missing functional and technical context.

## Principles

- Mandatory phase-based governance.
- End-to-end traceability (documentation -> scenarios -> scripts).
- Automation is allowed only after explicit QA approval.
- Exclusive automation stack: Playwright + JavaScript.

## How to use this project

### 1) Prepare required inputs

Before you start, consolidate:

- User Stories (US)
- Business Rules (BR)
- Technical contracts (Swagger/OpenAPI) and/or screen/route map

Without these inputs, the pipeline must not move forward.

### 2) Run the quality pipeline

#### Phase 1 - Planning
File: `docs/test_plan.md`

Expected content:

- Scope (In-scope / Out-of-scope)
- Test approach (API, E2E, contract, etc.)
- Entry (Ready) and Exit (Done) criteria

Mandatory checkpoint at the end of the phase:

> "Do you agree with this phase? Can I proceed to the next stage of the pipeline?"

#### Phase 2 - Risk Analysis
File: `docs/risk_analysis.md`

Expected content:

- Matrix with: Risk | Category | Probability | Impact | Mitigation

Mandatory checkpoint at the end of the phase:

> "Do you agree with this phase? Can I proceed to the next stage of the pipeline?"

#### Phase 3 - SDD Modeling
File: `docs/sdd_test_cases.md`

Expected content per specification:

- [ID] Specification name
- Expected behavior
- Scenario checklist:
	- Happy path
	- Exception/negative flows
	- Boundary values
- Preconditions and test data

Mandatory checkpoint at the end of the phase:

> "Do you agree with this phase? Can I proceed to the next stage of the pipeline?"

#### Phase 4 - Automation (only after Phase 3 approval)
Target: `tests/**/*.spec.js`

Rules:

- Implement only scenarios approved in SDD.
- Maintain traceability: include SDD ID in test title.
- Use Playwright Test with JavaScript exclusively.

## Project architecture

Current structure:

```text
Base-QA/
├── .copilot/
│   └── governance.md
├── .github/
│   └── copilot-instructions.md
├── docs/
│   └── qa-pipeline-guide.md
└── README.md
```

Target architecture after automation is unlocked (Phase 4):

```text
Base-QA/
├── .copilot/
│   └── governance.md
├── .github/
│   └── copilot-instructions.md
├── docs/
│   ├── test_plan.md
│   ├── risk_analysis.md
│   └── sdd_test_cases.md
├── pages/
├── fixtures/
├── utils/
├── tests/
│   └── *.spec.js
└── playwright.config.js
```

## Key files and ownership

- `.copilot/governance.md`: official pipeline rules and lock/unlock criteria.
- `.github/copilot-instructions.md`: operational instructions for any agent/Copilot working in this repo.
- `docs/test_plan.md`: tactical test plan.
- `docs/risk_analysis.md`: technical/business risk matrix.
- `docs/sdd_test_cases.md`: approved scenario base for automation.
- `tests/**/*.spec.js`: automated implementation traceable to SDD IDs.

## Recommended operating flow

1. Receive the validation request.
2. Collect US + BR + contracts.
3. Produce and approve Phase 1.
4. Produce and approve Phase 2.
5. Produce and approve Phase 3.
6. Only then start Phase 4 (code).

## Compliance rules

- Do not skip phases.
- Do not generate code before approvals.
- Do not use frameworks outside the defined stack.
- Do not create tests without explicit linkage to an SDD ID.

## Language and communication

- Default language: English.
- Tone: professional and objective.
- Documents must always be scannable (lists, tables, and clear structure).
