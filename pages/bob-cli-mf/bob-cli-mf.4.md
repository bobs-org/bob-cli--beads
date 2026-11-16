# Bead: bob-cli-mf.4 — Album Schema Card visual refresh and region painting

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.4` · **Size:** medium
**Created:** 2026-11-16 15:38:38 EST · **Closed:** 2026-11-16 17:18:53 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

album-card-shell: give the album card one title line, the details row as the header subtitle, pills, a one-line status rule, and a contextual hint strip with a ⋯ action list. Remove Preview this edit, latch Enter, and repaint regions instead of rebuilding the modal.

## Notes

[2026-11-16T22:18:20Z · bob-cli-mf.4] PROPOSED FOLLOW-UP: test-ledger-tools-bank-setup.cjs fails on HEAD after e35afc1 — category.set label is ☕ Cafe vs expected Cafe (lines 888 and 967) and q-cancel while a focused input is undefined; confirmed by overlaying HEAD main.js

[2026-11-16T22:18:36Z · bob-cli-mf.4] PROPOSED FOLLOW-UP: full npm test also reds on this tree for unrelated suites — Chromium missing for command-mode sheet-sequence-dom, perf budgets, walkMode API, navigation period-links, block-marks hardcoded dates, priority notice hex, bracket-mode indicator; album-header and shell were 38/38 green

[2026-11-16T22:18:37Z · bob-cli-mf.4] PROPOSED FOLLOW-UP: capture light and dark Schema Card screenshots of browsing, a stage, a refusal, and the ⋯ list — Obsidian snap at /snap/obsidian/current/app/obsidian is not executable and xvfb-run is not on PATH in this workspace

[2026-11-16T22:18:53Z · bob-cli-mf.4] Verified album-card-shell in bob-plugins (bob-ledger-tools 1.122.0). Region painters (header/lint/body/stage/status/hints) keep body and stage input node identity across selection and session paints; IME composition skips restage. Header is one title line plus details as subtitle; pills, count pills, dashed +choice/+field, 3px status rule hidden when empty, hint strip with ⋯ All actions. Preview this edit removed; stage is Save ⏎ / Cancel esc. Enter latches a pending preview of the current revision and applies when it succeeds; typing clears the latch; refused Enter does not re-preview; stale Save still runs schemaApply. album-header 34/34, shell 4/4, stats CSS contract 15/15, build:check, docs:check. bob plugins sync -p bob-ledger-tools copied manifest/main.js/styles. Light/dark screenshots skipped: Obsidian snap not executable and xvfb-run not on PATH. PROPOSED FOLLOW-UP notes record HEAD-reproducing npm-test reds (bank-setup emoji labels after e35afc1; unrelated Chromium/walkMode/period-links/block-marks/perf). No --epic-symbol leftovers. Parent epic bob-cli-mf left open.

## Dependencies

- **Depends on:** [bob-cli-mf.2](bob-cli-mf.2.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mf.5](bob-cli-mf.5.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.4/README.md) | [bob-cli-mf.4](bob-cli-mf.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3136865`](https://github.com/bobs-org/bob-plugins/commit/313686540a2b60943efce67ae2d8e50381a8a5fb) | feat(bob-ledger-tools): refresh Album Schema Card shell and region paint | [bob-cli-mf.4](bob-cli-mf.4.md) | 2026-11-16 17:20:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mf.4][1] | Need notes, remaining work, and design file from earlier agents before close-out | 6 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.4/README.md

<!-- sase:referenced-by:end -->
