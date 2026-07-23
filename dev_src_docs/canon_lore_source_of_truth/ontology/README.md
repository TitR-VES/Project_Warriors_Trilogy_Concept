# Project Warriors Ontology Layer

This directory contains machine-friendly projections and correction overlays for
Project Warriors canon. It does not replace durable narrative source pages.

## Current delivery stack

The uploaded `pw_world_event_timeline_rev1.yaml` is not currently repository-landed,
so the ontology is represented through deterministic, auditable transformation layers:

1. `pw_world_event_timeline_rev2_1.patch.yaml`
   - applies to the external/uploaded rev1 timeline
   - produces validated rev2.1
   - carries macro chronology, Game 1 correction, Game 4 split, The Storm landing,
     RETREAT, HELL, and the post-Game-4 bridge
2. `pw_war_within_rev2_2.delta.yaml`
   - rev2.1 -> rev2.2
   - War Within partial ladder, Zale correction, VIATECH ’31, GROUND ZERO,
     Chicago ordering, and SUCKER PUNCH
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
   - War Within finale detail, Permanent Record handoffs, The Storm / VOICE IN THE DARK,
     DEAD BLOW, and EASTERN PROMISE
7. `pw_full_transcript_recovery_rev2_7a.delta.yaml` + `pw_full_transcript_recovery_rev2_7b.delta.yaml`
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
   - advances the named-weapon projection with NOISE FLOOR, SECOND HORIZON, and HARD STAND
   - records the DEAD RECKONING collision without creating a duplicate identity

The full materialized `pw_world_event_timeline_rev2_8.yaml` and projected
`named_weapon_builds_v3_3.txt` remain handoff artifacts until a full-projection
import is explicitly approved.

## Current validated projection

Timeline rev2.8:
- 7 eras
- 121 events
- 21 campaign tracks
- 19 synchronization points
- zero duplicate IDs
- zero dangling references
- zero self references
- acyclic chronology graph
- zero events without source pointers

Named-weapon layer:
- base registry: `named_weapon_builds_v2_8.txt`
- projected registry after cumulative deltas: `named_weapon_builds_v3_3.txt`
- 42 unique stable identities
- 33 substantially specified/source-associated identities
- 9 recovery-status identities
- zero duplicate stable IDs

## Recovery-pass governance

- Later owner-approved and later source-landed decisions supersede older transcript drafts.
- A transcript is evidence, not automatic authority.
- Exact duplicates are counted once for source recovery.
- Existing durable pages remain controlling when they already absorb the transcript.
- Revised source pages explicitly state what earlier page, ladder, title, or ambiguity they supersede.
- Working choices and open flags remain working/open after source promotion.
- No missing mission, date, platform, or character detail may be invented merely to complete a projection.

## Current campaign notes affected through rev2.8

- Game 1 campaign labels are source-landed as CRITTER SQUAD: LEAD THE WAY,
  DO RIGHT, FEAR NONE, and RIPTIDE RED.
- Who Dares Wins uses the revised working ladder BLACK START through FAR SHORE;
  the earlier April title ladder is superseded for current development.
- FAILSAFE inherits the already-resolved Game 2 Tremblay confrontation and does not
  reopen it as a Game 3 mystery.
- DARK SKIES keeps OUTER PORT as its Japan contact mission and uses FRACTURE MAP
  instead of the older ORDER OF WEATHER direction.
- BODYWORK and NARROW WATER are optional NO KINGS branches and do not renumber the
  controlling early main ladder.
- The Wasp remains a Game-2-overlap campaign with selective flashbacks.
- Bakhmut is locked after HARD WINTER and before PERMAFROST.
- HOME DEFENSE is Australian-led with Lucas Hill as the baseline working protagonist;
  exact title and Game 3 synchronization remain open.

## Schemas

- `schema/pw_world_event.schema.yaml` controls event/era/track/synchronization shape.
- `schema/pw_weapon_build.schema.yaml` controls named-weapon identity, placement,
  availability, recovery governance, and base-plus-delta authority.

## Governance rules

- Narrative source pages control story meaning; ontology files project that meaning.
- Relative chronology is preferred over invented exact dates.
- Exact dates require an explicit lock source.
- Stable IDs survive title changes unless an ID migration is separately authorized.
- Historical titles and aliases do not replace canonical names.
- Player branches must not be collapsed into one outcome without owner adjudication.
- Partial ladders remain partial; missing titles are not invented.
- Old revisions are not retired until the PR merges, paths are checked on `main`,
  downstream consumers migrate, and a post-merge consistency pass succeeds.
