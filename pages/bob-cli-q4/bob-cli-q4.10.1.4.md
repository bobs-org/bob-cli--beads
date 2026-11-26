# Bead: bob-cli-q4.10.1.4 — Task moves and splits settle every written note

[Bead Pages](../README.md) / [bob-cli-q4.10.1](bob-cli-q4.10.1.md) / bob-cli-q4.10.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.md) · **Assignee:** `bob-cli-q4.10.1.4` · **Size:** medium
**Created:** 2026-11-25 14:29:10 EST · **Closed:** 2026-11-25 20:26:01 EST
**Plan:** [202611/navigation\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/navigation_gesture_settle.md)

## Description

relocation: settle move source/destination and Task Split same-note, cross-note, created-note, and requirement-carry postimages before persistence. Return final anchors and exact settled receipts, preserve rollback and recovery, and keep moves following their destination while parking the walk. Cover routed moves that share writers.

## Notes

[2026-11-26T01:25:52Z · bob-cli-q4.10.1.4--f] Verification on 2026-11-25/26: npm run build passed; all nine plugin build targets were unchanged. Focused node tests (test-navigation-inbox-route.cjs and test-navigation-task-split-carry-api.cjs) passed 36/36, 0 failed. npm test passed: build check and docs inventory check passed (inventory up to date); unit suite 9702 passed, 4 skipped, 0 failed; performance suite 26 passed, 0 skipped, 0 failed. BOB_CLI_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17 npm run docs:check passed all implemented gates; documentation tests 447 passed, 1 skipped, 0 failed. bob plugins sync -p bob-navigation-hotkeys succeeded: plugin up to date, 0 copied, 0 skipped, 3 unchanged. Full sequence exit 0.

[2026-11-26T01:26:01Z · bob-cli-q4.10.1.4--f] Closed after successful build, focused tests, full npm test, docs check, and scoped bob-navigation-hotkeys sync; exact results are recorded in the preceding bead note.

## Dependencies

- **Depends on:** [bob-cli-q4.10.1.3](bob-cli-q4.10.1.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.10.1.5](bob-cli-q4.10.1.5.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.10.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.1.4.md) | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 13 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@0e8c70b`](https://github.com/bobs-org/bob-plugins/commit/0e8c70b7fbbf65c33e4810ced2fdf17e4d9f1219) | feat(navigation): settle move and split postimages | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 17:14:50 EST |
| bob-plugins | [`bob-plugins@24dbb8a`](https://github.com/bobs-org/bob-plugins/commit/24dbb8a1e56b68701da356c5aac475e6132b0074) | test(navigation): respect live source path during split carry | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 17:24:16 EST |
| bob-plugins | [`bob-plugins@aecff7d`](https://github.com/bobs-org/bob-plugins/commit/aecff7d2463676b0232d901bd079bbcd2b92e175) | test(navigation): register open destination leaves in move fixtures | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 17:34:08 EST |
| bob-plugins | [`bob-plugins@f6167d4`](https://github.com/bobs-org/bob-plugins/commit/f6167d4c5bd47da44a33d11a7967c6848c0a9571) | test(bob-ledger-tools): await mention jump completion | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 18:09:25 EST |
| bob-cli | [`05dd83c`](https://github.com/bobs-org/bob-cli/commit/05dd83cf9f93c07825a30dfe508e530bc36f9d81) | docs: repair documentation gate consistency | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 18:31:13 EST |
| bob-plugins | [`bob-plugins@1c76c78`](https://github.com/bobs-org/bob-plugins/commit/1c76c782c8f48d8e1be7f66fe5dc74ca2a1bb0dc) | docs: trim plugin references below page budgets | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 18:31:56 EST |
| bob-cli | [`8850f2e`](https://github.com/bobs-org/bob-cli/commit/8850f2e639a862f5814eae348449ebd232053bb7) | docs(reference): satisfy word-budget lint | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 18:53:41 EST |
| bob-plugins | [`bob-plugins@f9a9e16`](https://github.com/bobs-org/bob-plugins/commit/f9a9e167a8fee9cf1653532e98bedfbf5208b30c) | fix(ledger): annotate parent stage text role | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 19:02:52 EST |
| bob-plugins | [`bob-plugins@79d71bf`](https://github.com/bobs-org/bob-plugins/commit/79d71bfd6bbd5ecc1c4919660b6ec92987f162bd) | docs(bob-navigation-hotkeys): meet docs budgets and mark literal input | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 19:17:39 EST |
| bob-cli | [`fc9c91c`](https://github.com/bobs-org/bob-cli/commit/fc9c91ca46026be17965509a4425273134b0eeea) | docs(memory): add planning-time decision roster policy | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 19:48:21 EST |
| bob-plugins | [`bob-plugins@2ff8fdd`](https://github.com/bobs-org/bob-plugins/commit/2ff8fdd555c847175cf16768c21d1592bc74a433) | docs(navigation): fix published reference links | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 19:49:05 EST |
| bob-cli | [`1c7a481`](https://github.com/bobs-org/bob-cli/commit/1c7a481c539a7677c8e2c9b04bfb554b18bd0ab5) | fix(docs): keep capture smoke query searchable | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 19:57:34 EST |
| bob-cli | [`926c925`](https://github.com/bobs-org/bob-cli/commit/926c92589bf68dc4df851e28a26999f67f2074cd) | docs(search): cover Go To capture token | [bob-cli-q4.10.1.4](bob-cli-q4.10.1.4.md) | 2026-11-25 20:15:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.10.1.4--1][1] | Need the phase scope, design, and recorded notes after monitored verification failed | 1 |
| read-by | [agent:bob-cli-q4.10.1.4--c][1] | Review the assigned epic before recording its verification, deployment, and close results | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.10.1.4.md

<!-- sase:referenced-by:end -->
