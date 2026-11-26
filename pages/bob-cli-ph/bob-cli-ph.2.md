# Bead: bob-cli-ph.2 — One plugin recognizer twin and dual-read plugin readers

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.2` · **Size:** large
**Created:** 2026-11-22 17:36:48 EST · **Closed:** 2026-11-23 18:31:21 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:9b7661cdd94a50ca73e00777 | attached via sase artifact create --bead |
| related | file:explicit:ea63e67c4a620dbad55354a6 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

plugin-readers: one byte-identical recognizer twin replaces every drifted plugin copy, the DV/DH vectors are copied, and every plugin reader accepts both drawer forms; deployed with plugin writers unchanged.

## Notes

[2026-11-23T21:46:41Z · bob-cli-ph.2] PROPOSED FOLLOW-UP: Full bob-plugins `npm test` remains red on the same two 25 ms wall-clock ledger nodes already tracked by bob-cli-km and bob-cli-io. On this phase tree (dirty only scripts/test-task-drawers-twin-copies.cjs over HEAD a73f70bf) the unit gate was 9153 pass / 2 fail / 5 skip: test-ledger-tools-event-link-times.cjs:1069 "perf — one build over a 200-link ledger stays under 25 ms" took 82.4 ms, and test-ledger-tools-frees-marks.cjs:481 "200-link / 2000-task build stays within the 25 ms budget" took 201 ms. Isolated `node --test scripts/test-ledger-tools-event-link-times.cjs scripts/test-ledger-tools-frees-marks.cjs` passed 40/40 (event-link build 11.8 ms). Identical failures on the clean pre-fix tree SHA a73f70bf4f22c0916e95546275594fd825036e9a: event-link 68.6 ms and frees-marks 183 ms; `test:perf` 26/26. Those two test files were unchanged by 19ac4a3e and by this test-only fixture-loading repair. `just check` on bob-cli 588c6210 exited 0. Do not keep this phase open for those flakes.

[2026-11-23T21:49:53Z · bob-cli-ph.2] Deployment status at HEAD d3a17f0c (fast-forwarded origin; dirty only scripts/test-task-drawers-twin-copies.cjs):
- task-status-cycler 1.58.3: list synced; source/vault main.js 451084581ab2305af4301315b9d47ca5ff7eda96b503e64fb3a72d647fe14fa3 equal; marker bob-task-drawer-dual-read-v1 present. Stamp still bob-cli_10 uncommitted 76565b6d.
- block-id-prompt 1.45.0: list synced; source/vault main.js 87fece9b22afd6d0a3fb1b5a2bf122c493369bad7b48abc5ac32a520e146dadd equal; marker present. Stamp still bob-cli_10 uncommitted 76565b6d.
- bob-ledger-tools 1.157.1: list drift. Sync refused: uncommitted deploy from bob-cli_10 on apollo (a73f70b, 2026-11-23T21:17:45Z). Author bob-cli-pf.5.1.7 is still RUNNING in workspace 10; do not -F. Vault already has the dual-read marker but main.js/styles.css differ (property-editor work). Wait for that agent to land, then sync from a clean committed tree.
- bob-navigation-hotkeys 2.107.0: list drift. Sync refused: uncommitted deploy from bob-cli_15 on apollo (8efc5a6, 2026-11-23T18:13:26Z). No running agent in workspace 15; that tree is now clean. Vault main.js d2b3bdd19c3bd292205b7a603906b37a2e081b35aa953c3e0caa2d41da76b5de lacks bob-task-drawer-dual-read-v1 and predates 19ac4a3e (dual-read) and 6d98af17 (diamond ink). Asking Bryan before -F.

[2026-11-23T23:30:53Z · bob-cli-ph.2--1] Deploy evidence from clean bob-plugins 63e9e760 (fixture-repair HEAD; working tree clean). Apollo vault restamped 2026-11-23T23:21:06Z without -F; Bryan had approved -F for abandoned nav 2.107.0, but vault bytes already matched the dual-read bundle so force was unnecessary. list: 12 synced / 0 drift (file:explicit:9b7661cdd94a50ca73e00777).
- task-status-cycler 1.58.3: sync=synced; stamp clean ws13 63e9e760; marker bob-task-drawer-dual-read-v1 present; main.js sha256 451084581ab2305af4301315b9d47ca5ff7eda96b503e64fb3a72d647fe14fa3 source=vault; styles.css 214c213ebd1fb132095ad7ae6606e60e7fc890980ef61b24729623752e41ea3a equal.
- block-id-prompt 1.45.0: sync=synced; stamp clean ws13 63e9e760; marker present; main.js sha256 87fece9b22afd6d0a3fb1b5a2bf122c493369bad7b48abc5ac32a520e146dadd source=vault; styles.css b3c53115b9b70638b2a4f990dec9026281b5428ed4f1ae22264ca30214a8aa49 equal.
- bob-ledger-tools 1.157.1: sync=synced; stamp clean ws13 63e9e760; marker present; main.js sha256 b6580dde7e5c60044e19af2d7470b980e896692f0bb90e1a2495c49774aab556 source=vault; styles.css ed12f955b5c31c478869489bf9151887850105b7e4ab16c817e8db928e160fa3 equal. Dry-run succeeded without -F (vault already matched landed bytes); pf.5.1.7 still running but ws10 plugin files for this id were clean.
- bob-navigation-hotkeys 2.107.0: sync=synced; stamp clean ws13 63e9e760; marker present; main.js sha256 c3c4bbdf4dbd4a076f9c3ae0eecd5bc66caa4b39f8292420ab3ce9f1c7c3d5c7 source=vault; styles.css 2e027c50083c9f48d1d52afda2b957b0a4e1afb904522574092c7bb58ad98149 equal.
Smoke: apollo lacks xvfb-run/Obsidian; ran on athena from a detached worktree at 63e9e760 with rsynced apollo vault plugins. xvfb-run -a node --experimental-websocket scripts/obsidian-startup-smoke.cjs -e /snap/bin/obsidian -d /tmp/ph2-deployed-vault -r report → PASS (file:explicit:ea63e67c4a620dbad55354a6). layout-ready 436 ms; heap 59.7 MiB; four editors ok; 0 exceptions/rejections/crashes; deployed-vault checked 12 synced / 0 drift. Offline self-test 17/17 (not an Obsidian pass). Newly created Notes headers remain legacy (`- NOTES`, not `**NOTES**`) per test-task-drawers-twin-copies.cjs 13/13 on this SHA.

[2026-11-23T23:31:21Z · bob-cli-ph.2--1] Verified dual-read readers on clean bob-plugins 63e9e760: drawer twin suite 13/13 (standalone fixture load + legacy NOTES writers); build:check 0. Unrelated npm test 25ms flakes remain as recorded (bob-cli-km/io). Deployed task-status-cycler 1.58.3, block-id-prompt 1.45.0, bob-ledger-tools 1.157.1, bob-navigation-hotkeys 2.107.0 from this SHA; all list synced, vault main.js equals source, bob-task-drawer-dual-read-v1 present. Nav -F approved but unused (bytes already dual-read). Athena Obsidian smoke PASS (layout-ready 436ms, heap 59.7MiB, 4 editors ok, deployed-vault 12/0). file:explicit:ea63e67c4a620dbad55354a6

## Dependencies

- **Depends on:** [bob-cli-ph.1](bob-cli-ph.1.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.3](bob-cli-ph.3.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.2.md) | [bob-cli-ph.2](bob-cli-ph.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b1fa8ad`](https://github.com/bobs-org/bob-cli/commit/b1fa8ad6de8c3818152296f7c9af7cb2ec21ed1e) | docs: document plugin task drawer reader parity | [bob-cli-ph.2](bob-cli-ph.2.md) | 2026-11-23 13:04:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.2--1][1] | Record exact check outcomes and deployment evidence before closing this assigned phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.2.md

<!-- sase:referenced-by:end -->
