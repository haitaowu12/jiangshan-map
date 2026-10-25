# V11 verification · 24 October 2026

Application 0.10.0 is a local continuation of V10 commit `921288bef93822f1be74c6a0d66e0bf62b778480`. This record distinguishes the local source checks from GitHub synchronization, hosted publication, historian review and learner acceptance.

## Inventory actually checked

| Measure | V10 | Local V11 |
| --- | ---: | ---: |
| Selectable records | 1,809 | 1,837 |
| Narrative biographies | 144 | 158 |
| Dated life milestones | 418 | 478 |
| Shared People identities | 245 | 259 |
| Political overviews | 161 | 161 |
| Regional reading paths | 32 | 32 |
| All reading paths | 55 | 55 |

The new biographies and contexts supply 42 distinct inspected URLs. A separate source-only follow-up adds the selected Samoa report OCR. The validator reports 1,643 unique cited pages across the complete narrative and map material. The new source counts concern URLs, not independent source families or fully checked historical claims.

Twelve regional paths gain entries and fifteen bilingual source-comparison questions. All earlier path IDs, stops and questions survive. Africa/West Asia contributes 8 records/4 biographies/16 milestones; Asia contributes 8/4/16; Americas/Oceania contributes 8/4/19; Europe contributes 4/2/9.

## Automated checks run

`npm run build:content` generated the V11 cumulative manifest and paths. `npm run check` completed on the shell's Node 22.18.0 with **160 passing tests, zero failures, zero skipped**. The corrected `--experimental-test-isolation=none` argument was also accepted by the bundled Node 24.19.0; a second complete V11 test run under Node 24 is not claimed. No dependency installation was needed.

The retained 154 tests protect the earlier application/data contracts. Six V11 tests check:

- Exact preservation of V10 expansion file descriptors, byte sizes and hashes, bounded new chunks, unique IDs and accounting for all new records/biographies/milestones.
- Bilingual names and aliases in shared discovery and Atlas filtering; related histories in both directions; the expected People inventory with inherited identity merges retained.
- Prior reading-path IDs, stops and questions, new paired questions, share URL dates and the unchanged political timeline eligibility.
- Rejection of missing source-access/bilingual scope, mismatched editions, broken connections and invalid life chronology.
- Source-only follow-ups preserving released narratives, dates, locations and original sources without mutating inputs; earlier review scope retained in exportable metadata.
- Rejection of unknown/duplicate evidence-review targets, duplicate citations, incomplete scope/access and credential-bearing source URLs.

The original imported China records and geometry remain unchanged. The validator continues to report 975 mapped China events, 104 profiles, six reviewed events and 24 chronicle annotations; 15 route collections/126 stops; 43 original checkpoints/516 territory instances/180 polity identities; and 242 contemporary reference units. These checks do not certify historical claims or boundary accuracy.

## Local browser checks

The repository's `npm run serve` served `dist/` on loopback. Checks used the Codex in-app browser on this Mac.

| Flow | Observed result |
| --- | --- |
| Full initialization | 1,837 entries, nine regions and 161 political overviews loaded without an initialization error. |
| New biography and life navigation | Lesia Ukrainka's English narrative, dates, source limits, related reading and four milestones displayed. Selecting the 1893 publication step changed the map/share year to 1893 and the life position to 3/4. |
| Chinese detail | Switching language preserved the selected biography/year and displayed translated narrative, chronology and bilingual evidence scope. Source titles and detailed source notes retain their source language. |
| People inventory/search | The shared directory displayed 259 people. Searching `Meg Taylor` from the Chinese UI returned the new profile, its bounded 1974–2019 focus and links to Somare, independence, the Forum and Boe context. |
| Regional reading path | AF2 opened Ahmad Baba at its fourth reading stop, with three milestones and no uncertain birth pin. The study guide displayed the new source-comparison question and contextual manuscript record; selecting that history opened the correct entry. |
| Samoa evidence addendum | The existing entry displayed the new 1919 commission link and bilingual current review scope describing selected OCR, colonial framing and distinct mortality estimates. |
| Narrow Chinese detail | A temporary preview-only harness loaded the app at 390 × 844 CSS pixels. Meg Taylor's title, narrative and life controls wrapped within the narrow frame. This was a visual iframe check, not a physical-device or complete accessibility test. |

Direct share checks initialized from reloaded URLs; no general claim about live address-bar hash editing is made. The temporary responsive harness was removed before final delivery. Browser error logs from the exercised preview contained no errors. Scope is the flows above, not every content record or every device.

## Editorial repairs and remaining limits

Cross-review removed Ahmad Baba's uncertain birth pin and distinguished Comenius's Sárospatak school from his patrons' Transylvanian connections. A Toronto migration pin for Bennett was replaced with a better-supported New York milestone. Dates of publication are distinguished from personal presence; posthumous institutions remain outside life navigation. The ledgers retain source conflicts, catalogue-only limits, same-institution evidence, and access failures.

The Europe cross-review found the geographic issue through the data and ledger; the reviewing agent's fresh browser source inspection was unavailable. The original author had inspected the cited museum and scholarly pages. This is a bounded editorial review, not independent specialist qualification. No claim is made that all inherited facts, translations, institutional outcomes or geographic gaps are resolved.

## Delivery state

V11 is local on `mac/world-atlas-v11-depth`. The baseline GitHub branch and hosted V10 publication were not modified. The original Jiangshan application outside `world/` remains unchanged; a new root `AGENTS.md` records atlas scope and local commands. Source changes and research are retained in the local repository. See [release notes](V11_RELEASE.md) and [next steps](NEXT_STEPS.md).
