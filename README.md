# Project Warriors Trilogy Concept

This repository is the working source home for **Project Warriors**, a grounded near-future military-thriller / tactical-shooter narrative-development project spanning the main trilogy, overlapping protagonist campaigns, and multiple DLC/side-story workstreams.

It is a docs-as-code content repository, not a software build repository. Its purpose is to keep canon, narrative, gameplay, audio, promotional, visual, and governance material organized, recoverable, and source-controlled.

## Start here

For current orientation, read:

1. `CONTENT_LIFECYCLE.md`
2. `source_audits_and_reports/PW_LLM_Handoff_Rev6_Consolidation_2026-07-06_rev1.txt`
3. `Project_Warriors_Knowledge_Compendia/PW_LLM_Handoff_Current_Project_State_2026-07-06_rev1.txt`
4. the six rev6 working compendia
5. `Project_Warriors_Knowledge_Compendia/PW_Canon_Decisions_Lock_2026-07-06_rev1.txt`
6. dated supplemental recovery addenda newer than rev6

At this recovery pass's baseline, no pre-existing open-PR dependencies remained. Always check the current pull-request list before making a new full-reconciliation claim.

## Current working knowledge set

The canonical day-to-day synthesis layer is:

- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_01_Core_Timeline_2026-07-06_rev6.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_02_Worldbuilding_Strategic_Architecture_2026-07-06_rev6.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_03_Characters_DLC_2026-07-06_rev6.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_04_Gameplay_Weapons_Style_2026-07-06_rev6.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_05_Missions_Scenes_Cinematics_2026-07-06_rev6.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Working_Compendium_06_Promotional_Sidebar_Development_2026-07-06_rev6.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Archival_Master_2026-07-06_rev6.txt`

Rev6 supersedes rev4/rev5 synthesis files. Older files remain useful as recovery evidence only.

### Supplemental addenda

Source-first addenda capture material landed after the rev6 consolidation without pretending the archival master has been milestone-refreshed after every small pass. Read the newest relevant addenda alongside rev6, including:

- `Project_Warriors_Knowledge_Compendia/PW_Recovered_Visual_Mechanics_Lore_Addendum_2026-07-25_rev1.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Supplemental_4_Thread_Recovery_Addendum_2026-07-24_rev1.txt`
- `Project_Warriors_Knowledge_Compendia/PW_Legacy_Thread_Recovery_Addendum_2026-07-24_rev1.txt`

## Repository layout

```text
ROOT_DIR/
├── dev_src_docs/                         durable active source pages
├── Project_Warriors_Knowledge_Compendia/ synthesis / working knowledge
├── incoming_patches_and_updates/         package staging
├── new_src_material/                     loose intake
├── source_audits_and_reports/            governance, manifests, audits
├── Recovered_Sources/                    legacy evidence / verification
├── archived/                             historical snapshots and bundles
└── temporary_files/                      disposable scratch
```

## Source model

- **Active authoring:** `dev_src_docs/`
- **Synthesis:** six working compendia plus dated addenda
- **Milestone ballast:** archival master
- **Governance:** audits, manifests, ledgers, changelogs
- **Recovery evidence:** `Recovered_Sources/` and `archived/`

## Preferred editing order

1. Create or update the durable topic source in `dev_src_docs/`.
2. Validate supersessions against later canon decisions.
3. Refresh or add the relevant compendium/addendum layer.
4. Update manifests/audits when source inventory or retirement state changes.
5. Refresh the archival master only at a meaningful milestone.

## Authority and supersession

When sources conflict, use this order:

1. later explicit owner adjudication;
2. later source-landed canon/correction pages;
3. current dedicated topic sources;
4. rev6 compendia and newer addenda;
5. older summaries, staging packages, and recovered evidence.

Promotional/sidebar material cannot silently override narrative or gameplay canon. Early summaries frequently contain stale dates, ranks, names, or campaign labels; always load the July 2026 canon decisions and later recovery landings.

## High-priority current controls

- PANDORA: **September 7, 2028**; U.S. election: **November 7, 2028**.
- Romeo: **SSG Ramon Alvarez**.
- Spook: **Trevor Albertson Gartner**, no military rank.
- Ducky Game 2 campaign: **Persistent Threat**; **AEGIS Falls** is the final mission title only.
- Dale spelling: **PRUETT**.
- La Avispa DLC title: **Project Warriors: Wasp**.
- TRU/SIGHT replaces PYTHIA; SBS operator Mags replaces operator Wren; weapon build WREN remains.

## Current recovery / governance references

- `dev_src_docs/canon_lore_source_of_truth/PW_Legacy_Thread_Canon_Landing_2026-07-24_rev1.txt`
- `source_audits_and_reports/PW_Legacy_Thread_Reconciliation_Audit_2026-07-24_rev1.txt`
- `source_audits_and_reports/PW_Source_Manifest_Addendum_2026-07-24_rev1.csv`
- `source_audits_and_reports/PW_Recovered_Visual_Mechanics_Lore_Transcript_Audit_2026-07-25_rev1.txt`
- `source_audits_and_reports/PW_Recovered_Visual_Mechanics_Lore_Manifest_2026-07-25_rev1.csv`

## Working rule

Compendia are orientation tools. When making the project more correct, edit or create the source page first.
