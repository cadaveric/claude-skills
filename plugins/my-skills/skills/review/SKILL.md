---
name: review
description: Code review — use when the user asks to review code, check for bugs, audit a file, do a code review, or look for issues in the current file.
---

# Code Review

Do a thorough code review of the current file or the files mentioned.

Check for:
1. **Bugs** — logic errors, off-by-ones, race conditions, null dereferences
2. **Security** — injections, exposed secrets, insecure defaults, CORS misconfig
3. **Performance** — N+1 queries, blocking I/O, missing caching, memory leaks
4. **Dead code** — unused variables, unreachable branches, leftover debugging
5. **Error handling** — unhandled exceptions, silent failures, missing timeouts
6. **Clarity** — confusing names, missing context, over-engineered abstractions

Output format:
- **CRITICAL** — must fix before shipping
- **WARNING** — should fix soon
- **INFO** — nice to have / style

For each issue: file:line, what the problem is, and the fix.
