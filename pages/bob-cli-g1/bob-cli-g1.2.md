# Bead: bob-cli-g1.2 — The mark in bob-ledger-tools (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-g1](README.md) / bob-cli-g1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.176](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.176.md) · **Size:** medium
**Created:** 2026-11-02 12:45:29 EST · **Closed:** 2026-11-02 14:42:12 EST
**Plan:** [202611/ledger\_frees\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ledger_frees_marks.md)

## Description

ledger_mark: implement the pure core, Live Preview and Reading mixin, CSS, wiring, vector tests with BLOCKS parity, docs inventory, and manifest bump; build, test, sync.

## Notes

[2026-11-02T19:13:16Z · bob-cli-g1.2--1] PROPOSED FOLLOW-UP: Regenerate the published docs glossary in bob-cli — npm run docs:check reports docs/reference/glossary.md out of date; the same failure reproduces from a clean bob-plugins worktree at base af97bcd.

[2026-11-02T19:28:46Z · bob-cli-g1.2--3] PROPOSED FOLLOW-UP: Restore the bob-plugins test baseline — npm test reproduces these seven failures on clean af97bcd and this phase tree: the two wikilink index performance budgets, freshness reload event, keep-inbox retry-time expectation, note-ready startup scan count, relation-index startup completion, and Pending scheduled-status expectation.

[2026-11-02T19:42:04Z · bob-cli-g1.2--4] PROPOSED FOLLOW-UP: Rebase frees-marks onto canonical 93d3859/289f764 then sync — bob plugins sync --repo refuses without -F because the phase tree sits on stale base af97bcd while canonical added block-reason chips and CSS-only block marks in the same files (141-blocks-model.js, styles.css, main.js); forcing would regress the vault deploy, so the land agent should rebase and sync.

[2026-11-02T19:42:12Z · bob-cli-g1.2--4] Verified: new frees-marks vectors 10/10 pass; npm run validate=0 and docs:check=0; full npm test shows only 5 pre-existing baseline failures (recorded) plus a motion-harness Chromium timeout that passes isolated in ~1.5s; lifecycle fragment limit fixed at 999 lines; read-only smoke with real plugin core confirms [[sase#^ref-task-backlog-cleanup-chain-review]] frees 1 with tooltip and BLOCKS parity; epic-symbols clean; vault sync deferred (refuses without -F on stale base, recorded as PROPOSED FOLLOW-UP for rebase+sync).

## Dependencies

- **Depends on:** [bob-cli-g1.1](bob-cli-g1.1.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-g1.3](bob-cli-g1.3.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-g1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-g1.2.md) | [bob-cli-g1.2](bob-cli-g1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f824dd1`](https://github.com/bobs-org/bob-plugins/commit/f824dd1c1f32031e02421261c1a269d3ae262026) | feat(ledger-tools): show quiet frees-N marks after last-blocker ledger links | [bob-cli-g1.2](bob-cli-g1.2.md) | 2026-11-02 14:45:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g1.2--4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-g1.2.md

<!-- sase:referenced-by:end -->
