# Story campaign sources

This tree is organized by installment and playable point of view.

## Main installments

Main-game sources live under `Game1/` through `Game4/`. Each installment contains:

- `Shared/` for installment-wide or genuinely multi-campaign material;
- one named directory for every playable character represented by the narrative ontology;
- character-specific source pages inside the relevant character directory.

Campaign mapping:

- Game 1: Romeo — **Critter Squad: Lead the Way**; Ducky/Frost/Lupin — **Do Right, Fear None**; Spook — **Riptide Red**.
- Game 2: Romeo — **American Freedom**; Ducky/Frost/Lupin — **Persistent Threat**; Spook — **Godkiller**.
- Game 3: Romeo — **No Kings**; Ducky — **Failsafe**; Spook — **Dark Skies**.
- Game 4: Romeo — **Command Authority**; Ducky — **Common Picture**; Spook — **Permanent Record**.

## DLC installments

All DLC campaign sources live under `DLC/<Installment>/`. Each DLC contains `Shared/` when campaign-wide material exists and a named directory for every playable protagonist or parallel playable perspective recorded by the ontology.

## Placement rules

- Put character-specific material in the named playable-character directory.
- Put campaign-wide, multi-character, or chronology/governance material in that installment's `Shared/` directory.
- Use the top-level `Shared/` directory only for material that genuinely crosses installments.
- Do not delete a source merely because another file looks similar. Proven exact duplicates may be retired; uncertain matches must remain and be recorded as possible duplicates.
- Do not park new DLC source files directly under `story_campaigns/DLC/`; sort them into the appropriate DLC directory or split mixed packets without dropping unique text.
