# Commit standards

Use Conventional Commits: `type(scope): imperative summary`.
Types: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, `build`, `ci`, `perf`. `style` is reserved for formatting-only changes; UI redesigns are generally `feat(ui)` or `fix(ui)`.

Examples:
- `feat(cafe): add ordering dialogue choices`
- `fix(audio): prevent overlapping playback`
- `docs(project): map simulation state ownership`
- `chore(repo): document recovery prerequisites`

Good commits answer **what** changed; for non-obvious work, add a body explaining **why**, constraints, trade-offs and migration impact. Do not claim changes were tested unless verified. Prefer coherent, reviewable commits over huge unrelated snapshots. Preserve original author history; never rewrite existing commits merely to make messages prettier. Commit messages do not replace PR descriptions, architecture decisions or code documentation.

For significant architecture decisions, create a short ADR only when warranted: context, decision, alternatives, consequences, date/status. Avoid ADRs for routine UI tweaks.