# World History Atlas local development

The active atlas is in `world/`. The original Jiangshan application outside that folder is a separate project; keep atlas changes within `world/`.

Read `world/CONTRIBUTING.md`, `world/docs/DATA_POLICY.md`, and `world/docs/NEXT_STEPS.md` before editorial work. Current research and verification records are under `world/docs/V11_*`. These documents distinguish source inspection from structural validation and specialist acceptance.

From `world/`, use Node.js 22 or later:

```sh
npm run build:content
npm run check
npm run serve
```

No dependency installation or application compilation is needed. The local server binds to `127.0.0.1:8080`; use `npm run serve -- --port 8081` if needed. It has a larger request queue for the atlas's concurrent local-data loads. The default stock Python server dropped some requests on this Mac; the socket-level cause was not proven.

V11 regional files are the current editable expansion inputs. The generator preserves the V9 and V10 input hashes and extends existing reading-path IDs. Keep historical release files, imported China data and geometry unchanged unless the task specifically requires a separately documented correction. New narrative dates and coordinates do not authorize new territorial geometry.

For UI/content integration, check bilingual search, People, related reading, life milestones, shared URLs and the affected reading path in the in-app browser. Tests check application/data contracts; historical source fit and translation still need editorial review.
