# Story campaign sources

This tree is organized first by installment, then by character state.

## Standard layout

Main installments:

- `GameN/Playable_Characters/<PlayableCharacter>/`
- `GameN/Named_NPCs/<PW-NPC-ID>__<PortableName>/`
- `GameN/Shared/`

DLC installments:

- `DLC/<DLC>/Playable_Characters/<PlayableCharacter>/`
- `DLC/<DLC>/Named_NPCs/<PW-NPC-ID>__<PortableName>/`
- `DLC/<DLC>/Shared/`

`Playable_Characters/` separates POV-bound authoring from named-NPC authoring. `Named_NPCs/` is projected from the named-NPC ontology. `Shared/` remains the home for installment-wide, campaign-wide, team-wide, multi-character, chronology, provenance, and governance material.

## Campaign mapping

- Game 1: Romeo — **Lead the Way**; Ducky/Frost/Lupin — **Do Right, Fear None**; Spook — **Riptide Red**.
- Game 2: Romeo — **American Freedom**; Ducky/Frost/Lupin — **Persistent Threat**; Spook — **Godkiller**.
- Game 3: Romeo — **No Kings**; Ducky — **Failsafe**; Spook — **Dark Skies**.
- Game 4: Romeo — **Command Authority**; Ducky — **Common Picture**; Spook — **Permanent Record**.

## Character placement rules

- Put campaign architecture, mission scripts, perspective mechanics, playable loadout continuity, and POV-specific presentation under the relevant playable-character directory.
- Put durable NPC profiles, NPC-specific scene or mission-presence notes, voice/behavior references, equipment continuity, branch-state references, and presentation material under the stable named-NPC directory.
- A character who is playable in an installment remains under `Playable_Characters/` there, even if that person is an NPC in another campaign.
- Do not duplicate team-wide packets into every member directory. Keep multi-NPC squad packages in `Shared/`.
- Use the stable `PW-NPC-*` identity in each NPC directory name. The following ASCII name slug is navigational only; canonical spelling remains controlled by the ontology.

## Preservation rules

- Use the top-level `Shared/` directory only for material that genuinely crosses installments.
- Do not delete a source merely because another file looks similar. Proven exact duplicates may be retired; uncertain matches must remain and be recorded as possible duplicates.
- Do not park new DLC source files directly under `story_campaigns/DLC/`; sort them into the appropriate DLC directory or split mixed packets without dropping unique text.
- When a path moves, preserve an auditable redirect or migration record so ontology source aliases and downstream references can be resolved.
