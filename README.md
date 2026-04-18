# Project Warriors Trilogy Concept

This repository is the working source home for **Project Warriors**: a grounded near-future military thriller / tactical shooter narrative-development project spanning three main games, multiple overlapping protagonist campaigns, and several DLC workstreams.

It is primarily a **source-development repo**, not a software build repo. Its job is to keep narrative, worldbuilding, gameplay, audio, promotional, and migration/governance materials organized, recoverable, and easy to refresh.

For repo-organization and intake rules, also see:

- `CONTENT_LIFECYCLE.md`
- the `README.md` files inside the major content directories

---

## What lives here

This repo currently holds:

- active development source pages
- working compendia used as the day-to-day synthesis layer
- incoming patch and update packages awaiting merge or cleanup
- recovered legacy source extracts kept for verification and reclamation
- audit, manifest, and migration-control documents
- archived bundles from earlier package drops

The current project source model is:

- **one archival master** for milestone-refresh consolidation
- **six working compendia** for everyday use

The six working compendia are:

1. Core / Timeline
2. Worldbuilding / Strategic Architecture
3. Characters / DLC
4. Gameplay / Weapons / Style
5. Missions / Scenes / Cinematics
6. Promotional / Sidebar Development

---

## Repo layout

```text
ROOT_DIR/
├── README.md
├── dev_src_docs/
│   ├── canon_lore_source_of_truth/
│   ├── diegetics_and_world-building/
│   ├── gameplay_mechanics/
│   ├── image_prompts/
│   ├── music_and_sound_design/
│   ├── story_campaigns/
│   │   ├── Game1/
│   │   ├── Game2/
│   │   ├── Game3/
│   │   ├── HomeDefenseDLC/
│   │   ├── SemperFiDLC/
│   │   ├── TheWaspDLC/
│   │   └── WhoDaresWinsDLC/
│   ├── templates/
│   └── PW_Source_Manifest_2026-04-13_rev2.csv
├── Project_Warriors_Knowledge_Compendia/
├── incoming_patches_and_updates/
├── new_src_material/
├── source_audits_and_reports/
├── Recovered_Sources/
├── archived/
└── temporary_files/
```

### Directory intent

#### `dev_src_docs/`
Primary authoring and landing area for current source-of-truth documents. This is the best first stop for live development work.

#### `Project_Warriors_Knowledge_Compendia/`
The normalized working knowledge layer. Use these when you need a compact but current view of the project without opening every underlying source page.

#### `incoming_patches_and_updates/`
Staging area for source inserts, patch bundles, closeout packets, and other materials that still need to be landed, merged forward, or checked.

#### `new_src_material/`
Loose or recently prepared source pages that are ready to be sorted into the proper long-term location.

#### `source_audits_and_reports/`
Governance layer: manifests, ledgers, audits, package changelogs, gap-hunt notes, and migration reports.

#### `Recovered_Sources/`
Legacy source material recovered from older consolidated packages. Keep for cross-checking and reclamation, not as the preferred everyday working layer.

#### `archived/`
Historical zip bundles and prior package drops. Useful for recovery and comparison, but not the default place to edit from.

#### `temporary_files/`
Scratch area. Treat as disposable unless an item is intentionally promoted elsewhere.

---

## Working conventions

### Content lifecycle

Use the repo as a layered system, not one flat document dump:

- `dev_src_docs/` is the durable authoring layer
- `Project_Warriors_Knowledge_Compendia/` is the synthesized reference layer
- `incoming_patches_and_updates/` and `new_src_material/` are intake layers
- `source_audits_and_reports/` is the governance layer
- `Recovered_Sources/` and `archived/` are recovery and history layers
- `temporary_files/` is scratch space

The full operating rule set lives in `CONTENT_LIFECYCLE.md`.

### Preferred editing order

1. Edit or create the relevant source page in `dev_src_docs/`.
2. Land any validated inserts from `incoming_patches_and_updates/` or `new_src_material/`.
3. Refresh the relevant working compendium(s).
4. Update manifests, ledgers, or audits if the source inventory or retirement state changed materially.
5. Refresh the archival master at milestones rather than after every minor change.

### Source-governance rules

- Preserve original filenames, stable document IDs, manifests, and clear source boundaries where practical.
- Treat the **archival master** as a milestone reference, not the everyday working ballast.
- Avoid treating original sources, working compendia, and the archival master as equally active authoring layers at the same time.
- If older files conflict with newer locked canon or newer integration patches, prefer the newer locked material.
- Promotional/sidebar material is useful creative reference, but it should not silently override main narrative or gameplay canon without cross-checking.

---

## Key reference files

### Core working set

- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_01_Core_Timeline_2026-04-13_rev2.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_02_Worldbuilding_Strategic_Architecture_2026-04-13_rev2.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_03_Characters_DLC_2026-04-13_rev2.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_04_Gameplay_Weapons_Style_2026-04-13_rev2.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_05_Missions_Scenes_Cinematics_2026-04-13_rev2.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_06_Promotional_Sidebar_Development_2026-04-13_rev2.txt`

### Governance / migration layer

- `Project_Warriors_Knowledge_Compendia/PW_Archival_Master_2026-04-13_rev2.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Project_Memory_Integration_Patch_2026-04-13_rev2.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Recommended_Upload_Order_2026-04-13_rev2.txt`
- `source_audits_and_reports/PW_Source_Manifest_2026-04-13_rev2.csv`
- `source_audits_and_reports/PW_Migration_Ledger_2026-04-13_rev2.txt`
- `source_audits_and_reports/PW_Thread_Archive_Audit_2026-04-13_rev2.txt`
- `source_audits_and_reports/PW_Package_ChangeLog_2026-04-13_rev2.txt`

### Canon overview

- `dev_src_docs/canon_lore_source_of_truth/PW_Updated_Canon_Overview_2026-04-13_rev1.docx`
- `dev_src_docs/canon_lore_source_of_truth/PW_Updated_Canon_Overview_2026-04-13_rev1.pdf`

---

## Suggested use pattern

### If you need the fastest project orientation

Read, in this order:

1. `README.md`
2. `Project_Warriors_Knowledge_Compendia/PW_Project_Memory_Integration_Patch_2026-04-13_rev2.txt`
3. the six working compendia
4. the migration ledger and thread archive audit if you are checking source coverage or retirement safety

### If you are landing new material

Start in `dev_src_docs/` or `incoming_patches_and_updates/`, then move changes forward into the compendia and governance layer as needed.

### If source-count pressure matters in ChatGPT or other constrained contexts

Use the six working compendia first, then pull in the memory integration patch, ledger, and audit only when needed.

---

## Current open development / revisit items

This section is intentionally selective: it lists the live items that appear most relevant for repo users and future cleanup, rather than every small parked note in the project.

### Source-integration and migration closeout

- Merge and verify the **Bakhmut visual reference packet** in final source-ready form.
- Merge and verify the dedicated **BODYWORK / Van Hult** source page.
- Merge and verify the consolidated **Boston weapons / Kearney armorer** packet.
- Merge and verify the **trilogy slogan / promo style** page.
- Land a stable source page for the **non-Romeo pilot radio-station follow-up**.
- Keep the **South Africa campaign viability** workstream live until it lands in source-ready form.

### Narrative structure and campaign gaps

- **Ducky Game 3** remains largely undeveloped.
- **Ducky Game 1** still needs a fully mapped mission arc between **Wirecutter** and the **Rotterdam** finale.
- The **time gap between Game 1 and Game 2** still needs cleaner determination.
- The **Romeo bridge from Kentucky to Boston** remains an active construction zone.
- Some broader **Game 3 campaign structure** work remains fragmentary outside the best-developed current lanes.

### Mission / scene development still worth revisiting

- **A-10 suburban attack-run scene** still needs a full development pass.
- **Red Dawn paratrooper callback** still needs final mission placement / execution.
- Additional aircraft-scene placements still merit final assignment cleanup where not already fixed.
- **Tea Party / Boston harbor** mission work remains a live revisit space.
- The **Boston foreign-civilian / wheelchair side quest** remains parked but still live.

### Design / presentation items still open

- Final visual execution of the **TITR studio logo**.
- Final visual execution of the **studio splash sequence**.
- Final decision / execution pass for the **campaign mission timestamp card** style system.

### DLC / theater-level items still parked for later

- **Home Defense DLC** protagonist/title/final shape remain provisional.
- **Middle Eastern theater** development remains parked for later Game 3 work.
- **India’s geopolitical role** remains a pinned later-development item.
- Some **British arc follow-up items** remain open even after recent expansion, including wider Royal Navy / RAF / heavier-force scope decisions.

---

## Status note

The repo is already strong enough to function as a practical working source set, but it should still be treated as a **living development repository** rather than a finished canon vault. Before retiring older material, cross-check repo-only additions, patch bundles, and partial-item packets so late-thread outputs are not silently lost.

---

## Maintenance note

When the structure changes materially, update this README alongside:

- the source manifest
- the migration ledger
- the thread archive audit
- the recommended upload order

That keeps the landing page aligned with the actual repo rather than becoming a stale description of an older package state.
