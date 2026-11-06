# Development

> Maintained by QuorQ AI SDLC. Text between `sdlc:auto` markers is regenerated; anything outside them is yours and is kept.

<!-- sdlc:auto:start narrative -->
### DEV-PLAN-OVERVIEW · approved · source: plan:v1

The development plan (version 1) is approved and organizes all 20 user stories into 7 sprints covering foundation, sign-in/accounts, child profiles, overview dashboard, measurement recording, units/settings, and growth charts.

Plan status: approved, version 1. Sprint capacities: Sprint 1=16, Sprint 2=11, Sprint 3=12, Sprint 4=5, Sprint 5=14, Sprint 6=5, Sprint 7=10 (total capacity 73 points). Sum of individual story points across US-001..US-020 also totals 73, so capacity allocation and story-point sum are consistent with no discrepancy. Each epic (EPIC-001..EPIC-007) groups one sprint's stories and is itself unassigned to any role, which is expected for organizational epics. Each story is assigned to a specific agent role (frontend-agent, backend-agent, or qa-agent) and has a point estimate, as listed in the per-sprint entries.

**Related:** EPIC-001, EPIC-002, EPIC-003, EPIC-004, EPIC-005, EPIC-006, EPIC-007, US-001, US-002, US-003, US-004, US-005, US-006, US-007, US-008, US-009, US-010, US-011, US-012, US-013, US-014, US-015, US-016, US-017, US-018, US-019, US-020

- ⚠ No actual development execution evidence (commits, code artifacts, ticket status, test results) has been provided for any sprint or story -- only the approved plan/backlog is available.
- ⚠ Role assignment for US-006 (qa-agent) differs from the otherwise backend/frontend split seen elsewhere in the backlog; input does not explain the rationale, so this is noted rather than assumed.

### SPRINT-1 · approved · source: plan:SPRINT-1

Sprint 1 (Foundation, capacity 16) builds the cross-cutting groundwork: a responsive web app shell and a private, per-account data store.

Goal: deliver a responsive web application that works on phone and desktop browsers, plus a private per-account data store keeping each parent's data isolated and available across their devices. Assumption: delivered as a responsive web app only (no native mobile app); data is held per account and never visible to any other account. Items: US-001 Responsive web application shell (8 pts, frontend-agent) with tasks T1 Set up React 19 app shell and routing, T2 Implement responsive layout system, T3 Establish plain-language UI conventions. US-002 Private per-account data store (8 pts, backend-agent) with tasks T1 Design PostgreSQL schema for parents, children and measurements, T2 Implement session/auth middleware, T3 Add account-scoped query guards.

**Related:** EPIC-001, US-001, US-001-T1, US-001-T2, US-001-T3, US-002, US-002-T1, US-002-T2, US-002-T3

- ⚠ No completion status, code commits, or test results reported for Sprint 1 items yet.

### SPRINT-2 · approved · source: plan:SPRINT-2

Sprint 2 (Sign-in & accounts, capacity 11) covers parent account creation, sign-in, sign-out, and cross-device access.

Goal: parents create and sign in to a private, password-protected account, sign out to protect their data, and reach the same account data from any device. Assumption: each parent account is protected by an email and password; the app is free with no payments or subscriptions. Items: US-003 Create a parent account (3 pts, backend-agent), US-004 Sign in to a parent account (3 pts, backend-agent), US-005 Sign out (2 pts, backend-agent), US-006 Access data on any device (3 pts, qa-agent).

**Related:** EPIC-002, US-003, US-004, US-005, US-006

- ⚠ No completion status, code commits, or test results reported for Sprint 2 items yet.
- ⚠ US-006 is assigned to qa-agent rather than a development role; input gives no rationale for this assignment.

### SPRINT-3 · approved · source: plan:SPRINT-3

Sprint 3 (Child profiles, capacity 12) lets parents create and manage multiple child profiles, each with its own measurement history.

Goal: parents create and manage one or more child profiles, each with a name, date of birth and optional sex, and each with its own separate measurement history and charts. Assumption: a single parent account can hold multiple child profiles; deleting a profile also removes that child's measurements. Items: US-007 Add a child profile (3 pts, backend-agent), US-008 Manage multiple child profiles (3 pts, backend-agent), US-009 Edit a child profile (3 pts, backend-agent), US-010 Delete a child profile (3 pts, backend-agent).

**Related:** EPIC-003, US-007, US-008, US-009, US-010

- ⚠ No completion status, code commits, or test results reported for Sprint 3 items yet.

### SPRINT-4 · approved · source: plan:SPRINT-4

Sprint 4 (Children overview, capacity 5) delivers the post-sign-in dashboard listing all child profiles.

Goal: after signing in, a parent sees a dashboard listing all of their child profiles and can open any one to view its details, measurements and charts. Items: US-011 View the children overview dashboard (3 pts, frontend-agent), US-012 Open a child from the overview (2 pts, frontend-agent).

**Related:** EPIC-004, US-011, US-012

- ⚠ No completion status, code commits, or test results reported for Sprint 4 items yet.

### SPRINT-5 · approved · source: plan:SPRINT-5

Sprint 5 (Recording measurements, capacity 14) covers manual entry, review, editing, and deletion of a child's weight and height measurements.

Goal: for a chosen child, a parent manually records dated weight and height measurements, reviews the recorded history, and edits or deletes individual entries. Assumption: all measurements are entered manually with a date; there is no scale or device integration. Items: US-013 Record a weight measurement (3 pts, backend-agent), US-014 Record a height measurement (3 pts, backend-agent), US-015 View a child's measurement history (3 pts, frontend-agent), US-016 Edit a measurement entry (3 pts, backend-agent), US-017 Delete a measurement entry (2 pts, backend-agent).

**Related:** EPIC-005, US-013, US-014, US-015, US-016, US-017

- ⚠ No completion status, code commits, or test results reported for Sprint 5 items yet.

### SPRINT-6 · approved · source: plan:SPRINT-6

Sprint 6 (Units & settings, capacity 5) adds the ability to choose metric or imperial units for entries and charts.

Goal: a parent can choose between metric (kg/cm) and imperial (lb/in) units, and entries and charts are shown in the chosen units. Assumption: both unit systems are supported and user-selectable. Item: US-018 Choose measurement units (5 pts, frontend-agent).

**Related:** EPIC-006, US-018

- ⚠ No completion status, code commits, or test results reported for Sprint 6 items yet.

### SPRINT-7 · approved · source: plan:SPRINT-7

Sprint 7 (Growth charts, capacity 10) displays each child's own weight and height trends over time as simple line charts.

Goal: the app displays each child's own weight and height over time as simple trend line charts, built only from that child's recorded entries and shown in the parent's chosen units. Assumption: charts show the child's own data only, with no comparison against WHO/CDC percentile curves. Items: US-019 Weight trend chart (5 pts, frontend-agent), US-020 Height trend chart (5 pts, frontend-agent).

**Related:** EPIC-007, US-019, US-020

- ⚠ No completion status, code commits, or test results reported for Sprint 7 items yet.
<!-- sdlc:auto:end narrative -->
