---
name: debug
description: Debug code issues — use when the user asks to debug, diagnose a bug, fix an error, trace a problem, or find out why something is not working.
---

# Debug

Systematically diagnose the issue described or visible in the current file.

Process:
1. State your hypothesis about the root cause (be specific)
2. Identify the exact lines/functions involved
3. Trace the data flow that leads to the bug
4. Propose the minimal fix — do not refactor surrounding code
5. Explain what you would add to prevent this class of bug in the future

If the bug is not reproducible from static analysis, list the exact commands/steps to reproduce it.
Do NOT speculatively refactor. Fix the bug, nothing else.
