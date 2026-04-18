# Project Warriors — Image Archive Handoff

Generated: 2026-04-18
Package status: **recovery / handoff package, not a complete image-binary archive**

## Important limitation

The current workspace does **not** expose the previously generated ChatGPT image binaries as files. A filesystem audit found only the current Project Warriors text/PDF migration sources in `/mnt/data`; no generated `.png`, `.jpg`, `.jpeg`, or `.webp` image files from earlier chats were available to package.

Because of that, this ZIP does **not** contain the actual preview images from prior project chats. It contains:

- a manifest of known/remembered visual assets from the visible project context
- a suggested repository folder structure
- a recovery checklist for manually saving the generated images from the ChatGPT UI
- empty image folders with `.gitkeep` files so the intended GitHub layout is easy to create

## Recommended next step

For each generated image visible in prior project chats, open the image in the ChatGPT UI, download/save it manually, and place it into the matching folder shown in `docs/SUGGESTED_REPO_LAYOUT.md`. Then update `manifests/generated_image_manifest.csv` from `missing_or_needs_manual_export` to `exported`.

## Why this package is still useful

It gives you a clean repository-facing structure and a checklist so the eventual image upload can be complete and reviewable by collaborators, without pretending that inaccessible image binaries were recovered.
