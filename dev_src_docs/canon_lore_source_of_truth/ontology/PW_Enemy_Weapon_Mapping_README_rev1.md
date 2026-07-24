# Project Warriors Enemy-to-Weapon Ontology

`pw_enemy_weapon_mapping_rev1.yaml` is the additive bundle manifest for enemy archetypes, named enemy roles, carried-weapon rules, ammunition references, encounter placement, and compatibility bindings to the merged portable-weapon catalog.

It does not replace narrative source pages, the named-build registry, or `pw_weapon_catalog_rev1.yaml`.

## Current projection

- 33 stable `PW-ENM-*` enemy-type identities
- 33 reciprocal `PW-ELD-*` loadout records
- 34 `PW-EEN-*` installment/campaign/mission encounter records
- 48 additive bindings to existing `PW-WOC-*` weapon occurrences
- 7 `PW-EDF-*` deferred campaign/opposition slots

The tactical-tier vocabulary distinguishes basic irregulars, trained military personnel, trained paramilitary personnel, special-operations elites, atypical conditioned units, and unresolved tiers.

## Access and drop rules

A weapon being carried does not imply that it drops, can be picked up, or persists after the encounter. Each loadout weapon rule therefore records independently:

- carry role and carry state;
- ammunition references;
- drop policy;
- player pickup state;
- conditional spawn or objective requirements.

This preserves alarm-dependent spawns, failed-objective pickups, fixed-world heavy weapons, collectible-only underwater equipment, missable named-enemy rewards, scripted inaccessible equipment, and unresolved drop behavior.

## Bundle parts

- `pw_enemy_types_state_forces_rev1.yaml`
- `pw_enemy_types_nonstate_named_rev1.yaml`
- `pw_enemy_loadouts_state_forces_rev1.yaml`
- `pw_enemy_loadouts_nonstate_named_rev1.yaml`
- `pw_enemy_encounters_state_forces_rev1.yaml`
- `pw_enemy_encounters_nonstate_named_rev1.yaml`
- `pw_enemy_mapping_deferred_slots_rev1.yaml`
- `pw_weapon_catalog_enemy_type_bindings_rev1.overlay.yaml`

`schema/pw_enemy_weapon_mapping.schema.yaml` controls enemy, loadout, encounter, deferred-slot, and cross-catalog reference structure. Weapon-catalog schema rev2 validates `PW-ENM-*` references and forbids compatibility overlays from changing access, retention, ammunition, or drop state.

## Deferred opposition lanes

The projection deliberately does not invent generic loadouts for undeveloped Game 3 PLA opposition, Game 4/War Within NAF or Vanguard hostile pools, Who Dares Wins, Sea Spear, Home Defense, The Storm, or The Collapse. These remain source-recovery or dedicated campaign-development tasks.

## Extension contract

Later passes may add AI behavior profiles, armor geometry, spawn weights, faction ontology references, and mission-specific weapon probabilities without changing the stable enemy, weapon, ammunition, or occurrence identities introduced here.
