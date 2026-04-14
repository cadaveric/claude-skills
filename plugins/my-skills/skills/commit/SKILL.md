---
name: commit
description: Create a git commit — use when the user asks to commit, stage changes, write a commit message, or save work to git.
---

# Smart Commit

Create a git commit for all staged/unstaged changes.

Steps:
1. Run `git status` and `git diff` to see everything
2. Stage relevant files (never .env, secrets, or binaries unless explicitly asked)
3. Write a commit message that explains WHY, not just what changed
4. Format: short subject line (≤72 chars) + blank line + bullet body if needed
5. Always append: `Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>`

Do NOT push unless the user explicitly asks.
