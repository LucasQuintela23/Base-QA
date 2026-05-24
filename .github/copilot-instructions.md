# Copilot Instructions — Base-QA

> **Source of truth:** [.copilot/governance.md](../.copilot/governance.md)

This repository operates under a **Zero-Code First** Software Quality pipeline.
Any agent/Copilot working here MUST follow the rules below without exception.

## Critical rules
1. **NEVER** generate automation code before Phases 1, 2, and 3 are produced under `docs/` and **explicitly approved** by QA.
2. For requests such as *"create automation"*, *"new test"*, *"new project"*, *"validate functionality"* -> interrupt and request: **User Stories + Business Rules + Contracts (Swagger/OpenAPI)**.
3. Mandatory artifact sequence:
   - Phase 1 -> `docs/test_plan.md`
   - Phase 2 -> `docs/risk_analysis.md`
   - Phase 3 -> `docs/sdd_test_cases.md` (SDD + BDD in Gherkin)
   - Phase 4 -> `tests/**/*.spec.js` (Playwright + JavaScript **exclusively**)
4. At the end of each phase, ask: *"Do you agree with this phase? Can I proceed to the next stage of the pipeline?"*
5. Traceability: every Playwright test references the SDD/BDD scenario ID in the title.
6. In Phase 3, include BDD scenarios using Gherkin (`Given/When/Then`) for each specification.
7. Commit messages must follow iuricode/padroes-de-commits semantic standard (Conventional Commits style with optional emoji).
8. Language: **English**. Tone: professional, balanced.

## Allowed stack (Phase 4)
- Playwright Test (`@playwright/test`)
- JavaScript (ES2022+)
- Patterns: Page Object Model, fixtures, semantic locators, web-first `expect`.

## What NOT to do
- Do not suggest TypeScript, Cypress, Selenium, WebdriverIO, or any other framework.
- Do not create `.spec.js` without an SDD/BDD-traceable ID.
- Do not skip phases "because the request is simple".
- Do not use non-semantic commit messages.
