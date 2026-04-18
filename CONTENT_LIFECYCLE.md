# Content Lifecycle

This repo is a content-development repository with a docs-as-code workflow.
The main problem to avoid is mixing active source pages, synthesis documents,
staging drops, recovered legacy material, and historical archives into one
undifferentiated working pile.

This file defines the intended lifecycle for material in the repository.

## Content Layers

### 1. Active authoring

Primary home: `dev_src_docs/`

Use this layer for stable, current source pages that should be treated as the
best editable version of a topic.

Examples:
- character profile pages
- mission reference pages
- screenplay passes
- gameplay mechanic references
- visual-identity or audio-design source pages

### 2. Synthesis / working knowledge

Primary home: `Project_Warriors_Knowledge_Compendia/`

Use this layer for compendia and milestone-level rollups that summarize or
normalize the live source set. These are high-value reference documents, but
they should not replace the underlying source pages as the main authoring layer.

### 3. Intake / staging

Primary homes:
- `incoming_patches_and_updates/`
- `new_src_material/`

Use these layers for material that has arrived but is not fully landed.

Use `incoming_patches_and_updates/` when:
- a package, bundle, thread closeout, or update drop arrives
- the material still needs validation, merge decisions, or breakup into
  long-term homes
- the drop includes multiple files that should stay together until reviewed

Use `new_src_material/` when:
- a loose source page or a very small set of related files is ready to sort
- there is no reason to keep it as a package
- the material should be promoted into `dev_src_docs/` soon

### 4. Governance / control

Primary home: `source_audits_and_reports/`

Use this layer for manifests, ledgers, audits, changelogs, gap maps, and other
documents that describe repo state rather than project fiction itself.

### 5. Recovery / verification

Primary home: `Recovered_Sources/`

Use this layer for recovered legacy extracts that are useful for cross-checking,
comparison, or reclamation. Treat them as evidence, not as the preferred place
to keep editing.

### 6. Historical archive

Primary home: `archived/`

Use this layer for zip bundles, frozen package drops, and older snapshots kept
for rollback or historical reference.

### 7. Scratch / disposable

Primary home: `temporary_files/`

Use this layer for notes, exports, or transient working scraps that have not
earned a durable home yet.

## Default Workflow

When new material arrives, use this sequence:

1. Put it in the correct intake layer.
2. Decide whether it is a package (`incoming_patches_and_updates/`) or a loose
   source page (`new_src_material/`).
3. Validate what should become durable source-of-truth material.
4. Promote that stable material into `dev_src_docs/`.
5. Refresh the affected compendium in
   `Project_Warriors_Knowledge_Compendia/`.
6. Update manifests, ledgers, or audits if source inventory or retirement state
   changed.
7. Archive the original package when it is no longer an active staging item.

## Intake Rules

- Do not let `incoming_patches_and_updates/` become a permanent second source
  tree. Promote stable pages out of it.
- Do not use `new_src_material/` as a long-term catch-all inbox. If something
  sits there for long, it probably needs a real home or an archive decision.
- Do not edit directly inside `archived/` or `Recovered_Sources/` unless the
  work is explicitly about preservation or reclamation.
- Do not treat the working compendia as the only source-of-truth for details
  that deserve their own source page.

## Naming Guidance

The repo already has a usable naming pattern. Keep using it consistently:

- stable project prefix such as `PW_`
- concise topic or document title
- absolute date in `YYYY-MM-DD` format when relevant
- explicit revision suffix such as `rev1`, `rev2`, `v1`, `v2`

Prefer preserving established names for imported materials unless there is a
strong reason to normalize them.

## Definition Of Done For A Landed Update

A content update is properly landed when:

- the stable source page lives in `dev_src_docs/`
- the relevant compendium reflects the change
- any needed manifest, ledger, or audit note is updated
- the original package is clearly still staging, or clearly archived
- a future repo user can tell which copy is the working copy
