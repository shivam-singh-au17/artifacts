# artifacts

Design and engineering documents, published with GitHub Pages.

**Live:** https://shivam-singh-au17.github.io/artifacts/

## Layout

```
index.html                            Introduction + list of every document
smooth-tabby-bnpl/index.html          Smooth × Tabby — Design Walkthrough
foodics-integration-review/index.html Smooth × Foodics — Integration Review
```

One folder per document. The folder name becomes the URL, so
`smooth-tabby-bnpl/` is served at
`https://shivam-singh-au17.github.io/artifacts/smooth-tabby-bnpl/`.

## Adding a document

1. Create a folder named after the document, using lowercase words joined by
   hyphens — that name is the URL a client will see.
2. Put a single `index.html` inside it. Keep it self-contained: no build step,
   no external fonts, scripts or images, so the page works offline and loads
   instantly.
3. Reuse the CSS custom properties defined at the top of any existing document
   (`--paper`, `--ink`, `--accent`, `--line`, and the rest). Every page shares
   the same palette and type scale, in both light and dark themes.
4. Copy the theme block from any existing document — the small `<script>` in the
   `<head>`, the `.theme-toggle` button, and the script beside it. See *Theme*
   below.
5. Add a back-link to `../` as the first element inside `<body>`.
6. Add an entry to the `.docs` list in the root `index.html`.

## Theme

Light is the default everywhere; the operating system's dark-mode setting is
deliberately ignored, so a page looks the same on every machine until a reader
asks for something else.

The toggle in the corner writes `light` or `dark` to `localStorage` under the
key **`ss-docs-theme`**. Every document reads that one key, so a choice made on
any page holds across the whole site — on the next page, on the next visit, and
live in other open tabs. Copy the key verbatim into new documents; a document
with its own key silently opts out of the shared setting.

The `<head>` script sets `data-theme` on `<html>` before the stylesheet is
parsed, which is what keeps a dark-mode reader from seeing a white flash. It has
to stay in the head, above the `<style>` block.

## Notes

Each document carries `<meta name="robots" content="noindex, nofollow">` so
search engines skip it. That is not access control — this repository is public,
and anyone with the URL can read the page.
