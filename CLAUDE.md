# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static portfolio website for Bruna Pimenta, a UGC (User Generated Content) creator. The site is a single HTML file (`index.html`) with no build process.

## Development

Since this is a pure static site, there is no development server or build step:
- Open `index.html` directly in a browser to preview
- Or serve locally: `npx serve .` or `python -m http.server`

## Architecture

- **`index.html`**: The complete portfolio site (homepage)
- **`stitch_ugc_esposa_do_zero/`**: Reference design source containing `DESIGN.md` (design system documentation) and `code.html` (original template)
- **`.vercel/`**: Vercel deployment configuration
- **`.agents/skills/deploy-to-vercel/`**: Automated deployment skill

## Tech Stack

- Tailwind CSS via CDN (with custom color palette)
- Google Fonts: Noto Serif (editorial headlines) + Manrope (body text)
- Material Symbols Outlined icon library
- No JavaScript framework

## Design System (from DESIGN.md)

Key principles when modifying this site:

- **No 1px borders for sectioning** — use background color shifts instead (tonal layering)
- **No pure black** — use `#39382c` ("ink" color) for text
- **No hard shadows** — use ambient shadows with 40-60px blur, 4-6% opacity, tinted with on-surface color
- **Typography hierarchy**: Noto Serif for display/headlines, Manrope for body/labels
- **Display text**: -0.02em tracking; Labels: +0.05em tracking
- **Tonal surface levels**: background → surface_container_low → surface_container → surface_container_highest

## Deployment

Deployed on Vercel. To redeploy, use the deploy-to-vercel skill or push to the git remote.