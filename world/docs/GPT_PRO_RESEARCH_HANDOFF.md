# GPT Pro research handoff — World History Atlas

## Start here

The owner will conduct this research in GPT Pro. No GPT Pro research report has yet been produced or incorporated. The earlier Gemini requests did not return a report; do not treat their prompts as evidence. This handoff and the complete implementation are in the `world/` directory of the `world-history-atlas` branch in `haitaowu12/jiangshan-map`.

Live V9: https://world-history-atlas-tony.techiesea.chatgpt.site

Deployed standalone source commit: `49aa61bdf270edb5d45d26a56abf95cd7ad6c47c`; application version `0.8.0`. The GitHub synchronization preserves the same application/data and adds this handoff and source-status documentation. It does not change the public deployment. The GitHub mirror commit has its own SHA because it retains the original project outside `world/`.

Read these files before proposing content:

1. `docs/CONTENT_EXPANSION_PLAN.md`: V8 baseline, all 32 workstreams, original three-release plan.
2. `docs/V9_RELEASES_IMPLEMENTED.md`: delivered scope, exact workstream counts, corrections, evidence limits and remaining gaps.
3. `docs/V9_VERIFICATION.md`: checks actually performed; local browser screenshots are not a fresh inspection of the live deployment.
4. `docs/V9_*_RESEARCH.md` and `docs/V9_CROSS_REGION_REVIEW.md`: regional source/access registers, disputed chronology and targeted independent samples.
5. `dist/data/content-expansion-v9.json`: eight added data files, file hashes, all workstreams, exact IDs and counts. Read the records before claiming a topic absent.
6. `dist/data/china-reviews.json`, `china-import-manifest.json` and `china-waterways-v9.json`: targeted amendments, raw provenance and inherited water-window limits.
7. `docs/MAP_METHODOLOGY.md`, `V7_MAP_COVERAGE_REVIEW.md`, `V8_GEOMETRY_FIX.md`: map selection and rendering rules.

## Current delivered scope

There are 1,713 selectable records: the previous 1,369 plus 344 bilingual additions. The additions include 81 full biographies and 70 political overviews, with 649 distinct cited URLs. The shared corpus contains 105 full biographies / 259 milestones; the People directory has 206 identities after three explicitly confirmed profile overlaps. Thirty-two new reading paths supplement sixteen existing study guides and seven guided readings. Counts describe inventory, not completeness or factual verification.

All three planned releases have selected batches (60, 121 and 163 new records), but many local histories and source-access gaps remain. A nonempty workstream is not a completed regional curriculum. East Asia remains much denser because of 975 inherited events. Do not repeat the claim that all original Chinese content is missing; distinguish inherited source coverage, independent corroboration and depth of a researched article.

The atlas also retains 166 inherited Chinese phase selections, 377 political shapes and 3,211 optional administrative shapes. V9 restores 187 river paths, 62 lake edges and 41 labels, plus 16 schematic corridors. CShapes provides dated annual selections for 1886–2019. The map remains selective outside those datasets. Article dates never authorize invented territorial geometry.

## Research mandate

Conduct independent historical research and critical review in English and Chinese where useful. Start from the actual current records, challenge their source-to-claim fit, and identify missing connected sequences. Use public scholarly research, primary texts, archives, museum/library object records, community sources and institutional documents. Distinguish an institution's interpretation from proof; two URLs from the same family are not independent corroboration. Do not pad bibliographies or describe indexed text as full-page reading.

Work in bounded packets rather than one enormous dossier:

### Packet A — Corrections and evidence access

Review a clearly identified, risk-based sample of current records, prioritizing indexed-only or same-institution evidence and claims affecting dates, identity, representative location or political timeline inclusion. Return stable record IDs and claim-level findings. Do not claim to have verified all 975 inherited events from a sample.

Specific China questions already have qualified amendments; test those amendments against sources rather than reverting them by intuition:

- Bi Sheng: the Qingli 1041–1048 interval versus an unsupported exact 1047; distinguish invention attribution, surviving textual account and unverified workshop location.
- Cai Lun: 105 CE court presentation versus paper predating it archaeologically.
- Wang Jing: 69–70 CE works versus the inherited Yellow River display window beginning in 11 CE. Reject the claim that this proves a millennium without floods.
- Zheng He: final-voyage return in 1433 versus uncertain 1433/1435 death; Calicut is not a verified death/burial point. Do not infer an immediate comprehensive maritime ban from the return date.
- Galle and Melaka: two separately sourced replacement subjects now exist. Galle's inscription date, installation chronology, discovery locality and present museum custody are different claims; institutional accounts disagree about the voyage associated with installation. The Malacca depot belongs to a separate port context and lacks a surveyed footprint or secure single foundation day. The raw conflated `china-landmark-412` remains held for provenance; it is not a selectable corrected entry.
- Li Qingzhao: conflicting death conventions and the Chinese afterword's textual transmission; keep confirmed identity linkage separate from chronology.

Other useful checks include Great Lakes/Congo chronology and oral evidence, dates attached to continuing Indigenous societies, precolonial Brunei/Ryukyu focus windows, FSM's inconsistent testimony date header, archaeological/state-territory distinctions in the Andes and North America, and publication/award milestones incorrectly pinned to a person's home city. Some were already corrected in V9; inspect the current record before reporting them as unfixed.

### Packet B — Global gaps and connected additions

Evaluate all 32 roadmap workstreams against the current data, with attention to weak sequences within broad region labels. Prioritize underrepresented societies and everyday experience alongside political institutions: Great Lakes/Congo, Sahel, Horn/eastern/southern Africa, pre-Goryeo Korea, Japanese regional/modern history, mainland and maritime Southeast Asia, South Asian regional institutions, later Central Asia, modern West Asia, distinct Indigenous North American sequences, Caribbean/Central American histories, pre-Inca Andes, Pacific networks and long Australian/New Guinea histories.

Return a ranked gap matrix. For a bounded first follow-up batch, propose 20–40 candidate records or substantial revisions only after deduplication. Prefer revising an existing weak ID over a near-duplicate. Connect political, social, cultural, place and biographical entries; do not produce another list of isolated famous monuments. The number is a planning range, not a publication quota.

Each candidate should include a proposed stable ID or existing target ID, English/Chinese title, type/region/workstream, qualified historical focus interval, representative location and its meaning, a bilingual narrative outline, 3–5 supported claims with source mapping, date/location uncertainty, related existing IDs and a reason it belongs in or out of the key political timeline. Include women and people beyond rulers where evidence supports a useful biography. Do not invent milestones, exact birth dates, personal itineraries or construction dates to fill a template.

### Packet C — Map evidence, separate from prose

Find bounded, reusable, dated map evidence for specific gaps. A map candidate must identify source vintage, depicted date, territorial meaning (administration, claim, influence, cultural distribution), license/derivation and known disagreement. Prioritize premodern regional gaps outside China and consequential transitions. A dated source map is not proof of annual frontiers; an article's lifespan is not permission to carry a polygon through that lifespan. Keep unsupported gaps visible.

For inherited waterways, walls, canals and roads, distinguish original feature/display parity from independent historical reconstruction. The source's water intervals are start-inclusive/end-exclusive; corridors are inclusive reference spans. Undated lines are geographic references. A lake edge is not a surveyed historic lake surface; a corridor is not a documented personal journey.

## Required research outputs

1. A claim-level correction register: current ID/claim, finding, supported amendment, sources actually inspected, conflicting evidence and unresolved questions.
2. A gap/delivery matrix for all 32 workstreams; no unsupported global percentage-complete score.
3. The bounded candidate/revision batch with bilingual outlines and a machine-readable field mapping to the current schema.
4. A source-access register distinguishing full relevant text, indexed extract, metadata, blocked retrieval and unread material. Report original versus derivative source families.
5. A separate geometry-evidence register; leave article and geometry acceptance independent.
6. A short list of held proposals that need further evidence rather than silently presenting them as settled history.

Provide exact inspectable public URLs and source-specific claim support. Explain when a conclusion is an inference. Model output is a research aid; it is not historical evidence itself.

## Integration constraints

- Keep a single shared Atlas/Timeline/Journeys/People/Places experience; do not split China into a separate add-on product.
- Main timeline bars are selected states/dynasties/comparable political formations. Events, biographies and places stay in search, map detail, milestones and related reading. Explicit secondary records stay outside the key view even with high importance.
- Retain frozen raw source IDs/hashes, explicit review overlays and source licenses. Never silently rewrite immutable input to hide an error.
- Preserve spherical polygon winding, holes and islands. Do not restore the full-globe fill defect. The requested Taiwan/mainland display shade is a palette convention; source records and their evidence remain inspectable.
- Keep English/Chinese claims and uncertainty aligned. A culture's focus interval is not an extinction date. Representative points are not precise borders, surveyed sites or guaranteed personal presence.
- Keep existing route evidence and schematic caveats. Linked ports do not by themselves prove a direct voyage. The current 15 mapped collections retain 126 stops; reading paths are not new route legs.
- Do not describe source availability, schema validation or test counts as historical correctness.

## Reproduce and verify

From `world/`, use Node 22+ and run `npm run check` (149 tests passed for V9). No package installation or GitHub Actions is needed. Serve `dist/` over HTTP, for example `python3 -m http.server 8080 --directory dist`.

Inspect `dist/data/expansion-*-v9.json` and `dist/core.mjs` for the record contract. Biography milestones require supported date, bilingual text and a location whose meaning is disclosed. Use `scripts/build-content-expansion-v9.mjs` after editing expansion files to rebuild hashes and courses, then rerun validation. The generator uses the separate `scripts/research-service-v9.json` disclosure; do not label a report complete or incorporated before it exists and has been reviewed.

Map-source rebuilding additionally needs the pinned upstream files described by each build script. Do not assume a repository checkout supplies unavailable source downloads or silently replace pinned versions. Use final geometry and immutable source inventories to detect accidental changes.

Historical review, translation review, local browser verification, public deployment verification and GitHub synchronization are separate evidence categories. Record only work actually performed.
