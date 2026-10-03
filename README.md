# Coderaft Labs

**Software, AI & Automation**

A portfolio for practical software engineering, AI applications, and business automation. The site is a home for finished projects and honest case studies.

## Project status

The portfolio foundation is live in the repository. Showcase ideas are marked as planned until each has a working implementation and a case study.

## Local development

Requirements: Node.js 20.19+ and npm.

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

- `src/main.js` — page structure and interactions
- `src/styles.css` — responsive design and themes
- `src/data/projects.js` — project showcase entries
- `public/` — static assets
- `.github/workflows/deploy.yml` — GitHub Pages build and deployment

Projects are data-driven. Each project has a status; planned work is never presented as completed work.

## Deployment

The repository includes a GitHub Pages workflow. In GitHub, set **Settings → Pages → Build and deployment → Source** to **GitHub Actions**. Each push to `main` builds and deploys the site to the repository's Pages URL.

Vite uses the `/portfolio/` base path for this project repository. Update `vite.config.js` if the repository name or hosting setup changes.

## Maintaining project entries

Edit `src/data/projects.js`. Keep project status accurate. Once a project is real, add its source repository, live demo, screenshots, and a short case study that covers the problem, architecture, key decisions, and limitations.
