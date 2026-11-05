# AI Project Handoff

**A reusable Agent Skill for safer AI-assisted software development and human developer handoff.**

Turns a fragile AI-built codebase into a project with an understandable structure, meaningful change history and an honest recovery status—without automatically rewriting working code.

## Modes
- `setup` — initial Git safety and minimal documentation.
- `maintain` — keep meaningful commits and context accurate as work progresses.
- `audit` — read-only readiness and risk review.
- `handoff` — verified developer transfer checklist.

## Install
Copy this folder into the skills directory supported by your agent, then ask it to use **ai-project-handoff**. Agent-specific paths and discovery mechanisms vary; consult your agent's current documentation. Alternatively, provide `SKILL.md` directly as project instructions along with its referenced files.

## Example prompts
- "Use ai-project-handoff in setup mode. Preserve all existing code and do not publish anything without confirmation."
- "Audit this repository for restore and developer-handoff readiness; read-only."
- "Prepare a human developer handoff, documenting only verified facts."

## Safety principles
- Existing uncommitted work is not expendable.
- Local Git history is not off-device backup.
- Remote configuration is not proof of a successful push.
- `.gitignore` does not remove secrets from existing history.
- A handoff is not complete because a README exists; validate paths, prerequisites and unknowns.
- Avoid mass comments and unrequested refactors.

## Contents
`SKILL.md` is the entry point. `references/` holds focused operational guidance; `templates/` are optional starting points; `examples/` demonstrates a SwiftUI project.

## License
No license is included yet. Choose a license before public redistribution or commercial packaging.