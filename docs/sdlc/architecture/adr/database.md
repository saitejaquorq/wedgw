<!-- sdlc:auto:start adr -->
# ADR-0003: Use PostgreSQL 16 for Database

Status: Accepted  
Date: 2026-11-06

## Context and Problem Statement

Which Database technology does the project use? Decided in architecture v1.

## Considered Options

- PostgreSQL 16
- MySQL
- SQLite

## Decision Outcome

Chosen option: PostgreSQL 16, because Approved stack. Relational model fits parents -> children -> measurements cleanly with cascade deletes and strong consistency across devices (NFR-003).

## Consequences

No special scaling needs at this scope; a single managed instance suffices.
<!-- sdlc:auto:end adr -->