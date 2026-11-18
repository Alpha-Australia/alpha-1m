# Alpha 1 Million

A lightweight WordPress theme for the Alpha Australia One Million site (`onemillion.alpha.org.au`), built by Beech Agency.

## Overview

`Alpha 1 Million` is a custom theme based on the Underscores starter theme and extended with ACF flexible content support. It is designed to provide a clean, modular base for building content-driven pages with custom sections, responsive layout components, and editable ACF blocks.

## Key features

- Custom, theme-specific templates for page content and posts
- Flexible section-based page building using ACF JSON definitions
- Organized template parts in `template-parts/` for reusable layout components
- Asset pipeline with SCSS source files under `assets/scss/` and compiled CSS in `assets/css/`
- Custom navigation and responsive menu support
- Support for custom logos, featured images, threaded comments, and translation-ready strings
- Minimal starter styles so the theme is easy to extend and customize

## Project structure

- `style.css` — theme metadata, base CSS, and information for WordPress
- `functions.php` — theme setup, script and style registration, and theme support features
- `header.php`, `footer.php`, `index.php`, `page.php`, `single.php`, `search.php`, `404.php` — main theme templates
- `inc/` — reusable PHP utilities, template helpers, custom query logic, and theme support functions
- `template-parts/` — modular content sections and UI components used by theme templates
- `assets/scss/` — source stylesheets organized into partials, sections, components, and vendor code
- `assets/js/` — theme JavaScript, including core behavior and admin helpers
- `acf-json/` — saved ACF field groups for ACF JSON syncing and local development

## Development notes

- Theme version, minimum PHP and tested WordPress version live in the `style.css` header (currently PHP `8.1`+, tested up to WordPress `6.9`).
- Text domain: `bfc`
- Third-party JS is vendored in `assets/js/vendor/` and pinned by version in the file name (e.g. Locomotive Scroll `5.1.1`). Don't load libraries from a CDN dist-tag such as `@beta` or `@latest`: tags move or get removed and the site breaks without any code change.
- Fonts are `.woff2` in `assets/fonts/`. Only add the weights the CSS actually uses.

## Releasing

Sites update through `inc/updater.php`, which checks the latest GitHub release of `Alpha-Australia/alpha-1m`.

1. Bump `Version` in `style.css`.
2. Push a tag matching that version (e.g. `1.1.1`). The `Package WordPress Theme` workflow zips the theme and attaches `alpha-1m.zip` to a release.

## Customization

Update the theme metadata in `style.css` and adjust the file and template content to match your project branding.

Use the `assets/scss/` source files to extend or override styling, then compile to `assets/css/styles.css` as needed.

## License

This theme is released under the GNU General Public License v2 or later.
