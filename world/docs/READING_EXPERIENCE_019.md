# Reading experience — application 0.19.0

Developed 29 October 2026 from owner baseline `ef916bd` on `mac/reading-experience`. This is a local candidate; this task did not push, merge or deploy it. The latest recorded public application remains 0.18.2, identified in [the China map publication receipt](CHINA_MAP_GAPS_PUBLICATION_2026_10_28.md).

## What changed and why

The live 0.18.2 reading catalogue offered 70 sequences in one long list. Opening the Pacific Northwest study from that list left the dialog at scroll position 120px, with its heading above the visible dialog. The shared `openDialog` function replaced the contents of an already-open dialog without resetting scroll or focus.

New dialog contents now start at scroll position zero and focus a named heading. The reading catalogue separately preserves its filters, selected study and return position. If the viewport changes, the selected card is brought into view when needed. The catalogue renders matching results without rebuilding the input controls on every keystroke.

The catalogue provides bilingual, accent-insensitive search across reading names, descriptions and linked entry titles; region and theme filters; and up-to-20/up-to-40-minute filters. A reading belongs to each region/theme represented by at least one linked entry; these filters describe included material, not exclusive geographic scope. The seven legacy journeys without duration estimates remain in unfiltered results and are excluded by a duration limit. Unknown duration is not treated as zero. Three existing short studies provide starting points; they are not duplicated in the rest of the catalogue.

Eleven English/Chinese titles and summaries replace editorial working language or generic descriptions. Earlier titles remain searchable. The five sequences of at least 90 estimated minutes gain 26 named chapters: eight in the US/Canada sequence, four in the African sequence, five in North American colonization, five in Pacific colonial/modern history and four in modern Europe. Existing course IDs and absolute stop positions remain unchanged. Chapter boundaries are anchored to record IDs, partition every original stop exactly once, and do not define new historical periods. All original questions and activities remain available; long sequences disclose their full question list separately.

Chapter links add an optional `chapter` parameter alongside the existing `reading` and absolute `step`. Reload restores the selected chapter and step; old links without `chapter` retain full-sequence behavior. Unknown chapter IDs fall back to the full sequence. Chapter navigation stops at its own endpoint, reports chapter completion and returns to the course guide. Full-sequence reading remains available.

The current instructions in README, CONTRIBUTING, the scoped AGENTS guide and NEXT_STEPS distinguish application 0.19.0, published 0.18.2 and narrative V15 / manifest 0.16.0. Historical next-step notes and release accounts remain explicitly grouped as earlier checkpoints.

## Implementation and checks

`dist/reading-catalog.mjs` owns editorial presentation, chapter bounds and filtering. `dist/reading-browser.mjs` owns the catalogue DOM and return state. `dist/reading.css` uses the existing palette, flat rows and responsive layout. The three files add approximately 19 KB of uncompressed local assets; no external dependency or network service was introduced. This is an asset-size observation, not a measured performance improvement.

`npm run check` runs structural validation and 294 tests. The three new tests exercise identity/stop/anchor preservation, complete chapter partitions and legacy index compatibility, combined bilingual/diacritic search, filtering and empty results. Inputs, historical records, published course JSON, geometry and source manifests were not edited.

Local in-app-browser checks exercised:

- Opening a study from a scrolled catalogue: scroll reset to zero and heading focus; returning preserved selected-card focus, filters and position.
- Search, combined region/theme/time filters, empty-result feedback and reset.
- Pacific Northwest study using keyboard activation: four anchors at 1951, 1952, 1953 and 1930; completion returned to its guide.
- US/Canada work chapter: starting at absolute step 19, advancing to step 20, reloading at chapter stop 2/7, jumping to stop 7 and finishing at the chapter boundary. The same link without `chapter` restored full-sequence stop 21/57.
- English and Chinese catalogue/study flows at desktop and 390px width. At 390px the dialog's content and client widths were both 324px; at 320px both were 254px. Chinese study entry reset to the heading; catalogue return kept the selected card visible and filters intact.

Review images are local artifacts under `/Users/tony/.codex/visualizations/2026/10/29/world-atlas-reading-019/`. The loopback preview uses `npm run serve -- --port 8083`. Temporary viewport overrides were reset after testing. These checks are bounded browser evidence; they do not establish full screen-reader support, real-device acceptance or learning effectiveness. Reading-time estimates retain the earlier editorial durations, allocated proportionally to chapters; they have not been timed with readers.

## Next acceptance

Trial the Pacific Northwest study with a reader, then incorporate bilingual and regional/community feedback. Observe discovery, evidence inspection and interpretation of dates; do not infer learning from completion or automated tests. A publication task should use the existing Site identity and audience and verify the deployed version separately.
