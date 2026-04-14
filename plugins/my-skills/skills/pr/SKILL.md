---
name: pr
description: Create a pull request — use when the user asks to open a PR, create a pull request, submit changes for review, or push a branch for review.
---

# Create Pull Request

Create a pull request for the current branch.

Steps:
1. `git status` + `git log main..HEAD` to see all changes
2. `git diff main...HEAD` for the full diff
3. Write a PR title (≤70 chars, imperative mood)
4. Write a body:
   - **Summary**: 2–4 bullets on what changed and why
   - **Test plan**: checklist of what to manually verify
   - **Screenshots**: note if UI changed (user will add)
   - Footer: `🤖 Generated with Claude Code`
5. `gh pr create` with the above

Do NOT force-push. Do NOT merge. Just open the PR.
