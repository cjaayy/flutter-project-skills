---
name: git-ship-clean
description: Keep Git history atomic, clean, and free of leftover debug code or sensitive files. Use when staging changes, writing commit messages, merging branches, or preparing deployments.
---

# Git Ship Clean

## Workflow
1. **Inspect Diff Before Commit:** Review staged changes to remove leftover console.log statements, commented-out dead code, unused imports, and temporary test files.
2. **Atomic Commits:** Group related changes into small, focused commits rather than massive catch-all commits.
3. **Conventional Commit Messages:** Use clear prefixes (feat:, fix:, refactor:, chore:, docs:) describing what changed and why.
4. **Secret Scan:** Confirm no .env files, private keys, or credentials are staged before pushing.
