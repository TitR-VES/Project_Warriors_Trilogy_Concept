# Project Warriors Ontology Layer

This directory contains machine-friendly projections and correction overlays for
Project Warriors canon. It is not a replacement for durable narrative source
pages in `dev_src_docs/`.

## Files

- `pw_world_event_timeline_rev2.patch.yaml` — deterministic correction overlay
  from the audited rev1 timeline to rev2.
- `schema/pw_world_event.schema.yaml` — structural and reference-integrity rules.
- `schema/pw_weapon_build.schema.yaml` — named-weapon entity schema rev2.

The fully materialized `pw_world_event_timeline_rev2.yaml` is generated from the
rev1 input plus the correction overlay. The audit records the generated graph
validation results and SHA-256.

## Authority

1. Locked correction/source pages in `dev_src_docs/`.
2. Dedicated current source pages.
3. Current human-readable registries, including the named-weapon registry.
4. Ontology projections and overlays.
5. Working compendia.
6. Archived, recovered, or intake copies.

The ontology is designed to make contradictions visible. It must never silently
invent missing canon to satisfy a field.

## Editing workflow

1. Land or correct the durable source page.
2. Update the human-readable registry when the domain uses one.
3. Update the ontology projection or correction overlay.
4. Validate YAML parsing, ID uniqueness, reference integrity, chronology cycles,
   status normalization, and source coverage.
5. Refresh the affected compendium and audit record.
6. Keep the superseded ontology revision for comparison until the replacement
   has merged and been spot-checked.

## Null and recovery rule

Use `null` plus an explicit `recovery_required` list when a value is not recovered.
Do not use plausible inference as a substitute for source recovery.

## Relative chronology rule

Prefer event anchors and broad windows over invented absolute dates. A relative
lock such as “roughly two years after Game 3” remains relative until an exact
calendar date is separately adjudicated.
