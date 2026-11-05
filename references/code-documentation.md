# Code clarity and comments

Prioritize clear names, small functions and consistent structure. Comments should explain *why* a surprising choice exists, invariants, edge cases, concurrency, ownership, external protocol assumptions, and security implications—not narrate obvious syntax.

Use language-native API docs (`///` in Swift) for important externally used types and methods where contracts, preconditions or side effects are not obvious. Update comments when behavior changes. Never mass-insert comments or refactor unrelated code as part of documentation setup.

Document boundaries: what data models represent, which layer owns state, persistence behavior, error handling, external services, and the path from user action to effect. Mark uncertain conclusions explicitly. Avoid brittle line-number references; prefer paths and symbols verified against the repository.