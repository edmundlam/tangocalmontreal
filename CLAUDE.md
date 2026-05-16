# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A simple static website displaying a calendar of weekly tango events (milongas and practicas) in Montreal. The site is bilingual (English/French) and served via GitHub Pages from the `gh-pages` branch.

- Live site: https://tangocalmontreal.ca

## Structure

```
├── index.html          # English homepage with embedded Google Calendar
├── about.html          # English about/contact page
├── schools.html        # English tango schools page
├── css/
│   ├── bootstrap.min.css
│   └── tangocalmontreal.css  # Custom styles
├── js/
│   ├── jquery.js            # jQuery v3.7.1
│   ├── bootstrap.min.js
│   └── utils.js             # Single-line referrer redirect (legacy)
├── fonts/              # Bootstrap Glyphicons
└── fr/                 # French versions of all HTML pages
    ├── index.html
    ├── about.html
    └── schools.html
```

## Development

No build process, package manager, or tests. This is a pure static site.

- **Local development**: Open `index.html` directly in a browser, or use any static file server (e.g., `python -m http.server 8000`)
- **Deploying to GitHub Pages**: Push to `gh-pages` branch. The root serves as the site root.

## Content Updates

When updating content:
- Keep English (`/`) and French (`/fr/`) versions in sync
- Update the "Last update" date in both `index.html` files
- Google Calendar embed URLs contain multiple calendar source IDs and timezone settings — modify carefully if changing the embedded calendars

## Tech Stack

- Bootstrap 3.7.1
- jQuery 3.7.1
- Google Fonts (Alegreya Sans)
- Google Analytics (gtag.js)
- Google Calendar Embed
