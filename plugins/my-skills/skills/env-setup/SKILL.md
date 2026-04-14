---
name: env-setup
description: Set up a development environment on a new machine — use when the user asks to set up their dev environment, bootstrap a new machine, or install project dependencies.
---

# Environment Setup

Bootstrap a working development environment for the current project on a new machine.

## Steps

1. **Detect the stack** — read `package.json`, `pyproject.toml`, `requirements.txt`, `Cargo.toml`, `go.mod`, `Makefile`, `.tool-versions`, `.nvmrc`, `.python-version`

2. **Check what's already installed** — run version checks (`node -v`, `python3 --version`, `docker --version`, etc.) before installing anything

3. **Install in order**:
   - Language runtime (nvm, pyenv, rbenv — use version managers, not system packages)
   - Package manager dependencies (`npm install`, `pip install -r requirements.txt`, etc.)
   - Dev tools (linters, formatters, pre-commit hooks)
   - Services (Docker containers for DB, cache, etc.)

4. **Environment variables** — list every required `env` var, where to get each value, and create a `.env.example` if one doesn't exist. Never fill in real secrets.

5. **Verify** — run the project's health check, test suite, or dev server to confirm everything works

## Rules

- Prefer version managers over system package managers for runtimes
- Never `sudo pip install` — always use virtualenvs
- If Docker is available, prefer containerized services over native installs
- Document any manual steps that can't be automated (license keys, hardware requirements, etc.)

## Output

A numbered checklist of commands to run, with explanations. Mark steps as optional vs. required.
