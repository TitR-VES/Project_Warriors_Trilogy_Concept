# dev_src_docs

This is the primary authoring layer for the repository.

Use this directory for stable source pages that should be treated as the current
working version of project material. If a document is meant to be edited,
cross-referenced, and kept alive, it usually belongs here.

## What Belongs Here

- canon overview material
- campaign and mission source pages
- gameplay-mechanics references
- diegetic worldbuilding documents
- audio, visual-identity, and other craft-domain source pages
- templates used to produce new durable project documents

## What Does Not Belong Here

- raw package drops that still need review
- archive zip bundles
- disposable scratch notes
- recovered legacy extracts kept only for verification

## Placement Rules

- Put campaign-specific material under `story_campaigns/`.
- Put cross-cutting worldbuilding under
  `diegetics_and_world-building/`.
- Put mechanics and systems under `gameplay_mechanics/`.
- Keep templates in `templates/`.
- If a new file does not yet have a clear durable home, stage it first in
  `new_src_material/` or `incoming_patches_and_updates/` instead of parking it
  here prematurely.

## Working Rule

When an incoming package produces a stable source page, promote the stable page
here and then update the appropriate compendium.
