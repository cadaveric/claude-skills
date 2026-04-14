---
name: docker
description: Generate Docker configuration — use when the user asks for a Dockerfile, docker-compose, to containerize the app, or set up Docker for the project.
---

# Docker

Generate or improve Docker configuration for the current project.

Produce:
1. A production-ready `Dockerfile` (multi-stage if beneficial, minimal image)
2. A `docker-compose.yml` with named volumes, health checks, restart policy
3. A `.dockerignore` that excludes secrets, caches, dev artifacts
4. Startup notes: build command, env vars required, ports exposed

Rules:
- Never COPY .env into the image — use env_file or runtime secrets
- Pin base image to a specific minor version (e.g. python:3.11-slim)
- HEALTHCHECK must verify the app is actually responding, not just running
- Volumes for anything that must survive container restarts (caches, data)
