# AGENTS.md

## Cursor Cloud specific instructions

### Overview

This is a **single-file static web application** — a Markdown editor called "Console Markdown Enterprise". The entire app lives in `index.html` with no build step, no package manager, no backend, and no database. All JS/CSS dependencies are loaded from CDNs at runtime.

### Running the application

Serve the project root with any static HTTP server:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080/index.html` in a browser. Internet access is required for CDN-hosted libraries (Vue 3, Element Plus, markdown-it, Highlight.js, Mermaid, DOMPurify, Google Fonts).

### Key caveats

- There is **no build step**, no `package.json`, no linter, and no test framework. Validation is done by opening the app in a browser and testing interactively.
- Data is persisted in the browser's `localStorage` — there is no server-side state.
- The `.md` files in the repository root are **template/snippet files** loaded by the editor as sample content; they are not documentation or build inputs.
- The `README.md` (in Portuguese) describes the product features and template organization.
