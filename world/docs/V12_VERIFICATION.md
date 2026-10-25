# V12 local verification · 24 October 2026

Application 0.11.0 continues committed local V11 `b762e906cfaf7450c95e90e9eb2275485d69f3f6` on `mac/us-canada-atlas-depth`. This record distinguishes source inspection, automated contracts, observed browser behavior and local delivery from specialist acceptance or hosted publication.

## Inventory

| Measure | V11 | V12 |
| --- | ---: | ---: |
| Selectable entries | 1,837 | 1,863 |
| North America entries | 80 | 106 |
| Narrative biographies | 158 | 170 |
| Life milestones | 478 | 534 |
| Shared People identities | 259 | 271 |
| Political overviews | 161 | 161 |
| Regional / all reading paths | 32 / 55 | 32 / 55 |
| Optional US/Canada administrative reference units | 0 | 64 |

The addition is 26 records, 12 biographies, 56 milestones and 36 distinct narrative-source URLs. Three regional paths gain entries and fifteen bilingual source-comparison questions. The validator reports 1,690 distinct cited pages including the geographic reference and named-place evidence. These are URL/inventory counts, not evidence of complete or independently accepted coverage.

## Automated checks

`npm run build:content` produces the V12 cumulative manifest, paths and geographic history index. `npm run check` passes **176 tests**, with zero failed or skipped, on Node **22.18.0**. No dependency installation is required. The frozen V11 tests now explicitly read their historical manifest rather than assuming that V11 is the current release.

Eight V12 integration tests protect exact V11 file descriptors/hashes, the 26/12/56 addition and its sources, bilingual shared discovery, related reading, prior path IDs/stops/questions, source-comparison questions, focus/milestone share years, unchanged political timeline membership, and rejection of incomplete evidence/scope/chronology. They compare the generated 64-area index with the combined reviewed runtime records and actual reference geometry, including 22 explicit named-place associations and inclusive focus-year semantics. The inputs remain unmutated; unknown/duplicate association targets are rejected.

Eight geographic/helper tests protect the pinned source commit/hash, exact 51/13 inventories, independent state/province ID sets, shard byte/hash limits, bilingual names, all label anchors, closed finite spherical rings, finite Equal Earth render paths, eight known interior/island locations, nonoverlap with unrelated continents, representative/milestone associations, year filtering and bilingual/country search. DC is disambiguated from Washington state by ID, type, display label and search alias. An additional source-to-output comparison against the pinned Git asset found zero undeclared geometry changes; the selected geometry has 334 polygons/rings and no hole rings.

The validator now checks the regional metadata, public-domain notice, shard hashes/counts/size limits, generated-index version, record references, roles, milestone years and named-place receipts. It keeps the modern outlines outside historical snapshot membership. Existing import, map, discovery, learning and notebook contracts continue to pass. Historical geometry, imported China source files, V9–V11 narrative inputs and the original application remain intact. The root atlas `AGENTS.md` and current contribution/continuation records are updated for V12.

## Browser observations

Checks used the local loopback server and Codex in-app browser on this Mac.

| Flow | Observed result |
| --- | --- |
| Initialization | 1,863 entries, nine regions, 161 political overviews and 106 North America records loaded. |
| Area discovery | The browser listed 64 areas, country filtering reduced the list to 13 Canadian units, and Saskatchewan search returned the correct province. DC displayed as District of Columbia. |
| Area history/time choice | Saskatchewan opened three connected records. Selecting the existing year 1867 produced an explicit empty result, while all dates restored the histories. Geography stayed labeled as modern reference. |
| Map interaction | Explore on the map enabled outlines and focused Saskatchewan; 64 modern area buttons were present. Activating the province by Enter opened its history. Modern source-year status moved to the map footer to avoid adding to the existing status stack above zoom controls. |
| Developed biography | Tommy Douglas's full English synthesis, source links, review limits, four life milestones and connected Medicare record displayed. The 1947 hospital-insurance milestone changed the year/share URL to 1947 and life position to 3/4. |
| Bilingual continuity | Switching to Chinese retained Douglas, year 1947 and milestone 3/4, with translated narrative and dates. Shared People discovery reported 271 identities; searching Kenojuak in the Chinese interface found the new artist biography. |
| Regional reading share | A fresh NA3 link opened Douglas at stop 22/49; its study guide displayed the new Douglas/Medicare source-comparison question and contextual record. |
| Coastal place evidence | Nunavut listed both Kenojuak's biography and the Kinngait cooperative. Its method disclosure showed the reviewed named place, unmoved-point explanation and Inuit Art Foundation link. |
| Narrow layout | A temporary iframe preview at 390 × 844 CSS pixels displayed Chinese geographic search and the Nunavut history page with wrapped headings/actions/cards and scrollable detail. This is a narrow visual/interaction check, not physical-device or complete accessibility acceptance. |
| Missing-data recovery | The generated index was temporarily held out of the local data directory. The rest of the atlas stayed usable; the modern layer displayed an unavailable/retry action, and opening it showed the missing-file message. After restoring the original file, retry recovered the 64-area browser, all 64 outline buttons and normal source-year status. The intentional 404s belong to this test. No source file remained held out. |

Normal-flow error logs from the main preview contained no errors. Layer preferences used for verification were restored: historical territories on and the new optional reference off.

Direct shared links were checked from fresh loads. Editing a hash while an older modal remains open is not claimed as a general acceptance result. The responsive harness and owned preview server are temporary; they are removed/stopped after verification. Saved preview images and the current launcher/review are in the originating chat's outputs.

## Source review and limits

The four V12 research ledgers map sources to chronology and place meaning. Actual accessible page text was captured by the root in-app browser and read by the regional authors when their own in-app browser was unavailable. Sources disclose central-capture access rather than implying separate browser visits or exhaustive primary-archive reading. Original bilingual synthesis and bounded cross-review narrowed unsupported or conflicting claims, including Lincoln's proclamation exceptions, Macdonald's years in opposition, Champlain's uncertain birth, Sacagawea's competing histories, Ware's ranch date, Douglas's implementation chronology and Addams's 1931 location.

The 2022 Natural Earth source is public-domain modern orientation. The 22 named-place links address demonstrated generalization omissions without shifting pins. There are linked entries in 39 of 64 areas; nonempty areas can still have very little local history. The Mount Hope point remains unlinked after an authoritative state page encountered security verification. No blocked destination was accessed by another route/tool. A guessed U’mista contact page returned 404; the actual inspected homepage supported the location.

The source and translation checks are bounded editorial work. They do not establish full historical accuracy, community/specialist acceptance, representative coverage, measured policy outcomes, broad accessibility or learner understanding. Optional reference assets add 562,729 uncompressed bytes on first use; no frame-rate/latency improvement is claimed. All runtime assets remain local, and no external tile/API/database dependency is introduced.

## Delivery

The source, data, tests and ledgers are retained in the local repository. This task performs no GitHub push, merge or hosted deployment. The earlier V10 hosted publication and V11 local release records remain separate checkpoints. See [release](V12_RELEASE.md) and [next steps](NEXT_STEPS.md).
