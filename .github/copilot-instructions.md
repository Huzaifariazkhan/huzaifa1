This repository is a small collection of static HTML/CSS experiments and examples. The guidance below is focused on enabling an AI coding agent to be immediately productive editing and extending this project.

- **Project Type:** static frontend (plain HTML + CSS files). No build system, package.json, or tests are present.
- **Primary files:** `index.html`, `pract.html`, `stickydiv.html`, `tablecolor.html` and their matching CSS files `style.css`, `pract.css`, `stickydiv.css`, `tablecolor.css`.

- **Big picture / intent:**
  - This workspace contains small, independent example pages demonstrating CSS layouts, borders, sticky elements, and table styling. Each page is generally self-contained: HTML files link to a same-directory CSS file.
  - The repository appears to be a learning / playground repo rather than a production site. Many files contain isolated experiments (for example, `index.html` includes multiple HTML fragments one after another).

- **Conventions & patterns to follow:**
  - Files are edited in place; keep CSS edits scoped to the CSS file referenced by the page you change (e.g., edit `style.css` for `index.html`).
  - Class naming is informal and short (single letters like `.a`, `.b`, etc.). When adding new, prefer clear names only when the user asks — the repo owner is using short names intentionally for experiments.
  - Avoid consolidating or removing experimental sections (for example, the duplicated HTML blocks in `index.html`) without asking the user — these are likely intentional snapshots of different attempts.

- **How to run & debug locally:**
  - No build step. Open the HTML file directly in a browser or serve the directory with a static server to test multiple pages.
  - Quick static server (PowerShell / Windows):
    - If Python is available: `python -m http.server 8000` then visit `http://localhost:8000/pract.html`.
    - If Node is available: install `http-server` once with `npm install -g http-server` then run `http-server -p 8000`.
  - Use browser devtools to inspect CSS, classes and to try live style tweaks.

- **Editing guidance for AI agents:**
  - Make minimal, local changes. Modify only the specific CSS/HTML file that relates to the requested change.
  - Preserve existing experimental content unless the user explicitly requests cleanup.
  - When adding new styles, prefer creating or editing the CSS file that the HTML page already links to (do not create global styles unless user asks).
  - Use explicit relative paths when creating new files (files are served from the repo root).

- **Examples of project-specific actions:**
  - To change the appearance of `pract.html`, update `pract.css` and confirm by opening `pract.html` in a browser.
  - To add a new demo page, create `new-demo.html` and `new-demo.css`, link the stylesheet in the head with `<link rel="stylesheet" href="new-demo.css">`.

- **What not to do:**
  - Do not reorganize files into a build pipeline, or introduce a framework, without explicit instruction from the owner.
  - Do not delete duplicated or commented-out snippets; they are likely intentional experiments.

If any section is unclear or you'd like additional examples (naming suggestions, a small starter `index.html` with tidy structure, or a recommended local launch script), tell me which part to expand.
