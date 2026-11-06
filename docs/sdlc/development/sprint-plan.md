# Sprint Plan

> Maintained by QuorQ AI SDLC. Text between `sdlc:auto` markers is regenerated; anything outside them is yours and is kept.

<!-- sdlc:auto:start sprints -->
## Sprint 1: Foundation

Cross-cutting groundwork every other area depends on: a responsive web application that works on phone and desktop browsers, and a private per-account data store that keeps each parent's data isolated and available across their devices. Assumption: delivered as a responsive web application only, with no native mobile app; data is held per account and is never visible to any other account.

Committed: 16 points

| Key | Type | Title | Points | Role | Depends on |
|---|---|---|---|---|---|
| US-001 | Story | Responsive web application shell | 8 | frontend-agent | — |
| ↳ US-001-T1 | Task | Set up React 19 app shell and routing | — | frontend-agent | — |
| ↳ US-001-T2 | Task | Implement responsive layout system | — | frontend-agent | — |
| ↳ US-001-T3 | Task | Establish plain-language UI conventions | — | frontend-agent | — |
| US-002 | Story | Private per-account data store | 8 | backend-agent | — |
| ↳ US-002-T1 | Task | Design PostgreSQL schema for parents, children and measurements | — | backend-agent | — |
| ↳ US-002-T2 | Task | Implement session/auth middleware | — | backend-agent | — |
| ↳ US-002-T3 | Task | Add account-scoped query guards | — | backend-agent | — |

## Sprint 2: Sign-in & accounts

Parents create and sign in to a private, password-protected account, sign out to protect their data, and reach the same account data from any device. Assumption: each parent account is protected by an email and password; the app is free with no payments or subscriptions.

Committed: 11 points

| Key | Type | Title | Points | Role | Depends on |
|---|---|---|---|---|---|
| US-003 | Story | Create a parent account | 3 | backend-agent | US-002 |
| US-004 | Story | Sign in to a parent account | 3 | backend-agent | US-003 |
| US-005 | Story | Sign out | 2 | backend-agent | US-004 |
| US-006 | Story | Access data on any device | 3 | qa-agent | US-002, US-004 |

## Sprint 3: Child profiles

Parents create and manage one or more child profiles, each with a name, date of birth and optional sex, and each with its own separate measurement history and charts. Assumption: a single parent account can hold multiple child profiles; deleting a profile also removes that child's measurements.

Committed: 12 points

| Key | Type | Title | Points | Role | Depends on |
|---|---|---|---|---|---|
| US-007 | Story | Add a child profile | 3 | backend-agent | US-002 |
| US-008 | Story | Manage multiple child profiles | 3 | backend-agent | US-007 |
| US-009 | Story | Edit a child profile | 3 | backend-agent | US-007 |
| US-010 | Story | Delete a child profile | 3 | backend-agent | US-007 |

## Sprint 4: Children overview

After signing in, a parent sees a dashboard listing all of their child profiles and can open any one to view its details, measurements and charts.

Committed: 5 points

| Key | Type | Title | Points | Role | Depends on |
|---|---|---|---|---|---|
| US-011 | Story | View the children overview dashboard | 3 | frontend-agent | US-007 |
| US-012 | Story | Open a child from the overview | 2 | frontend-agent | US-011 |

## Sprint 5: Recording measurements

For a chosen child, a parent manually records dated weight and height measurements, reviews the recorded history, and edits or deletes individual entries. Assumption: all measurements are entered manually with a date; there is no scale or device integration.

Committed: 14 points

| Key | Type | Title | Points | Role | Depends on |
|---|---|---|---|---|---|
| US-013 | Story | Record a weight measurement | 3 | backend-agent | US-007 |
| US-014 | Story | Record a height measurement | 3 | backend-agent | US-007 |
| US-015 | Story | View a child's measurement history | 3 | frontend-agent | US-013, US-014 |
| US-016 | Story | Edit a measurement entry | 3 | backend-agent | US-013, US-014 |
| US-017 | Story | Delete a measurement entry | 2 | backend-agent | US-013, US-014 |

## Sprint 6: Units & settings

A parent can choose between metric (kg/cm) and imperial (lb/in) units, and entries and charts are shown in the chosen units. Assumption: both unit systems are supported and user-selectable.

Committed: 5 points

| Key | Type | Title | Points | Role | Depends on |
|---|---|---|---|---|---|
| US-018 | Story | Choose measurement units | 5 | frontend-agent | US-004 |

## Sprint 7: Growth charts

The app displays each child's own weight and height over time as simple trend line charts, built only from that child's recorded entries and shown in the parent's chosen units. Assumption: charts show the child's own data only, with no comparison against WHO/CDC percentile curves.

Committed: 10 points

| Key | Type | Title | Points | Role | Depends on |
|---|---|---|---|---|---|
| US-019 | Story | Weight trend chart | 5 | frontend-agent | US-013, US-018 |
| US-020 | Story | Height trend chart | 5 | frontend-agent | US-014, US-018 |

## Unscheduled

_Nothing unscheduled._
<!-- sdlc:auto:end sprints -->
