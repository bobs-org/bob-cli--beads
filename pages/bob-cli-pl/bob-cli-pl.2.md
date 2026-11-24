# Bead: bob-cli-pl.2 — Area/project roles, validation, and setting ops in bob props (bob-cli)

[Bead Pages](../README.md) / [bob-cli-pl](README.md) / bob-cli-pl.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5y.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5y.linker.w1.md) · **Assignee:** `bob-cli-pl.2` · **Size:** medium
**Created:** 2026-11-22 20:56:40 EST · **Closed:** 2026-11-24 10:58:20 EST
**Plan:** [202611/area\_project\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_cards.md)

## Description

contract-writes: complete the role table for area/project notes and bank.md, validate contract keys on every write path, and add bob-expanded setting.set / setting.clear ops with golden byte tests.

## Notes

[2026-11-23T02:10:48Z · bob-cli-pl.2] BLOCKED BY LAUNCH PRECONDITION: Audited bob-cli-pf before coding; it is still in_progress (pf.1, pf.2, pf.4, pf.5, and pf.6 remain in_progress). The approved area_project_cards plan explicitly requires bob-cli-pf to be closed before any phase starts and directs workers to stop with a note and change no files otherwise. No implementation edits or tests were performed, and this phase was not closed or reopened. Earlier generic props work is present (3e480e4a, fdd94725); after the prerequisite closes, resume contract-writes against the landed APIs and complete its roles, validation, setting ops, goldens, and docs.

[2026-11-23T02:31:36Z · bob-cli-pl.2] PREREQUISITE WAIT: Re-read bob-cli-pf and the approved area_project_cards design; pf remains in_progress, so the launch precondition still prohibits implementation. No source files changed. Added the missing dependency edge and staging a zero-weight monitor to resume contract-writes only after pf closes; the successor must verify its resolution and inspect as-landed APIs before coding.

[2026-11-24T15:23:44Z · bob-cli-pl.2--1] PROPOSED FOLLOW-UP: Corroborate bob-cli-gd completion deadline flake — ToolRun 16a907966e938c1d477e2afcb6027c7c on e3e437ba plus this props implementation failed albums_update::completion_offers_update_stems_and_input_files with members: [] (tests/cli/albums_update.rs:1088). The exact unchanged compiled cli test binary passed that isolated test immediately (1/1, 1.15s). Existing bob-cli-gd already tracks this exact unpinned 150ms __complete helper through bob-cli-os.land and bob-cli-on.land corroboration. No unrelated completion code changed.

[2026-11-24T15:25:05Z · bob-cli-pl.2--1] Implementation is present on foundation master e3e437ba: shared area/project/bank setting table, role and legacy metadata, generic-path validation, setting.set/clear expansion with primitive byte-exact inverses, lock-time dependency refresh, docs, 42 explicit byte goldens, and CLI race/atomicity tests. Live read-only role acceptance passed on dev, sase_blog, mac_inbox, bank. Foundation now uses bare + instead of the old plan spelling =+; docs follow landed behavior. props_contract_v1 remains for phase 3. First full check ToolRun 16a907966e938c1d477e2afcb6027c7c passed fmt/clippy and all but two new contract tests, stale generated CLI help, and the separately recorded known completion flake. Fixed semantic parent reads through comments, proposed-edge cycle repair, and pre-splice invalid value checks; added regression and idempotence tests. Remaining work is verification and review of generated docs, then epic-symbols and close only this phase; it clearly fits one coder. No memory or linked-repo changes.

[2026-11-24T15:58:20Z · bob-cli-pl.2--2] Completed contract-writes: area/project/bank roles and legacy metadata, shared domain validation for generic write paths, strict setting.set/setting.clear expansion, lock-time parent revalidation, warning responses, and byte-exact inverse operations. All 42 setting golden cases and regression tests pass. Canonical ToolRun c9e8f38e5d008646553c147a7649d9cf passed fmt, Clippy, and the complete workspace suite (8004 library tests, 4080 CLI tests, all remaining integration suites and doctests). just docs-gen passed and its only generated diff was the two setting operations in props update help; just docs-check passed all implemented gates (447 tests, one optional font-dependency skip). Recovered stale ignored mounted-doc outputs by backing them up and regenerating; no linked-repo or memory changes. Prior live read-only role checks on dev, sase_blog, mac_inbox, and bank remain valid. Rechecked epic-symbols: no entries. props_contract_v1 remains deferred to contract-reads (phase 3). Closed only this phase; the ancestor epic remains open.

## Dependencies

- **Depends on:** [bob-cli-pf](../bob-cli-pf/README.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.3](bob-cli-pl.3.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.2.md) | [bob-cli-pl.2](bob-cli-pl.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d39680d`](https://github.com/bobs-org/bob-cli/commit/d39680dda4120b90602467ec812ec819d7a984d2) | feat(props): validate area and project setting writes | [bob-cli-pl.2](bob-cli-pl.2.md) | 2026-11-24 10:59:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.2--2][1] | Check phase notes before recording a documentation gate discovery | 2 |
| read-by | [agent:fx][2] | Research whether the pl epic's dependency on pf is necessary | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
