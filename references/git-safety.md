# Git safety and backup policy

## Before any mutation
- `git rev-parse --show-toplevel`, `git status --short`, `git branch --show-current`, `git log -5 --oneline`, `git remote -v`.
- Inspect `.gitignore`, `.git/info/exclude`, `git ls-files`, `git status --ignored --short` for required ignored files.
- Verify actual remote visibility using trusted repository metadata or authenticated hosting UI/API. A remote URL alone does not prove privacy.
- Review staged changes with `git diff --cached --stat` and `git diff --cached`; check filenames and contents for secrets. Never print secret values into reports.
- Check binary/large files and Git LFS needs; avoid introducing LFS without approval.

## Safe actions
- Initialize Git only if absent; preserve existing history and branch.
- Use `git add -- <explicit paths>` rather than `git add .` when existing user work is present.
- If a file already has unstaged user edits, read and reconcile or stop; don't stage it blindly.
- Commit only finished, coherent changes with a descriptive message.
- Push only when destination, access, privacy and branch are verified; never auto-create a public repository.
- Verify push exit status and remote branch SHA when possible.

## Backup levels
- Level 0: no Git history.
- Level 1: local commit exists (not disaster recovery).
- Level 2: verified commit pushed to a private remote; inspect missing/ignored assets and external dependencies.
- Level 3: restore tested from a clean clone with documented environment and assets. Do not claim Level 3 without performing it.

## Special cases
- Existing dirty tree: leave untouched unless changes are explicitly within scope; if no safe snapshot possible, report blockers.
- Existing public remote: do not push sensitive project files without explicit user decision.
- Secrets already tracked: stop and report remediation need; `.gitignore` alone does not remove secrets from Git history.
- Xcode: ignore DerivedData, user-specific xcuserdata and build outputs, but verify shared schemes, project files, assets and package resolution are tracked when needed.