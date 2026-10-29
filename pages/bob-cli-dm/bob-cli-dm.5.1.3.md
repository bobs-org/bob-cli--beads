# Bead: bob-cli-dm.5.1.3 — Render task-theme pills in Reading view and query rows

[Bead Pages](../README.md) / [bob-cli-dm.5.1](bob-cli-dm.5.1.md) / bob-cli-dm.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-dm.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.5.md) · **Assignee:** `bob-cli-dm.5.1.3` · **Size:** medium
**Created:** 2026-10-28 17:46:54 EDT · **Closed:** 2026-10-28 19:07:16 EDT
**Plan:** [202610/ledger\_task\_theme\_mirror.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ledger_task_theme_mirror.md)

## Description

task-theme-rendered: reuse the mark model in Reading view, Tasks, and Dataview rows; preserve native content and inline markup, handle deferred query rendering, replace only explicit task-field Dataview chips, and support lazy hover, toggle restoration, and teardown. Complete cross-surface tests, docs, and deployment evidence for the child epic land agent.

## Notes

[2026-10-28T23:07:16Z · bob-cli-dm.5.1.3] Reading, Tasks, and Dataview task rows reuse the PT13 mark model: explicit [theme::]/ (theme::) fields wrap as pills with a native sibling; Dataview chips wrap only .dataview.inline-field theme keys on task rows; dashboard ctx.sourcePath is never the origin; deferred Tasks/Dataview rows retry like date marks (detached 3 / pending-data-task 60); toggle and unload restore natives. Verified: npm run build; npm test 4053/4053 including scripts/test-ledger-tools-task-theme-rendered.cjs (11) and test-ledger-tools-task-theme-marks.cjs; npm run docs:check; bob plugins sync --repo this checkout copied bob-ledger-tools manifest.json, main.js, styles.css. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-dm.5.1.2](bob-cli-dm.5.1.2.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.5.1.3/README.md) | [bob-cli-dm.5.1.3](bob-cli-dm.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ae40495`](https://github.com/bobs-org/bob-plugins/commit/ae40495ab5f98a458358dcfb62dffb5be51ccf98) | feat(ledger-tools): render task-theme pills in Reading view and query rows | [bob-cli-dm.5.1.3](bob-cli-dm.5.1.3.md) | 2026-10-28 19:09:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.5.1.3][1] | Need DECISIONS, notes, and whether earlier work landed | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.5.1.3/README.md

<!-- sase:referenced-by:end -->
