# Setup checklist

1. Confirm root, branch, working-tree state and remotes.
2. Check existing docs and relevant manifests; identify the minimum docs to add/update.
3. Review `.gitignore` without hiding required project assets.
4. Inventory required local environment by variable names only; never copy secrets into docs.
5. Create README, PROJECT_CONTEXT and AGENTS only where useful and absent/outdated.
6. Review the diff for unintended code changes, fabricated claims and accidental secrets.
7. Commit scoped files only when safe. Push only to verified intended private remote when authorized.
8. Report actual backup level and what remains unverified. No runtime test claim if no build was run.