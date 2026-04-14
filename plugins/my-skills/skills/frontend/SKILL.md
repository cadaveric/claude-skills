---
name: frontend
description: Frontend UI/UX work — use when the user asks to build a new component/page, polish existing UI, fix styling, or improve visual design.
---

# Frontend

Detect the mode from context, then execute:

---

## Mode A — Polish (existing UI/file)

When the user asks to improve, fix, or polish an existing file:

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

---

## Mode B — Create (new component/page/UI from scratch)

When the user asks to build something new:

### Design Thinking (do this before writing code)

Commit to a **bold aesthetic direction**:
- **Purpose**: What problem does this interface solve? Who uses it?
- **Tone**: Pick a clear extreme — brutally minimal, maximalist, retro-futuristic, organic, luxury, playful, editorial, brutalist, art deco, industrial, etc.
- **Differentiation**: What's the one thing someone will remember about this UI?

NEVER default to generic aesthetics: no Inter/Roboto/Arial, no purple gradients on white, no cookie-cutter layouts.

### Implementation Rules

- **Typography**: Choose distinctive, characterful fonts — pair a display font with a refined body font
- **Color**: Commit to a cohesive palette with CSS variables. Dominant colors + sharp accents over timid evenly-distributed palettes
- **Motion**: CSS transitions for HTML, Motion library for React. One well-orchestrated page load (staggered reveals) beats scattered micro-interactions
- **Layout**: Unexpected compositions — asymmetry, overlap, diagonal flow, grid-breaking elements, generous negative space OR controlled density
- **Backgrounds**: Atmosphere over flat colors — gradient meshes, noise textures, geometric patterns, layered transparencies, dramatic shadows

Deliver production-grade, functional code (HTML/CSS/JS, React, Vue — match the project stack).
