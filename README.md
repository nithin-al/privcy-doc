# Privcy AI - API Documentation

Interactive Swagger UI for the Privcy AI BFF API, with Postman collections for manual testing.

## Live Docs (GitHub Pages)

Once GitHub Pages is enabled, the docs are published at:

**https://rayblaze-global.github.io/privcy-ai-api-docs/**

Pushes to `main` automatically redeploy the site via GitHub Actions.

### One-time GitHub setup

1. Open the repository on GitHub: [Rayblaze-Global/privcy-ai-api-docs](https://github.com/Rayblaze-Global/privcy-ai-api-docs)
2. Go to **Settings → Pages**
3. Under **Build and deployment**, set **Source** to **GitHub Actions**
4. Push these changes to `main` (or re-run the **Deploy API Docs to GitHub Pages** workflow from the Actions tab)

## Local Development

```bash
cd privcy-ai-api-docs
docker compose up --build -d
```

Open **http://localhost:<PORT_IN_ENV>** in your browser.

### Commands

| Action | Command |
|--------|---------|
| Start | `docker compose up -d` |
| Stop | `docker compose down` |

### Custom Port

Create a copy of `.env.example` as `.env` file:

```
SWAGGER_PORT=8888
```

## Repository Layout

| Path | Description |
|------|-------------|
| `swagger/privacy_api.yml` | OpenAPI 3.0 specification (source of truth) |
| `docs/index.html` | Static Swagger UI shell used by GitHub Pages |
| `postman/` | Postman collection and environment files |
| `.github/workflows/deploy-pages.yml` | GitHub Pages deployment workflow |

## Postman

Import the files in `postman/` into Postman to test the API against Dev or Staging environments.
