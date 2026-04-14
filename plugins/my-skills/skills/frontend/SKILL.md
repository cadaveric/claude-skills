---
name: frontend
description: Polish frontend UI/UX — use when the user asks to improve the UI, polish the frontend, fix styling, make it look better, or improve visual design.
---

# Frontend Polish

Review the current file (or files mentioned) and improve the UI/UX to production quality.

Rules:
- Do NOT change any backend logic, API calls, data structures, or endpoint URLs
- Do NOT remove any functionality — only improve how it looks and feels
- Preserve all existing JavaScript behavior exactly
- Use the existing CSS variables already defined in the file
- Mobile-first, responsive layouts
- Smooth transitions (150–250ms), no janky repaints
- Typography hierarchy must be clear
- Empty/loading/error states must look intentional, not broken
- Spacing rhythm: 4px base unit, multiples of 4
- Color meaning must be consistent: green=positive/win, amber=draw/warning, red=loss/danger, blue=info

Deliver:
1. A list of every UI problem you found
2. The fixed code with inline comments only where the change is non-obvious
