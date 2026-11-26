# Bead: bob-cli-ph.10 — Retire ALL-CAPS drawer recognition

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.10

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.10` · **Size:** medium
**Created:** 2026-11-22 17:36:49 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

cutover: once no unreleased legacy drawer remains, remove ALL-CAPS recognition, the legacy casing helpers and vectors, and the ALL-CAPS import escape in bob-cli and the plugins; grammar 31.

## Dependencies

- **Blocks:** [bob-cli-ph.11](bob-cli-ph.11.md) ◐ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.9](bob-cli-ph.9.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.10.md) | [bob-cli-ph.10](bob-cli-ph.10.md) | 8 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9573ff8`](https://github.com/bobs-org/bob-cli/commit/9573ff869fbef177ff041e78bcf28ddac85a71be) | feat: retire all-caps task drawer recognition | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 21:51:35 EST |
| bob-plugins | [`bob-plugins@fda0ef2`](https://github.com/bobs-org/bob-plugins/commit/fda0ef27749b2b1feae59841ea1024911ff38bc1) | feat: retire all-caps plugin drawer readers | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 21:52:59 EST |
| bob-cli | [`46aba67`](https://github.com/bobs-org/bob-cli/commit/46aba67724194df951bf2c23132f15861d2351ec) | fix(drawers): restore rename flow and complete bold-only cutover verification | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 22:21:33 EST |
| bob-cli | [`5d5509d`](https://github.com/bobs-org/bob-cli/commit/5d5509de4f27f4042eccf52b1c0f6171e43e88d9) | fix(capture): update drawer parser test fixtures | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 22:36:58 EST |
| bob-cli | [`d820323`](https://github.com/bobs-org/bob-cli/commit/d8203235ac54ac416160d34f5e4080499315bbfe) | fix(capture): borrow parsed drawer kind in record fixture | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 22:51:25 EST |
| bob-plugins | [`bob-plugins@4f55996`](https://github.com/bobs-org/bob-plugins/commit/4f5599677a44d4eb98fedef23fa96e193edd02f1) | test(drawers): fix uppercase subtree expectation | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 23:11:23 EST |
| bob-cli | [`c3a9bdd`](https://github.com/bobs-org/bob-cli/commit/c3a9bdd9088399cf4da683b6a0cfccb515fcb68e) | test(drawers): migrate task-requirements fixture vectors to bold headers | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 23:54:14 EST |
| bob-plugins | [`bob-plugins@2ba3315`](https://github.com/bobs-org/bob-plugins/commit/2ba3315d12b714469eeaa7747db0f054602a27ec) | test(drawers): align plugin fixtures with bold-only readers | [bob-cli-ph.10](bob-cli-ph.10.md) | 2026-11-25 23:55:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.10--1][1] | Need the phase scope, design file, and recorded work state before recovering failed verification | 1 |
| read-by | [agent:bob-cli-ph.10--2][1] | Verify current phase scope and allowed closeout target | 1 |
| read-by | [agent:bob-cli-ph.10--3][1] | Confirm phase scope and recorded work before repairing its verification failures | 1 |
| read-by | [agent:bob-cli-ph.10--4][1] | Confirm the drawer retirement phase scope and current status | 1 |
| read-by | [agent:g1][2] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.10.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
