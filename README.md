# Vue Interview Roadmap (MkDocs Material)

This repository now uses [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) to build and publish the Vue interview roadmap and related study notes.

## Project structure

```
.
├── docs/
│   ├── index.md
│   └── vue-interview-roadmap.md
└── mkdocs.yml
```

- All content lives inside the `docs/` directory.
- Navigation, theme settings, and metadata are configured in `mkdocs.yml`.

## Local development

1. Install MkDocs Material:
   ```bash
   pip install mkdocs-material
   ```
2. Run the local development server:
   ```bash
   mkdocs serve
   ```
3. Open your browser at <http://127.0.0.1:8000> to preview the site.

## Deployment

Build the static site output with:
```bash
mkdocs build
```
The generated files will appear in the `site/` directory, ready to be published (for example, via GitHub Pages).
