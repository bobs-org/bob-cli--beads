# Bead: bob-cli-3f.3 — bob-ledger-tools noteReady API

[Bead Pages](../README.md) / [bob-cli-3f](README.md) / bob-cli-3f.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0v5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v5.md) · **Assignee:** `bob-cli-3f.3` · **Size:** medium
**Created:** 2026-10-01 17:55:47 EDT · **Closed:** 2026-10-01 18:46:33 EDT
**Plan:** [202610/per\_note\_ready\_cap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/per_note_ready_cap.md)

## Description

ledger-api: add api.noteReady v1 (snapshot, forNote, counted, inCrowdedNote, groupLabel), built in one memoized O(tasks) pass with live invalidation. Also a stat-cached loadPlanCaps, a shared getFileCache frontmatter reader (fixes bob-cli-3e), and the R1–R14 JS vectors. Deploys the plugin.

## Notes

[2026-10-01T22:46:33Z · bob-cli-3f.3] ledger-api done: api.noteReady v1 (snapshot/forNote/counted/inCrowdedNote/groupLabel) in one memoized O(tasks) pass, stat-cached loadPlanCaps with maxReadyPerNote 1-999, shared noteFrontmatter reader fixing 3e, R1-R14 JS vectors in scripts/test-ledger-tools-note-ready.cjs (37 tests). Gates: npm test 1138/1138 incl. existing ready-badge/freshness/plan-budget suites, npm run validate 6/6, deployed bob-ledger-tools 1.15.0 via plugins sync, bob-cli tree untouched + cargo fmt clean, no epic symbols.

## Dependencies

- **Depends on:** [bob-cli-3f.1](bob-cli-3f.1.md) ✓ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-3f.4](bob-cli-3f.4.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3f.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.3/README.md) | [bob-cli-3f.3](bob-cli-3f.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@03fbd18`](https://github.com/bobs-org/bob-plugins/commit/03fbd18367f00fa6b2bdf997131588e0bd866d04) | feat(ledger-tools): per-note Ready cap api.noteReady v1 (1.15.0) | [bob-cli-3f.3](bob-cli-3f.3.md) | 2026-10-01 18:47:49 EDT |
