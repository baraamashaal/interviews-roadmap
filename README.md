# Vue Interview Roadmap (MkDocs Material)

This repository uses [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) to build and publish the Vue interview
roadmap and related study notes.


## Project structure

```
.
├── docs/
│   ├── index.md
│   ├── vue-interview-roadmap.md
│   └── vue-interview-roadmap/
│       └── *.md
├── mkdocs.yml
└── .github/workflows/deploy.yml
```

- All documentation content lives inside the `docs/` directory so MkDocs can resolve the navigation correctly.
- Navigation, theme settings, and metadata are configured in `mkdocs.yml`.
- GitHub Pages deployment is automated through `.github/workflows/deploy.yml`.


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

### Manual build

Build the static site output with:
```bash
mkdocs build
```
The generated files will appear in the `site/` directory, ready to be published.

### GitHub Pages (recommended)

1. Ensure GitHub Pages is set to deploy from the `gh-pages` branch (Settings → Pages → Build and deployment).
2. Push to the `main` branch. The GitHub Actions workflow automatically builds the site with MkDocs Material and publishes it to the `gh-pages` branch using the repository's default `GITHUB_TOKEN`.
3. Your site will be available at `https://<username>.github.io/interviews-roadmap/` after the workflow completes.

