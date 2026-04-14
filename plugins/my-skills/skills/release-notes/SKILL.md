---
name: release-notes
description: Generate release notes or a changelog from git history — use when the user asks for release notes, a changelog, or a summary of what changed since the last release/tag.
---

# Release Notes

Generate release notes from git history for the version or range described.

## Steps

1. **Find the range** — if the user specified a version/tag, use it. Otherwise:
   ```bash
   git tag --sort=-version:refname | head -5   # recent tags
   git log --oneline -20                        # recent commits if no tags
   ```

2. **Get commits in range**:
   ```bash
   git log <prev-tag>..HEAD --oneline --no-merges
   # or for a specific range:
   git log v1.0.0..v1.1.0 --oneline --no-merges
   ```

3. **Categorize** each commit:
   - **Features** — new capabilities (feat:, add, implement, introduce)
   - **Bug Fixes** — fixes (fix:, bug, patch, resolve)
   - **Performance** — speed/memory improvements
   - **Breaking Changes** — anything requiring user action
   - **Internal** — refactors, deps updates, CI — omit from user-facing notes unless asked

4. **Write** in plain language for the audience (users, not developers):
   - Lead with breaking changes (if any)
   - Group by category
   - Each item: one sentence, present tense, what the user can now do or what no longer breaks

## Output Format

```markdown
## v1.2.0 — 2026-04-14

### Breaking Changes
- ...

### New Features
- ...

### Bug Fixes
- ...
```

Keep it short. Link to PRs/issues if the project uses them (`#123`).
