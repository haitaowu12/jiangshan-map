# Active World Atlas guidance

This scoped guide supersedes the root guide's V12-era input and verification pointers. Work within `world/`; preserve the original Jiangshan application outside it.

Read `CONTRIBUTING.md`, `docs/DATA_POLICY.md` and the current queue at the top of `docs/NEXT_STEPS.md`. `README.md` distinguishes the local candidate, published application, and narrative manifest. Release-specific notes under V12 and earlier are historical evidence.

The current narrative manifest is `dist/data/content-expansion-v15.json`. `npm run build:content` invokes the V15 generator and verifies the frozen V14 input baseline. `dist/reading-catalog.mjs` owns presentation-only reading overrides and chapter boundaries; those edits need no narrative regeneration. Preserve course IDs, original stops, map anchors and old shared links.

Run `npm run check` and inspect affected English/Chinese reading flows in the in-app browser. `npm run serve -- --port 8083` provides a loopback preview. Keep local verification and public delivery separate; do not claim learning outcomes from software tests.
