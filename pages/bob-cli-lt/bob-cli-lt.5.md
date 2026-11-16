# Bead: bob-cli-lt.5 — Account, rule, and setting ops with the migration refusals

[Bead Pages](../README.md) / [bob-cli-lt](README.md) / bob-cli-lt.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1co](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1co.md) · **Assignee:** `bob-cli-lt.5` · **Size:** medium
**Created:** 2026-11-15 13:16:08 EST · **Closed:** 2026-11-15 19:40:54 EST
**Plan:** [202611/bank\_setup\_render\_and\_edit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_setup_render_and_edit.md)

## Description

writer-ops: add account, rule, and stale_after ops plus the typed refusals that keep history-bearing edits in YAML.

## Notes

[2026-11-16T00:10:54Z · bob-cli-lt.5] PROPOSED FOLLOW-UP: Bring docs/reference/plugins/bob-ledger-tools.md under the 6,000-word docs-reference cap — just docs-check fails at 6,146 words, and the file is unchanged by this phase.

[2026-11-16T00:40:54Z · bob-cli-lt.5--1] Closed by explicit `sase stitch create -B close` after create_commit landed 893bd2af ("feat(bank): add account, rule, and setting writer ops"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-lt.5` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-lt.4](bob-cli-lt.4.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-lt.8](bob-cli-lt.8.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lt.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lt.5.md) | [bob-cli-lt.5](bob-cli-lt.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`893bd2a`](https://github.com/bobs-org/bob-cli/commit/893bd2afa2c5f6e339d7f5e32b21c8187dff92e3) | feat(bank): add account, rule, and setting writer ops | [bob-cli-lt.5](bob-cli-lt.5.md) | 2026-11-15 19:40:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ls.7][1] | Need whether the workspace-10 agent still owns the protected bob-ledger-tools vault deploy | 1 |
| read-by | [agent:bob-cli-lt.5--1][2] | Need phase scope and prior verification status to finish the prepared completion | 1 |
| read-by | [agent:bob-cli-lt.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lt.5.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lt.land.md

<!-- sase:referenced-by:end -->
