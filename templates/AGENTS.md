# Agent working rules

1. Read README.md and PROJECT_CONTEXT.md, then inspect the current code before changing it.
2. Check `git status --short` and branch; preserve unrelated user edits.
3. Make only requested changes; do not redesign, refactor or add dependencies without approval.
4. Use meaningful Conventional Commits; explain non-obvious decisions.
5. Add comments only for contracts, invariants and non-obvious logic; update stale comments.
6. Never stage secrets or unrelated changes; do not rewrite history or use destructive Git commands.
7. Push only to an authorized, verified destination; report actual backup status.
8. Update PROJECT_CONTEXT.md when architecture or significant behavior changes.
9. Coordinate file ownership before concurrent agents edit the same code.
10. Report verification performed and remaining unknowns; never fabricate success.