# wedgw — SDLC Documentation

> Maintained by QuorQ AI SDLC. Text between `sdlc:auto` markers is regenerated; anything outside them is yours and is kept.

<!-- sdlc:auto:start overview -->
weight and height tracker for kids

**Documentation version:** v2
<!-- sdlc:auto:end overview -->

## Contents

<!-- sdlc:auto:start contents -->
| Document | State |
|---|---|
| [Requirements](requirements/README.md) | v1 approved |
| [Architecture](architecture/README.md) | 13 entries |
| [Development](development/README.md) | 1 entry |
| [Testing](testing/README.md) | 1 entry |
| [Deployment](deployment/README.md) | 1 entry |
| [Maintenance](maintenance/README.md) | 1 entry |
| [Data model](architecture/data-model.md) | generated |
| [API (OpenAPI)](architecture/api/openapi.yaml) | generated |
| [Decisions (ADRs)](architecture/adr/README.md) | 4 decisions |
| [Sprint plan](development/sprint-plan.md) | not generated yet |
| [Developer guide](development/developer-guide.md) | not generated yet |
| [API reference](development/api-reference.md) | 0 routes |
| [Test report](testing/test-report.md) | not run yet |
| [Tests](testing/test-cases.md) | 0 tests |
| [Deployment guide](deployment/deployment-guide.md) | not deployed yet |
| [Runbook](deployment/runbook.md) | not deployed yet |
| [Release notes](deployment/release-notes.md) | 0 releases |
| [Traceability matrix](traceability-matrix.md) | 0 requirements |
| [Changelog](CHANGELOG.md) | 2 versions |
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

- Development phase has not started; no implementation of any requirement is documented.

### Testing

- Testing phase has not started.

### Deployment

- No deployment recorded yet.

### Maintenance

- Maintenance phase has no data because the application has not been deployed.
<!-- sdlc:auto:end open-gaps -->
