# Deployment Guide

> Maintained by QuorQ AI SDLC. Text between `sdlc:auto` markers is regenerated; anything outside them is yours and is kept.

<!-- sdlc:auto:start how-it-deploys -->
Pushes to `main` run `.github/workflows/deploy.yml`, which builds the API image (if there is a backend) and deploys the SPA to AWS Amplify. Commits touching only `docs/sdlc/**` don't deploy. Deployments can also be started from the platform's Deployment tab.
<!-- sdlc:auto:end how-it-deploys -->

<!-- sdlc:auto:start environments -->
| Name | Service | Runtime | Scaling | Environment |
|---|---|---|---|---|
| Frontend hosting | AWS S3 + CloudFront | React 19 static build | CDN edge, auto | dev |
| Backend service | AWS ECS Fargate | FastAPI 0.115 on Python 3.12 (Uvicorn) | 1 task for dev, horizontally scalable | dev |
| Database | AWS RDS for PostgreSQL 16 | PostgreSQL 16 | single instance for dev | dev |
<!-- sdlc:auto:end environments -->

<!-- sdlc:auto:start live -->
_Not deployed yet._
<!-- sdlc:auto:end live -->

<!-- sdlc:auto:start topology -->
```mermaid
graph LR
  n_Frontend_hosting["Frontend hosting<br/>AWS S3 + CloudFront"]
  n_Backend_service["Backend service<br/>AWS ECS Fargate"]
  n_Database["Database<br/>AWS RDS for PostgreSQL 16"]
  n_Frontend_hosting -->|"HTTPS"| n_Backend_service
  n_Backend_service -->|"TLS/5432"| n_Database
```
<!-- sdlc:auto:end topology -->
