# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```sh
npm run dev      # Start dev server at localhost:4321
npm run build    # Build for production to ./dist/
npm run preview  # Preview production build locally
```

## Architecture

Single-page portfolio site built with Astro 5 (static output).

**Structure:**
- `src/pages/index.astro` - Main page with hero and projects sections
- `src/layouts/Layout.astro` - Base HTML layout with global styles
- `public/` - Static assets (favicon)

**Styling:** Scoped CSS in `.astro` files + CSS variables in Layout for theming.

**Deployment:** GitHub Actions (`.github/workflows/deploy.yml`) auto-deploys to GitHub Pages on push to `main`. Site URL: `https://viktoriukhlin.github.io/PersonalWebSite/`

## Key Configuration

- `astro.config.mjs` - Sets `site` and `base` for GitHub Pages subpath
- Use `import.meta.env.BASE_URL` for asset paths in templates
