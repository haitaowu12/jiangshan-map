# China map gaps publication receipt

- Reviewed implementation: `51094c58897b11ea309f9d77dea53f429fa5e418` on `world-history-atlas`.
- Exact atlas `world/` tree and Sites source tree: `370596b4c610bd5fc5554f944070807236d61ec6`.
- Sites project `appgprj_6ad99670954c81919b26d00c89ff19f4`, source commit `eddb8a248965bd31046edbf4570fb794cde5e3f9`, saved version 34 (`appgprj_6ad99670954c81919b26d00c89ff19f4~appgver_75979829e1a881918f3f740804cd6d92`), deployment `appgdep_6ae2cd3f48a08191ba03af5adc0ab2e3`: succeeded, public audience unchanged.
- Local source-helper tar SHA-256 `2f3a50e9294c3fce2deba3e28921d1c8deb09cbf620d33623f29229b9fbc216a`; the saved archive service reported its own content hash `sha256:c11fc1e3e62c1c8c932b07ebf7eb453976b4e52ba62ab89d0a0beceb9111dfd0` and 486 files.
- Validation: `npm run check` passed structural validation and 291 tests; after the final source-credit text edit, the affected focused checks and JavaScript syntax check passed. The local and deployed Site were checked in the in-app browser at 1200 and 1415, including Chinese notes, source dates, credits and the Ming-related story correction. Source regions were visually checked against coastlines and inland geography. Local browser console reported no warnings or errors.
- GitHub branch push confirmed. The repository reported zero Actions runs after the implementation push; no action-based publication was used.
- **Known gaps:** 400 BCE and 1600 CE are not resolved by this release. The 1141 outline is a fixed, approximate source map shown only in the reviewed periods; Jin's northeast is cropped. The 1415 Ming source is restricted to 1415–1417 and combines unevenly administered frontiers and occupied territory. See [the evidence review](CHINA_MAP_GAPS_2026_10_28.md).

This receipt is a documentation-only commit after publication; the published artifact is the exact tree at the implementation commit above, not this later receipt commit.
