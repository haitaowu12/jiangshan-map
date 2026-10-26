# Neighboring political colors · 0.15 display patch

26 October 2026. Requested behavior: nearby countries and political regions should have distinguishable fills unless a shared shade has a specific display meaning.

## Correction

The earlier eight-color identity palette had no spatial constraint. Different identities could hash to the same shade, including neighboring Albania/Serbia and Armenia/Azerbaijan in the shipped modern data. Adding individual country overrides would leave the same failure available elsewhere and at other dates.

`dist/map-palette.mjs` now builds a proximity graph from the currently selected political/cultural source geometries, then assigns deterministic mineral colors. Borders are sampled on the sphere at intervals of at most 100 km and compacted into approximately 25 km geocentric cells. Samples within 250 km connect display groups. This captures shared borders and nearby islands; it also handles the antimeridian, polar areas and long borders whose centroids are far apart. The distance is a cartographic display heuristic, not a border or sovereignty test. It is intentionally approximate near the distance cutoff.

A saturation/degree ordering separates connected groups. Among available shades, perceptual distance favors clearer contrast while retaining an identity's preferred color when practical. Extra muted shades, followed by deterministic overflow colors, handle dense overlapping/colonial networks without silently reusing a neighboring shade. Source order and UI language do not determine the result. Distant regions may reuse a shade; a new date/source composition can change the assignment. Zooming, panning and story filters do not recolor an unchanged composition.

## Deliberate shared or neutral styling

- Taiwan/mainland China retain the user's requested shared display shade. Source identities, dates, dispute qualifiers and geometry remain distinct.
- Multiple pieces of the same political identity retain one shade. Dated US/Canada source divisions retain their national/parent grouping with internal boundaries; statehood does not substitute for an acquisition date. Independent parent groups such as Newfoundland remain separate graph nodes.
- Recorded competing claims retain their existing hatch treatment. Gray 2022 administrative reference outlines remain geographic reference; they do not become political fills or acquire historical meaning.

No historical geometry, narrative, source color, date or source ID changes. Color assignment is a display operation. The map, legend and evidence list use the same palette. The North American parent-group key now reads the actual composed palette rather than independently calculating a preferred color from an isolated label feature.

## Verification

- `npm run check`: **221 tests passed**, including six new palette regressions.
- Synthetic negative control reproduces identical preferred shades on touching independent polygons. Tests check nearby islands, long borders, antimeridian and polar neighbors, explicit shared groups, source immutability, reversed input order, cache isolation and a 16-node overlap requiring overflow colors.
- Actual modern country pairs and the selected 399 BCE China phase have separate neighboring colors. Taiwan/mainland China and national parent pieces retain the intended exceptions.
- `node scripts/audit-map-palette.mjs <output.json>` composes the same historical, China, CShapes, contemporary and dated North American layers at **64 checkpoint/transition years**. It prepares modern preferred colors as the renderer does. Across **6,285 sampled neighboring group pairs** (including repeated pairs in different views), the former preferred palette had **1,089 same-color collisions**; the revised assignment has **0**. Shared display groups are merged before this comparison, and neutral modern reference outlines are excluded. This checks the graph's assignment contract, not exhaustive geographical adjacency or frontier correctness. Independent fixtures and named real-country checks supplement it.
- Local browser review: ancient China, modern Europe and dated North America; actual Taiwan/mainland fills match. The 1900 evidence list's **216 swatches** match rendered solid fills. The three North American parent swatches match their current source-group colors. All 216 mapped units keep their colors after a zoom.
- Performance: weak geometry caches and a bounded 64-composition palette cache avoid recomputing unchanged geometry during redraws. In the local Mac audit, maximum uncached palette time was **161 ms**, and maximum cached time **0.18 ms**. A separate cold modern-only run was approximately **208 ms**. The working check was below 500 ms cold and 5 ms cached on this machine. These are palette timings, not page-load or mobile performance claims.

The current soft theme, names, boundary strokes and hatch meanings remain available alongside color. This bounded review does not claim universal color-vision accessibility or exact detection of every possible neighboring source geometry.

Publication identifiers and live verification are recorded separately in `MAP_COLOR_PUBLICATION.json` after deployment.
