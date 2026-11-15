# Bead: bob-cli-ln — Generated "## Areas" catalogs for area notes and the area root

[Bead Pages](../README.md) / bob-cli-ln

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e2.md) · **Assignee:** `bob-cli-ln.land`
**Created:** 2026-11-14 16:33:03 EST · **Closed:** 2026-11-15 07:19:25 EST
**Plan:** [202611/areas\_catalog.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/areas_catalog.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md

<!-- sase:links:end -->

## Description

Every area note with sub-areas, and the root note `[[area]]` resolves to (today `area.md`), carries a bob-owned, nested `## Areas` catalog that stays correct through `bob areas sync` and nightly, always sits above `## Projects`, is protected from capture, turns the "areas parent only areas" convention into checked findings, and renders as a calm, colored map card in Obsidian while staying readable as plain Markdown everywhere else.

## Notes

[2026-11-15T12:19:00Z · bob-cli-ln.land] LAND FOLLOW-UP TRIAGE (bob-cli-ln.land): (1) ln.3 #1 and ln.4 #1, docs-check lychee bank.md Bank-walk link: DECLINED, already fixed by 92f5d1c8 / closed bob-cli-lo; just docs-check now passes offline lychee. (2) ln.5 #1, json-outputs.md word cap: DECLINED, resolved; bob-docs lint passes on current master. (3) ln.5 #2 and ln.6 #3, glossary.md generated drift: CAUSED BY THIS EPIC (57e0f3c8 edited glossary:area-note without just docs-gen; bob-plugins docs:check runs bob-cli's gate). Fixed in this landing by regenerating docs/reference/glossary.md. (4) ln.7 #1, every_native_command_is_on_exactly_one_canonical_path 89 vs 88: CAUSED BY THIS EPIC (81a4b022 mounted AreasSync without updating the expected list). Fixed in this landing. (5) ln.5 #3/#5 and ln.6 #2, full npm test timing flakes: corroborated with +1 on bob-cli-io (frees-marks), bob-cli-km (event-link-times), bob-cli-ki (keep-moving-marks-surface), bob-cli-ju (off-clock-link-chips), and bob-cli-3w (stage ranker 16.12 ms). The relation-chips MN-click cursor/focus failure (ln.5 #5) had no task, so it was filed as new flake task bob-cli-lp (small, ready; also seen in kb.2 #1; 3/3 serial isolated runs pass). (6) ln.6 #1, CI=true Chromium hard-fail: DECLINED. It throws only when CI is set, the deliberate contract from closed bob-cli-f1, matching the bob-cli-lj.land precedent; with CI unset on apollo it skips.

[2026-11-15T12:19:25Z · bob-cli-ln.land] Landing verified (bob-cli-ln.land). All 7 phases closed, and every child note was reviewed. Source and commits were checked against the plan: 13fdf78d (AREAS spec first in GENERATED_CATALOGS, PROJECTS AfterSectionThenFirstH2(Areas), heading adoption via adopted_insert for every plan_host family including records, areas_section_generated guard); 719dbd45 (snapshot root retention, graph, nested planner); 92813d08 (areas list/check, JSON v1, registration in native.rs, runner.rs, completion tree, and command-mode rows); 81a4b022 (guarded sync, nightly areas step before projects, Highlights [!areas] test, CLI integration tests); 57e0f3c8 (glossary:area-note only, per memory_glossary_area=yes and memory_decision_record=no). bob-plugins 6615a3f, 5023787, and 3a41a3e (bob-ledger-tools 1.118.0) hold the Areas card. card_auto_sync=no is honored (sync only via the explicit click path), and card_titles=tooltip is honored (title in the tooltip, stem text stays visible). The 15 areas data and catalog tests pass. The real vault is already synced (29ceef997 'areas: sync catalogs (5 notes)'). A read-only 'areas check -b ~/bob' shows ok, 19 areas, 7 top-level, 5 hosts (area, cash, gtd, inbox, love) all current, and 0 findings. Epic-caused gaps fixed in this landing: AreasSync added to the runner canonical-path expected list (89 vs 88 failure); docs/reference/glossary.md regenerated (stale since 57e0f3c8); and the phase-1 docs sentences that were missing were added (projects.md first-write after ## Areas plus adoption, notebooks.md and records.md adoption, capture.md and notebooks.md areas_section_generated). Integration: the non-epic commits since the epic began (88fb9cb4, ff272bc6, 92f5d1c8, 49231b37 gmail) touch no catalog, nightly, or registration code. The GENERATED_CATALOGS consumers (capture sections, drawers) pick up Areas automatically. The plugin project-reversal heading logic never sees ## Areas hosts. just check passes, and just docs-check passes (lint, drift, strict build, offline lychee). No --epic-symbol entries. Follow-up triage is recorded in the epic notes: +1 on io, km, ki, ju, and 3w; new flake task bob-cli-lp; Chromium CI, bank link, and json cap declined.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ln.1](bob-cli-ln.1.md) | Shared catalog engine - AREAS spec, placement order, heading adoption, capture guard | ✓ closed | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-ln.2](bob-cli-ln.2.md) | Area graph and pure catalog planner | ✓ closed | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-ln.3](bob-cli-ln.3.md) | bob areas list and check | ✓ closed | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-ln.4](bob-cli-ln.4.md) | bob areas sync, nightly step, and Highlights coverage | ✓ closed | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-ln.5](bob-cli-ln.5.md) | bob-ledger-tools Areas card shell | ✓ closed | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-ln.6](bob-cli-ln.6.md) | Areas card folds, chips, tooltips, and add-summary | ✓ closed | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-ln.7](bob-cli-ln.7.md) | Decision record and glossary update | ✓ closed | small | 2026-11-14 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ln: Generated \"## Areas\" catalogs for area notes and the area root [closed]"]
    n1["bob-cli-ln.1: Shared catalog engine - AREAS spec, placement order, heading adoption, capture guard [closed]"]
    n2["bob-cli-ln.2: Area graph and pure catalog planner [closed]"]
    n3["bob-cli-ln.3: bob areas list and check [closed]"]
    n4["bob-cli-ln.4: bob areas sync, nightly step, and Highlights coverage [closed]"]
    n5["bob-cli-ln.5: bob-ledger-tools Areas card shell [closed]"]
    n6["bob-cli-ln.6: Areas card folds, chips, tooltips, and add-summary [closed]"]
    n7["bob-cli-ln.7: Decision record and glossary update [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
    n3 -.-> n5
    n4 -.-> n6
    n4 -.-> n7
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ln.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.1/README.md) | [bob-cli-ln.1](bob-cli-ln.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ln.2.md) | [bob-cli-ln.2](bob-cli-ln.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ln.3.md) | [bob-cli-ln.3](bob-cli-ln.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.4/README.md) | [bob-cli-ln.4](bob-cli-ln.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.5/README.md) | [bob-cli-ln.5](bob-cli-ln.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.6/README.md) | [bob-cli-ln.6](bob-cli-ln.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.7/README.md) | [bob-cli-ln.7](bob-cli-ln.7.md) | 1 |
| [bbugyi200.apollo.bob-cli-ln.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.land/README.md) | [bob-cli-ln](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`13fdf78`](https://github.com/bobs-org/bob-cli/commit/13fdf78d201c696cb0501c1b6b60c45246db1b45) | feat(areas): shared catalog engine for generated Areas catalogs | [bob-cli-ln.1](bob-cli-ln.1.md) | 2026-11-14 17:15:25 EST |
| bob-cli | [`719dbd4`](https://github.com/bobs-org/bob-cli/commit/719dbd45cbf4eaf21cdf96bd3f46eaa6da2c5974) | feat(areas): validated area graph and pure nested catalog planner | [bob-cli-ln.2](bob-cli-ln.2.md) | 2026-11-14 19:10:11 EST |
| bob-cli | [`92813d0`](https://github.com/bobs-org/bob-cli/commit/92813d08ea57e1f2c5cff2ae6a85e0232ed0390e) | feat(areas): add read-only bob areas list and check | [bob-cli-ln.3](bob-cli-ln.3.md) | 2026-11-14 21:17:28 EST |
| bob-cli | [`81a4b02`](https://github.com/bobs-org/bob-cli/commit/81a4b022a8037eee9f734f50ade09c284362dd89) | feat(areas): add guarded areas sync writer, nightly step, and coverage | [bob-cli-ln.4](bob-cli-ln.4.md) | 2026-11-14 22:31:31 EST |
| bob-cli | [`57e0f3c`](https://github.com/bobs-org/bob-cli/commit/57e0f3c8bc4e5291b375058b6c51b1a26842b37d) | docs(memory): note optional area summary in Area Note glossary strand | [bob-cli-ln.7](bob-cli-ln.7.md) | 2026-11-14 22:58:39 EST |
| bob-plugins | [`bob-plugins@5023787`](https://github.com/bobs-org/bob-plugins/commit/5023787e4064941477fdf0d7cc78f8fbd5db8a48) | fix(areas): bound failed refresh retries and restore card icon | [bob-cli-ln.5](bob-cli-ln.5.md) | 2026-11-15 06:08:39 EST |
| bob-plugins | [`bob-plugins@3a41a3e`](https://github.com/bobs-org/bob-plugins/commit/3a41a3e901edac12252458d074e2655225e5b190) | feat(areas): add Areas card folds, chips, tooltips, and add-summary | [bob-cli-ln.6](bob-cli-ln.6.md) | 2026-11-15 06:37:34 EST |
| bob-cli | [`86ec139`](https://github.com/bobs-org/bob-cli/commit/86ec139cf1c114754dc1db698c960f912aa272f6) | fix(areas): land Areas catalogs epic with command-count, glossary, and catalog docs fixes | [bob-cli-ln](README.md) | 2026-11-15 07:21:59 EST |
