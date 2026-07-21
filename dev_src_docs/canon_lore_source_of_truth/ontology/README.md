# Project Warriors Ontology Layer

This directory contains machine-friendly projections and correction overlays for
Project Warriors canon. It does not replace durable narrative source pages.

## Current delivery stack

The uploaded `pw_world_event_timeline_rev1.yaml` is not currently repository-landed,
so the ontology is represented through deterministic, auditable transformation layers:

1. `pw_world_event_timeline_rev2_1.patch.yaml`
   - applies to the external/uploaded rev1 timeline
   - produces the validated rev2.1 base projection
   - contains the Game 1 campaign correction, ZERO HOUR retitle, macro chronology,
     Game 4 split, The Storm source landing, RETREAT, HELL, and post-Game-4 bridge

2. `pw_war_within_rev2_2.delta.yaml`
   - applies to materialized rev2.1
   - produces the validated rev2.2 projection
   - adds the recovered War Within partial ladder, Zale Jacobs correction, exact
     VIATECH ’31 anchor, GROUND ZERO / Chicago ordering, and SUCKER PUNCH resolution

The full materialized `pw_world_event_timeline_rev2_2.yaml` is maintained as a handoff
artifact until the repository receives either the original rev1 input or an explicitly
approved full-projection import.

## Current validated projection

Timeline rev2.2:
- 7 eras
- 57 events
- 20 campaign tracks
- 14 synchronization points
- zero duplicate IDs
- zero dangling references
- acyclic chronology graph
- zero events without source pointers

Named-weapon layer:
- base registry: `named_weapon_builds_v2_8.txt`
- War Within delta projection: `named_weapon_builds_v2_9.txt`
- 36 unique stable identities
- 26 substantially specified/source-associated identities
- 10 recovery-status identities

## Schemas

- `schema/pw_world_event.schema.yaml` controls event/era/track/synchronization shape.
- `schema/pw_weapon_build.schema.yaml` controls named-weapon identity, placement,
  availability, recovery governance, and base-plus-delta registry authority.

## Governance rules

- Narrative source pages control story meaning; ontology files project that meaning.
- Relative chronology is preferred over invented exact dates.
- Exact dates require an explicit lock source.
- Stable IDs survive title changes unless an ID migration is separately authorized.
- Historical titles and aliases do not replace canonical names.
- Partial ladders must remain partial: do not invent missing mission titles or numbering.
- Registry deltas supersede base fields only for explicitly matched stable IDs.
- Old revisions should not be retired until the PR is merged, source paths are checked
  on `main`, downstream consumers migrate, and at least one consistency pass succeeds.
