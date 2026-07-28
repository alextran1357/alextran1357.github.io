# Alex Tran Portfolio

Personal portfolio built with [Jekyll](https://jekyllrb.com/) and the
[al-folio](https://github.com/alshedivat/al-folio) theme.

## Local preview

Docker Desktop must be running. From the repository root:

```powershell
docker compose up
```

Open <http://localhost:8080/>. Changes to content files are rebuilt
automatically. Stop the preview with `Ctrl+C`.

## Deployment

Pushing site changes to `main` runs the deployment workflow. The generated
site is published to the `gh-pages` branch.

## Main content

- `_config.yml`: site identity, URLs, features, and theme settings
- `_pages/`: top-level pages and navigation
- `_posts/`: blog posts
- `_projects/`: portfolio projects
- `_data/cv.yml`: CV data
- `_data/socials.yml`: contact and social links
- `assets/`: portfolio images and downloadable documents

Detailed setup and customization guidance is available in [`docs/`](docs/README.md).
