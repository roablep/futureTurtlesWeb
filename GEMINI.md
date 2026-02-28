# Future Turtles Web Project

## Project Overview
This repository contains the static website for **Future Turtles**, a Burning Man theme camp. The site serves as a historical record of the camp's activities (via yearly "AfterBurner" reports), provides information for current and prospective members, and manages community engagement through newsletter signups and social media links.

The project is built using a modified version of the **Polymorph** theme by [Pixelarity](https://pixelarity.com).

## Tech Stack
- **HTML5/CSS3**: Core structure and styling.
- **Sass (SCSS)**: Source files for CSS located in `assets/sass/`.
- **JavaScript (jQuery)**: Used for UI components like navigation panels and dropdowns.
- **Swiper.js**: Used for image galleries in reports (loaded via CDN).
- **Mailchimp**: Integrated for newsletter subscriptions.
- **Responsive Design**: Uses `breakpoints.js` and custom Sass mixins for various device sizes.

## Directory Structure
- `/` (Root): Main entry points like `index.html`, `about.html`, `camp.html`, `members.html`, and `contact.html`.
- `/2022/`, `/2023/`: Yearly directories containing historical reports (`report.html`) along with their specific media assets.
- `/assets/`:
  - `css/`: Compiled CSS files. `main.css` is the theme core; `futureturtles.css` contains project-specific overrides (e.g., Swiper configuration).
  - `js/`: Theme-related JavaScript files and `main.js` for initialization.
  - `sass/`: SCSS source files for the theme.
  - `webfonts/`: Font Awesome and other web fonts.
- `/images/`: Shared image assets for the main pages.
- `/video/`: Shared video assets for the main pages.

## Development & Maintenance

### Building and Running
As this is a static website, there is no specialized build command required to run it locally. You can serve it using any local web server (e.g., `npx serve`, `python -m http.server`, or Live Server in VS Code).

**TODO:** Identify or set up a build script for Sass compilation.
Currently, styles are compiled from `assets/sass/` to `assets/css/`. If changes are made to `.scss` files, they must be manually recompiled using a Sass compiler or a VS Code extension like "Live Sass Compiler".

### Development Conventions
- **New Reports**: When creating a new yearly report, create a new directory (e.g., `2024/`), copy a previous `report.html` as a template, and store related images and videos within that directory.
- **Media Optimization**: 
  - Prefer **WebP** for images to maintain high quality with low file sizes.
  - Prefer **WebM** (with MP4 fallback) for background videos to ensure broad compatibility and performance.
- **Custom Styling**: Add camp-specific style overrides to `assets/css/futureturtles.css` rather than modifying the core theme files in `assets/sass/` unless fundamental theme changes are required.
- **Interactive Elements**: The theme uses `dropotron` for navigation and `panel` for mobile menus. Refer to `elements.html` for examples of available UI components provided by the theme.

## Licensing
The content of this website is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](http://creativecommons.org/licenses/by-nc/4.0/).
The theme is licensed from [Pixelarity](https://pixelarity.com/license).
