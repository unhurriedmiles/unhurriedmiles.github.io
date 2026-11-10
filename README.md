# Unhurried Miles — migration notes

Standalone Jekyll user site for `https://unhurriedmiles.github.io/`.

## Site setup

- `_config.yml` sets `url: https://unhurriedmiles.github.io` and an empty `baseurl`.
- `_layouts/default.html` and `assets/css/site.css` provide a self-contained layout and styling.
- `index.html` is the personal homepage; `travel/index.html` is the journal; `travel/august-2026.md` is the monthly entry.
- Navigation and internal links stay within this site. The only external link included is the sitter's TrustedHousesitters profile, using its clean profile URL.
- The generated `_site` directory was not copied.

## Source inventory reviewed

Source `dev` branch of `Abster101/Abster101.github.io`:

- `travel/index.html`: travel journal, slow living, June 2026 monthly recap, Croatia highlights, destinations, featured entries, and a sitter section plus request form.
- `travel/august-2026.html`: August 2026 recap about Quebec, Maine, outdoor activities, routines, and reflections.
- `index.html`: professional homepage's Travel and House & Pet Sitting sections.
- `_layouts/default.html`: Travel navigation item.
- `about/index.md`: house- and pet-sitting mention in the Contact section.
- `css/main.css`: travel, journal, pet-sitting, and form styling mixed with professional-site styles.
- `images/travel/`: `Croatia1.jpg`, `Croatia2.jpg`, `Croatia_nature1.jpg`, `Croatia_nature2.jpg`, and `kenzie1.png`.
- Other referenced art: `images/spain-mountains.svg` and `images/IMG_5935.CR2.jpg` (the latter's source is under `images/originals/`).

## Items requiring review before being added

- The source publishes the personal email `abiola.ace1@gmail.com`; the house-sitting form posts to `https://formsubmit.co/abiola.ace1@gmail.com`. Neither the address nor a working form endpoint is included in this migration. Confirm the desired contact address and endpoint before adding a form or email link.
- The TrustedHousesitters profile link is retained without source-account, employer, or tracking links. Confirm that the profile should remain public.
- The source journal includes planned destinations and personal itinerary context; review it for time-sensitive details before adding further entries.

## Migration limitations and validation

The GitHub file-reading interface did not provide the full original contents of some long HTML paragraphs, and binary image files cannot be committed through the available text-file migration interface. The destination therefore has a standalone rebuild of the journal's visible structure and writing, but its source travel photographs and Kenzie portrait still need to be copied as binary assets before image-based designs can be restored. Some long August recap prose is adapted from the source excerpts available during migration rather than copied verbatim; compare it with the original before treating it as an archival transcription.

Static review: front matter, Jekyll layout references, `relative_url` local links, and configured user-site URL/baseurl were checked. A local `jekyll build` could not be run in this GitHub-only environment. No source files were changed, deleted, committed, or pushed.

## Professional-site cleanup after you verify the migration

Once the new site is reviewed and published, consider removing from the professional source site:

- Travel and House & Pet Sitting sections from its `index.html` (on the `dev` branch).
- The Travel navigation item from `_layouts/default.html`.
- The house/pet-sitting line from `about/index.md`.
- Travel, journal, pet-sitting, and form CSS from `css/main.css`, after checking for shared styling.
- Travel-only images under `images/travel/` after verifying they're not used by professional content.

Do not remove the professional homepage, CV, or unrelated shared assets as part of this cleanup.
