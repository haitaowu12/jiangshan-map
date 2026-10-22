# V2 verification — 22 October 2026

## Delivered collection

The final validator reports 192 entries: 168 historical records and 24 biographies. There are 75 biographical milestones; 8 journey/network layers with 58 stops and 51 explicit legs; 6 original reading sequences plus 8 study guides; and 15 dated territorial snapshots with 106 feature instances representing 67 polity IDs. The fixed-year 1200 reading sequence now visits all nine regions.

The regional entry counts are Africa 29, West/Central Asia 23, Europe 26, South Asia 18, East Asia 29, Southeast Asia 15, North America 15, Latin America 20, and Oceania 17. Across record, route and territory evidence lists, the validator counts 298 distinct source URLs after removing fragment identifiers. This is a provenance count, not a claim of independent historical peer review.

## Automated checks

`npm run check` passes the structural validator and 37 Node tests. No dependency installation is needed. The suites cover civil chronology without year zero; slider and URL behavior; inclusive focus intervals and combined filters; comparison selection; safe HTTPS sources; notebook validation and merge rules; snapshot selection that never pulls a future map backward; endpoint visibility in chronology bars; geographic distance across the antimeridian; bounded challenge scoring; dated biographies and journeys; explicit network legs; and valid study-guide references.

The structural validator checks the complete combined record set, all course/route references, bilingual field presence, valid coordinates and dates, unique IDs, snapshot membership/counts, three historical layer checksums/notices, and four vendored asset checksums/notices. It does not prove that every narrative claim or border vertex is historically correct.

`node --check dist/app.mjs` and `git diff --check` pass. Historical geometry additionally received the projection, winding, source-date and coarse comparison checks documented in [MAP_METHODOLOGY.md](MAP_METHODOLOGY.md), [map-validation.json](map-validation.json), and [map-modern-comparison.json](map-modern-comparison.json).

## Browser acceptance

The application was exercised in Chrome against the managed local preview. These were interaction checks, not merely screenshots of a static mockup:

- The final home view loads 192 entries and 15 maps; 24 records are active at 1200, including Latin American material added during the coverage review.
- The 1200 reading path contains nine stops across nine regions. Advancing to Chan Chan retains 1200; reloading preserves the path and its second stop.
- The full chronology contains all nine regional lanes. Its 600-year view around 1200 renders 69 entries, and changing the time window works.
- Roman territory in 200 CE opens its AWMC evidence and ODbL attribution. Opening its related Rome story retains 200 CE. Modern outlines and previous-snapshot overlays can be toggled independently.
- English/Chinese search returns the relevant records. The Chang’an place-history panel links Zhou, Qin, Han, Sui, Tang, Xuanzang and the Silk Roads with stated distances and periods.
- Biographies render their milestones. Xuanzang’s approximate Nalanda study date is visibly qualified. Selected milestone years and map locations move together.
- The Beagle journey advances from its first to its next dated stop. The Salt March’s final stop displays 5–6 April 1930 and distinguishes arrival from the salt-law action. Reloading restores stop 7 of 7.
- A study guide opens its reading list, questions and comparison activity; finishing its reading path returns to the guide. A shared guide step survives reload.
- A five-round map challenge was completed through the accessible coordinate form. It displays a distance, bounded score, target and guess, cumulative results, and links back to the selected histories. The close-to-target Mohenjo-daro check reported approximately 5 km and 997/1000.
- A notebook note survived reload and rendered literal markup as text. No injected bold element appeared. The temporary test note and bookmark were restored to their prior values afterward. Comparing Southern Song and Abbasid entries produced the correct overlapping focus interval, 1127–1258.
- Responsive harnesses used 390px and 320px frames in English and Chinese. Their content widths were 375px and 305px with scrollbars, respectively, and neither body overflowed horizontally. The mobile reading panel leaves map space above it. Milestone navigation was also exercised with a direct pointer tap.
- The inspected browser console records contained no errors from the application origin. Browser-extension metadata errors were excluded from application findings.

The temporary responsive harness is not part of the shipped application. Screenshots: [overview](preview-v2-20261022.jpg), [parallel timeline](timeline-v2-20261022.jpg), [mobile](mobile-v2-verified-20261022.jpg).

## Limits of this verification

The mobile checks use browser frames, not physical iOS/Android devices. Safari, Firefox, screen readers and the full range of reduced-motion/assistive-technology configurations were not independently exercised. No blanket WCAG conformance claim is made. Notebook JSON parsing has regression coverage; a final browser file-picker import/export cycle was not repeated during this v2 pass.

Preview acceptance and production deployment are separate checks. This document records the source/data/preview verification; publication is confirmed separately by the hosting deployment result. Historical coverage remains selective, and territory maps retain their actual source dates rather than claiming annual reconstruction.
