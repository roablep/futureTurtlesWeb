# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static HTML website for **Future Turtles**, a gay Burning Man theme camp. No build system, no package manager — raw HTML/CSS/JS files served directly.

## Local Development

The site is designed to be previewed with [VS Code Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) at `http://localhost:5500/index.html`. Any static file server works (e.g., `python3 -m http.server 5500`).

## CSS / SASS

Styles are compiled from SASS source in `assets/sass/` to `assets/css/main.css`. The entry point is `assets/sass/main.scss`, which imports libs → base → components → layout in that order.

To recompile CSS after editing SASS files:
```
sass assets/sass/main.scss assets/css/main.css
```

Custom site-specific styles (not from the Polymorph template) live in `assets/css/futureturtles.css`, which is loaded separately in pages that need it (e.g., image carousels using the Swiper web component).

## Site Structure

- **Root pages**: `index.html` (home/splash), `about.html`, `camp.html` (join the camp), `members.html`, `contact.html`
- **Archived year reports**: `2022/report.html`, `2023/report.html` — each year directory has its own `images/` and `video/` subdirectories
- **Template reference pages**: `elements.html`, `generic.html` — Pixelarity template demo pages, not linked in nav

## Page Conventions

Every page follows the same structure:
1. `<header id="header">` — logo + nav (identical across all root pages)
2. `<div id="main">` — content area
3. `<footer id="footer">` — social links (Instagram, Discord) + Mailchimp newsletter signup form
4. Script tags at bottom loading jQuery, dropotron, browser, breakpoints, util, and main JS

The nav links use absolute paths (`/about.html`, `/camp.html`, etc.) so the site must be served from root.

## Media

Videos are provided in three formats for broad browser compatibility: `.webm`, `.vp8.webm` (VP8 codec fallback), and `.mp4`. Each video element has a poster image (`.jpg`) for the initial frame. Videos autoplay muted and loop.

## External Integrations

- **Mailchimp**: Newsletter signup form embedded in the footer of most pages
- **Discord**: `https://discord.com/invite/rpqSEVWy2Y`
- **Instagram**: `https://instagram.com/futureturtles`
- **Google Fonts**: Source Sans Pro (loaded in main.scss)
