<!-- sdlc:auto:start adr -->
# ADR-0002: Use FastAPI 0.115 for Backend

Status: Accepted  
Date: 2026-11-06

## Context and Problem Statement

Which Backend technology does the project use? Decided in architecture v1.

## Considered Options

- FastAPI 0.115
- Django REST Framework
- Flask

## Decision Outcome

Chosen option: FastAPI 0.115, because Approved stack. Hosts JWT auth, CRUD and unit conversion, enforcing per-account isolation on every request (NFR-002).

## Consequences

Requires explicit auth and password-hashing libraries rather than a bundled auth system.
<!-- sdlc:auto:end adr -->