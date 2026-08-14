# Project Warriors World Geography Projection

`pw_world_geography_reference_rev1.yaml` is the additive machine-friendly registry for
the owner-provided Post-PANDORA / World War III world-events geography map.

It exists because the chronology ontology and the geography layer answer different
questions:

- `pw_world_event_timeline_*` answers **what happens and in what relative order**.
- `pw_world_geography_reference_rev1.yaml` answers **where mapped events, territorial
  states, blockades, routes, and reference anchors are located**.
- `pw_world_geography_chronology_rev1.yaml` answers **which calendar anchors are locked
  and what temporal relationship each PW-GEO feature currently has to them**.
- the corrected KML/KMZ artifact carries the detailed geometry.
- narrative source pages remain authoritative for story meaning.

## Current source map

Repository preservation package:

`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-14_rev1_kmz_parts/`

The six Base64 parts reconstruct:

`PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-14_rev1.kmz`

Expected SHA-256:

`18acfae12d78923615cc750574df1e5c87cf3a97245b57ac750cc7b8b91ca029`

This split transport form exists only because the connected GitHub binary-write path
truncated the direct KMZ upload. It is not a content or format change to the corrected
map. The normal corrected KML and KMZ remain the handoff/use artifacts.

Current registry counts:
- 133 geographic features
- 87 points
- 35 polygons
- 11 line strings

## Geography chronology projection

The chronology layer is intentionally separate from the geometry carrier so calendar
precision can mature without rewriting stable PW-GEO identities.

Files:

- `pw_world_geography_chronology_rev1.yaml`
- `schema/pw_world_geography_chronology.schema.yaml`
- `../worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Chronology_Overlay_2026-08-14_rev1.csv`
- `../worldbuilding/geography/PW_World_Events_Canon_Chronology_Anchors_2026-08-14_rev1.kml`

Current chronology state:
- 5 exact day-level canon anchors encoded as KML `TimeStamp` features
- 12 PW-GEO features with source-backed relative, theater-anchor, or event bindings
- 121 PW-GEO features still unresolved at feature-date level
- 0 original spatial placemarks assigned direct `TimeStamp` / `TimeSpan` values so far

That final zero is deliberate. A locked theater date does not automatically become the
onset date of every occupation or blockade polygon inside that theater. Direct time
primitives should be added feature-by-feature only when the represented event/state has
its own locked date or bounded interval.

Current exact anchors:
- 2028-06-04 — Glushkin activation / Lebedev Boston staging
- 2028-09-07 — PANDORA attacks
- 2028-09-07 — Hudson Overlook
- 2028-09-07 — coordinated hostile West Coast offensives begin
- 2028-11-07 — U.S. presidential election

## Important 2026-08-14 geography changes

- Added the U.S. Army / 75th Ranger movement reference into Harlan County that the
  source description associates with Romeo's reunion with Dingo, Beaver, and Howler.
- Added Cumberland Gap west-portal cross-reference geometry.
- Repaired the Pacific Northwestern Russian Occupation Zone around Seattle so the
  Seattle-to-Canadian-border corridor is contiguous and the polygon no longer carries
  the northern-Washington sliver/self-crossing defect.
- Detailed chronology is not inferred from KML ordering.
- Persistent territorial-control polygons are not automatically converted into events.

See:
- `dev_src_docs/worldbuilding/PW_Post_PANDORA_WW3_World_Events_Geography_Source_2026-08-14_rev2.txt`
- `dev_src_docs/worldbuilding/PW_World_Events_Geography_Chronology_Source_2026-08-14_rev1.txt`
- `source_audits_and_reports/PW_World_Events_Geography_Source_Landing_Audit_2026-08-14_rev1.txt`
- `source_audits_and_reports/PW_World_Events_Geography_Chronology_Audit_2026-08-14_rev1.txt`
