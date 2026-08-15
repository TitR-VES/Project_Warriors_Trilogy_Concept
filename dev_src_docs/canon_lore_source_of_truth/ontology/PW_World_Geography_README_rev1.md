# Project Warriors World Geography Projection

`pw_world_geography_reference_rev1.yaml` is the additive machine-friendly registry for the owner-provided Post-PANDORA / World War III world-events geography map.

The layers answer different questions:
- `pw_world_event_timeline_*`: what happens and in what relative order.
- `pw_world_geography_reference_rev1.yaml`: where mapped events, territorial states, routes, corridors, and reference anchors are located.
- `pw_world_geography_chronology_rev1.yaml`: which exact calendar anchors and relative temporal bindings are currently source-supported.
- the current corrected KML: detailed geometry.
- narrative source pages: authoritative story meaning.

## Current source map — 2026-08-15 rev2

Current validated handoff artifact:
`PW_Post_PANDORA_WW3_World_Events_Geography_Reference_2026-08-15_rev2.kml`

The owner has stated this corrected KML will be the basis of the next map update, so exact repository preservation of this interim artifact is deferred; its SHA-256 and validated feature/geometry state are retained here.

SHA-256:
`11470187f821fc54f55011627687fa543dcfc7fdd8a45d13df26c0ad11d4692e`

Current map counts:
- 174 placemarks
- 105 points
- 36 polygons
- 32 line strings
- 1 geometry-less/other placemark
- 128 named placemarks
- 46 unnamed placemarks
- all 36 polygons topologically valid

The previous six-part KMZ reconstruction package remains preserved as the earlier 133-feature geometry revision. It no longer controls current-map feature coverage.

## Stable feature identity

To avoid renumbering the already-landed PW-GEO identity base, current coverage is composite:

Base 133-feature inventory:
`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Placemark_Inventory_2026-08-14_rev1.csv`

41-feature additive extension:
`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Placemark_Inventory_Extension_2026-08-15_rev1.csv`

Inherited-feature correction overlay:
`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Feature_Revision_Overlay_2026-08-15_rev1.csv`

The correction overlay records topology/label changes without changing stable IDs.

## 2026-08-15 geography additions

The current map adds, among other owner-supplied material:
- broader Midwest/Northeast U.S. campaign geography and the strategic eastbound context that includes Romeo's route toward Boston;
- late-Game-3 British Boston widening and Battle-of-Boston geography;
- the ensuing post-Game-3 U.S./UK Northeast/Capital liberation campaign;
- New York, Philadelphia, Washington and associated Allied naval sustainment geography;
- UNHMNA formalized maritime humanitarian corridors shortly after Game 2;
- the rule that Gulf relief receives no direct UNHMNA maritime corridor and instead moves overland from Charleston and Miami receiving corridors;
- Canadian liberation of Maine and Vermont;
- Canadian supply support to Maine local-defense forces;
- CFB Valcartier as Canadian staging point;
- Highgate Springs–St-Armand/Philipsburg as the Vermont liberation-axis border-crossing reference;
- Woodstock border-crossing geography for the Maine axis.

Exact dates remain open unless explicitly represented in the chronology projection.

## Geometry repairs

Two inherited locked polygons contained self-intersection artifacts:
- Volunteer Corps of Maine controlled area;
- South Carolina State Defense Force/local volunteer militia area.

The current KML removes only microscopic malformed loops. The intended territorial footprints remain unchanged at narrative scale. All current polygons validate.

## Geography chronology projection

Exact anchor KML remains:
`dev_src_docs/worldbuilding/geography/PW_World_Events_Canon_Chronology_Anchors_2026-08-14_rev1.kml`

The five exact locked anchors remain:
- 2028-06-04 — Glushkin activation / Lebedev Boston staging
- 2028-09-07 — PANDORA attacks
- 2028-09-07 — Hudson Overlook
- 2028-09-07 — coordinated hostile West Coast offensives begin
- 2028-11-07 — U.S. presidential election

Chronology feature coverage is composite:

Base 133-feature overlay:
`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Chronology_Overlay_2026-08-14_rev1.csv`

41-feature extension:
`dev_src_docs/worldbuilding/geography/PW_Post_PANDORA_WW3_World_Events_Geography_Chronology_Overlay_Extension_2026-08-15_rev1.csv`

Current chronology state:
- 174 current PW-GEO features
- 40 with source-backed relative/theater/event bindings
- 134 unresolved at feature-date level
- 0 source-map features assigned direct `TimeStamp` / `TimeSpan`
- 0 invented exact dates

New relative chronology preserved in this pass:
- Romeo-associated eastbound strategic geography remains intergame and exact-date open.
- overt British Boston landing is late Game 3.
- ensuing Allied Northeast/Capital liberation campaign is post-Game 3.
- formalized UNHMNA maritime corridors are shortly after Game 2.
- Canadian Maine/Vermont liberation is owner-supplied but exact calendar placement remains open.

## Source and audit

Current geography source:
`dev_src_docs/worldbuilding/PW_Post_PANDORA_WW3_World_Events_Geography_Source_2026-08-15_rev3.txt`

174-feature update audit:
`source_audits_and_reports/PW_World_Events_Geography_174_Feature_Update_Audit_2026-08-15_rev1.txt`

The earlier 2026-08-14 chronology source/audit remain the baseline documentation for the 133-feature chronology layer; the 2026-08-15 extension and registry counts supersede their feature-count totals for current-map use.

## Open hygiene

Current non-blocking flags include unnamed/untitled features, Alaska/dateline normalization, rough wording on the UK naval-disruption map label, a future Pacific-Northwest/Canadian-border continuity recheck, and explicit confirmation of the current KML's USS Wyoming label versus the older USS Nebraska stable-ID wording.
