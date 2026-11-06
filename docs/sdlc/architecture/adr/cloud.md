<!-- sdlc:auto:start adr -->
# ADR-0004: Use AWS for Cloud

Status: Accepted  
Date: 2026-11-06

## Context and Problem Statement

Which Cloud technology does the project use? Decided in architecture v1.

## Considered Options

- AWS
- GCP
- Azure

## Decision Outcome

Chosen option: AWS, because Approved stack. S3/CloudFront for the SPA, Fargate for the API and RDS PostgreSQL with encryption at rest and TLS in transit (NFR-001).

## Consequences

Managed services simplify ops at the cost of AWS coupling.
<!-- sdlc:auto:end adr -->