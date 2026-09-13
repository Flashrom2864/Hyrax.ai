# Hyrax.ai

A GitHub Pages-ready landing page and command-center demo.

## What is included
- `index.html` — landing page + dashboard + built-in WebGL GLB viewer
- `assets/hyrax.glb` — real bundled 3D hyrax model
- `data/status.json` — dashboard data
- `.github/workflows/pages.yml` — GitHub Pages deployment workflow
- `.nojekyll` — tells GitHub Pages to serve the files directly

## Important detail
The 3D viewer does **not** use Three.js, model-viewer, or any other external JavaScript library.
The page fetches the bundled `assets/hyrax.glb` and renders it with WebGL2.

## Publish on GitHub Pages
1. Create a new GitHub repository, for example `hyrax-ai`.
2. Put these files in the repository root.
3. Push to the `main` branch.
4. In GitHub: **Settings → Pages → Build and deployment → Source → GitHub Actions**.
5. Open the Actions tab and let `Deploy Hyrax.ai to GitHub Pages` finish.

Your URL will look like:
`https://YOUR_GITHUB_USERNAME.github.io/hyrax-ai/`

## Update the dashboard
Edit `data/status.json`. The site reads that file at runtime.

## Later upgrades
- Replace `assets/hyrax.glb` with a better rigged/animated model.
- Generate `data/status.json` automatically from GitHub Actions.
- Add build/test badges and artifact links.
- Add a custom domain such as `hyrax.ai`.
