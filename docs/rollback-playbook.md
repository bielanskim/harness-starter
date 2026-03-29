# Rollback Playbook (Harness Engineering)

## Never
- Force push to main
- Push directly to main
- Hotfix without PR + full harness

## Safe Rollback Process

1. Inspect history
   `ash
   git log --oneline --graph --decorate
   git reflog

Create rescue branch (never touch main directly)Bashgit checkout -b rescue/-incident
Restore known-good commitBashgit checkout <good-commit-hash>
Create fix branch from good stateBashgit checkout -b agent/-rollback-fix
Push and open PR
Let the full harness (lint + tests + simulations) validate
Get human approval
Merge via PR only (Squash and merge preferred)


Core Rule
main must always remain clean verified truth.
Bad branches are deleted, never fixed in place.
All recovery must go through the same PR + harness gate as normal changes.
