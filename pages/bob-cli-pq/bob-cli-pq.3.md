# Bead: bob-cli-pq.3 — Obsidian draws the criterion diamond in notes

[Bead Pages](../README.md) / [bob-cli-pq](README.md) / bob-cli-pq.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1f8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1f8.md) · **Assignee:** `bob-cli-pq.3` · **Size:** medium
**Created:** 2026-11-23 03:54:18 EST · **Closed:** 2026-11-23 10:45:51 EST
**Plan:** [202611/task\_reqs\_criterion\_diamond.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_reqs_criterion_diamond.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:6ceb733e2949af5516d84d19 | attached via sase artifact create --bead |
| related | file:explicit:ae1aca54e926a5909978092a | attached via sase artifact create --bead |
| related | file:explicit:b73f229ae4902cd628bd0a39 | attached via sase artifact create --bead |
| related | file:explicit:ca9bfcba02f2502cd9513085 | attached via sase artifact create --bead |
| related | file:explicit:d3a8bc5a7270ff27ea05e3dc | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

obsidian-marks: bob-ledger-tools replaces the hash-run mask with four diamond masks in a constant 1em slot, state by fill, owner ink, the verified display fixes, real tooltips, a click guard that teaches instead of ticking, the shared card mark, and a light/dark taste pass.

## Notes

[2026-11-23T09:00:16Z · bob-cli-pq.3] Sequencing wait: plan step 0 requires bob-cli-ph.7 (obsidian-drawers) and bob-cli-ph.8 (mac-drawers) to close before this phase edits bob-ledger-tools styles.css. Both are still in_progress; drawer tray CSS has not landed (requirement section still uses the 32x16 hash-run mask). Added deps and a wait monitor so a follow-up implements the diamond once they close.

[2026-11-23T09:00:20Z · bob-cli-pq.3] PROPOSED FOLLOW-UP: Add a Requirements Wear The Criterion Diamond decision record — epic decision memory_req_mark_record was declined (auto, no human review); land agent should file a memory task bead for decisions:requirements-wear-the-criterion-diamond as specified in the plan declined branch, linked to [[decisions:task-reqs-are-met-with-their-task]].

[2026-11-23T15:14:42Z · bob-cli-pq.3] Proceeding under Bryan’s sequencing waiver recorded on parent bob-cli-pq note #1 (2026-11-23 10:08 EST). Removed obsolete ph.7/ph.8 dependency edges; preserving drawer words and leaving the joint drawer/diamond taste pass to the lander.

[2026-11-23T15:35:03Z · bob-cli-pq.3] PROPOSED FOLLOW-UP: Repair pre-existing drawer-reader Clippy denies — just check fails identically on this change and on the clean e6a6326a base with clippy::collapsible_if at src/native/task_children.rs:129 and src/native/task_reqs.rs:319. ToolRuns c1e6581ef0697c230237dcd913e334df (working tree) and 81a2ff47533495f836ba419d5d1eb2ad (clean base); no Rust source changed in pq.3. Drawer rollout belongs to bob-cli-ph.

[2026-11-23T15:35:08Z · bob-cli-pq.3] PROPOSED FOLLOW-UP: Resync task_reqs fixture documentation during drawer rollout — npm test fails the two canonical README.md byte-copy checks in test-task-reqs-twin-copies.cjs and test-task-status-cycler-task-reqs-vectors.cjs; both reproduce on clean bob-plugins b75ed489 against bob-cli e6a6326a. Requirement semantic vectors are unchanged by pq.3.

[2026-11-23T15:35:12Z · bob-cli-pq.3] PROPOSED FOLLOW-UP: Stabilize plugin timing tests under suite load — npm test hit event-link-times (28.4ms >25), frees-marks (43ms >25), and task-wikilink cold-build chunk (17.7ms >16). All 45 tests across the same three files passed on the unchanged implementation in a serial rerun.

[2026-11-23T15:35:33Z · bob-cli-pq.3] PROPOSED FOLLOW-UP: Finish drawer contract documentation registration — just docs-gen succeeds, but just docs-check then fails identically after regenerating on clean e6a6326a: test_contracts.py expects 56 entries versus 57, llmstxt omits task-drawers.md, and the README contract-table digest is stale. pq.3 retains the three generated task-drawers navigation additions; no memory edited. This belongs with the bob-cli-ph drawer rollout.

[2026-11-23T15:41:53Z · bob-cli-pq.3] Validation update: final npm test ran 9,048 unit tests (9,040 passed, 4 skipped, 4 failed) and all 26 performance-suite tests passed. The two deterministic failures are the clean-base fixture README mismatches already noted. The other two are timing flakes (frees-marks and dependencies-stage CPU clock); all 139 targeted tests, including those files, requirement/type rendering, and the newly fetched property-editor shell, passed serially after merging bob-plugins e60541b.

[2026-11-23T15:44:19Z · bob-cli-pq.3] PROPOSED FOLLOW-UP: Reconcile deployed task-status-cycler drift during drawer rollout — bob-ledger-tools sync succeeded (main.js and styles.css copied from e60541b plus this phase); the mandatory all-plugin post-sync gate failed before launch because task-status-cycler reports drift. Command: xvfb-run -a node scripts/obsidian-startup-smoke.cjs -e /snap/obsidian/current/app/obsidian --deployed-vault /home/bryan/bob --report /tmp/pq3-smoke.json. No report was written; stderr retained in /tmp/pq3-smoke.log. The unrelated plugin was not deployed by this phase; full rollout verification remains outstanding.

[2026-11-23T15:45:45Z · bob-cli-pq.3] Implemented the four diamond masks in fixed 1em slots, owner ink with inherited-type parity, state-aware glyph tooltips and teaching click guard, toggle restoration, Reading-view blank-checkbox recognition, native-style resets, and shared card marks. Drawer words are unchanged. Four real-Obsidian light/dark Live Preview/Reading cases pass, including tooltip/real click/no-write checks, nested depth geometry, derived-met versus hand-met, forced colors, reduced motion, and toggle cycles; screenshots and report are attached (report file:explicit:ae1aca54e926a5909978092a). The final isolated all-plugin startup smoke also PASSed on e60541b plus phase changes: layout-ready 331ms, peak heap 55.9MiB, all four editor mounts, no exceptions/rejections/crashes. Report /tmp/pq3-source-smoke.json; command xvfb-run -a node scripts/obsidian-startup-smoke.cjs -e /snap/obsidian/current/app/obsidian --report /tmp/pq3-source-smoke.json with TMPDIR=/tmp, DBUS_SESSION_BUS_ADDRESS=disabled:, and an isolated XDG_CONFIG_HOME. The all-plugin deployed-vault gate remains blocked by the separately recorded task-status-cycler drift. Build, 139 merged targeted tests, and both diff whitespace checks pass. Broad-suite clean-base failures and load-sensitive timing flakes are recorded above; the joint drawer taste pass remains with the lander per Bryan’s waiver.

[2026-11-23T15:45:51Z · bob-cli-pq.3] Verified criterion-diamond implementation, generated bundle and docs; 139 targeted tests, four real-Obsidian appearance/interaction cases, and isolated startup smoke pass. Four screenshots and passing look report attached. Synced only bob-ledger-tools without force while preserving landed upstream work. Clean-base Clippy/docs/fixture failures, timing flakes, and unrelated deployed task-status-cycler drift are documented as proposed follow-ups. No epic-symbol leftovers; drawer words untouched under Bryan’s sequencing waiver.

## Dependencies

- **Blocks:** [bob-cli-pq.4](bob-cli-pq.4.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pq.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pq.3/README.md) | [bob-cli-pq.3](bob-cli-pq.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f6cf62c`](https://github.com/bobs-org/bob-cli/commit/f6cf62cf7a415ca75bebf31a744a286fbba09f5c) | docs(task-reqs): document criterion diamonds and teaching clicks | [bob-cli-pq.3](bob-cli-pq.3.md) | 2026-11-23 10:47:01 EST |
| bob-plugins | [`bob-plugins@c884675`](https://github.com/bobs-org/bob-plugins/commit/c884675435beab310eaa1bf041a4939828ca4a77) | feat(task-reqs): render criterion diamonds with state-aware tooltips | [bob-cli-pq.3](bob-cli-pq.3.md) | 2026-11-23 10:47:29 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-pq.3][2] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pq.3.md

<!-- sase:referenced-by:end -->
