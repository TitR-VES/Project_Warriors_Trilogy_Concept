# Project Warriors World Geography Projection

`pw_world_geography_reference_rev1.yaml` is the additive machine-friendly registry for
the owner-provided Post-PANDORA / World War III world-events geography map.

It exists because the chronology ontology and the geography layer answer different
questions:

- `pw_world_event_timeline_*` answers **what happens and in what relative order**.
- `pw_world_geography_reference_rev1.yaml` answers **where mapped events, territorial
  states, blockades, routes, and reference anchors are located**.
- the KML carries the detailed geometry.
- narrative source pages remain authoritative for story meaning.

## Current source map

`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-14_rev1.kml`

Current registry counts:
- 133 geographic features
- 87 points
- 35 polygons
- 11 line strings

## Important 2026-08-14 changes

- Added the U.S. Army / 75th Ranger movement reference into Harlan County that the
  source description associates with Romeo's reunion with Dingo, Beaver, and Howler.
- Added Cumberland Gap west-portal cross-reference geometry.
- Repaired the Pacific Northwestern Russian Occupation Zone around Seattle so the
  Seattle-to-Canadian-border corridor is contiguous and the polygon no longer carries
  the northern-Washington sliver/self-crossing defect.
- Detailed chronology is not inferred from KML ordering.
- Persistent territorial-control polygons are not automatically converted into events.

See:
- `dev_src_docs/worldbuilding/PW_Post_PANDORA_WW3_World_Events_Geography_Source_2026-08-14_rev1.txt`
- `source_audits_and_reports/PW_World_Events_Geography_Source_Landing_Audit_2026-08-14_rev1.txt`
