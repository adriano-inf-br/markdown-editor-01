# AGENTS.md

## Cursor Cloud specific instructions

### Overview

This is a static single-page Markdown editor ("Console Markdown Enterprise" / "Gerador Markdown + Mermaid") built with Vue 3, Element Plus, markdown-it, highlight.js, DOMPurify, and Mermaid. All dependencies are loaded from CDNs — there is no build system, no `package.json`, and no backend.

### Running the application

Serve the repository root with any static HTTP server. The app uses `fetch()` to load `.md` template files, so `file://` protocol will not work.

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080` in a browser.

### Key notes

- **No build step, no linter, no test framework**: This project has no `package.json`, `node_modules`, or CI pipeline. There is nothing to `npm install` or `pnpm install`.
- **CDN dependencies require internet**: Vue 3, Element Plus, markdown-it, highlight.js, DOMPurify, and Mermaid are all loaded from `unpkg.com` and `cdn.jsdelivr.net`. The VM must have internet access for the app to function.
- **Data persistence**: All document data is stored in the browser's `localStorage` under the key `console_markdown_mermaid_enterprise_fixed_v1`.
- **Template files**: The `.md` files in the repository root (e.g. `modelo-html-01.md`, `modelo-php-01.md`) are code snippet templates fetched at runtime via the toolbar buttons. They are not documentation files.
