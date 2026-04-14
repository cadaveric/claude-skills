---
name: test
description: Write tests — use when the user asks to write tests, add test coverage, create unit or integration tests, or test a function or class.
---

# Write Tests

Write tests for the current file or the function/class described.

Rules:
- Test behaviour, not implementation — tests should survive refactors
- Each test has one clear reason to fail
- Name tests: `test_<what>_<when>_<expected>`
- Cover: happy path, edge cases, error cases, boundary values
- Do NOT mock what you can use for real (prefer integration over unit for I/O)
- If mocking is necessary, mock at the boundary (HTTP, DB), not internal functions

Use the same testing framework already in the project. If none exists, use pytest for Python, Jest for JS/TS.
