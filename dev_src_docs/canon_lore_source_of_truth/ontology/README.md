# Project Warriors Ontology Layer

This directory contains machine-friendly projections and correction overlays for
Project Warriors canon. It does not replace durable narrative source pages.

## Files

- `pw_world_event_timeline_rev2_1.yaml` — fully materialized validated projection.
- `pw_world_event_timeline_rev2_1.patch.yaml` — deterministic rev1 -> rev2.1
  correction overlay.
- `schema/pw_world_event.schema.yaml` — structural/reference-integrity rules.
- `schema/pw_weapon_build.schema.yaml` — named-weapon entity schema rev3.

## Current validation

Timeline rev2.1:
- 7 eras
- 53 events
- 20 campaign tracks
- 13 synchronization points
- zero duplicate IDs
- zero dangling references
- acyclic ordering graph

Named-weapon layer:
- authoritative registry: `named_weapon_builds_v2_8.txt`
- 36 stable named identities
- zero duplicate stable IDs
- zero unmapped live status strings

## Authority

1. Locked correction/source pages in `dev_src_docs/`.
2. Dedicated current source pages.
3. Current human-readable registries.
4. Ontology projections and overlays.
5. Working compendia.
6. Archived/recovered/intake copies.

The ontology makes contradictions visible. It must never invent missing canon.

## Editing workflow

1. Land/correct the durable source.
2. Update the human-readable registry where applicable.
3. Update materialized ontology and deterministic patch.
4. Validate YAML, IDs, references, cycles, source coverage, and statuses.
5. Refresh compendium/audit.
6. Retain superseded revisions until merge and downstream migration are verified.

## Null and recovery rule

Use `null` plus explicit recovery metadata when a value is not recovered. Do not
substitute plausible inference for source recovery.

## Relative chronology rule

Prefer event anchors and broad windows over invented dates. “Approximately two
to three years after Game 4” remains relative until separately adjudicated.

## Title-collision rule

Do not hard-lock two active missions to the same title without owner adjudication.
The Storm opening mission currently conflicts with Spook Game 3's SOUTH CULVERT
and remains rename-required.

END
