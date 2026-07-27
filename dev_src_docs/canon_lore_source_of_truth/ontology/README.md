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
   - War Within installment / American Guerrilla campaign partial ladder, Zale
     correction, VIATECH ’31, GROUND ZERO, Chicago ordering, and SUCKER PUNCH
3. `pw_blommaert_game3_rev2_3.delta.yaml`
   - rev2.2 -> rev2.3
   - locks NO KINGS / FAILSAFE / DARK SKIES, adds Blommaert, DUE DILIGENCE,
     and JUDGE ME NOT
4. `pw_no_kings_bridge_rev2_4.delta.yaml`
   - rev2.3 -> rev2.4
   - Kentucky-to-Boston bridge and NO KINGS early Act I through THE POCKET
5. `pw_permanent_record_rev2_5.delta.yaml`
   - rev2.4 -> rev2.5
   - Permanent Record chronology through ONE HEAD OF THE HYDRA
6. `pw_transcript_batch_rev2_6.delta.yaml`
   - rev2.5 -> rev2.6
   - American Guerrilla finale detail, Permanent Record handoffs, The Storm /
     VOICE IN THE DARK, DEAD BLOW, and EASTERN PROMISE
7. `pw_full_transcript_recovery_rev2_7a.delta.yaml` +
   `pw_full_transcript_recovery_rev2_7b.delta.yaml`
   - rev2.6 -> rev2.7a -> rev2.7
   - projects the 65-member / 59-unique extracted-thread recovery pass
   - anchors the three Game 1 campaign spines
   - adds the Coronado-to-Calloway bridge, Bakhmut and ASML mission packages
   - updates Who Dares Wins to its revised eight-rung ladder
   - adds The Wasp campaign arc, BODYWORK and NARROW WATER optional branches
   - maps the reconciled FAILSAFE and DARK SKIES openings/closures
   - adds The Collapse Missions 14–17 and the VIGILAN trust-chain arc
   - adds MOR HO! and LAST KNOWN GOOD to projected registry v3.2
8. `pw_supplemental_transcripts_rev2_8.delta.yaml`
   - rev2.7 -> rev2.8
   - expands Bakhmut into DEAD GROUND / DARK FIBER / ASH RELAY at its locked slot
   - lands the nine-mission HOME DEFENSE / Pine Gap working spine
   - advances the named-weapon projection with NOISE FLOOR, SECOND HORIZON,
     and HARD STAND
   - records the initial DEAD RECKONING collision without creating a duplicate identity
9. `pw_true_blue_registry_v3_4.delta.yaml`
   - leaves timeline rev2.8 unchanged
   - advances registry v3.3 -> v3.4
   - resolves Lucas Hill's placeholder as TRUE BLUE under
     PW-WPN-HILL-TRUE-BLUE
   - preserves Sakhalin's separate DEAD RECKONING stable identity
10. `pw_war_within_title_hierarchy_rev2_9.delta.yaml`
    - rev2.8 -> rev2.9; registry remains v3.4
    - corrects the title hierarchy without changing stable event or track IDs
    - PROJECT WARRIORS: WAR WITHIN is the installment / DLC title
    - PROJECT WARRIORS III: WAR WITHIN is the alternative numbered styling
    - AMERICAN GUERRILLA is the campaign title
11. `pw_narrative_structure_timeline_rev2_10.delta.yaml`
    - rev2.9 -> rev2.10; no chronology or registry change
    - links 18 repository-verifiable campaign tracks to stable `PW-CMP-*` identities
    - enriches selected synchronization points with campaign references and
      controlled touchpoint types
    - defers Godkiller, Sea Spear, and Semper Fi track bindings rather than guessing
      identifiers that are not present in the repository-landed auditable chain

The full materialized `pw_world_event_timeline_rev2_10.yaml` and projected
`named_weapon_builds_v3_4.txt` remain handoff artifacts until a full-projection
import is explicitly approved.

## Narrative structure projection

`pw_narrative_structure_rev1.yaml` is the independently valid bundle manifest. Its four entity parts contain:

- 1 series root
- 13 installments
- 21 campaigns
- 18 resolved timeline-track bindings
- 3 explicit recovery-required bindings
- 7 controlled cross-story touchpoint types

`schema/pw_narrative_structure.schema.yaml` controls identity, containment,
track-binding, status, source, bundle-part, and touchpoint-vocabulary rules.

Bundle parts:

- `pw_narrative_structure_installments_rev1.yaml`
- `pw_narrative_structure_campaigns_main_rev1.yaml`
- `pw_narrative_structure_campaigns_extended_rev1.yaml`
- `pw_narrative_structure_bindings_rev1.yaml`

The three deferred bindings are:

- Godkiller
- Project Warriors: Sea Spear
- Project Warriors: Semper Fi

Their campaigns and installments are present, but their timeline-track fields remain
null until authoritative stable IDs are recovered or explicitly source-locked.
Do not infer replacement IDs from naming convention or add tracks that may duplicate
the external base.

## Weapon catalog projection

`pw_weapon_catalog_rev1.yaml` is an independently valid, additive catalog of portable
base weapons, ammunition, occurrence/access records, and named-build platform bindings.
It does not replace the named-build registry.

Current catalog:

- 111 portable weapon/platform identities
- 35 ammunition identities
- 128 source-backed occurrence/access records
- 43 named-build bindings
- 34 resolved platform bindings
- 9 explicit platform-recovery-required bindings

The manifest lists 17 segmented entity parts: four firearm-platform segments, one
support/melee segment, two ammunition segments, eight occurrence segments, and two
named-build binding segments. It also contains a compact source-alias index resolving
every source token used by the entity parts to a durable repository path.

The occurrence model separates presence from player access, acquisition, retention,
and drop policy. A weapon may therefore occur as NPC or enemy equipment while remaining
`not_accessible`, `conditional`, `temporary`, `mission_only`, or `collectible_only`.

Open flags remain explicit for incomplete campaign rosters, Troy Barry's exact reward
table, Dragon's Breath timing and fire-propagation support, nine unrecovered named-build
platforms, prototype/caliber lanes, and unresolved enemy carry/drop probabilities.

Enemy mappings reference stable `PW-WEP-*` and `PW-AMM-*` values and populate occurrence
`enemy_type_refs` rather than duplicating platform strings.

## Enemy / weapon mapping projection

`pw_enemy_weapon_mapping_rev1.yaml` extends the merged portable-weapon catalog with
stable enemy-type, loadout, encounter, and compatibility-binding identities. It does
not replace narrative enemy descriptions or the weapon catalog.

Current mapping:

- 33 enemy-type identities (`PW-ENM-*`)
- 33 enemy-loadout identities (`PW-ELD-*`)
- 34 enemy-encounter identities (`PW-EEN-*`)
- 48 additive weapon-occurrence bindings
- 7 deferred campaign/opposition slots (`PW-EDF-*`)

The mapping covers the current source-backed Russian, FSB/Vympel, KPA, IRGC,
Los Sietes, KYSC, Atlas, War Wolves, and named/conditional enemy roster. Weapon
rules retain separate carry, drop, and player-pickup fields. A weapon carried by an
enemy is therefore not assumed to drop, remain usable, or become persistent.

Campaign opposition whose order of battle or arsenal is not source-landed remains
deferred rather than guessed. This currently includes generic Game 3 PLA opposition,
NAF/Vanguard hostile forces, Who Dares Wins, Sea Spear, Home Defense, The Storm,
and The Collapse.

`pw_weapon_catalog_enemy_type_bindings_rev1.overlay.yaml` only adds `PW-ENM-*`
references to existing `PW-WOC-*` records. It changes no weapon access, acquisition,
retention, ammunition, or drop state.

## Current validated projection

Timeline rev2.9 remains the last fully materialized and validated chronology projection:

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
Its independent narrative-structure validation target is:

- 1 series
- 13 installments
- 21 campaigns
- 18 resolved track bindings
- 3 deferred track bindings
- zero duplicate new IDs

Named-weapon layer:

- base registry: `named_weapon_builds_v2_8.txt`
- projected registry after cumulative deltas: `named_weapon_builds_v3_4.txt`
- 43 unique stable identities
- 34 substantially specified/source-associated identities
- 9 recovery-status identities
- zero duplicate stable IDs

## Recovery-pass governance

- Later owner-approved and later source-landed decisions supersede older transcript drafts.
- A transcript is evidence, not automatic authority.
- Exact duplicates are counted once for source recovery.
- Existing durable pages remain controlling when they already absorb the transcript.
- Revised source pages explicitly state what earlier page, ladder, title, or ambiguity they supersede.
- Working choices and open flags remain working/open after source promotion.
- No missing mission, date, platform, character detail, stable ontology ID, weapon ID, ammunition mapping, enemy type, or drop rule may be
  invented merely to complete a projection.

## Current campaign notes

- Game 1 campaign labels are LEAD THE WAY, DO RIGHT, FEAR NONE, and RIPTIDE RED.
- “Critter Squad” remains available as an in-world reference but is not part of Romeo's campaign title.
- Game 2 campaign labels are AMERICAN FREEDOM, PERSISTENT THREAT, and GODKILLER.
- Game 3 campaign labels are NO KINGS, FAILSAFE, and DARK SKIES.
- Game 4 contains COMMAND AUTHORITY, COMMON PICTURE, and PERMANENT RECORD.
- PROJECT WARRIORS: WAR WITHIN is an installment / DLC title; AMERICAN GUERRILLA
  is its campaign.
- Who Dares Wins uses the revised working ladder BLACK START through FAR SHORE.
- The Wasp remains a Game-2-overlap campaign with selective flashbacks.
- Bakhmut is locked after HARD WINTER and before PERMAFROST.
- HOME DEFENSE is Australian-led with Lucas Hill as the baseline working protagonist;
  exact title and Game 3 synchronization remain open.
- Lucas Hill's named build is TRUE BLUE; DEAD RECKONING remains Sakhalin's build.

## Schemas

- `schema/pw_world_event.schema.yaml` controls event/era/track/synchronization shape
  and, from rev2.10, campaign references and touchpoint classification.
- `schema/pw_weapon_build.schema.yaml` controls named-weapon identity, placement,
  availability, recovery governance, base-plus-delta authority, and optional base-catalog links.
- `schema/pw_narrative_structure.schema.yaml` controls series/installment/campaign
  identity, containment, timeline bindings, and touchpoint vocabulary.
- `schema/pw_weapon_catalog.schema.yaml` controls base-weapon identity, ammunition,
  occurrences, acquisition/retention/drop state, named-build platform bindings, and
  compatible `PW-ENM-*` references.
- `schema/pw_enemy_weapon_mapping.schema.yaml` controls enemy types, tactical tiers,
  loadout rules, encounter placement, deferred opposition slots, and weapon-catalog
  compatibility bindings.

## Governance rules

- Narrative source pages control story meaning; ontology files project that meaning.
- Relative chronology is preferred over invented exact dates.
- Exact dates require an explicit lock source.
- Stable IDs survive title changes unless an ID migration is separately authorized.
- Historical titles and aliases do not replace canonical names.
- Player branches must not be collapsed into one outcome without owner adjudication.
- Partial ladders remain partial; missing titles, incomplete weapon rosters, and undeveloped enemy orders of battle are not invented.
- Release/numbered series order is not fictional chronology.
- Installment membership is derived through `campaign_ref`, not the legacy free-text
  track `installment` field.
- Base-platform presence never automatically implies player access, retention, or enemy drop.
- Enemy carriage never automatically implies a drop, player pickup, or persistent ownership.
- Old revisions are not retired until the PR merges, paths are checked on `main`,
  downstream consumers migrate, and a post-merge consistency pass succeeds.
