# Bead: bob-cli-c9.4.1.9.3 — Harden the overwrite transaction and prove it with failpoints

[Bead Pages](../README.md) / [bob-cli-c9.4.1.9](bob-cli-c9.4.1.9.md) / bob-cli-c9.4.1.9.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.land.md) · **Assignee:** `bob-cli-c9.4.1.9.3` · **Size:** medium
**Created:** 2026-10-26 03:39:12 EDT · **Closed:** 2026-10-26 06:25:32 EDT
**Plan:** [202610/overwrite\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/overwrite_landing_fixes.md)

## Description

safety: recheck selection after the locked pre-sync, refuse ignored or untracked files inside touched directories, tighten intent path validation, stop other pre-syncs from committing a crashed overwrite, drop blanket lint allows, add executor failpoint tests, and run the full gates.

## Notes

[2026-10-26T10:25:18Z · bob-cli-c9.4.1.9.3] PROPOSED FOLLOW-UP: just check lib flake native::capture_related::tests::synthetic_vault_draft_contract_is_under_250ms took 855ms (debug target allows 500ms under parallel just check load); passed in isolation; already tracked by bob-cli-ca

[2026-10-26T10:25:32Z · bob-cli-c9.4.1.9.3] Harden overwrite transaction: reselect after locked pre-sync (preimage_changed when a later reading appears, a named member vanishes, or bytes change); refuse gitignored/untracked files under touched dirs as dirty_paths; restore only base-tracked paths; reject empty/CurDir/dot intent paths; standalone vault-sync recovers a planted intent; task-move refuses while pending; executor failpoints leave intact old state or verified committed new state. Dropped blanket dead_code allows on mod overwrite and recovery save/load/clear. Documented interrupted overwrite recovery in docs/highlights-ref-sync.md. keep_user_fields=keep unchanged. Verified: 35 overwrite::* lib tests, ignored_paths_under unit, CLI gitignored sidecar dirty_paths, vault-sync recover, task-move refuse; just fmt --check; clippy -D unused; just docs-gen; just docs-check. just check: fmt+clippy green, CLI/integration green; only lib failure is capture_related synthetic_vault_draft_contract_is_under_250ms (855ms vs 500ms) which passed in isolation and is tracked by bob-cli-ca. epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-c9.4.1.9.2](bob-cli-c9.4.1.9.2.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.9.3/README.md) | [bob-cli-c9.4.1.9.3](bob-cli-c9.4.1.9.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`66f9d67`](https://github.com/bobs-org/bob-cli/commit/66f9d67f6573048b76a1d34274a95e7fc4b438c2) | fix(highlights): harden overwrite recovery, selection recheck, and failpoints | [bob-cli-c9.4.1.9.3](bob-cli-c9.4.1.9.3.md) | 2026-10-26 06:26:32 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.4.1.9.3][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.9.3/README.md

<!-- sase:referenced-by:end -->
