# Traceability Matrix

> Maintained by QuorQ AI SDLC. Text between `sdlc:auto` markers is regenerated; anything outside them is yours and is kept.

<!-- sdlc:auto:start legend -->
Built from recorded links, not written by a model: requirement key → plan item (`source_stable_key`) → development ticket (`stable_key`) → the ticket's test steps → the last live deployment that started after the work finished. **AC tests** counts the story's acceptance criteria that have a test case, and those whose test cases all passed in the latest finished E2E run.
<!-- sdlc:auto:end legend -->

<!-- sdlc:auto:start matrix -->
| Requirement | Epic | Title | Plan items | Sprint | Design | Code | Commits | Ticket | Tests | AC tests | Deployed |
|---|---|---|---|---|---|---|---|---|---|---|---|
| US-001 | EPIC-001 | Responsive web application shell | US-001, US-001-T1, US-001-T2, US-001-T3 | 1 | web_app | — | — | not started | not run | 0/3 tested · 0/3 passing | — |
| US-002 | EPIC-001 | Private per-account data store | US-002, US-002-T1, US-002-T2, US-002-T3 | 1 | api, children, db, measurements, parents | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-003 | EPIC-002 | Create a parent account | US-003 | 2 | POST /auth/register, api, parents | — | — | not started | not run | 0/3 tested · 0/3 passing | — |
| US-004 | EPIC-002 | Sign in to a parent account | US-004 | 2 | POST /auth/login, api, parents | — | — | not started | not run | 0/3 tested · 0/3 passing | — |
| US-005 | EPIC-002 | Sign out | US-005 | 2 | POST /auth/logout, api | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-006 | EPIC-002 | Access data on any device | US-006 | 2 | GET /me, api, parents | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-007 | EPIC-003 | Add a child profile | US-007 | 3 | POST /children, api, children | — | — | not started | not run | 0/3 tested · 0/3 passing | — |
| US-008 | EPIC-003 | Manage multiple child profiles | US-008 | 3 | GET /children, api, children, measurements | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-009 | EPIC-003 | Edit a child profile | US-009 | 3 | PATCH /children/{child_id}, api, children | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-010 | EPIC-003 | Delete a child profile | US-010 | 3 | DELETE /children/{child_id}, api, children, measurements | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-011 | EPIC-004 | View the children overview dashboard | US-011 | 4 | GET /children, children, web_app | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-012 | EPIC-004 | Open a child from the overview | US-012 | 4 | GET /children/{child_id}, children, web_app | — | — | not started | not run | 0/1 tested · 0/1 passing | — |
| US-013 | EPIC-005 | Record a weight measurement | US-013 | 5 | POST /children/{child_id}/measurements, api, measurements | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-014 | EPIC-005 | Record a height measurement | US-014 | 5 | POST /children/{child_id}/measurements, api, measurements | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-015 | EPIC-005 | View a child's measurement history | US-015 | 5 | GET /children/{child_id}/measurements, measurements, web_app | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-016 | EPIC-005 | Edit a measurement entry | US-016 | 5 | PATCH /children/{child_id}/measurements/{id}, api, measurements | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-017 | EPIC-005 | Delete a measurement entry | US-017 | 5 | DELETE /children/{child_id}/measurements/{id}, api, measurements | — | — | not started | not run | 0/2 tested · 0/2 passing | — |
| US-018 | EPIC-006 | Choose measurement units | US-018 | 6 | GET /me, PATCH /me/preferences, api, parents, web_app | — | — | not started | not run | 0/3 tested · 0/3 passing | — |
| US-019 | EPIC-007 | Weight trend chart | US-019 | 7 | GET /children/{child_id}/measurements, measurements, web_app | — | — | not started | not run | 0/3 tested · 0/3 passing | — |
| US-020 | EPIC-007 | Height trend chart | US-020 | 7 | GET /children/{child_id}/measurements, measurements, web_app | — | — | not started | not run | 0/3 tested · 0/3 passing | — |
<!-- sdlc:auto:end matrix -->
