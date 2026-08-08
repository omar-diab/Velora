# VELORA Development Rules

These rules govern how VELORA is built. They exist to protect the project's real goal: turning the developer into a strong full-stack engineer, not just producing a working app. Read this before writing any code.

## 1. Roles

- **The human developer writes all production code.** No exceptions, regardless of how small or "obvious" the code seems.
- **The AI acts as mentor, coordinator, and reviewer** — not as an implementer. It provides explanations, requirements, acceptance criteria, hints, and code review, and only shows small illustrative examples clearly marked as such (never production-ready, drop-in code).
- If the AI ever finds itself about to write a full component, service, API route, or schema for VELORA, that's a signal to stop and hand it back as a task with guidance instead.

## 2. No Blind Copying

- Do not copy-paste code (from AI, tutorials, or elsewhere) without understanding every line.
- If you can't explain why a line of code exists, don't ship it. Ask instead.

## 3. Git Workflow

**Branching:**

- `main` — always deployable/stable.
- `feature/*` — new functionality (e.g., `feature/product-catalog`).
- `fix/*` — bug fixes (e.g., `fix/cart-total-rounding`).
- `refactor/*` — internal restructuring with no behavior change.
- `docs/*` — documentation-only changes.
- `test/*` — adding or restructuring tests.
- `chore/*` — tooling, dependencies, config.

**Commits:**

- Small, focused, and frequent — one logical change per commit.
- Format: `type: short imperative description` (e.g., `feat: add product listing UI`, `fix: handle invalid product response`, `docs: document authentication flow`).
- Never commit with vague messages like "update", "stuff", "changes", "final", "wip", "test".
- Never commit secrets, API keys, tokens, `.env` files, or credentials of any kind.

## 4. Tests

- Tests are required where they add real value: business logic, validation, critical user flows.
- Trivial code (pure template bindings, one-line getters) does not need a dedicated test — use judgment, and ask the mentor if unsure.

## 5. Documentation

- Significant decisions (architecture, library choices, trade-offs) are recorded as an ADR in [ARCHITECTURE.md](ARCHITECTURE.md).
- [PROCESS.md](PROCESS.md) always reflects current phase/step status.
- [LEARNING.md](LEARNING.md) is updated whenever a skill's status changes.

## 6. Dependencies

- No new library/framework is added without first explaining: what problem it solves, what the alternative (doing it manually) would look like, and what the developer needs to learn before using it responsibly.
- Avoid dependencies chosen purely for popularity. Prefer understanding fundamentals before reaching for an abstraction.

## 7. Security

- Never commit secrets, passwords, tokens, private keys, or database credentials.
- All environment-specific configuration goes through environment variables, never hardcoded literals.
- Validate and sanitize input at every trust boundary (client input, third-party API responses).
- Server-side code must never trust client-side authorization checks alone.

## 8. Accessibility & Performance

- Consider accessibility (semantic HTML, keyboard navigation, labels/alt text) as features are built, not retrofitted at the end.
- Consider performance (avoiding unnecessary re-renders, lazy loading, image sizing) as part of normal implementation, proportionate to what's being built.

## 9. Code Review

- Code is reviewed (by the AI mentor, and ideally re-read by the developer a day later) before being considered "done."
- Review findings are classified CRITICAL / HIGH / MEDIUM / LOW / OPTIONAL, with the reasoning explained — not just "fix this."

## 10. Simplicity

- Prefer the simplest solution that satisfies the current requirement.
- No microservices, complex state management libraries, event-driven architecture, multiple databases, or heavy design patterns until a real, demonstrated problem justifies them (see ARCHITECTURE.md's "No Premature Complexity" principle).
- YAGNI: don't build for hypothetical future requirements not yet in [REQUIREMENTS.md](REQUIREMENTS.md).

## 11. Definition of Done

A task is done only when, as appropriate to its size:

- The requirement is understood (not just "it compiles").
- The implementation exists and the developer can explain it unprompted.
- Edge cases and error handling have been considered.
- Tests exist where they add value.
- Accessibility and performance have been considered where relevant.
- Documentation is updated where necessary.
- A meaningful Git commit exists.

Not every micro-task requires every item above — use engineering judgment, and when in doubt, ask.
