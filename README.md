# Vue Interview Roadmap

This repository hosts my Vue interview roadmap and notes. The static site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and published via GitHub Pages.

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

## Content overview

- Site home: `docs/index.md`
- Roadmap overview: `docs/vue-interview-roadmap.md`
- Detailed Q&A: `docs/vue-interview-roadmap/*.md`

## Local editing

Update any of the Markdown files under `docs/` and preview the result locally with MkDocs.

### Prerequisites

Install MkDocs Material (which bundles MkDocs itself) in your Python environment:

```bash
pip install mkdocs-material
```

### Live preview

Serve the documentation locally and open <http://127.0.0.1:8000>:

```bash
mkdocs serve
```

### Static build

Create the production-ready static files in the `site/` directory:

```bash
mkdocs build --strict
```

## Deployment

### GitHub Pages (recommended)

1. In **Settings → Pages → Build and deployment**, choose **GitHub Actions**.
2. Push to the `main` branch. The GitHub Actions workflow builds the MkDocs Material site, uploads it as a Pages artifact, and deploys it with `actions/deploy-pages`.
3. Your site will be available at `https://<username>.github.io/interviews-roadmap/` after the workflow completes.

### Manual publishing

If you prefer to publish the static files yourself, run `mkdocs build --strict` and upload the generated `site/` directory to any static hosting provider.
