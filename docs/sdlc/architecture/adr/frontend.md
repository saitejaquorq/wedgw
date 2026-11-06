<!-- sdlc:auto:start adr -->
# ADR-0001: Use React 19 for Frontend

Status: Accepted  
Date: 2026-11-06

## Context and Problem Statement

Which Frontend technology does the project use? Decided in architecture v1.

## Considered Options

- React 19
- Vue
- Svelte

## Decision Outcome

Chosen option: React 19, because Approved stack. Built as a responsive SPA so parents get the same UI on phone and desktop browsers (NFR-004) with a simple, non-technical layout (NFR-005).

## Consequences

SPA needs a charting library and client routing, added below; no SSR, which is fine for a private authenticated app.
<!-- sdlc:auto:end adr -->