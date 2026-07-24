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
4. Add a back-link to `../` as the first element inside `<body>`.
5. Add an entry to the `.docs` list in the root `index.html`.

## Notes

Each document carries `<meta name="robots" content="noindex, nofollow">` so
search engines skip it. That is not access control — this repository is public,
and anyone with the URL can read the page.
