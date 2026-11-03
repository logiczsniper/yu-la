<img src="./src/assets/title-ja.webp" style="background-color:white;border-radius:12px" />

<br />

A bilingual website for Yu-La Salon, built with 🚀 Astro. The site provides salon
information in English and Japanese, including services and prices, location,
contact details, and a language-selection page.

## Requirements

- Node.js `>=22.23.4`
- npm

## Getting started

From the `ui` directory, install dependencies and start the development server:

```sh
npm ci
npm run dev
```

Astro prints the local development URL in the terminal.

## Commands

Run these commands from the `ui` directory:

| Command | Description |
| --- | --- |
| `npm run dev` | Start the local Astro development server. |
| `npm run build` | Build the site into `dist/`. |
| `npm run preview` | Preview the production build locally. Run `npm run build` first. |
| `npm run astro -- <command>` | Run an Astro CLI command, such as `npm run astro -- check`. |

## Pages and languages

- `/` redirects to the default language.
- `/en/` and `/ja/` are the English and Japanese home pages.
- Each language has `about`, `contact`, `location`, and `price` pages.
- The default language is English. Astro's i18n routing prefixes both
  languages and redirects to the default locale.

## Project structure

```text
src/
  assets/       Images used by the pages
  components/   Shared welcome, language selection, navigation, and reviews
  icons/        SVG icons used by astro-icon
  layouts/
    en/         English page shell and content navigation
    ja/         Japanese page shell and content navigation
  pages/
    en/         English routes
    ja/         Japanese routes
    index.astro Default-locale redirect
public/         Static files served from the site root
```

Page files in `src/pages/` define the routes. English and Japanese pages use
separate layouts to provide localized navigation, document language, and footer
content. Shared interface elements live in `src/components/`.
