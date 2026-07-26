# dev_src_docs

This is the primary authoring layer for the repository.

Use this directory for stable source pages that should be treated as the current working version of project material. If a document is meant to be edited, cross-referenced, and kept alive, it usually belongs here.

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
- Organize main-installment story material as `story_campaigns/GameN/Playable_Characters/<PlayableCharacter>/`, `story_campaigns/GameN/Named_NPCs/<PW-NPC-ID>__<PortableName>/`, or `story_campaigns/GameN/Shared/`.
- Organize DLC story material using the same three layers under `story_campaigns/DLC/<DLC>/`.
- Every playable character listed by the narrative ontology must have a named source directory in every campaign where that character is playable, even when a dedicated source page has not yet landed.
- Every source-backed named NPC appearance must have an ontology-bound source home in the relevant installment or DLC. The named-NPC ontology controls identity and story meaning.
- Keep a playable character in `Playable_Characters/` for installments where that character is playable. Do not duplicate the same source into `Named_NPCs/`.
- Keep global, cross-game character profiles in `characters/`; use the campaign tree for installment-specific profiles, scenes, mission presence, branch state, equipment continuity, voice, or presentation material.
- Keep team-wide and multi-character packets in the relevant `Shared/` directory rather than copying them into every character home.
- Put cross-cutting worldbuilding under `diegetics_and_world-building/`.
- Put mechanics and systems under `gameplay_mechanics/`.
- Keep templates in `templates/`.
- If a new file does not yet have a clear durable home, stage it first in `new_src_material/` or `incoming_patches_and_updates/` instead of parking it here prematurely.
- Never delete a source merely because it resembles another file. Remove only a proven duplicate; retain and mark uncertain matches as possible duplicates.

## Working Rule

When an incoming package produces a stable source page, promote the stable page here and then update the appropriate compendium. When source paths move, preserve a redirect or migration record so ontology and governance references can be reconciled without losing provenance.
