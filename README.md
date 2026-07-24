# artifacts

Static documents published with GitHub Pages.

## Smooth × Tabby — Design Walkthrough

`index.html` — a screen-by-screen walkthrough of how Tabby "Pay in 4" will work
across Smooth's admin panel, merchant panel and customer app. Written for a
product audience: design decisions, edge-case flows, and the open questions for
both the client and the Tabby team.

Self-contained: one HTML file, no build step, no external requests. Light and
dark themes, with a toggle in the bottom-right corner.

**Live:** https://shivam-singh-au17.github.io/artifacts/

### Publishing

Settings → Pages → Build and deployment → Deploy from a branch → `main` / `/ (root)`.

The page carries `<meta name="robots" content="noindex, nofollow">` so search
engines skip it. That is not access control — anyone with the URL can read it.
