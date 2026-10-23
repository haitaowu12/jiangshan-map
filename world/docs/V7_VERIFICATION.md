# V7 verification and remaining scope

23 October 2026. This release responds to disappearing intermediate-year shading, missing China map depth, thin political context elsewhere, and an overfilled timeline.

## What changed

The old temporal test established that at least one historical feature survived in each year. It did not establish regional coverage. Many existing intervals ended before the next checkpoint; the original China stage maps and settlement labels had also been left out of the renderer.

The runtime now composes three source types:

1. Premodern selected world outlines plus the source-defined China stage layer, replacing duplicate dynasty outlines. Political stages are preloaded and selected synchronously; administrative chunks load on local zoom with stale-phase checks.
2. From 1886 through 2019, exact-date CShapes periods sampled at 31 December of each selected year. Its state and dependency conventions, source geometry dates, and de jure limitations are visible. It is not a war-front reconstruction.
3. From 2020 through 2026, the existing dated Natural Earth country reference, with its source vintage displayed.

China adds 166 source stage selections, 377 stored political shapes, historical place labels, and 3,211 optional administrative shapes. These are inherited schematics, not independently reconstructed borders. Static neighbor templates with anachronisms remain excluded. Wu Zhou receives a separate 690–705 label correction; the original Tang label stays visible in its evidence. Source chronology conflicts and unresolved licensing provenance are documented in V7_CHINA_REVIEW.md and the source notice.

The main political timeline admits polity overviews only. It excludes events, people, cultures and place-occupation spans regardless of their importance or theme. It has key/all-state scope, a separate regional filter, time-window controls, bounded packing, and explicit regional expansion. Detail remains in map/search/reading. Modern continuing states have their own overviews instead of a mostly empty post-1922 political timeline.

The shared collection contains **1,369 entries**, including **112 polity overviews**: 52 new entries supplement the retained 1,317. This is a content expansion, not equal event-level coverage of all regions.

## Automated verification

`npm run check`: structural validator and **137 passing tests**. The added checks cover:

- Every annual CShapes sample from 1886 through 2019 (134 years), source-date eligibility, unique unit identities and bilingual label presence.
- German reunification, Soviet dissolution, Sudan/South Sudan, source polygon winding and representative geography checks.
- Every civil year in the China source display scope from 403 BCE through 2026, unique stage choice, source-phase transitions, modern empty stage, administrative lazy loading/deduplication, and exclusive settlement disappearance dates.
- Political-only timeline membership, selected-year packing priority, explicit omitted-state accounting, six-region modern overview coverage, source-stage captions without fabricated snapshot dates, and balanced nearby events despite imported collection density.
- The previous source import accounting, notebook, discovery, bilingual data, URL, chronology and map regression checks.

Structural validation now reads all three V7 addition files as well as the retained narrative, biography and imported event collections. Passing it does not verify every historical claim or boundary vertex.

## Browser observations

Checked the local preview in the supported browser. These were actual UI interactions, not JSON replay:

- Intermediate years 950, 1050, 1250 and 1630 retain China phase shading. At 1250 the source stage is 1234–1252; at 1630 it is 1616–1642. These are visibly source schematic windows, not invented annual surveys.
- Annual modern views at 1887, 1955, 1990, 1991, 1992, 2005 and 2015 render 129, 169, 157, 172, 175, 178 and 181 source-coded units respectively. The 2025 view renders the 242-unit contemporary reference.
- The Soviet label appears in the checked 1990 year-end context; the checked 1991 and 1992 year-end contexts show Russia. Checked 1990 no longer shows divided Germany.
- Selecting the 1050 Song source outline opens its stage evidence, relevant polity overviews and events. Zooming revealed 22 historical place labels and 294 regional outlines in the checked view. These are observations of one viewport, not exhaustive label counts.
- Keyboard selection of the 1992 Russia source unit writes `unit=CS365` into the shared URL without changing the year; reloading restores the country detail and year.
- The timeline default renders state/dynasty bars and excludes the short event and biography clutter seen in V6. Region and time-window controls work. A narrow-view check found no non-political bars.
- Narrow QA used 390px and 320px iframe browsing contexts, with Chinese and English respectively. Their available root widths after browser scrollbars were 375px and 305px. Both rendered their maps without document horizontal overflow. The timeline scrolls within its own viewport. These were responsive browser-context checks, not physical-device tests.

A pointer-based automated click on a large SVG territory did not establish selection, so country sharing was verified through the supported keyboard path and its visible result. No claim is made that every small territory is easy to hit by touch.

## Remaining limitations

- Premodern global polygon coverage is still selective; one populated region does not prove worldwide coverage. Source presence and readable shading do not certify annual borders.
- The China source layer restores much of the map structure, but is inherited and has not had all 377 shapes independently checked. Known review limits and source chronology disagreements remain visible. Historical hydrology and every original transport interaction are not reproduced.
- Other regions do not match China's 975 inherited-event density. V7 adds political sequences and modern continuity, not a complete world-history curriculum.
- CShapes is a source-coded de jure international-system dataset including dependencies, with omissions and generalization. Its unit count is not a sovereign-country count and differs from Natural Earth's units. Its CC BY-NC-SA 4.0 license is preserved separately.
- Browser work checks selected flows and years; it does not establish full accessibility, every device interaction, every historical label, or every source-to-claim fit.
