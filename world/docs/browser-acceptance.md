> Historical browser acceptance for the first edition. The expanded application is covered by [V2_VERIFICATION.md](V2_VERIFICATION.md).

# Browser acceptance — first edition

Checked with the managed Chromium preview of this source on 21 October 2026 (Vancouver date). This is browser QA, separate from structural validation and historical source review.

## Observed passing

- The physical world map and local history JSON load; 16 stories match 1200 CE from the 62-record collection.
- Selecting Great Zimbabwe opens its narrative, date note, representative-location statement, source link and contemporaries.
- Comparing Great Zimbabwe with Cahokia shows the overlapping focus period 1100–1400 CE and retains each source/date note.
- Filtering to Africa clears an excluded selected story and removes its pin. The filtered count and visible marker agree.
- The fixed-year journey keeps 1200 CE when advancing from Cahokia to Great Zimbabwe.
- English UI search for the Chinese term 印加 returns the Andean road and Inca entries in all-time mode.
- Switching to Chinese updates the visible UI and chronology. Jumping to 13,000 BCE sets the input maximum to 13000; the native form accepts Go.
- A note containing an HTML-like image tag renders as text. The notebook DOM contains no injected image.
- Notes and bookmarks survive a page reload on the same origin.
- A notebook JSON file imports through the file chooser. Export downloads JSON; the exported version, bookmarks and imported note match the expected values when read back from the downloaded file.
- Responsive layouts checked in 390- and 320-pixel iframe viewports, including Chinese. Actual content widths were 375/305 pixels after classic scrollbars, with no horizontal document overflow. Story selection scrolls the detail panel into view. Crowded narrow Chinese timeline labels and the header were repaired and visually rechecked.
- The desktop overview was captured in `preview.jpg` from the final application code/data.

## Limits

The narrow layouts were browser viewports, not tests on physical phones or Safari. This pass does not establish every keyboard/screen-reader combination, browser engine, hosting authentication path, historical correctness, or coverage completeness. Browser-extension telemetry errors were observed; no application error was identified in the exercised behaviors. Source links were researched through retrieval, not all followed again in this browser pass. Test notebook files and the temporary responsive harness are not part of the distributed application.
