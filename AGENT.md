# Agent Instructions

## Project Overview

This repository is a static website for **BrainComp: Modeling and Understanding Human Brain Computation at Scale**, a **CCN 2026 satellite event** at the Zuckerman Mind Brain Behavior Institute, Columbia University, NYC.

There is no package manager, build system, framework, test runner, or server-side code in the repo.

Primary first-party files:

- `index.html`: active BrainComp homepage.
- `README.md`: project summary based on the current homepage content.
- `assets/css/style.css`: shared Squadfree-derived site CSS plus local layout and image rules.
- `assets/js/main.js`: shared Squadfree-derived JavaScript for navigation, scrolling, AOS, GLightbox, Isotope, Swiper, and PureCounter.
- `images/`: event images, favicons, placeholders, and other static assets.

Template files:

- `portfolio-details.html`: upstream Squadfree sample page. Do not treat as active production content.

Vendor files:

- `assets/vendor/` contains vendored Bootstrap, Bootstrap Icons, Boxicons, AOS, GLightbox, Isotope, Swiper, PureCounter, and php-email-form assets. Treat these as third-party dependencies; do not edit them for site-specific behavior unless the user explicitly asks.

## Active Homepage Content

The active `index.html` page currently has these sections and nav items:

- `#hero`: title, CCN 2026 satellite-event link, and Zuckerman/Columbia venue.
- `#intro`: About section on large-scale human brain encoding/decoding models and human brain foundation models.
- `#schedule`: Satellite Event Schedule placeholder.
- `#speaker`: placeholder speaker cards.
- `#organizer`: placeholder organizer cards.
- `#attend`: attendance information, expected participant count, venue, and registration steps.

The visible navbar is centered and currently links to Home, About, Schedule, Speakers, Organizers, and Attend. The homepage does not have a visible PVUW logo or `Previous PVUW` dropdown.

## Local Development

Because this is a static site, pages can be opened directly in a browser. A local HTTP server is useful for checking relative asset loading:

```sh
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/index.html
```

If port `8000` is occupied, use another port with `python3 -m http.server <port>`.

## Editing Guidelines

- Keep edits small and localized. Most content changes should be made in `index.html`; shared presentation changes belong in `assets/css/style.css`.
- Preserve the existing Bootstrap/Squadfree structure unless a requested change requires broader cleanup.
- The HTML contains many inline styles and commented-out legacy sections. Match the local style for narrow content updates instead of introducing a new styling system.
- Do not rewrite vendored files in `assets/vendor/` for first-party changes.
- Keep image references relative, e.g. `images/zuckerman.jpg` or `images/favicon/favicon-32x32.png`.
- Speaker and organizer cards currently use `images/portrait_placeholder.png`; replace with square or crop-friendly portraits when real people are added.
- Validate externally sourced dates, schedules, venue/room details, speaker names/affiliations, registration links, and conference links before changing public event information.
- Treat `index.html` as the only active site page unless the user adds another page explicitly.

## Validation Checklist

After content or style changes:

- Open `index.html` locally and check desktop and mobile widths.
- Confirm the header navigation scrolls to existing section IDs.
- Confirm image paths resolve, including `images/zuckerman.jpg`, `images/portrait_placeholder.png`, and favicon files under `images/favicon/`.
- Check browser console errors for missing assets or JavaScript exceptions.
- If changing shared CSS or `assets/js/main.js`, spot-check archived pages only if the shared change could affect them.

Optional static preview:

```sh
python3 -m http.server 8000
```

There is no configured automated test suite in this repo.

## Repository Notes

- `.gitignore` ignores `.DS_Store`, editor files, logs/temp files, dependency folders, and common build/cache outputs.
- Favicons are loaded from `images/favicon/`; browsers may cache them aggressively.
- `.DS_Store` files may already exist in the working tree; avoid adding more.
- The old `gitpush.sh` deployment script may be deleted or absent. If present in history, note that it force-pushed rewritten `main`; do not recreate or run that workflow unless explicitly requested.
