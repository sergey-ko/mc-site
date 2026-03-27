# Mission Control Landing Page

## What is this

Single-page marketing landing page for Mission Control — the SDLC control plane that orchestrates fleets of AI coding agents to produce auditable, policy-governed pull requests at scale.

## Tech stack

- **Astro** (static output) — framework
- **Tailwind CSS v4** — styling via `@astrojs/tailwind`
- **@fce/shared** — shared design system (tokens, components, layouts) from `github:sergey-ko/fce-website-shared`
- **GitHub Pages** — hosting via GitHub Actions

## Project structure

```
src/
  components/
    DogfoodDemo.astro    # Terminal demo showing MC building itself
    HowItWorks.astro     # 4-step workflow explanation
  pages/
    index.astro          # Single landing page (all sections)
  styles/
    theme.css            # Blue accent overrides on shared tokens
public/
  favicon.svg
.github/workflows/
  deploy.yml             # GitHub Pages deploy on push to main
```

## Design

- Dark theme, blue accent (#3B82F6)
- Fonts: Inter (body) + JetBrains Mono (code/monospace)
- Shared tokens from `@fce/shared/styles/tokens.css`
- Custom components only where shared ones don't fit (DogfoodDemo, HowItWorks)

## Dev commands

```bash
npm run dev       # Start dev server (localhost:4321)
npm run build     # Build static site to dist/
npm run preview   # Preview built site locally
```

## Deployment

Automatic via GitHub Actions on push to `main`. Deploys to GitHub Pages.

## Content source

All copy comes from `c:\Projects\FaW\products\mission-control\website-spec.md`.
