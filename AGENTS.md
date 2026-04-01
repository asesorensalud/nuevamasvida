# AGENTS.md — Agent Coding Guidelines

This file provides context and guidelines for AI agents operating in this repository.

---

## 1. Project Overview

**Project**: gonzalo — Static landing page for a health insurance advisor (Gonzalo Díaz)

**Type**: Single-page static HTML website with embedded CSS and JavaScript

**Purpose**: Landing page to generate leads for health insurance advisory services in Chile (Fonasa / Isapre Nueva Masvida)

**Stack**: Plain HTML5, CSS3, vanilla JavaScript (no frameworks)

---

## 2. File Structure

```
/Users/aalamo/repos/gonzalo/
├── index.html         # Main landing page (HTML + embedded CSS + JS)
├── gonzalo_diaz.jpeg  # Profile photo (optimized)
└── gonzalo_diaz.png   # Alternate profile photo
```

---

## 3. Build / Preview Commands

Since this is a static HTML project, there is **no build process**. To preview:

### Preview locally

**Using Python 3** (pre-installed on macOS):
```bash
python3 -m http.server 8000
# Then open http://localhost:8000
```

**Using Node.js (if available)**:
```bash
npx serve .
# Then open the URL shown
```

**Using PHP (if available)**:
```bash
php -S localhost:8000
```

### No linting or testing

This project has **no automated tests, linting, or build commands** since it's pure static HTML. Any changes can be verified by refreshing the browser.

---

## 4. Code Style Guidelines

### General Principles

- Keep changes minimal and focused — this is a simple marketing landing page
- Maintain the existing visual design and color scheme
- Do not add new dependencies or build tools
- Preserve responsive behavior (mobile-first)

### HTML Conventions

- Use semantic HTML5 elements (`<header>`, `<section>`, `<footer>`, `<nav>`)
- All attributes use double quotes: `<a href="...">`
- Self-closing tags: `<img />`, `<meta />` (XHTML style is fine)
- Indent with 4 spaces
- Attributes order: `type`, `id`, `name`, `class`, `src`/`href`, `alt`, `required`

### CSS Conventions

- Use CSS custom properties (variables) for colors — they exist in `:root`
- Keep existing color variables:
  - `--azul-oscuro: #0a1628` (dark blue)
  - `--azul-medio: #1a2d4a` (medium blue)
  - `--dorado: #c9a227` (gold)
  - `--dorado-claro: #e8d48b` (light gold)
  - `--blanco: #fafafa` (white)
  - `--gris-claro: #f0f0f0` (light gray)
  - `--texto-gris: #6b7280` (text gray)
- Use BEM-like naming for custom classes: `.plan-card`, `.plan-header`, `.hero-content`
- Prefer flexbox and grid over floats
- Mobile-first: default styles first, `@media (max-width: 768px)` for mobile overrides

### JavaScript Conventions

- Keep scripts minimal — only what's needed for the contact form
- Use `const` and `let`; never `var`
- Prefer template literals: `` `Hello ${name}` ``
- Use arrow functions for callbacks
- Add event listeners via `addEventListener`, not inline handlers
- Always use `e.preventDefault()` on form submit handlers

### Accessibility

- Always include `alt` attributes on images
- Use `<label for="...">` paired with form inputs
- Include `required` attribute on mandatory fields
- Use semantic elements for screen readers
- Ensure color contrast meets WCAG AA standards (existing colors are compliant)

### Image Handling

- Use WebP format for new images (convert from JPEG/PNG if needed)
- Keep file sizes under 200KB for photos
- Ensure `alt` text describes the image content and context

---

## 5. Prohibited Actions

- **Do not** add build tools (Webpack, Vite, Parcel, etc.)
- **Do not** add frameworks (React, Vue, Angular, etc.)
- **Do not** add CSS frameworks (Tailwind, Bootstrap, etc.)
- **Do not** add JavaScript libraries (jQuery, etc.)
- **Do not** add testing or linting tools
- **Do not** modify the color scheme without explicit user approval
- **Do not** add new pages — this is a single-page site

---

## 6. Making Changes

When editing `index.html`:

1. **Read the file first** — understand the structure before modifying
2. **Preserve indentation** — match the surrounding code style
3. **Test locally** — serve the file and verify in browser
4. **Keep it simple** — avoid over-engineering

---

## 7. Contact Information

- **WhatsApp**: +56 9 6510 7706
- **Advisor**: Gonzalo Díaz — Asesor Profesional de Salud
- **Services**: Fonasa and Isapre Nueva Masvida health plan advisory

---

*Last updated: March 2026*
