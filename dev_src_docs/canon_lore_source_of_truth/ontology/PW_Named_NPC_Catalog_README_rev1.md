# Project Warriors Named NPC Ontology — rev1

This additive ontology catalogs source-backed named non-player characters and their
NPC-state appearances without replacing durable character profiles, campaign sources,
the named-weapon registry, or the enemy/weapon mapping.

## Inventory

- 88 stable `PW-NPC-*` named-character identities
- 116 `PW-NPA-*` appearance records
- 7 bindings to existing named `PW-ENM-*` enemy identities
- 30 named-weapon relationships
- 7 characters who are playable elsewhere but have a separately meaningful NPC-state appearance

## Model

Character identity is separated from appearance. One person may therefore appear in
multiple games, campaigns, missions, allegiance states, or encounter modes without
receiving duplicate stable IDs.

Each appearance can record:

- installment and campaign
- mission labels where source-landed
- in-person, radio, briefing, public-broadcast, voice-only, archival, environmental,
  posthumous, scripted-perspective, or branch-dependent presence
- relationship state and participation mode
- named weapon builds carried, owned, provided, built, inherited, or temporarily handed off
- separate storytelling, environmental, and community functions

## Scope rule

Primary playable protagonists are not duplicated merely because they exist. A character
who is playable in another campaign may enter this catalog only when a distinct NPC-state
appearance is source-backed, such as André Bridges, Grim, Mace, La Avispa, or Sakhalin.

## Open governance

Incomplete mission ladders remain incomplete. Callsign-only figures retain working legal
names. Optional-target survival, branch outcomes, ambiguous faction relationships, and
working corporate links remain explicit rather than being collapsed into one canonical
outcome.
