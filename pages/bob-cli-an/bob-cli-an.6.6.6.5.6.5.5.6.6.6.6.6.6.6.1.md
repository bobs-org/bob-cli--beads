# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1 — Stop -b runs from pre-syncing the default vault

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1` · **Size:** medium
**Created:** 2026-10-26 15:53:09 EDT · **Closed:** 2026-10-26 22:38:54 EDT
**Plan:** [202610/backlog\_batch15\_vault\_safety\_pdf\_moves\_and\_red\_gates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md)

## Description

vault-flag-presync: resolve bob-cli-cj by making bob ref rename and every other -b-capable pre-sync caller refuse when the selected vault is not BOB_DIR, with regression tests proving the default vault is never touched.

## Notes

[2026-10-27T02:18:49Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1] Baseline reproduction on the installed bob: two temporary Git vaults, BOB_DIR=B with a local bare origin and pending.md, rename old to new with -b A. Command exited 0, committed and pushed pending.md in B (vault(athena): 1 file - pending.md), and committed bob ref rename: old → new in A despite A having no remote. No live vault was used. Caller audit: task_move Report::new and randomize run both get their vault only from bob_env::bob_dir(); neither exposes -b, so neither can mismatch. nightly likewise uses bob_env::bob_dir(). Override-capable online paths are ref rename, migrate-tasks, migrate-zorg, and vault_rewrite (themes/relations rename); intake and create --force already guard identity.

[2026-10-27T02:24:09Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1] Implementation complete pending final verification: shared canonical vault identity helper reused by intake; online guards before locks in ref rename, migrate-tasks, migrate-zorg, and vault_rewrite (themes/relations). Added isolated two-vault regressions for all five commands, offline/preview rename compatibility, missing/default-path and symlink tests, and hermetic BOB_DIR in CLI test helper. Initial full just check (ToolRun c6802037b79ff67aff9cccd782a99ee9) passed formatting, clippy, all 3674 active lib tests, and existing CLI tests; only two new tests misread the existing top-level theme/relation JSON error envelope. Fixed the helper to accept the correct envelopes. CLI help and three behavior contracts updated; final docs-gen, full check, and docs-check are next. No epic-symbol entries. Target task cj and all ancestors stay open for the lander.

[2026-10-27T02:38:54Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1--1] Verified the completed wrong-vault pre-sync fix. Online ref rename, migrate-tasks, migrate-zorg, themes rename, and relations rename refuse canonical vault mismatches before locks or sync, preserving existing JSON envelopes. Two-vault regressions prove files, Git heads, remote HEAD, status, sync state, and lock files stay unchanged; preview/offline rename, symlink aliases, missing paths, and HOME fallback are covered. CLI test helper isolates BOB_DIR. Monitor 0xyrqcctmx5c / ToolRun 5b67c92f0732c8e995cd2a2a52cf1138 completed docs-gen, full sase tool run check, and docs-check with exit 0 on the final tree: 3674 lib tests passed and all CLI/integration suites passed; docs had 447 passed, 1 skipped, with all implemented gates passing. Reviewed the 22-file diff, confirmed generated themes/relations CLI identity paragraphs and affected contracts, and git diff --check passed. No code or documentation changed after verification. epic-symbols reports no entries. Target task bob-cli-cj and all ancestors remain for the lander.

## Dependencies

- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dc040b0`](https://github.com/bobs-org/bob-cli/commit/dc040b02c8bd2dfc7b60f5999b2a2f9fce0251d2) | fix(vault-sync)!: refuse online writes to a different vault | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1.md) | 2026-10-26 22:39:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1.md

<!-- sase:referenced-by:end -->
