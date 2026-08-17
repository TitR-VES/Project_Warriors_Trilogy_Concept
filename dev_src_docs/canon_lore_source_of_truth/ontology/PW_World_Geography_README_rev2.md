# Project Warriors World Geography Projection

The current machine-friendly registries are:
- `pw_world_geography_reference_rev2.yaml` — where mapped events, territorial states, routes, corridors, and reference anchors are located.
- `pw_world_geography_chronology_rev2.yaml` — which exact calendar anchors and relative temporal bindings are currently source-supported.
- `pw_world_event_timeline_*` — event/timeline ontology outside the geography-specific projection.
- the repository-preserved KML reconstruction package — detailed geometry recoverable byte-for-byte.
- narrative source pages — authoritative story meaning.

## Current source map — 2026-08-17 rev5

Original / reconstructed KML name:
`PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-17_rev5.kml`

Repository preservation manifest:
`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-17_rev5_kml_parts/README.txt`

The exact KML bytes are stored as compressed Base64 reconstruction parts; following the manifest reproduces the original KML byte-for-byte.

SHA-256:
`0539b7e133c9968744afd3ce3af1bacf91043d75345ca9a62306d00bcc7527d8`

Current map counts:
- 255 placemarks
- 165 points
- 40 polygons
- 49 line strings
- 1 geometry-less/other placemark
- 195 named / 60 unnamed
- all 40 polygons valid
- 48/49 line strings simple
- the sole non-simple line is the owner-confirmed intentional Ventura→Coronado Long Beach backtrack

## Stable feature identity

Coverage is composite:
1. base ordinals 1–133:
   `dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Placemark_Inventory_2026-08-14_rev1.csv`
2. extension ordinals 134–174:
   `dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Placemark_Inventory_Extension_2026-08-15_rev1.csv`
3. extension ordinals 175–255:
   `dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Placemark_Inventory_Extension_2026-08-17_rev2.csv`

Inherited corrections:
`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Feature_Revision_Overlay_2026-08-17_rev2.csv`

The first 174 PW-GEO identities are never renumbered. Intermediate accidental/deleted map features receive no durable IDs.

## Current major additions

The 2026-08-17 map generation adds:
- the Spokane–Missoula–Salt Lake City–Billings–Butte–Pocatello western reversal arc;
- converging Northwestern Counteroffensive routes through California/Oregon, Portland/Seattle, Billings/Spokane/Seattle, and Yakima/Ellensburg;
- Canadian northern support into Seattle;
- Southern California airport/invasion geography and Romeo/Delta Ventura→Coronado movement;
- a tightened CIA/authorized-USAF southern Nevada classified-site security area;
- Canadian Operation Buffalo Trail and Great Lakes/Detroit liberation geography;
- selected Russian bridge destruction / chokepoint geography;
- the Dawn of Mercy Seattle incident;
- UNHMNA Texas–Mexico land access and a Canadian-origin humanitarian air corridor into North/South Dakota;
- Monterrey Treaty / Alaska demilitarization geography.

## Chronology

Exact sidecar:
`dev_src_docs/worldbuilding/geography/PW_World_Events_Canon_Chronology_Anchors_2026-08-17_rev2.kml`

It carries 9 exact semantic anchors:
- 2028-06-04 — Glushkin activation / Lebedev Boston staging
- 2028-09-07 — PANDORA
- 2028-09-07 — Hudson Overlook
- 2028-09-07 — hostile West Coast offensives begin
- 2028-11-07 — U.S. presidential election
- 2030-04-13 through 2030-04-17 — Monterrey Conference
- 2032-05-28 — final Russian withdrawal from Alaska / end of occupation
- 2032-05-28 — Alaska demilitarization begins
- 2032-11-02 — Ainsley Taylor wins restoration-era U.S. presidential election

The Treaty of Monterrey signature day remains open within the conference window. Alaska demilitarization completion remains coarse as early 2035.

Composite feature chronology:
- 255 current PW-GEO features
- 95 with source-backed exact-context / relative / theater / event bindings
- 160 unresolved at feature-date level
- 0 source-map features with direct TimeStamp/TimeSpan

## Important relative locks

- Russian bridge denial occurs after the Battle of Cumberland Gap **and** after the successful turn of the Northwestern Counteroffensive.
- The I-35W St. Anthony Falls crossing remains partly passable but enemy-held from the east side.
- DAWN OF MERCY is Spook Game 3 DARK SKIES Mission 01; BAD OMENS is Act I.
- Buffalo Trail is a Canadian military corridor-opening operation later used by UNHMNA aid; do not merge those functions.
- Russian withdrawal from Alaska and the subsequent demilitarization process are separate.
- Fragmentation/NAF/collapse and Taylor Calgary→Cheltenham exile dates remain open.

## Source and audit

Current geography source:
`dev_src_docs/worldbuilding/PW_Post_PANDORA_WW3_World_Events_Geography_Source_2026-08-17_rev4.txt`

Current chronology update:
`dev_src_docs/worldbuilding/PW_World_Events_Geography_Chronology_Update_2026-08-17_rev3.txt`

Current audit:
`source_audits_and_reports/PW_World_Events_Geography_255_Feature_Update_Audit_2026-08-17_rev1.txt`

## Open hygiene

Non-blocking:
- 60 unnamed placemarks;
- one geometry-less Untitled slide;
- Alaska/dateline normalization;
- typo-prone owner labels pending a dedicated cleanup pass;
- one unlabeled Calgary-area point with unclear role;
- schematic UNHMNA air-corridor vertices not exactly snapped to every airport/base marker.

Do not silently alter these fields while doing unrelated chronology or ontology work.
