# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

The Promoter Blueprint is a single-page interactive website presenting a four-step promotional framework (Traffic → Holding Pattern → Selling Event → Outcomes). Originally based on promoter-blueprint.vercel.app by Jicecream/AJ&Smart, modified by C.W.

## Architecture

This is a purely static site — a single `index.html` file with all CSS and JavaScript inline. No build tools, frameworks, or dependencies.

- `index.html` — Entire site (HTML structure, `<style>` block, `<script>` block)
- `images/` — Static assets (floating head images for Jicecream/chaos mode)

## Key Features

- **AI Use-Case Mode toggle** — Checkbox at top toggles visibility of `.ai-use-case` and `.ai-section-insight` elements via the `toggleAI()` function. Adds `jicecream-mode` class to `<body>` for visual transformation.
- **Floating heads** — 10 `<img>` elements with CSS animations (chaos, spin, bounce, wobble) that appear only when `jicecream-mode` is active.
- **Column hover expand** — Columns scale to 1.15x on hover.
- **Toggle reset** — `DOMContentLoaded` listener forces the checkbox to unchecked state on page load.

## Development

Open `index.html` directly in a browser. No server or build step required.

```bash
# Open in default browser (Windows)
start index.html
```

## Deployment

Hosted on GitHub at C2cpwilson/promoter-blueprint. Can be deployed to any static host (Vercel, Netlify, GitHub Pages) with no configuration needed.

## Commented-Out Code

The ice cream cursor CSS (lines ~504-510) is commented out but preserved for potential re-enabling.
