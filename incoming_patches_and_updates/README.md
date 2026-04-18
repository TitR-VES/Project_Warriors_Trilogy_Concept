# incoming_patches_and_updates

This is the staging queue for material that has arrived but is not fully landed.

Use this directory for update drops, thread closeouts, package handoffs,
multi-file inserts, and other bundles that still need validation, merge
decisions, or breakup into long-term homes.

## Use This Directory When

- a bundle should stay intact during review
- a handoff note explains how the package should be landed
- multiple files need to be compared before choosing the stable working copy
- a package may later move to archive once its contents are promoted

## Do Not Use This Directory As

- a permanent second source tree
- the default place to keep editing a topic after it has been landed
- a substitute for `new_src_material/` when the item is just a loose source page

## Expected Workflow

1. Receive the package here.
2. Review what is durable, duplicate, or obsolete.
3. Promote stable source pages into `dev_src_docs/`.
4. Refresh the affected compendium.
5. Update governance documents if inventory or retirement state changed.
6. Leave the package here only while it is still an active staging item.
7. Move its historical copy to `archived/` when the drop is closed out.

## Recommended Hygiene

- Keep package folders intact until landing decisions are complete.
- Prefer a short landing or handoff note when a package contains many files.
- If a package produces only one or two stable pages, do not keep treating the
  staging copy as the working copy after promotion.
