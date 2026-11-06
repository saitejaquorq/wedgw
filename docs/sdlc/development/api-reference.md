# API Reference

> Maintained by QuorQ AI SDLC. Text between `sdlc:auto` markers is regenerated; anything outside them is yours and is kept.

<!-- sdlc:auto:start endpoints -->
| Method | Path | Handler | Source | Summary |
|---|---|---|---|---|
| GET | /health | health | `backend/app/main.py:42` | Liveness probe, and the only route here that is not a stub. |
<!-- sdlc:auto:end endpoints -->

<!-- sdlc:auto:start drift -->
**Designed but missing:**

- DELETE /children/{child_id}
- DELETE /children/{child_id}/measurements/{id}
- GET /children
- GET /children/{child_id}
- GET /children/{child_id}/measurements
- GET /me
- PATCH /children/{child_id}
- PATCH /children/{child_id}/measurements/{id}
- PATCH /me/preferences
- POST /auth/login
- POST /auth/logout
- POST /auth/register
- POST /children
- POST /children/{child_id}/measurements
<!-- sdlc:auto:end drift -->

<!-- sdlc:auto:start source -->
Generated from commit `0a3e2c5`
<!-- sdlc:auto:end source -->
