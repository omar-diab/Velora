# VELORA Architecture

This document captures the project's architectural vision, current assumptions, and the decision log. It intentionally starts small — architecture is documented as real decisions are made, not invented up front. Do not treat the "Future System Areas" section as a design; it is a map of topics the project may eventually need to make decisions about.

## Project Vision

VELORA is a fictional fashion-commerce platform built incrementally as a full-stack learning and portfolio project. The architecture should stay as simple as possible for as long as possible, and grow only when a real requirement (see [REQUIREMENTS.md](REQUIREMENTS.md)) demands it.

## Current Architectural Assumptions

These are the only decisions fixed at this point (Phase 0):

1. **Frontend framework: Angular, with TypeScript.** Chosen because the developer wants to learn Angular specifically. This will not change without an explicit developer decision (see ADR-001).
2. **Styling: Tailwind CSS** is the intended utility-first styling approach, to be introduced once Angular fundamentals are in place (not before).
3. **No backend technology has been chosen yet.** This will be decided in Phase 7 (Backend Fundamentals), after the developer has enough grounding to make an informed choice, and will be recorded as an ADR.
4. **No database technology has been chosen yet.** Decided in Phase 8, recorded as an ADR.
5. **No hosting/cloud provider work has started.** AWS is the intended target per the project brief, decided in detail in Phase 24.

Everything else — state management approach, API style (REST vs. GraphQL), search infrastructure, real-time transport — is deliberately undecided until the relevant phase is reached and the developer has the prerequisite knowledge to participate in the decision.

## Future System Areas (Not Designed Yet)

This is a list of areas VELORA may eventually need architecture for. Listing them here is not a commitment to build them a particular way — it's a reminder of scope so nothing is designed in a vacuum later.

- Frontend application structure (modules/standalone components, routing, lazy loading)
- State management strategy (component state vs. services vs. Signals/RxJS vs. a state library)
- Backend API design (REST and/or GraphQL)
- Authentication & authorization architecture
- Database schema and data modeling
- Search infrastructure (Elasticsearch)
- Real-time communication (WebSockets)
- Maps integration (Google Maps)
- Admin dashboard architecture
- Testing strategy across unit/integration/E2E
- CI/CD pipeline design
- AWS deployment topology
- Observability (logging, monitoring, error tracking)

## No Premature Complexity

The following are explicitly **out of scope** until a concrete, demonstrated problem justifies them:

- Microservices
- Kubernetes
- Complex state management libraries (e.g., NgRx) before component state and services have been learned and found insufficient
- Event-driven architecture
- Multiple databases
- Complex cloud infrastructure beyond what a small learning project needs
- Design patterns applied for their own sake rather than to solve a real problem in this codebase

## Architecture Decision Log

Decisions are recorded below using the ADR format. Each ADR is permanent once written — if a decision is later reversed, add a new ADR that supersedes it rather than editing history.

### ADR-001

**Decision:** Use Angular (with TypeScript) as the frontend framework for VELORA.

**Context:** The developer's learning goal is to become a strong full-stack developer, with an explicit interest in learning Angular and TypeScript. A framework decision is needed before any frontend work can begin in later phases.

**Options Considered:**
- Angular
- React
- Vue

**Decision Made:** Angular.

**Why:** This is the developer's stated learning objective, not a technical trade-off between frameworks. Per the project's technology rule, Angular is used as the primary frontend framework unless the developer explicitly changes this decision.

**Consequences:** All frontend-phase guidance (Phases 4–6 and beyond) will be Angular-specific (components, modules/standalone APIs, RxJS/Signals, Angular CLI tooling, etc.). Changing frameworks later would require a new ADR and would affect a significant portion of already-written guidance and code.

---

_(Further ADRs are appended here as real decisions are made — e.g., backend framework in Phase 7, database in Phase 8, state management approach when it becomes necessary.)_
