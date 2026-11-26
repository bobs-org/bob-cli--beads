# Bead: bob-cli-ph.10 — Retire ALL-CAPS drawer recognition

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.10` · **Size:** medium
**Created:** 2026-11-22 17:36:49 EST · **Closed:** 2026-11-26 03:55:01 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

cutover: once no unreleased legacy drawer remains, remove ALL-CAPS recognition, the legacy casing helpers and vectors, and the ALL-CAPS import escape in bob-cli and the plugins; grammar 31.

## Notes

[2026-11-26T08:40:10Z · bob-cli-ph.10] PROPOSED FOLLOW-UP: Regenerate the navigation plugin bundle — npm test on untouched bob-plugins b4ab2cbb16c2fe21004d8790367e69d38926705c stops at build:check with stale generated plugins/bob-navigation-hotkeys/main.js. The focused drawer/requirement twin, split, promotion and reversal suites pass, and all canonical drawer/requirement/layout/write/split JSON fixtures match their plugin copies byte for byte. This is clean-base generated-bundle drift, not a change made by this verification turn.

[2026-11-26T08:42:01Z · bob-cli-ph.10] Scope audit: implementation already landed in bob-cli 9573ff86/46aba677/5d5509de/c3a9bdd9 and bob-plugins fda0ef27/2ba3315d. Read migration artifact file:explicit:1d4db13a0a6ed86a7c2d0374: all legacy drawers renamed or released; only DONE was released. No legacy drawer predicate/marker or legacy casing branches remain in Rust/plugin readers; import defusing is bold-only, caps_drawer_retired is a nonblocking catalog-key warning, and cutover is grammar 32 (31 was consumed by Go To; current 33 adds snooze). Focused plugin drawer, requirement twin/vector, split, promotion and reversal tests pass; all 13 canonical JSON fixture copies match. Remaining closeout is current clean-base Rust gate evidence and clarifying current versus historical preview markers in docs/task-drawers.md. No product implementation remainder identified.

[2026-11-26T08:49:40Z · bob-cli-ph.10] PROPOSED FOLLOW-UP: Repair remaining clean-base Rust test expectations after drawer cutover — sase tool run check 4876c0a4839710c7f43bebcafc8d84fe on untouched bob-cli 1c23bce7 completed exit 101 with 42 lib failures (8181 passed) and 55 CLI failures (4156 passed), corroborating bob-cli-ph note #4 and bob-cli-q8 land notes; formatting and gated Clippy pass, and all other test binaries pass. Most failures retain plain ALL-CAPS drawer fixtures, pre-cutover importer escaping, or old completion/summary/JSON expectations. The three project/area Tasks-summary failures already described on the parent are separate. No Rust source or test was changed in this turn. Per the assigned-phase instruction, these baseline failures are recorded for lander triage and do not leave this phase open.

[2026-11-26T08:52:25Z · bob-cli-ph.10] PROPOSED FOLLOW-UP: Update current capture grammar documentation for the snooze revision — src/native/capture_language/mod.rs now reports grammar 33 from 1b386638, while docs/capture.md, docs/reference/compatibility.md, and docs/reference/json-outputs.md still advertise 32 as current. Revision 32 remains the correct historical drawer-cutover revision; coordinate the current-version update with the snooze documentation work.

[2026-11-26T08:55:01Z · bob-cli-ph.10] Verified the already-landed bold-only CLI/plugin cutover, removal of legacy predicates/casing/import escaping, catalog-key warning semantics, grammar 32 retirement (current 33), approved migration record, and byte parity of all 13 shared JSON fixture copies. Focused plugin drawer/requirement/split/promotion/reversal suites pass. Clarified current preview markers versus Mac legacy decoding in docs/task-drawers.md; just docs-check passes all gates (447 tests passed, 1 optional-font skip). Clean-base check 4876c0a4839710c7f43bebcafc8d84fe confirms unchanged 1c23bce7 with no mutated input: fmt/Clippy pass, 42 lib and 55 CLI failures reproduce the existing parent report. Recorded baseline Rust failures, stale plugin bundle, and separate snooze grammar-doc drift as PROPOSED FOLLOW-UP notes per instruction. No epic-symbol entries remain. Closed only this phase; no ancestor or memory edited.

## Dependencies

- **Blocks:** [bob-cli-ph.11](bob-cli-ph.11.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.9](bob-cli-ph.9.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.10/README.md) | [bob-cli-ph.10](bob-cli-ph.10.md) | 6 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9573ff8`](https://github.com/bobs-org/bob-cli/commit/9573ff869fbef177ff041e78bcf28ddac85a71be) | feat: retire all-caps task drawer recognition | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 21:51:35 EST |
| bob-cli | [`46aba67`](https://github.com/bobs-org/bob-cli/commit/46aba67724194df951bf2c23132f15861d2351ec) | fix(drawers): restore rename flow and complete bold-only cutover verification | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 22:21:33 EST |
| bob-cli | [`5d5509d`](https://github.com/bobs-org/bob-cli/commit/5d5509de4f27f4042eccf52b1c0f6171e43e88d9) | fix(capture): update drawer parser test fixtures | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 22:36:58 EST |
| bob-cli | [`d820323`](https://github.com/bobs-org/bob-cli/commit/d8203235ac54ac416160d34f5e4080499315bbfe) | fix(capture): borrow parsed drawer kind in record fixture | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 22:51:25 EST |
| bob-cli | [`c3a9bdd`](https://github.com/bobs-org/bob-cli/commit/c3a9bdd9088399cf4da683b6a0cfccb515fcb68e) | test(drawers): migrate task-requirements fixture vectors to bold headers | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 23:54:14 EST |
| bob-cli | [`1d6df8d`](https://github.com/bobs-org/bob-cli/commit/1d6df8d1dbf6087210f6546c3b798edfaaa29ef5) | docs(drawers): clarify preview marker compatibility after cutover | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-26 03:56:51 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.10][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-ph.10--1][1] | Need the phase scope, design file, and recorded work state before recovering failed verification | 1 |
| read-by | [agent:bob-cli-ph.10--2][1] | Verify current phase scope and allowed closeout target | 1 |
| read-by | [agent:bob-cli-ph.10--3][1] | Confirm phase scope and recorded work before repairing its verification failures | 1 |
| read-by | [agent:bob-cli-ph.10--4][1] | Confirm the drawer retirement phase scope and current status | 1 |
| read-by | [agent:bob-cli-ph.10--5][1] | Confirm phase scope and current status before repairing failed checks | 1 |
| read-by | [agent:bob-cli-q4.10.1.land][2] | Check whether ph.10 deliberately withheld plugin deployment of retired drawer readers | 2 |
| read-by | [agent:bob-cli-q8.land][3] | Lander q8: check whether the drawer cutover phase is still open and owns the 97 drawer test failures | 1 |
| read-by | [agent:g1][4] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.10.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q4.10.1.land/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-q8.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
