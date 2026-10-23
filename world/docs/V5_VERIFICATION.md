# V5 verification: China collection and wider historical depth

Verified on **23 October 2026 UTC** against the final V5 data and application source. This document records automated checks and the managed local preview. Production deployment is confirmed separately by the Sites deployment receipt; a preview check alone is not evidence of publication or a GitHub push.

## Collection and provenance

| Material | Verified count |
| --- | ---: |
| Combined selectable entries | 1,317 |
| Original historical essays | 318 |
| Researched biographies / milestones | 24 / 75 |
| Mapped Jiangshan event imports | 975 |
| Source rows accounted for | 978: 975 mapped, 2 exact duplicate rows merged, 1 held |
| Imported person indexes | 104 |
| Imported chronicles / stops | 7 / 68 |
| Imported period-place rows | 1,387 |
| Imported corridor descriptions | 16 |
| Original essays added in V5 | 78 |
| Source pages in the full structural inventory | 715 |
| Routes, networks and inherited chronicles / stops | 15 / 126 |
| Study guides / additional guided readings | 16 / 7 |
| Historical map checkpoints / feature instances | 43 / 516 |
| Contemporary map units | 242 |

The 104 person indexes are not 104 newly written full biographies. Period-place rows repeat across source display windows. Source-page counts identify distinct cited URLs, not independently verified claims. The seven inherited chronicles contain schematic connections and preserve their source evidence status.

The importer checks fixed source-file hashes and extracts JSON literals without executing upstream JavaScript. Its ledger accounts for every chronology and landmark row. Exact duplicates preserve all original pointers and period memberships. One event with a narrative/location mismatch remains held in the manifest. The independent display overlay retains original wording and dates while adding two event revisions and 24 chronicle annotations.

The [source index](V5_SOURCE_INDEX.json) covers all 78 new essays and 26 review targets: 184 citation references, deduplicated to 169 exact URLs. Every indexed citation was reconciled to its integrated data record. This is an index of the additions and review layer, not the complete atlas bibliography.

## Automated acceptance

`npm run check` passed after the final label-spacing changes:

- Structural validation passed for 1,317 entries, bilingual fields, civil years, coordinates, identifiers, related-reading links, course references, map manifests, import outcomes and chunk integrity.
- **103 tests passed; 0 failed, 0 skipped, 0 cancelled.**
- Import regressions cover the 978-row accounting, duplicate membership, held-location handling, source pointers, preserved notices and chunk hashes.
- Review regressions cover immutable originals, Bi Sheng's revised interval and workshop caveat, Su Shi's chapter/quotation distinctions, Wang Yangming's family date, disputed Xuanzang dates, retained route annotations, aliases and unknown review IDs.
- Existing temporal-map, modern-state, calendar and input-scheduler regressions remain passing, including USSR/Germany/Yugoslav transitions and no year zero.
- Collection filtering and URL round trips are checked alongside the combined learning-path references.
- `node --check` passed for `dist/app.mjs`, `dist/china-library.mjs` and `dist/china-review.mjs`; `git diff --check` passed.

Tests check specified invariants and regressions; they cannot establish the truth of every historical sentence or frontier vertex.

## Browser acceptance

The following checks used the visible managed preview and its rendered DOM, including a reload of the final source.

| Interaction | Observed result |
| --- | --- |
| China library, English and Chinese | 975 mapped events, 104 profiles, 1,387 period-place rows and seven chronicles; all eight tabs render |
| Period cards | Eighteen cards use the explicit label **Source display window**, with a note distinguishing these bounds from dynasty lifespans |
| All history → Jiangshan collection | 975 eligible entries; first page renders 80 cards, Show more expands it to 160 |
| People search for Su Shi | One matching index, 1037–1101, four linked event mentions, and the ten-stop source chronicle |
| Place alias search for 成周 | Resolves to the Luoyi/Luoyang directory record, with 14 period-name rows and 52 nearby events; the 20-kilometre proximity caveat remains visible |
| Bi Sheng search and detail | Revised 1041–1048 interval, independent citation, source provenance, original wording disclosure, workshop-location caveat and related essays |
| Roads & walls | All 16 descriptions render; source date windows and schematic-line limitations are explicit |
| Sources tab | Shows 975 mapped, two merged rows, one held record, two event revisions and 24 chronicle annotations, plus manifest and review downloads |
| Su Shi chronicle | Ten numbered stops remain selectable; five dating notes render beside their chapters; original quotations, review evidence and inherited status remain visible |
| Dense chronicle label spacing | Active stop is prioritized; route names avoid other numbered stops, territory names and visible story labels; full names remain in accessible stop labels and the reading panel |
| Guided reading library | 23 paths render, including the four new study guides |
| Printing study guide → Begin → Stop 3 | Opens the Diamond Sutra entry, then the Tripitaka Koreana entry at its own date, with citations, location/date qualifications and related reading |
| Tripitaka entry → Chinese | Chinese narrative, key facts and chronology qualifications render; original source titles and evidence notes remain available |
| 1960 → 1992 → 2026 via year control | 73 / 93 / 242 shaded features and 35 / 39 / 53 names respectively; USSR present at 1960 and absent at 1992 and 2026 |
| Timeline keyboard Home → End | 13,000 BCE shows no invented political shapes; returning to 2026 restores 242 shaded map units and 53 names |
| 390-pixel and 320-pixel responsive frames | No horizontal document overflow: client/scroll widths 375/375 and 305/305 CSS pixels after scrollbars |
| China library at 320 pixels | Dialog client and scroll widths both 254 CSS pixels; cards and tabs wrap; person search works |

No application error was returned by the browser log filtered to the preview origin. Browser-extension metadata errors were present and are unrelated to the atlas. No controlled frame-rate, cold-load or network-performance benchmark is claimed. Search caching and list pagination were verified functionally.

Screenshots from the final interface:

- [China library desktop](preview-v5-20261023.jpg)
- [Su Shi chronicle and map](chronicle-v5-20261023.jpg)
- [390- and 320-pixel responsive layouts](mobile-v5-20261023.jpg)

The temporary responsive test page is excluded from the committed source and deployment package.

## Review scope and remaining work

The atlas now preserves the reference project's event corpus with explicit import outcomes, but independent historical review of that corpus remains incomplete. Source windows, person indexes, nearby-event discovery and schematic chronicles are clearly labelled for their actual roles. Original authorship and notices are retained; the upstream repository's conflicting license statements are documented rather than resolved by assumption.

The 76 new regional essays and two additional China essays improve local detail, but worldwide density remains uneven. A second reviewer checked the 76 regional records structurally and consulted additional sources for six consequential claims; this is not independent verification of every sentence or all cited pages. Broader city timelines, biographies, regional chronologies and source review remain priorities.

See [research and corrections](V5_RESEARCH_AND_REVIEW.md), [China import accounting](V5_CHINA_IMPORT.md), [data policy](DATA_POLICY.md), [content and data notices](CONTENT_LICENSE.md), and [next priorities](NEXT_STEPS.md).
