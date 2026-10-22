# Verification notes

## Independent core probes

Run from the repository root:

```sh
node tests/core.test.mjs
```

The file uses Node's built-in test/assert modules and has no npm dependencies. The direct command runs the Node test harness. In the authoring executor, the default isolated test child process failed without a useful error. The package scripts use `--test-isolation=none`; both `npm test` and `npm run check` completed successfully with that setting.

Current result: **17 tests passed, 0 failed**.

The suite covers:

- no year zero and the adjacency of 1 BCE / 1 CE;
- year limits, invalid inputs and fractional-step handling;
- both languages' date display and single-year events;
- all **15,026** supported civil years through year → slider → year, plus bounded error when the slider position is integer-quantized;
- inclusive focus intervals and exact-year point events;
- combined time, region, theme, saved and bilingual search filters;
- regional spread and capacity in contemporary suggestions;
- unknown or malicious URL values, query length and stable encoded state round trips;
- credential-free HTTPS source URLs;
- malformed data records, missing localizations, invalid coordinates, duplicate IDs and invalid source objects;
- notebook schema, unknown IDs, oversized fields/counts, prototype-oriented keys, duplicate bookmarks and merge precedence.

Tests initially reproduced six failing cases. Repairs hardened coercion and interval matching, prevented fractional dates, filled contemporary suggestions after regional coverage, and made validation return errors for malformed data rather than throw.

## Asset geometry probe

A separate Node VM probe loaded the locally bundled D3 v7.9.0 and Natural Earth land data:

- 127 land features;
- spherical area 3.627891493630341 steradians (the geometry is not inverted into near-global fill);
- Equal Earth projection produced a finite SVG path with no `NaN` or `Infinity`;
- geographic bounds span −180° to 180° longitude and −90° to 83.64513° latitude.

File hashes and immutable source references are recorded in `dist/assets/PROVENANCE.json`.

## Independent application source review

The completed `dist/app.mjs` was inspected for map/time/filter consistency, notebook import and merge, source-link handling, journey references, marker keyboard behavior and selection focus. Follow-up inspection confirmed these repairs:

- year input limits now update when the timeline changes between BCE and CE, preventing a stale CE limit from blocking a BCE form submission;
- filtered-out selections are cleared; an explicit story selection from another region clears incompatible filters before revealing that story;
- mobile story selection brings the map/detail panel into view;
- the “Skip to stories” link preserves hash-based atlas state instead of replacing it with an unrelated fragment;
- the empty CSS import was removed.

The combined corpus passed structural validation with **62 records**, including **16 records active at 1200 CE**. Every stop in the fixed-year 1200 reading sequence exists and includes that year. This checks the sequence's mechanical premise, not the accuracy of its historical dates.

The notebook import UI caps files at 1 MiB before parsing; validation then checks known IDs, note lengths and record counts. Source URLs are validated before display; text, source fields and notes are escaped for HTML insertion. No browser execution was performed as part of this independent source review.

## Scope and limits

Core tests establish application mechanics and data structure, not historical accuracy or source fit. A source URL passing validation means it is an HTTPS URL without credentials; it does not mean its page was fetched or its claims verified.

The notebook import UI must impose a file-size cap before reading/parsing JSON. Core validation happens after parsing and limits individual note length and entry counts.

Desktop/mobile layout, keyboard focus, screen-reader experience, map interactions, actual browser storage, live publication and network error handling require browser or deployment checks beyond this core suite. Record those results separately rather than infer them from Node test success.

