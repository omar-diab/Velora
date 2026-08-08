# VELORA

A fictional fashion-commerce platform built from scratch as a full-stack engineering learning and portfolio project.

## Project Purpose

VELORA exists to take a developer from JavaScript/TypeScript fundamentals to a strong Mid-level (or better) full-stack engineer, by building a realistic, production-shaped fashion e-commerce platform — one deliberate, understood step at a time.

The human developer writes all production code. An AI mentor provides specifications, requirements, architecture guidance, hints, and code review, but does not implement the application. See [DEVELOPMENT.md](DEVELOPMENT.md) for the full rules.

## Current Status

**PLANNED** — the project is in Phase 0 (Project Setup and Engineering Workflow). No application code has been written yet. See [PROCESS.md](PROCESS.md) for the current phase, step, and status.

## Planned Capabilities

Everything below is **PLANNED**, not implemented, unless a phase's status in [PROCESS.md](PROCESS.md) says otherwise.

### Frontend
Angular, TypeScript, Tailwind CSS, responsive design, component architecture, routing & lazy loading, state management, forms & validation, animations, theming, i18n, accessibility, SEO, PWA, performance optimization.

### Backend
REST API, GraphQL, authentication & authorization, error handling & validation, email, WebSockets, customer support/chatbot, database, search infrastructure.

### Search
Elasticsearch.

### Real-Time
WebSockets, Firebase where appropriate.

### Maps
Google Maps, store locations, marker clustering.

### User Features
Login/signup, social auth, profile, favorites, reviews & comments, similar products, contact us, customer support, feedback.

### Admin
Dashboard, product/user/order/inventory/store management, customer support, analytics, email management, data visualization.

### Infrastructure
Git/GitHub, CI/CD, AWS, DevOps practices, deployment.

### Quality
Unit/integration/E2E testing, cross-browser and accessibility testing, performance testing, error handling, documentation.

Full detail: see [REQUIREMENTS.md](REQUIREMENTS.md) for specific, ID-tagged requirements per area.

## Technology Decisions Made So Far

- **Frontend framework:** Angular + TypeScript (see [ARCHITECTURE.md](ARCHITECTURE.md), ADR-001).
- Everything else (backend framework, database, state management approach, etc.) is intentionally undecided until the relevant project phase — see [ARCHITECTURE.md](ARCHITECTURE.md).

## Development Philosophy

- Spec before code: every feature starts as a requirement and acceptance criteria, not a prompt.
- Learn → Understand → Practice → Verify → Implement → Test → Review → Document → Commit → Next step.
- No premature complexity: no microservices, heavy state libraries, or elaborate infrastructure until a real, demonstrated need justifies them.
- Small, meaningful commits on purpose-named branches. See [DEVELOPMENT.md](DEVELOPMENT.md).

## Learning Approach

The project is organized into 26 phases, from JavaScript fundamentals through production hardening and a final architecture review. Only the current phase and next step are actively worked on at any time — the full phase list exists to give shape to the project, not to be rushed through.

- Current phase & step: [PROCESS.md](PROCESS.md)
- Skill-by-skill learning log: [LEARNING.md](LEARNING.md)
- Product specification: [REQUIREMENTS.md](REQUIREMENTS.md)
- Architecture decisions: [ARCHITECTURE.md](ARCHITECTURE.md)
- Development rules: [DEVELOPMENT.md](DEVELOPMENT.md)

## Documentation

Additional documentation lives under [docs/](docs/):

- `docs/learning/` — learning notes and exercises
- `docs/architecture/` — deeper architecture write-ups as they're needed
- `docs/api/` — API documentation, once an API exists
- `docs/testing/` — testing strategy and notes
- `docs/devops/` — CI/CD and deployment notes

These are created only as they become useful, not pre-populated.
