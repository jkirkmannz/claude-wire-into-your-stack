---
description: Summarize what has changed in the repo
argument-hint: [base-branch-or-commit]
allowed-tools: allowed-tools: Bash(git branch --show-current), Bash(git status --short), Bash(git diff --stat HEAD), Bash(git log --oneline -10)
---

## Context

- Current branch: !`git branch --show-current`
- Status: !`git status --short`
- Recent commits: !`git log --oneline -10`
- Comparison base: $ARGUMENTS (use HEAD when empty). Before summarizing, run `git diff --stat` against this base.

## Task

Summarize what has changed, using the context above.
If a base was given ($ARGUMENTS), compare against it; otherwise cover uncommitted changes.
Run `git diff` on specific files if you need detail.

Output:

1. One-sentence overview
2. Changes grouped by area or feature (bullets, with file paths)
3. Anything risky or worth reviewing (deleted code, config changes, missing tests)

Keep it under 20 lines.
