---
name: refactor
description: Refactor code — use when the user asks to refactor, clean up, restructure, or improve code organization without changing behavior.
---

# Refactor

Refactor the current file or the code described. Behaviour must not change.

Rules:
- Run (or describe how to run) existing tests before and after to verify nothing broke
- One concern per function/class — split if mixed responsibilities
- Names must be self-documenting — remove comments that just repeat the code
- Eliminate duplication only when the same logic appears ≥3 times
- Do NOT add new features or error handling during a refactor
- Do NOT change public interfaces or API shapes

Output:
1. What you changed and why
2. The refactored code
3. What tests to run to verify correctness
