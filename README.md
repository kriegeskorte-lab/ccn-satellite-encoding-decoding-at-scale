# BrainComp: Modeling and Understanding Human Brain Computation at Scale

This repository hosts the static website for **Modeling and Understanding Human Brain Computation at Scale**, a **CCN 2026 satellite event** at the Zuckerman Mind Brain Behavior Institute, Columbia University, NYC.

The event focuses on large-scale human brain encoding and decoding models, human brain foundation models, and how modern deep learning methods can support both theoretical neuroscience and practical applications.

## Website Content

The homepage currently includes:

- **Home**: event title, CCN 2026 satellite-event link, and venue.
- **About**: motivation for modeling human brain computation at scale using fMRI, EEG, MEG, intracranial recordings, and multimodal deep learning.
- **Satellite Event Schedule**: placeholder schedule area with local-time note.
- **Speakers**: placeholder speaker cards.
- **Organizers**: placeholder organizer cards.
- **Attend**: attendance information for CCN 2026 attendees, expected participant count, venue, and registration steps.

## Project Structure

- `index.html`: main homepage for the BrainComp satellite event.
- `assets/css/style.css`: shared styling based on the Squadfree Bootstrap template.
- `assets/js/main.js`: shared navigation, scrolling, animation, and plugin initialization.
- `assets/vendor/`: vendored frontend dependencies such as Bootstrap, AOS, GLightbox, Swiper, Isotope, and icons.
- `images/`: event images, favicons, placeholders, and other static assets.

Template pages still present:

- `portfolio-details.html`: upstream Squadfree sample page.

## Local Preview

This is a static site. You can preview it with:

```sh
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/index.html
```

No package installation or build step is required.

## Notes

- Favicons are loaded from `images/favicon/`.
- The site is based on the BootstrapMade Squadfree template.
- Speaker and organizer entries currently use placeholder names, affiliations, and portraits.
