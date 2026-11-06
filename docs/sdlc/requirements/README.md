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
## EPIC-001: Foundation

Cross-cutting groundwork every other area depends on: a responsive web application that works on phone and desktop browsers, and a private per-account data store that keeps each parent's data isolated and available across their devices. Assumption: delivered as a responsive web application only, with no native mobile app; data is held per account and is never visible to any other account.

### US-001: Responsive web application shell

**Priority:** high

> As a parent, I want the app to work comfortably in my phone or desktop browser, so that I can track my children's growth from whichever device I have to hand.

| ID | Given | When | Then |
|---|---|---|---|
| AC-001 | I open the app on a mobile phone browser | the page loads | the layout adapts to the small screen and all controls are usable without horizontal scrolling |
| AC-002 | I open the app on a desktop browser | the page loads | the layout adapts to the larger screen and remains clear and readable |
| AC-003 | I am a non-technical parent | I use the core screens (entering a measurement, reading a chart, switching units) | the actions are presented plainly with no technical jargon |

### US-002: Private per-account data store

**Priority:** high

> As a parent, I want my children, measurements and charts stored against my account rather than my device, so that my data stays private to me and is the same wherever I sign in.

| ID | Given | When | Then |
|---|---|---|---|
| AC-004 | two different parent accounts exist with their own children | one parent is signed in | only that parent's children and measurements are accessible and no data from the other account is visible |
| AC-005 | I save a child or measurement while signed in on one device | I later sign in on another device | the same saved data is present and up to date |

## EPIC-002: Sign-in & accounts

Parents create and sign in to a private, password-protected account, sign out to protect their data, and reach the same account data from any device. Assumption: each parent account is protected by an email and password; the app is free with no payments or subscriptions.

### US-003: Create a parent account

**Priority:** high

> As a new parent, I want to create my own account with an email and password, so that I can start privately tracking my children's growth.

| ID | Given | When | Then |
|---|---|---|---|
| AC-006 | I am on the account creation screen and have no account | I enter a valid email and a password and submit | a new private account is created for me and I am signed in |
| AC-007 | I try to create an account with an email that is already registered | I submit | account creation is rejected and I am told the email is already in use |
| AC-008 | I have just created my account | I view my data | the account starts empty and holds only data I add, private to me |

### US-004: Sign in to a parent account

**Priority:** critical

> As a parent with an account, I want to sign in with my email and password, so that only I can see and change my children's data.

| ID | Given | When | Then |
|---|---|---|---|
| AC-009 | I have a registered account | I enter my correct email and password | I am signed in and taken to my children overview |
| AC-010 | I am on the sign-in screen | I enter an incorrect email or password | I am not signed in and I see a message that the credentials are invalid |
| AC-011 | I am not signed in | I try to open any children, measurements or charts | I am required to sign in first and no account data is shown |

### US-005: Sign out

**Priority:** high

> As a signed-in parent, I want to sign out of my account, so that my data is protected when I finish using the app.

| ID | Given | When | Then |
|---|---|---|---|
| AC-012 | I am signed in | I choose to sign out | my session ends and I am returned to the sign-in screen |
| AC-013 | I have signed out | I try to open my children or measurements without signing back in | the data is not shown and I am prompted to sign in |

### US-006: Access data on any device

**Priority:** high

> As a parent, I want to sign in from a phone or desktop and see the same data, so that my children, measurements and charts follow my account rather than the device.

| ID | Given | When | Then |
|---|---|---|---|
| AC-014 | I have added children and measurements while signed in on one device | I sign in to the same account on a different device | I see the same children, measurements and charts |
| AC-015 | I update data on one device | I next sign in on another device | the change is reflected there |

## EPIC-003: Child profiles

Parents create and manage one or more child profiles, each with a name, date of birth and optional sex, and each with its own separate measurement history and charts. Assumption: a single parent account can hold multiple child profiles; deleting a profile also removes that child's measurements.

### US-007: Add a child profile

**Priority:** high

> As a parent, I want to create a child profile with name, date of birth and optional sex, so that the child has its own measurement history and charts.

| ID | Given | When | Then |
|---|---|---|---|
| AC-016 | I am signed in | I enter a name and date of birth (and optionally a sex) and save | a new child profile is created under my account with its own empty history |
| AC-017 | I am adding a child profile | I leave the name or date of birth blank and try to save | the profile is not saved and I am told which required detail is missing |
| AC-018 | I choose not to record a sex | I save the profile | the profile is created with sex left unset |

### US-008: Manage multiple child profiles

**Priority:** high

> As a parent, I want to keep several child profiles under one account, so that each of my children has separate records and charts.

| ID | Given | When | Then |
|---|---|---|---|
| AC-019 | I already have one child profile | I add another child profile | both profiles exist under my account, each with its own separate measurement history |
| AC-020 | I have more than one child profile | I add a measurement to one child | it appears only in that child's history and not in any other child's history |

### US-009: Edit a child profile

**Priority:** medium

> As a parent, I want to update a child's name, date of birth or sex, so that I can correct mistakes or reflect changed details.

| ID | Given | When | Then |
|---|---|---|---|
| AC-021 | I am viewing one of my child profiles | I change the name, date of birth or sex and save | the updated details are stored and shown for that child |
| AC-022 | I edit a profile | I clear a required detail (name or date of birth) and try to save | the change is rejected and I am told the detail is required |

### US-010: Delete a child profile

**Priority:** medium

> As a parent, I want to remove a child profile I no longer need, so that my account only holds the children I want to track.

| ID | Given | When | Then |
|---|---|---|---|
| AC-023 | I am viewing one of my child profiles | I choose to delete it and confirm | the child profile and all of that child's measurements are removed from my account |
| AC-024 | I choose to delete a child profile | I am asked to confirm and I cancel | the profile and its measurements remain unchanged |

## EPIC-004: Children overview

After signing in, a parent sees a dashboard listing all of their child profiles and can open any one to view its details, measurements and charts.

### US-011: View the children overview dashboard

**Priority:** high

> As a signed-in parent, I want to see a dashboard listing all of my child profiles, so that I have a single place to see every child I am tracking.

| ID | Given | When | Then |
|---|---|---|---|
| AC-025 | I am signed in and have one or more child profiles | I reach the overview after signing in | all of my child profiles are listed |
| AC-026 | I am signed in and have no child profiles yet | I view the overview | I see an empty state that lets me add my first child |

### US-012: Open a child from the overview

**Priority:** high

> As a parent, I want to select a child shown on the overview, so that I can view that child's profile and growth history.

| ID | Given | When | Then |
|---|---|---|---|
| AC-027 | I am viewing the overview with my children listed | I select a child | I am taken to that child's profile showing its details, measurements and charts |

## EPIC-005: Recording measurements

For a chosen child, a parent manually records dated weight and height measurements, reviews the recorded history, and edits or deletes individual entries. Assumption: all measurements are entered manually with a date; there is no scale or device integration.

### US-013: Record a weight measurement

**Priority:** high

> As a parent, I want to add a weight measurement with its date for a chosen child, so that the child's weight history builds up over time.

| ID | Given | When | Then |
|---|---|---|---|
| AC-028 | I am viewing a child's profile | I enter a weight value and the date it was taken and save | the entry is saved to that child's history with its value and date |
| AC-029 | I am adding a weight measurement | I leave the value or date blank, or enter a non-numeric weight, and try to save | the entry is not saved and I am told what to correct |

### US-014: Record a height measurement

**Priority:** high

> As a parent, I want to add a height measurement with its date for a chosen child, so that the child's height history builds up over time.

| ID | Given | When | Then |
|---|---|---|---|
| AC-030 | I am viewing a child's profile | I enter a height value and the date it was taken and save | the entry is saved to that child's history with its value and date |
| AC-031 | I am adding a height measurement | I leave the value or date blank, or enter a non-numeric height, and try to save | the entry is not saved and I am told what to correct |

### US-015: View a child's measurement history

**Priority:** medium

> As a parent, I want to see a list of a child's recorded weight and height entries with their dates, so that I can review what has been logged.

| ID | Given | When | Then |
|---|---|---|---|
| AC-032 | a child has recorded weight and height entries | I view that child's measurement history | each entry is listed with its type, value and date |
| AC-033 | a child has no measurements yet | I view the history | I see an empty state indicating no measurements have been recorded |

### US-016: Edit a measurement entry

**Priority:** medium

> As a parent, I want to change the value or date of a weight or height entry, so that I can correct a mistake.

| ID | Given | When | Then |
|---|---|---|---|
| AC-034 | a child has a recorded measurement | I change its value or date and save | the entry is updated and the history and charts reflect the change |
| AC-035 | I am editing a measurement | I clear the value or date, or enter a non-numeric value, and try to save | the change is rejected and I am told what to correct |

### US-017: Delete a measurement entry

**Priority:** medium

> As a parent, I want to remove a weight or height entry, so that entries added by mistake or no longer wanted are gone.

| ID | Given | When | Then |
|---|---|---|---|
| AC-036 | a child has a recorded measurement | I choose to delete it and confirm | the entry is removed from the history and no longer appears on the charts |
| AC-037 | I choose to delete a measurement | I cancel the confirmation | the entry remains unchanged |

## EPIC-006: Units & settings

A parent can choose between metric (kg/cm) and imperial (lb/in) units, and entries and charts are shown in the chosen units. Assumption: both unit systems are supported and user-selectable.

### US-018: Choose measurement units

**Priority:** medium

> As a parent, I want to choose between metric and imperial units, so that measurements and charts are shown in the units I understand.

| ID | Given | When | Then |
|---|---|---|---|
| AC-038 | I am signed in | I select metric units | weights are shown and entered in kg and heights in cm across entries and charts |
| AC-039 | I am signed in | I select imperial units | weights are shown and entered in lb and heights in in across entries and charts |
| AC-040 | I have chosen a unit preference | I return to the app later on the same account | my chosen units are still applied |

## EPIC-007: Growth charts

The app displays each child's own weight and height over time as simple trend line charts, built only from that child's recorded entries and shown in the parent's chosen units. Assumption: charts show the child's own data only, with no comparison against WHO/CDC percentile curves.

### US-019: Weight trend chart

**Priority:** high

> As a parent, I want to see my child's weight over time as a simple trend line chart, so that I can see how my child is growing.

| ID | Given | When | Then |
|---|---|---|---|
| AC-041 | a child has recorded weight entries | I view the weight chart | a trend line is shown plotting that child's weight values against their dates in my chosen units |
| AC-042 | a child has no weight entries | I view the weight chart | I see an empty state indicating there is nothing to chart yet |
| AC-043 | I am viewing the weight chart | I look at the plotted data | it contains only that child's own entries and no percentile or standard growth curve |

### US-020: Height trend chart

**Priority:** high

> As a parent, I want to see my child's height over time as a simple trend line chart, so that I can see how my child is growing.

| ID | Given | When | Then |
|---|---|---|---|
| AC-044 | a child has recorded height entries | I view the height chart | a trend line is shown plotting that child's height values against their dates in my chosen units |
| AC-045 | a child has no height entries | I view the height chart | I see an empty state indicating there is nothing to chart yet |
| AC-046 | I am viewing the height chart | I look at the plotted data | it contains only that child's own entries and no percentile or standard growth curve |
<!-- sdlc:auto:end epics -->
