# VELORA Development Process

This file always reflects the CURRENT state of the project. It is updated after every completed step — not the whole roadmap, just where we are now.

## Current Phase

PHASE 0 — Project Setup and Engineering Workflow

## Current Step

Step 0.1 — Establish the engineering workflow and Git discipline before any code is written.

## Status

IN_PROGRESS

## Objective

Before writing a single line of VELORA application code, set up the project so that development follows a professional, disciplined workflow: proper Git branching, meaningful commits, and a shared understanding (between you and your AI mentor) of how work will be planned, reviewed, and documented.

## Why This Matters

Most self-taught developers skip process and jump straight to code. This produces projects that work but that the developer can't fully explain, extend, or defend in an interview. Professional engineers spend real time on workflow: branching strategy, commit hygiene, and definition-of-done — because it's what makes a codebase maintainable by a team (or by future-you). Practicing this from commit #1 is cheaper than retrofitting it later.

## Prerequisites

- A GitHub (or equivalent) account for the remote repository (can be added later; not blocking).
- Git installed locally and basic familiarity with `git init`, `add`, `commit`, `status`, `log`.
- Willingness to read and follow [DEVELOPMENT.md](DEVELOPMENT.md) rules for the rest of the project.

## Tasks

- [x] Initialize Git repository (already done).
- [x] Create project documentation scaffold (PROCESS.md, REQUIREMENTS.md, DEVELOPMENT.md, LEARNING.md, ARCHITECTURE.md, README.md).
- [x] Create docs/ directory structure.
- [ ] Developer reads DEVELOPMENT.md and confirms understanding of the branching model and commit conventions.
- [ ] Developer reads REQUIREMENTS.md and ARCHITECTURE.md to understand the shape of the project (no implementation yet).
- [ ] Developer sets up a `.gitignore` appropriate for the eventual tooling (this will be revisited once a package manager is chosen in Phase 1/4 — not needed yet).
- [ ] Developer explains back, in their own words, the branch naming convention and commit message format.

## Acceptance Criteria

- [ ] Developer can state, without looking, the branch prefixes used in this project (`feature/`, `fix/`, `refactor/`, `docs/`, `test/`, `chore/`) and when to use each.
- [ ] Developer can write a correctly-formatted commit message for a hypothetical change.
- [ ] Developer understands that AI will not write production code, and can explain why that constraint exists.

## Verification

Verification for this step is conversational, not code-based (there is no code yet):

1. Developer summarizes, in their own words, the roles defined in DEVELOPMENT.md (human vs. AI mentor).
2. Developer proposes a branch name and commit message for a fictional first task ("set up Angular workspace").
3. Once both are correct, this step is marked COMPLETED.

## Developer Notes

_(Record important discoveries, decisions, or deviations from the plan here as they happen.)_

- 2026-08-08: Project initialized. Documentation scaffold created. No application code exists yet.

## Completed Steps

- 2026-08-08: Repository initialized with Git.
- 2026-08-08: Documentation scaffold created (PROCESS.md, REQUIREMENTS.md, DEVELOPMENT.md, LEARNING.md, ARCHITECTURE.md, README.md, docs/ structure).

## Next Step

Once the developer confirms understanding of the workflow rules (see Verification above), the next step is **Step 0.2 — Development environment and tooling baseline**, which will cover: Node.js/npm version, editor setup, and preparing for Phase 1 (JavaScript fundamentals). This will be introduced only after Step 0.1 is verified — not before.
