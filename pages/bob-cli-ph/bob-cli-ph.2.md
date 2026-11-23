# Bead: bob-cli-ph.2 — One plugin recognizer twin and dual-read plugin readers

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.2` · **Size:** large
**Created:** 2026-11-22 17:36:48 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

plugin-readers: one byte-identical recognizer twin replaces every drifted plugin copy, the DV/DH vectors are copied, and every plugin reader accepts both drawer forms; deployed with plugin writers unchanged.

## Notes

[2026-11-23T21:46:41Z · bob-cli-ph.2] PROPOSED FOLLOW-UP: Full bob-plugins `npm test` remains red on the same two 25 ms wall-clock ledger nodes already tracked by bob-cli-km and bob-cli-io. On this phase tree (dirty only scripts/test-task-drawers-twin-copies.cjs over HEAD a73f70bf) the unit gate was 9153 pass / 2 fail / 5 skip: test-ledger-tools-event-link-times.cjs:1069 "perf — one build over a 200-link ledger stays under 25 ms" took 82.4 ms, and test-ledger-tools-frees-marks.cjs:481 "200-link / 2000-task build stays within the 25 ms budget" took 201 ms. Isolated `node --test scripts/test-ledger-tools-event-link-times.cjs scripts/test-ledger-tools-frees-marks.cjs` passed 40/40 (event-link build 11.8 ms). Identical failures on the clean pre-fix tree SHA a73f70bf4f22c0916e95546275594fd825036e9a: event-link 68.6 ms and frees-marks 183 ms; `test:perf` 26/26. Those two test files were unchanged by 19ac4a3e and by this test-only fixture-loading repair. `just check` on bob-cli 588c6210 exited 0. Do not keep this phase open for those flakes.

[2026-11-23T21:49:53Z · bob-cli-ph.2] Deployment status at HEAD d3a17f0c (fast-forwarded origin; dirty only scripts/test-task-drawers-twin-copies.cjs):
- task-status-cycler 1.58.3: list synced; source/vault main.js 451084581ab2305af4301315b9d47ca5ff7eda96b503e64fb3a72d647fe14fa3 equal; marker bob-task-drawer-dual-read-v1 present. Stamp still bob-cli_10 uncommitted 76565b6d.
- block-id-prompt 1.45.0: list synced; source/vault main.js 87fece9b22afd6d0a3fb1b5a2bf122c493369bad7b48abc5ac32a520e146dadd equal; marker present. Stamp still bob-cli_10 uncommitted 76565b6d.
- bob-ledger-tools 1.157.1: list drift. Sync refused: uncommitted deploy from bob-cli_10 on apollo (a73f70b, 2026-11-23T21:17:45Z). Author bob-cli-pf.5.1.7 is still RUNNING in workspace 10; do not -F. Vault already has the dual-read marker but main.js/styles.css differ (property-editor work). Wait for that agent to land, then sync from a clean committed tree.
- bob-navigation-hotkeys 2.107.0: list drift. Sync refused: uncommitted deploy from bob-cli_15 on apollo (8efc5a6, 2026-11-23T18:13:26Z). No running agent in workspace 15; that tree is now clean. Vault main.js d2b3bdd19c3bd292205b7a603906b37a2e081b35aa953c3e0caa2d41da76b5de lacks bob-task-drawer-dual-read-v1 and predates 19ac4a3e (dual-read) and 6d98af17 (diamond ink). Asking Bryan before -F.

## Dependencies

- **Depends on:** [bob-cli-ph.1](bob-cli-ph.1.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.3](bob-cli-ph.3.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.2.md) | [bob-cli-ph.2](bob-cli-ph.2.md) | 4 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b1fa8ad`](https://github.com/bobs-org/bob-cli/commit/b1fa8ad6de8c3818152296f7c9af7cb2ec21ed1e) | docs: document plugin task drawer reader parity | [bob-cli-ph.2](bob-cli-ph.2.md) | 2026-11-23 13:04:10 EST |
| bob-plugins | [`bob-plugins@19ac4a3`](https://github.com/bobs-org/bob-plugins/commit/19ac4a3e4bafc2362b2b6189553dec99cfba1500) | feat: unify task drawer readers across plugins | [bob-cli-ph.2](bob-cli-ph.2.md) | 2026-11-23 13:05:47 EST |
| bob-plugins | [`bob-plugins@6268f24`](https://github.com/bobs-org/bob-plugins/commit/6268f246c33434e1c3da94213ca5e4d76a8eccd5) | test(plugins): anchor keep-moving style assertion to picker rule | [bob-cli-ph.2](bob-cli-ph.2.md) | 2026-11-23 13:20:45 EST |
| bob-plugins | [`bob-plugins@63e9e76`](https://github.com/bobs-org/bob-plugins/commit/63e9e7609338d91de8f592c3c134d69abd92b9ab) | test(plugins): load drawer DV/DH vectors from the cycler fixture | [bob-cli-ph.2](bob-cli-ph.2.md) | 2026-11-23 16:51:32 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.2--1][1] | Record exact check outcomes and deployment evidence before closing this assigned phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.2.md

<!-- sase:referenced-by:end -->
