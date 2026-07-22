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

3. `pw_blommaert_game3_rev2_3.delta.yaml`
   - applies to materialized rev2.2
   - produces the validated rev2.3 projection
   - locks the three Game 3 campaign titles as NO KINGS / FAILSAFE / DARK SKIES
   - replaces the provisional Boston track with NO KINGS / Romeo
   - adds FAILSAFE as the missing Ducky Game 3 track
   - promotes DARK SKIES from candidate to locked title
   - adds the Infrastructure Day / Blommaert optional-branch event
   - adds DUE DILIGENCE to the projected named-weapon registry
   - records JUDGE ME NOT as a conditional achievement-layer record

The full materialized `pw_world_event_timeline_rev2_3.yaml` is maintained as a handoff
artifact until the repository receives either the original rev1 input or an explicitly
approved full-projection import.

## Current validated projection

Timeline rev2.3:
- 7 eras
- 58 events
- 21 campaign tracks
- 15 synchronization points
- zero duplicate IDs
- zero dangling references
- acyclic chronology graph
- zero events without source pointers

Named-weapon layer:
- base registry: `named_weapon_builds_v2_8.txt`
- War Within delta projection: `named_weapon_builds_v2_9.txt`
- Blommaert delta projection: `named_weapon_builds_v3_0.txt`
- 37 unique stable identities
- 27 substantially specified/source-associated identities
- 10 recovery-status identities

## Current Game 3 title governance

- Romeo: `PW-TRK-G3-NO-KINGS` — NO KINGS
- Ducky: `PW-TRK-G3-FAILSAFE` — FAILSAFE
- Spook: `PW-TRK-G3-DARK-SKIES` — DARK SKIES

Campaign titles are locked even where exact opening events, dates, or individual scene
and mission implementation details remain working.

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
- A campaign title can be locked while its dates or mission implementation remain open.
- Player-branch options must not be collapsed into one canonical outcome without an
  explicit later adjudication.
- Partial ladders must remain partial: do not invent missing mission titles or numbering.
- Registry deltas supersede base fields only for explicitly matched stable IDs.
- Old revisions should not be retired until the PR is merged, source paths are checked
  on `main`, downstream consumers migrate, and at least one consistency pass succeeds.
