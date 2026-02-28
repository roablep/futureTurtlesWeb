# Repository Guidelines

## Project Structure & Module Organization
This repository is a static website (no app framework or package-based build pipeline).

- Root pages: `index.html`, `about.html`, `camp.html`, `members.html`, `contact.html`, `events-2023.html`
- Year archives: `2022/report.html`, `2023/report.html` with year-specific `images/` and `video/`
- Shared assets: `assets/css/`, `assets/js/`, `assets/sass/`, `assets/webfonts/`, `assets/svg/`
- Shared media: `images/`, `video/`

Edit `assets/sass/` for theme-level style changes and `assets/css/futureturtles.css` for project-specific overrides.

## Build, Test, and Development Commands
Use a static server for local development:

- `python3 -m http.server 5500` - serve site locally
- `npx serve .` - alternative static server
- `sass assets/sass/main.scss assets/css/main.css` - compile SCSS to CSS

Open `http://localhost:5500/index.html` after starting a server.

## Coding Style & Naming Conventions
- Use 2-space indentation in HTML, CSS, and JS to match existing files.
- Keep page layout consistent: `#header`, `#main`, `#footer` across root pages.
- Prefer lowercase, hyphenated file names for pages/assets (for example, `events-2023.html`).
- Minimize direct edits to minified vendor files in `assets/js/*.min.js` and `assets/css/fontawesome-all.min.css`.
- Keep custom camp styles in `assets/css/futureturtles.css` unless changing shared theme behavior.

## Testing Guidelines
There is no automated test suite in this repository. Validate changes manually:

- Smoke test all updated pages in desktop and mobile viewports
- Verify nav links, footer links, and Mailchimp form presence
- Confirm media loads correctly (`.webm`/`.mp4`, image paths, posters)
- After SCSS edits, recompile and verify `assets/css/main.css` updates cleanly

## Commit & Pull Request Guidelines
Recent history favors short, imperative commit messages (for example, `fix broken links`, `update 2024 fees`).

- Keep commits focused and scoped to one change type
- Use present-tense, action-first subjects
- PRs should include: summary, affected pages/assets, screenshots for UI/content changes, and linked issue (if applicable)
- Call out any path or URL migrations explicitly to simplify review

## Content & Media Tips
- Prefer optimized `.webp` images when adding new photos.
- For video backgrounds, include compatible formats and poster images.
- Keep year-specific media inside that year folder to avoid cross-directory path issues.
