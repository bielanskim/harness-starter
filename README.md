# harness-starter

A governance template for safe, controlled **agentic development** using **Harness Engineering + Symphony** in Cursor.

## Purpose
This template provides the mechanical rules, guardrails, and structure needed to build reliable multi-agent systems while keeping strong human oversight and machine-legible enforcement.

It establishes:
- **Harness Engineering** — the controlled execution surface (branch strategy, PR gate, full harness validation, failure policy)
- **Symphony readiness** — a machine-legible foundation for safe multi-agent orchestration

## What's Included
- .githooks/pre-push — local enforcement against direct pushes to main
- .github/workflows/ — CI harness (ci/lint, ci/tests, ci/simulations)
- AGENTS.md — strict mechanical contract for all agents
- docs/rollback-playbook.md — safe recovery procedures
- docs/ — documentation, plans, and task handoff context
- Specialized rules in .cursor/rules/
- Skills system in .cursor/skills/
- SOUL.md — agent persona and behavioral boundaries

## Core Harness Principles
- main is immutable verified truth
- All changes go through gent/YYYY-MM-DD-... branches + PR + full harness
- Failure policy: delete bad branches, never fix in place
- Pre-push hook + GitHub branch protection enforce the rules mechanically
- Progressive disclosure: Human intent → Agent proposal → Harness validation → Human approval

## Symphony Readiness
This repo is now fully machine-legible and ready for Symphony multi-agent orchestration:
- Parallel agents can propose changes safely
- All proposals are independently validated by the harness
- Clear handoff via docs/ and AGENTS.md

When you are ready, bring in the Symphony orchestrator on top of this guarded foundation.

## How to Use
1. Use this repo as a GitHub template for new projects.
2. Open in Cursor.
3. Follow AGENTS.md for all agent behavior.
4. Start every session by reading SOUL.md and AGENTS.md.
5. All work happens via agent branches + PRs.

Last updated: March 2026
