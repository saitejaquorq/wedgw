# Product Requirements

> Maintained by QuorQ AI SDLC. Text between `sdlc:auto` markers is regenerated; anything outside them is yours and is kept.

<!-- sdlc:auto:start narrative -->
## Summary

### REQ-000 · approved · source: requirements:tech-stack

Product owner approved an exact technology stack for the project.

Backend: FastAPI 0.115. Cloud: AWS. Database: PostgreSQL 16. Frontend: React 19. Instruction given: design and build against exactly these versions/technologies, no substitutions.

- ⚠ No architecture input yet confirms this stack is actually being used for design -- architecture phase has not started.

### REQ-SCOPE-EXCLUSIONS · approved · source: requirements:scope

Two capabilities are explicitly out of scope for this delivery.

Out of scope, not to be designed or built: (1) Growth percentile charts comparing children against WHO/CDC standard curves. (2) Milestone/growth alerts and shareable exportable doctor reports. Delivery scope is marked 'lightweight', requirements version 1.

**Related:** REQ-016, REQ-017

### REQ-001 · approved · source: requirements:Sign in to parent account

A parent signs in to a private, password-protected account using email and password.

Only the signed-in parent can see the data in their own account. Sign-in is required before viewing or changing any data.

**Related:** NFR-001, NFR-002

### REQ-002 · approved · source: requirements:Create a parent account

A new parent can create their own account with email and password.

Account creation lets a parent start tracking children. The account keeps all of that parent's data private from other accounts.

**Related:** NFR-002

### REQ-003 · approved · source: requirements:Sign out

A parent can sign out to protect their data when finished using the app.

Sign-out ends the authenticated session.

**Related:** NFR-001

### REQ-004 · approved · source: requirements:Access data on any device

A parent sees the same children, measurements and charts regardless of device.

Data is tied to the account, not the device, so signing in from a phone or desktop shows the same up-to-date data.

**Related:** NFR-003, NFR-004

### REQ-005 · approved · source: requirements:View children overview

After sign-in, a dashboard lists all of the parent's child profiles.

From the overview, the parent can open any child to view details, measurements and charts.

**Related:** REQ-006

### REQ-006 · approved · source: requirements:Open a child from the overview

Selecting a child on the overview navigates to that child's profile and growth history.

Opens the chosen child's dedicated profile/history view.

**Related:** REQ-005

### REQ-007 · approved · source: requirements:Add a child profile

A parent creates a child profile with name, date of birth, and optional sex.

The profile gives the child its own measurement history and charts.

**Related:** REQ-008, REQ-009, REQ-010

### REQ-008 · approved · source: requirements:Manage multiple children

A parent can keep several child profiles under one account.

Each child profile has its own separate records and charts.

**Related:** REQ-007

### REQ-009 · approved · source: requirements:Edit a child profile

A parent can update a child's name, date of birth, or sex.

Used to correct details entered incorrectly or that have changed.

**Related:** REQ-007

### REQ-010 · approved · source: requirements:Delete a child profile

A parent can remove a child profile they no longer need.

Deleting a child profile also removes that child's measurements.

**Related:** REQ-007

### REQ-011 · approved · source: requirements:Record a weight measurement

A parent manually adds a weight measurement with a date for a chosen child.

Each entry is saved to that child's history.

**Related:** REQ-013, REQ-016

### REQ-012 · approved · source: requirements:Record a height measurement

A parent manually adds a height measurement with a date for a chosen child.

Each entry is saved to that child's history.

**Related:** REQ-013, REQ-017

### REQ-013 · approved · source: requirements:View a child's measurement history

A parent can see a list of a child's recorded weight and height entries with their dates.

Lets the parent review what has been logged.

**Related:** REQ-011, REQ-012

### REQ-014 · approved · source: requirements:Edit a measurement entry

A parent can change the value or date of any weight or height entry.

Used to correct a mistake in a previously logged entry.

**Related:** REQ-013

### REQ-015 · approved · source: requirements:Delete a measurement entry

A parent can remove a weight or height entry added by mistake or no longer wanted.

Removes a single measurement record from the child's history.

**Related:** REQ-013

### REQ-016 · approved · source: requirements:Weight trend chart

A simple trend-line chart shows a child's weight over time from their own entries.

Built only from the child's own recorded data; no percentile/standard-curve comparison (explicitly out of scope).

**Related:** REQ-011, REQ-018

### REQ-017 · approved · source: requirements:Height trend chart

A simple trend-line chart shows a child's height over time from their own entries.

Built only from the child's own recorded data; no percentile/standard-curve comparison (explicitly out of scope).

**Related:** REQ-012, REQ-018

### REQ-018 · approved · source: requirements:Choose measurement units

A parent can choose metric (kg/cm) or imperial (lb/in) units.

Entries and charts are displayed in the chosen unit system.

**Related:** REQ-016, REQ-017, NFR-005

### NFR-001 · approved · source: requirements:NFR-001

Security: accounts must be password-protected.

Applies to whole system. A parent must sign in with email and password before viewing or changing any data; signing out protects data afterward.

**Related:** REQ-001, REQ-003

### NFR-002 · approved · source: requirements:NFR-002

Privacy: each parent's data stays private to their own account.

Applies to whole system. Children's records, measurements, and charts are visible only to the owning parent; no cross-account visibility.

**Related:** REQ-001, REQ-002

### NFR-003 · approved · source: requirements:NFR-003

Availability: same data available on any device.

Applies to whole system. Data is tied to the account rather than the device.

**Related:** REQ-004

### NFR-004 · approved · source: requirements:NFR-004

Compatibility: responsive web app works on phone and desktop browsers.

Applies to whole system. No separate native mobile app is provided.

**Related:** REQ-004

### NFR-005 · approved · source: requirements:NFR-005

Usability: must be simple for non-technical parents.

Applies to whole system. Entering measurements, reading trend charts, and switching between metric/imperial units must be clear for users with no technical background.

**Related:** REQ-011, REQ-012, REQ-016, REQ-017, REQ-018
<!-- sdlc:auto:end narrative -->

<!-- sdlc:auto:start summary -->
**Requirements version:** v1  
**Delivery scope:** lightweight  
**Approved:** 2026-11-06

**Capabilities in scope:** Parent account sign-in, Child profile creation (name, date of birth, optional sex), Manual weight and height entry by date, Edit and delete measurement entries, Weight-over-time trend line chart, Height-over-time trend line chart, Metric and imperial unit selection, Multiple child profiles per account, Cross-device access to a parent's own data, Children overview dashboard

**Approved technology stack:**

| Layer | Choice | Rationale |
|---|---|---|
| backend | FastAPI | — |
| cloud | AWS | — |
| database | PostgreSQL | — |
| frontend | React | — |
<!-- sdlc:auto:end summary -->

<!-- sdlc:auto:start epics -->
_No epics recorded._
<!-- sdlc:auto:end epics -->
