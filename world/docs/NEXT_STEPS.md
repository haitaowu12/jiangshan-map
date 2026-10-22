# Expansion priorities after v2

V2 establishes a broader learning atlas: 168 historical entries, 24 people with 75 milestones, 15 selected territorial snapshots, eight routes/networks and fourteen reading paths. The app now has comparative chronology, source panels, people and route navigation, a geographic challenge and a local notebook. These capabilities provide a foundation for deeper research; counts do not measure completeness.

## 1. Deepen regional history and everyday experience

The next content additions should fill a defined gap in place, period or subject. Prioritize sequences that let a reader follow change through time rather than adding isolated famous monuments.

Useful areas include West and Central African social and political history; Indigenous histories in the Americas and Oceania; South and Southeast Asian regional institutions and maritime societies; women beyond rulers and exceptional biographies; food, labour, technology and environment; and the local experiences of imperialism, resistance and decolonisation.

A regional pack should combine places, processes, people and contemporary viewpoints where evidence permits. Give living-community perspectives space alongside institutional summaries. Check English and Chinese terminology together, especially where names might imply a modern national identity or an abrupt end to a continuing culture.

**Acceptance:** inspected per-claim sources, explained focus intervals, representative locations, bilingual review and visible uncertainty. Record what remains missing. Preserve existing IDs when improving records.

## 2. Improve dated territories where gaps matter

The current layer contains 106 selected territory instances across 15 snapshots. It deliberately excludes shapes with known chronological or geographic problems. [MAP_METHODOLOGY.md](MAP_METHODOLOGY.md) is the current selection and exclusion record; the earlier geodata review describes the first prototype.

Priorities include usable source-backed snapshots before 500 BCE, better medieval coverage, regional detail across Africa and the Americas, and carefully dated twentieth-century transitions. Specific unresolved gaps include a suitable Ming outline for 1400 and a better Byzantine outline for 1200. Existing rejected shapes should not return simply because an empty region looks sparse.

Seek map evidence and reusable geometry for a specific year and claim. Review the territory's meaning as well as its label: direct administration, disputed claims, dependencies and influence cannot be treated as equivalent. Resolve the derivation of the three reused Jiangshan schematics where possible and retain all current notices in the meantime.

Additional snapshots should reduce large temporal gaps. They must not create the appearance of annual frontier knowledge through interpolation. A future interface could let readers choose exact available map years more directly while still distinguishing the selected story year.

**Acceptance:** immutable sources, reviewed chronology and broad geography, explicit geometry precision, retained licenses and provenance, and spherical rendering checks. Where evidence does not support a footprint, keep the gap visible and explain it.

## 3. Strengthen connections and person histories

Eight route/network collections now use 58 stops and 51 explicit connections. Extend them only when the connection itself is supported. A source that identifies two ports does not by itself establish a direct voyage between them.

Future work can add dated branches, uncertainty at the leg level and evidence distinguishing a documented journey from a long-running network. Keep undocumented arrival years empty. Do not turn all visits by a traveler into one continuous surveyed route. For forced migration and imperial expansion, retain the roles of coercion, resistance and unequal power.

People can gain more context through relationships to institutions, communities, texts and contemporaries. Additional milestones should explain a historical development rather than filling a predetermined biography template.

**Acceptance:** clear journey/network type, source-supported legs and milestones, honest schematic geometry, meaningful date notes and consistent references.

## 4. Build deeper teaching paths

The six original readings and eight new study guides already support structured exploration. The next improvement should test whether a learner can explain a comparison, distinguish evidence from interpretation and identify what the map leaves unknown.

Add source-reading activities, local or regional pathways and prompts comparing several types of evidence. A teacher-authored path could reuse stable record IDs and the existing notebook export. Keep learning tools useful without requiring accounts or a server.

The location challenge is an orientation activity. More substantial assessments should follow a learning goal and respect uncertain dates and representative points. Avoid scoring contested historical interpretations as a single correct fact.

**Acceptance:** clear audience and learning aim, inspectable evidence, questions consistent with the linked content, accessible controls and a way to revisit the supporting record.

## 5. Maintain evidence and application quality

Source pages, institutional interpretations and modern-period summaries can change. Keep reviewed dates and evidence notes meaningful, revisit broken or redirected links, and update specific claims when new evidence warrants it. Do not confuse URL availability with source accuracy.

Continue checking chronology, shared URLs, notebook imports, route references and map source hashes. For relevant interface changes, inspect the affected behavior at desktop and narrow widths, including keyboard focus and error states. Record checks actually performed; do not infer a completed browser review or deployment from a passing unit test.

The current territorial checks support technical integrity and limited geographic review, not independent verification of every border. A stronger future review should document source-map comparisons and disagreement at a useful geographic scale.

## 6. Keep the world extension independently maintainable

The delivery remains the **`world-history-atlas` branch with a `world/` directory** in the user's Jiangshan fork. The original China application on `main` remains separate. This layout lets the extension be reviewed without replacing the base experience.

The application directory is self-contained and can be moved to the root of a dedicated repository when repository creation is available. Preserve the data files, source-specific notices, provenance and attribution during that move. Update links and hosting paths as needed, then review the actual target checkout and preview.

A dedicated repository or publication is a separate delivery step. The project remains runnable as a static local app without a backend, package installation or a GitHub Actions workflow.
