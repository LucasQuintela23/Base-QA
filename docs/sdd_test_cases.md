# SDD + BDD Test Cases (Gherkin)

## Document Control
- Project:
- Version:
- Owner:
- Date:
- Status: Draft

## Modeling Rules
- Every specification must have a unique SDD/BDD ID.
- Every scenario must include Given/When/Then.
- Every scenario must map to at least one business rule.
- Scenario IDs must be used later in automation titles.

## Specification Template

### [SDD-BDD-001] - Specification Name

#### Expected Behavior
Describe the rule validated by this specification.

#### Related Business Rules
- BR-001

#### Preconditions and Test Data
- Preconditions:
- Test data:

#### Scenario Checklist
- [ ] Happy path
- [ ] Exception/negative flow
- [ ] Boundary limits

#### Gherkin Scenarios
```gherkin
Feature: <Feature name>

  Scenario: [SDD-BDD-001] Happy path
    Given <initial context>
    When <action>
    Then <expected outcome>

  Scenario: [SDD-BDD-001-N01] Negative flow
    Given <initial context>
    When <invalid action>
    Then <error or rejection>

  Scenario: [SDD-BDD-001-B01] Boundary limit
    Given <boundary condition>
    When <action at limit>
    Then <expected boundary behavior>
```

#### Acceptance Notes
- 

---

## Traceability Matrix
| Scenario ID | Specification | Business Rule | Contract/Endpoint or Screen | Planned Automation File |
|---|---|---|---|---|
| SDD-BDD-001 |  |  |  | tests/*.spec.js |

## Approval Checkpoint
Do you agree with this phase? Can I proceed to the next stage of the pipeline?
