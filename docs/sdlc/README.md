# wedgw — SDLC Documentation

> Maintained by QuorQ AI SDLC. Text between `sdlc:auto` markers is regenerated; anything outside them is yours and is kept.

<!-- sdlc:auto:start overview -->
weight and height tracker for kids

**Documentation version:** v3
<!-- sdlc:auto:end overview -->

## Contents

<!-- sdlc:auto:start contents -->
| Document | State |
|---|---|
| [Requirements](requirements/README.md) | v1 approved |
| [Architecture](architecture/README.md) | 13 entries |
| [Development](development/README.md) | 8 entries |
| [Testing](testing/README.md) | 1 entry |
| [Deployment](deployment/README.md) | 1 entry |
| [Maintenance](maintenance/README.md) | 1 entry |
| [Data model](architecture/data-model.md) | generated |
| [API (OpenAPI)](architecture/api/openapi.yaml) | generated |
| [Decisions (ADRs)](architecture/adr/README.md) | 4 decisions |
| [Sprint plan](development/sprint-plan.md) | 7 sprints |
| [Developer guide](development/developer-guide.md) | generated |
| [API reference](development/api-reference.md) | 1 route |
| [Test report](testing/test-report.md) | not run yet |
| [Tests](testing/test-cases.md) | 0 tests |
| [Deployment guide](deployment/deployment-guide.md) | not deployed yet |
| [Runbook](deployment/runbook.md) | not deployed yet |
| [Release notes](deployment/release-notes.md) | 0 releases |
| [Traceability matrix](traceability-matrix.md) | 20 requirements |
| [Changelog](CHANGELOG.md) | 3 versions |
<!-- sdlc:auto:end contents -->

## Open gaps

<!-- sdlc:auto:start open-gaps -->
### Requirements

- No architecture input yet confirms this stack is actually being used for design -- architecture phase has not started.

### Architecture

- No requirements-phase input was provided for this project, so this architecture's references to NFR-001 through NFR-005 cannot be traced back to an approved requirements document.
- Entity list does not include a units/preferences table separate from parents.preferred_unit_system -- confirm this single field is sufficient for the PATCH /me/preferences endpoint's needs.
- NFR-004 and NFR-005 are referenced but no requirements-phase input exists yet to confirm their exact wording or approval.
- NFR-002 is referenced but no requirements-phase input exists yet to confirm its exact wording or approval.
- NFR-003 is referenced but no requirements-phase input exists yet to confirm its exact wording or approval.
- NFR-001 is referenced but no requirements-phase input exists yet to confirm its exact wording or approval.

### Development

- No actual development execution evidence (commits, code artifacts, ticket status, test results) has been provided for any sprint or story -- only the approved plan/backlog is available.
- Role assignment for US-006 (qa-agent) differs from the otherwise backend/frontend split seen elsewhere in the backlog; input does not explain the rationale, so this is noted rather than assumed.
- No completion status, code commits, or test results reported for Sprint 1 items yet.
- No completion status, code commits, or test results reported for Sprint 2 items yet.
- US-006 is assigned to qa-agent rather than a development role; input gives no rationale for this assignment.
- No completion status, code commits, or test results reported for Sprint 3 items yet.
- No completion status, code commits, or test results reported for Sprint 4 items yet.
- No completion status, code commits, or test results reported for Sprint 5 items yet.
- No completion status, code commits, or test results reported for Sprint 6 items yet.
- No completion status, code commits, or test results reported for Sprint 7 items yet.

### Testing

- Testing phase has not started.

### Deployment

- No deployment recorded yet.

### Maintenance

- Maintenance phase has no data because the application has not been deployed.
<!-- sdlc:auto:end open-gaps -->
