# Bead: bob-cli-nh.6.1.2 — Shared Reading and Live Preview host lifecycle

[Bead Pages](../README.md) / [bob-cli-nh.6.1](bob-cli-nh.6.1.md) / bob-cli-nh.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.md) · **Assignee:** `bob-cli-nh.6.1.2` · **Size:** medium
**Created:** 2026-11-19 09:44:34 EST · **Closed:** 2026-11-19 14:41:25 EST
**Plan:** [202611/property\_card\_kit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_kit.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:b9fee3d94935c22cdac23dbb | attached via sase artifact create --bead |
| related | file:explicit:e0c4d18220635127d479ffc0 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

host: extract createPropertyCardHost and move album, record, and bank lifecycle plumbing onto it. Preserve species models, anchors, caches, record-walk integration, Source-mode bank lint, embed display behavior, and cleanup.

## Notes

[2026-11-19T17:08:10Z · bob-cli-nh.6.1.2] Host implementation landed (uncommitted in linked bob-plugins): createPropertyCardHost in 240c/240d; album/record/bank adapters are thin wrappers. Focused card/rail + host unit tests pass (host 8/8). npm test: 7416 pass / 1 load-flake / 2 skipped; isolated stage-performance passed in 33ms. npm run validate 12/12. Fragments ≤1000 lines. Real Obsidian e2e handed to /sase_monitor; reports will land in /tmp/nh612-e2e/out. Ownership baselines already consumed: file:explicit:d19bd1571d8869c3fbd0f94c, file:explicit:6ef537cd9927c600b96c5526, file:explicit:5366ba3f1c91e381b416eb0b. bob-cli 5b4c2636 debug bob sha256 979bdf8993f9866fb6b12e29c8a3e447e74d19b3e49f47f76451d7a706fd5ed9. -r Record host implementation and pending e2e

[2026-11-19T17:08:18Z · bob-cli-nh.6.1.2] PROPOSED FOLLOW-UP: perf flake — scripts/test-navigation-dependencies-stage-performance.cjs "stage opening builds 200/400/1000-task notes without cubic growth" failed once in full parallel npm test (400-task 382.3 ms vs 250 ms budget) and passed isolated in 33 ms; same load-flake class as ownership-phase event-link-times / bob-cli-ki. Does not keep this phase open. -r Record npm test load-flake as follow-up

[2026-11-19T19:40:12Z · bob-cli-nh.6.1.2] Host phase verified. The earlier uncommitted host work was evicted by a launch-time re-clone of the linked bob-plugins checkout, then restored from the SASE rescue patch (base e2cdc8d) onto bob-plugins ccc0f72. Fixed a new regression: the record adapter file-open/layout-change ran a full host refresh, which made bank walk-real-key-swallowed fail 3/3. onWorkspaceEvent now replaces the default refresh, and unit tests pin both cases. Final tree: album 120/121 and bank 75/78, both the same failure sets as ownership; record full 144/144 twice (one earlier run hit a markdown-neutral flake). bob-cli 5b4c2636, bob sha256 979bdf89. Bank screenshots 20/20 byte-identical; album 35/36 (the 1 diff is a transient toast); record diffs are known noise. npm run validate 12/12; focused suites 317/317; npm test 7500 pass / 2 unrelated failures. Evidence: file:explicit:b9fee3d94935c22cdac23dbb (summary), file:explicit:e0c4d18220635127d479ffc0 (bundle). Deployed via bob plugins sync (ccc0f72 + uncommitted host diff).

[2026-11-19T19:40:30Z · bob-cli-nh.6.1.2] PROPOSED FOLLOW-UP: copy-card model row-order test fails on clean master — scripts/test-navigation-copy-card-model.cjs "model: row order is file builtins, file templates, then TASK group" gets an extra copy-chip row between note and template-2. Fails identically on clean bob-plugins ccc0f72 (upstream bob-copy-chips / navigation copy-chip row commits), so it reddens npm test independently of the property-card kit.

[2026-11-19T19:40:36Z · bob-cli-nh.6.1.2] PROPOSED FOLLOW-UP: record e2e markdown-neutral flake — scripts/obsidian-record-card-e2e.cjs render-fold-collapse-and-navigation-are-markdown-neutral failed once in 3 full-scope runs on the final host tree (passiveMarkdownBytesUnchanged=false) and passed on the other 2. The scratch vault shows background bob albums sync / projects sync commits landing during the run (projects sync adds a Projects callout to body.md), so the hash window can race startup sync. Also seen: event-link-times 200-link perf budget failed once in full npm test and passed 3/3 isolated (bob-cli-ki class). Bank base failures stay on bob-cli-m6 (invalid-fence) and bob-cli-m7 (walk-learn getLine(-1)); album schema-field-jump-ctrl-j still fails identically to the ownership baseline.

[2026-11-19T19:41:25Z · bob-cli-nh.6.1.2] Verified createPropertyCardHost (240c/240d) with album, record, and bank as thin adapters, restored from the SASE rescue patch onto bob-plugins ccc0f72. Fixed the record file-open full-refresh regression that broke bank walk-real-key-swallowed (3/3 fail before, 2/2 pass after; clean base passes). Final e2e on the same bob binary (5b4c2636, sha256 979bdf89): album 120/121 and bank 75/78 match ownership exactly; record full 144/144 x2 (one flaky markdown-neutral run). Bank screenshots 20/20 byte-identical. validate 12/12; focused suites 317/317; npm test 7500 pass, 2 unrelated failures (base copy-card row order; perf load flake). Evidence: file:explicit:b9fee3d94935c22cdac23dbb, file:explicit:e0c4d18220635127d479ffc0. Deployed with bob plugins sync. No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-nh.6.1.1](bob-cli-nh.6.1.1.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.6.1.3](bob-cli-nh.6.1.3.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.6.1.2/README.md) | [bob-cli-nh.6.1.2](bob-cli-nh.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@946ef56`](https://github.com/bobs-org/bob-plugins/commit/946ef56589c2650807bdf45c3dfd0eb59005c956) | feat(ledger-tools): share one property-card host lifecycle | [bob-cli-nh.6.1.2](bob-cli-nh.6.1.2.md) | 2026-11-19 14:42:27 EST |
