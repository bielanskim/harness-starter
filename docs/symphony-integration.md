# Symphony Integration Guide

This document explains how to integrate **Symphony** (multi-agent orchestration) on top of the Harness Engineering foundation provided by this template.

## Overview

- **Harness Engineering** = The governing rules and safety layer (progressive disclosure, autonomy levels, checklists, human approval).
- **Symphony** = The orchestration layer that coordinates multiple specialized agents.

The template provides the necessary foundation so Symphony can plug in cleanly and safely.

## What the Template Already Provides

- Clear governance via `harness-engineering.mdc`
- Autonomy levels and inheritance (`autonomy-levels.md`)
- Shared ground truth (`AGENTS.md` + `docs/`)
- Task handoff protocol (write context to `docs/`)
- Pre-plan and post-execution checklists
- Modular folder structure (`docs/exec-plans/`, `docs/references/`, etc.)

## How to Integrate Symphony

1. **Bring in the Symphony orchestrator**
   - Add the Symphony framework (your forked repo or official implementation) to the project.
   - Configure the central orchestrator agent to respect the Harness rules.

2. **Task Decomposition & Handoff**
   - The orchestrator breaks high-level goals into modular subtasks.
   - Each subtask is assigned to a specialized agent.
   - Handoff context is always written to `docs/exec-plans/` or `docs/references/` as structured markdown/JSON.

3. **Enforce Harness Rules**
   - All agents (including the orchestrator) must follow progressive disclosure.
   - Every significant step requires explicit human approval.
   - Autonomy level inheritance is enforced (no agent exceeds the granted level).

4. **Use the Checklists**
   - Pre-plan checklist before any plan is presented.
   - Post-execution checklist after any task completion.

5. **Recommended Folder Usage**
   - `docs/exec-plans/` → Store approved orchestration plans and subtasks
   - `docs/references/` → Landscape reviews and research findings
   - `docs/generated/` → Agent outputs and artifacts
   - `docs/autonomy-grants/` → Written approvals for any L4 actions

## Best Practices

- Start small: Use Symphony for 2–3 agents first.
- Keep the central orchestrator at L2 or L3 until you are comfortable.
- Always document handoff context clearly.
- Review `AGENTS.md` and `autonomy-levels.md` regularly.

## When to Integrate Symphony

Integrate Symphony when you need coordinated multi-agent workflows (parallel tasks, specialized agents, complex project management).

Until then, the Harness rules alone provide a safe, controlled single-agent or small-team agentic environment.

Last updated: March 2026