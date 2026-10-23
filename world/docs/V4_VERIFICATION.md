# V4 verification: continuous map context and deeper history

Verification performed on 23 October 2026 UTC. This record describes the checked source package and managed browser preview. A successful local check is not, by itself, proof of a GitHub push or a live deployment.

## Result and scope

V4 fixes the empty map between V3's exact source checkpoints. The renderer now selects eligible outlines from explicitly reviewed phases and shows their original source years. It does not interpolate frontiers or equate an entire dynasty's lifespan with unchanged territory. Mixed source dates remain labeled historical context.

The package contains 240 historical entries and 24 biographies, 75 person milestones, 43 source checkpoints, 516 historical feature instances, 180 state/cultural-region identities, 242 contemporary map units, eight routes/networks, seven guided readings and twelve study guides. The structural validator counts 549 distinct source pages. These counts describe the collection, not comprehensive world-history coverage or the number of sovereign states.

## Changes checked

- Historical shading, map names, legends and evidence panels use the same per-feature temporal selection. Exact source years and selected years are distinct throughout the interface.
- An outline outside its source year needs a finite reviewed interval. Earlier use of a later source also requires an explicit backward-review decision. Only one phase per polity is selected.
- Modern context covers the reviewed 2011–2026 annual range. The 2011–2013 Russia and Ukraine units use their actual 2010 historical geometry, preserving its sources and license. Later Natural Earth reference geometry keeps its 2022 vintage visible.
- Dated names and Palestine's dated category/notes use the selected year. The country directory explicitly opens 2026, while map selection and country share links preserve their existing year.
- Country and state names use stronger halos and screen-space collision checks. Selected or hovered labels have priority; story labels avoid territory-label boxes. Full names such as United Kingdom and Russian Empire are preserved.
- Geographic area/anchor calculations and projected paths are cached. Pointer input is coalesced to the latest requested year per animation frame. Direct navigation cancels an older queued update.
- Keyboard arrows advance one civil year, Shift plus an arrow advances ten, Page Up/Down advances a century, and Home/End selects the time bounds. This fixes an observed rounding problem where a native range arrow could stay on the same year. There is no year zero.
- If shading or labels are disabled, the map exposes a direct control to restore them.
- The 46 new bilingual entries include two key facts each, dated interpretation, per-record references and related-reading links. Three new study guides reuse the evidence-bearing records.

## Automated checks

`npm run check` completed successfully against the final data and application source:

| Check | Result |
| --- | --- |
| Structural validator | Passed: identifiers, civil years, bilingual fields, related-reading/course references, source URL format, manifest membership and file checksums |
| Full Node test suite | **88 passed; 0 failed** |
| Focused temporal/modern-map/scheduler tests | **51 passed**, included in the full suite |
| Civil-year continuity sweep | Some reviewed map context in every one of the **4,526 civil years from 2500 BCE through 2026** |
| Map chunk integrity | 17 historical layers, seven country chunks and two dispute overlays discovered through their manifests; every map chunk below 450,000 bytes |
| JavaScript parsing | `node --check dist/app.mjs` passed |

The generated map-data review separately reports some eligible historical context from 2600 BCE through 2010 CE. Neither continuity result means that every region is shaded or that an outline is an annual frontier survey.

Transition regressions cover the USSR, divided Germany, Ming, Qing, the Russian Empire and separate Yugoslav phases. Targeted geometric checks protect the 2011–2013 Crimea assignment and the exclusion of the Irish Free State from later UK outlines. A final review caught the 1783 Russian outline being displayed too early; its interval now starts in 1783, and a dated 1715 predecessor excludes Simferopol at 1750. See [the temporal review](V4_TEMPORAL_REVIEW.md) for evidence, exact assertions and limits.

## Browser acceptance

The managed local preview was exercised through the visible interface. It was not tested through an uninstrumented live production deployment.

| Interaction | Observed result |
| --- | --- |
| Year form at 2500 BCE, 2000 BCE, 950, 1150, 1750, 1972, 1992, 2011, 2013, 2014, 2025 and 2026 | Nonempty shaded features and visible names at every checked year; source dates remain separate |
| 1972 → 1992 → 2026 | USSR present in the checked 1972 context and absent at 1992 and 2026 |
| 2011 and 2013 | Country map reports both 2010 and 2022 outline sources; 242 map units |
| Ukraine selection at 2011, followed by page reload | Detail remains at 2011 with a 2010 outline; URL retains `country=UKR` and `year=2011` |
| Palestine evidence-card selection at 2011 | Detail uses the earlier category and explicitly distinguishes the later 2012 UN observer-State change |
| About these outlines | Lists current features and their source/review periods; selecting a card preserves the year |
| Slider keyboard arrow at 1750 | Advances to 1751 while keeping shading visible |
| Slider keyboard arrow at 1 BCE | Advances directly to 1 CE |
| Labels disabled, then Show map names | Names disappear when disabled and the recovery control restores them |
| Chinese interface at 1750 | Chinese map names, status text and date labels render |
| New Malaya entry | Two key facts, three references and four related-reading links render |
| New self-government study guide | Twelve linked records, three questions and the evidence-based activity render |
| 390- and 320-pixel responsive frames | Historical and contemporary shading/names visible; no horizontal page overflow (375/305 CSS-pixel body widths after scrollbars) |
| Qing evidence selection in the 390-pixel frame | Visible 275-pixel detail panel; selected year 1750 and outline source 1715 remain distinct |
| Final corrected source reload | The 1750 map uses `1715-russian`, with source year 1715 |

No atlas initialization error was observed in the filtered browser log. Browser-extension metadata errors were unrelated to the application and are not treated as atlas errors. Screenshots were captured from the final refreshed source, and the temporary responsive harness was removed before packaging.

- [Desktop preview](preview-v4-20261022.jpg)
- [Responsive overview](mobile-v4-20261022.jpg)

## Remaining limits

The map is a selective educational atlas. Some regions have no reviewed political outline at a given year, and some country panels do not yet contain a locally pinned narrative. Early cultural footprints are not claims of unified political rule. Source scale and disputed control remain source-specific. The new instances have chronology and broad-geography review, but every frontier vertex has not been independently reconstructed or validated across its display period.

Performance changes were checked functionally and in the browser; no controlled frame-rate or network benchmark is claimed. All current map chunks still load during initialization. The application remains buildless and self-contained, while external references require internet access.

See [history research](V4_HISTORY_RESEARCH.md), [map context review](MAP_CONTEXT_V4.md), [map methodology](MAP_METHODOLOGY.md), [contemporary methodology](CONTEMPORARY_MAP_METHODOLOGY.md) and [remaining priorities](NEXT_STEPS.md).
