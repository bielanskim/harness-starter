# harness-starter

A clean, reusable starter template for **Harness Engineering + Symphony** agentic development in Cursor.

## What This Is
This repository provides a battle-tested foundation for building safe, controlled, and auditable agentic projects using Cursor.

## Included
- `.cursor/rules/harness-engineering.mdc` — Core governing rules (always active)
- `AGENTS.md` — Central contract and table of contents
- `autonomy-levels.md` — Autonomy framework (L0–L4)
- `docs/checklists/` — Pre-plan and post-execution checklists
- `docs/autonomy-grants/` — For L4 supervised autonomy grants
- `scripts/` — Utility scripts

## How to Use This Template
1. Click **"Use this template"** on GitHub to create a new repository
2. Open the new repo in Cursor using the **Harness-Agentic** profile
3. Add project-specific rules in `.cursor/rules/[project-name]-rules.mdc` when needed
4. Update `AGENTS.md` with your project name and constraints
5. Start every session in Plan Mode

## Core Principles
- Progressive disclosure: Plan → Approve → Execute → Review
- Repository is the single source of truth
- Humans provide intent. Agents propose plans and wait for approval
- Cloud Agents only for heavy tasks, with explicit approval

Last updated: March 2026