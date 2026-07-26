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
- Organize main-installment story material as `story_campaigns/GameN/<PlayableCharacter>/`, with `Shared/` reserved for installment-wide or genuinely multi-character material.
- Organize all DLC story material as `story_campaigns/DLC/<DLC>/<PlayableCharacter>/`, again using `Shared/` only for campaign-wide or multi-character material.
- Every playable character listed by the narrative ontology must have a named source directory in every campaign where that character is playable, even when a dedicated source page has not yet landed.
- Keep global, cross-game character profiles in `characters/`; do not duplicate them into every campaign directory unless a campaign-specific profile or scene treatment exists.
- Put cross-cutting worldbuilding under `diegetics_and_world-building/`.
- Put mechanics and systems under `gameplay_mechanics/`.
- Keep templates in `templates/`.
- If a new file does not yet have a clear durable home, stage it first in `new_src_material/` or `incoming_patches_and_updates/` instead of parking it here prematurely.
- Never delete a source merely because it resembles another file. Remove only a proven duplicate; retain and mark uncertain matches as possible duplicates.

## Working Rule

When an incoming package produces a stable source page, promote the stable page here and then update the appropriate compendium. When source paths move, preserve a redirect or migration record so ontology and governance references can be reconciled without losing provenance.
