# Coderaft Labs

**Software, AI & Automation**

A portfolio for practical software engineering, AI applications, and business automation. The site is being built as a home for finished projects and honest case studies.

## Project status

The portfolio foundation is in progress. The showcase ideas are marked as planned until each has a working implementation and a case study.

## Local development

Requirements: Node.js 20 or newer and npm.

```sh
npm install
npm run dev
```

Useful checks:

```sh
npm run lint
npm run format:check
npm run build
```

## Structure

- `src/` — page behavior, project data, and styles
- `public/` — static assets
- `.github/workflows/deploy.yml` — GitHub Pages build and deployment

Projects are maintained as data in `src/data/projects.js`. Each project has a status; planned work is never presented as completed work.

## Deployment

The repository includes a GitHub Pages workflow. In GitHub, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions**. Each push to `main` builds and deploys the site to the repository's Pages URL.

The Vite base path is configured for the `portfolio` project repository. If the repository name or hosting setup changes, update `base` in `vite.config.js`.

## Personal details

Update the contact links and biography in `src/main.js` when needed. Add a project only when its status and evidence are clear: source code, a demo, screenshots, and an accurate case study.
