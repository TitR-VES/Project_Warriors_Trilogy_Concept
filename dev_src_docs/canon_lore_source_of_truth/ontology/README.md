# Project Warriors Ontology Layer

This directory contains machine-friendly projections and correction overlays for
Project Warriors canon. It does not replace durable narrative source pages.

## Current delivery stack

The uploaded `pw_world_event_timeline_rev1.yaml` is not currently repository-landed,
so the timeline ontology is represented through deterministic, auditable
transformation layers:

1. `pw_world_event_timeline_rev2_1.patch.yaml`
   - applies to the external/uploaded rev1 timeline
   - produces validated rev2.1
   - carries macro chronology, Game 1 correction, Game 4 split, The Storm landing,
     RETREAT, HELL, and the post-Game-4 bridge
2. `pw_war_within_rev2_2.delta.yaml`
   - rev2.1 -> rev2.2
   - War Within / American Guerrilla partial ladder, Zale correction,
     VIATECH ’31, GROUND ZERO, Chicago ordering, and SUCKER PUNCH
3. `pw_blommaert_game3_rev2_3.delta.yaml`
   - rev2.2 -> rev2.3
   - locks NO KINGS / FAILSAFE / DARK SKIES and adds Blommaert,
     DUE DILIGENCE, and JUDGE ME NOT
4. `pw_no_kings_bridge_rev2_4.delta.yaml`
   - rev2.3 -> rev2.4
   - Kentucky-to-Boston bridge and NO KINGS early Act I through THE POCKET
5. `pw_permanent_record_rev2_5.delta.yaml`
   - rev2.4 -> rev2.5
   - Permanent Record chronology through ONE HEAD OF THE HYDRA
6. `pw_transcript_batch_rev2_6.delta.yaml`
   - rev2.5 -> rev2.6
   - American Guerrilla finale detail, Permanent Record handoffs,
     The Storm / VOICE IN THE DARK, DEAD BLOW, and EASTERN PROMISE
7. `pw_full_transcript_recovery_rev2_7a.delta.yaml` +
   `pw_full_transcript_recovery_rev2_7b.delta.yaml`
   - rev2.6 -> rev2.7a -> rev2.7
   - anchors the Game 1 campaign spines and recovered campaign/weapon material
8. `pw_supplemental_transcripts_rev2_8.delta.yaml`
   - rev2.7 -> rev2.8
   - expands Bakhmut and HOME DEFENSE and adds its named equipment set
9. `pw_true_blue_registry_v3_4.delta.yaml`
   - leaves timeline rev2.8 unchanged
   - resolves Lucas Hill's TRUE BLUE identity
10. `pw_war_within_title_hierarchy_rev2_9.delta.yaml`
    - rev2.8 -> rev2.9
    - War Within is the DLC title; American Guerrilla is its campaign
11. `pw_narrative_structure_timeline_rev2_10.delta.yaml`
    - rev2.9 -> rev2.10; no chronology or registry change
    - links repository-verifiable campaign tracks to stable campaign identities

The full materialized `pw_world_event_timeline_rev2_10.yaml` and projected
`named_weapon_builds_v3_4.txt` remain handoff artifacts until a full-projection
import is explicitly approved.

## Narrative structure projection

`pw_narrative_structure_rev1.yaml` is the independently valid bundle manifest.

Current validated structure:

- 1 series
- 13 installments
- 21 campaigns
- 18 resolved timeline-track bindings
- 3 recovery-required timeline-track bindings
- 7 controlled cross-story touchpoint types

Bundle parts:

- `pw_narrative_structure_installments_rev1.yaml`
- `pw_narrative_structure_campaigns_main_rev1.yaml`
- `pw_narrative_structure_campaigns_extended_rev1.yaml`
- `pw_narrative_structure_bindings_rev1.yaml`

The deferred timeline bindings remain Godkiller, Sea Spear, and Semper Fi.
Do not infer replacement track IDs from naming convention.

## Weapon catalog projection

`pw_weapon_catalog_rev1.yaml` is the independently valid base-weapon and
ammunition bundle manifest. It is additive to the named-build registry.

Current catalog:

- 111 portable weapon/platform identities
- 35 ammunition identities
- 128 source-backed occurrence/access records
- 43 named-build crosswalk entries
- 34 resolved named-build-to-platform bindings
- 9 platform-recovery-required named-build bindings

Bundle parts are segmented for additive maintenance:

- `pw_weapon_catalog_platforms_firearms_1_rev1.yaml` through
  `pw_weapon_catalog_platforms_firearms_4_rev1.yaml`
- `pw_weapon_catalog_platforms_support_melee_rev1.yaml`
- `pw_weapon_catalog_ammunition_1_rev1.yaml` and
  `pw_weapon_catalog_ammunition_2_rev1.yaml`
- Game 1 occurrence segments for Romeo, Ducky/Spook, and shared faction pools
- later-main-game occurrence segments 1–2
- extended-installment occurrence segments 1–2
- named-build binding segments 1–2

The bundle manifest contains the exact part paths and a compact source-alias index.

The weapon catalog separates:

- base platform identity
- ammunition compatibility/economy
- story/game/campaign occurrence
- player access
- acquisition method
- retention state
- enemy or NPC drop policy
- named-build identity

An equipped weapon does not automatically become a player pickup. Records may
explicitly be `not_accessible`, `conditional`, `mission_only`, `temporary`,
or `collectible_only`.

Current open flags include:

- incomplete campaign roster passes
- exact Troy Barry reward/unlock table
- Dragon's Breath availability timing and supported fire-propagation levels
- enemy-type carry/drop matrices
- nine named identities whose base platforms remain unrecovered
- several prototype or roster-level caliber decisions

Future enemy-type ontology entries should reference stable `PW-WEP-*` and
`PW-AMM-*` identities and populate occurrence `enemy_type_refs` rather than
duplicating weapon strings.

## Current validated chronology projection

Timeline rev2.9 remains the last fully materialized chronology projection:

- 7 eras
- 121 events
- 21 campaign tracks
- 19 synchronization points
- zero duplicate IDs
- zero dangling references
- zero self references
- acyclic chronology graph
- zero events without source pointers

The rev2.10 compatibility delta changes no chronology counts or ordering edges.

## Named-weapon layer

- base registry: `named_weapon_builds_v2_8.txt`
- current correction/index layer: `named_weapon_builds_v2_9.txt`
- projected registry after cumulative deltas: `named_weapon_builds_v3_4.txt`
- 43 unique stable identities
- 34 substantially specified/source-associated identities
- 9 recovery-status identities
- zero duplicate stable IDs

Named-build sources remain authoritative for build names, ownership,
configuration, and placement. The weapon catalog binds those identities to a
shared base platform without replacing the registry.

## Schemas

- `schema/pw_world_event.schema.yaml`
  controls event, era, track, synchronization, campaign-reference, and
  touchpoint-classification shape.
- `schema/pw_narrative_structure.schema.yaml`
  controls series, installment, campaign, containment, and timeline bindings.
- `schema/pw_weapon_build.schema.yaml`
  controls named-weapon identity, placement, availability, configuration,
  recovery governance, and optional base-catalog links.
- `schema/pw_weapon_catalog.schema.yaml`
  controls base weapons, ammunition, occurrence/access records, and
  named-build crosswalks.

## Recovery-pass governance

- Later owner-approved and later source-landed decisions supersede older drafts.
- A transcript is evidence, not automatic authority.
- Existing durable pages remain controlling when they absorb the transcript.
- Working choices and open flags remain working/open after source promotion.
- Missing missions, dates, platforms, characters, weapon IDs, or ammunition
  mappings may not be invented merely to complete a projection.

## General governance rules

- Narrative source pages control story meaning; ontology files project that meaning.
- Relative chronology is preferred over invented exact dates.
- Exact dates require an explicit lock source.
- Stable IDs survive title changes unless an ID migration is separately authorized.
- Historical titles and aliases do not replace canonical names.
- Player branches must not be collapsed without owner adjudication.
- Partial ladders and incomplete weapon rosters remain partial.
- Release/numbered series order is not fictional chronology.
- Campaign membership is derived through stable campaign references.
- Base platform presence does not imply player access, persistence, or enemy drop.
- Old revisions are not retired until the PR merges, paths are checked on `main`,
  downstream consumers migrate, and a post-merge consistency pass succeeds.
