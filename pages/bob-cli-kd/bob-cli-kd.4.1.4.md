# Bead: bob-cli-kd.4.1.4 — Document the import and install the Monday ritual

[Bead Pages](../README.md) / [bob-cli-kd.4.1](bob-cli-kd.4.1.md) / bob-cli-kd.4.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.md) · **Assignee:** `bob-cli-kd.4.1.4` · **Size:** small
**Created:** 2026-11-11 14:24:04 EST · **Closed:** 2026-11-11 19:53:10 EST
**Plan:** [202611/bank\_import.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import.md)

## Description

docs-ritual: finish the import and sync documentation, regenerate CLI references, verify the installed command, and idempotently capture the weekly Bank import PRE chore; leave closure evidence for the land agent.

## Notes

[2026-11-12T00:52:51Z · bob-cli-kd.4.1.4] PROPOSED FOLLOW-UP: just docs-check fails identically on the clean base tree with 3 pre-existing issues (broken page link to bob-vim-yank-flash.md#verification, broken anchor task-dependencies.md#1217-lp---leaf-vector, broken anchor gcal.md#events at vault-git-sync.md:271); none are in docs-ritual sections

[2026-11-12T00:52:56Z · bob-cli-kd.4.1.4] PROPOSED FOLLOW-UP: live vault ~/bob/.gitignore has no !/.bob/bank/*.jsonl allowlist line and .gitattributes has no .bob/bank merge=union entry, so git check-ignore marks .bob/bank/athena.jsonl ignored and the first real Monday import would commit month rows without its journal; apply the lines documented in docs/vault-git-sync.md#bank-import-journal to the live vault and sync

[2026-11-12T00:53:10Z · bob-cli-kd.4.1.4] docs-ritual done: docs/bank.md gained the full Import contract (sources, account resolution, matching, naming, hashed IDs, journal schema, commit/preview/replay, limits) plus import usage/exits/JSON; docs/vault-git-sync.md gained the Bank import journal section with allowlist, subject, and revert runbook; json-outputs.md lists import. just docs-gen clean (CLI ref already current); just docs-check fails only on 3 pre-existing base-tree issues (noted as follow-up). Verified: cargo test --lib bank 92 passed; just check exit 0; just install then synthetic-vault proof (dry-run New 2 exit 0, one scoped bank: import 2 rows (checking) commit with rows+journal and sync ok, replay no-op). Installed bob bank import --help verified. Exactly one Monday PRE Bank import chore captured into gtd_daily.md ([repeat:: every week on Monday when done], scheduled 2026-11-16, #gtd #pre); daily Acknowledge bank chore untouched. Live-vault .gitignore/.gitattributes bank gap noted as follow-up. No SASE memory touched.

## Dependencies

- **Depends on:** [bob-cli-kd.4.1.3](bob-cli-kd.4.1.3.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.4/README.md) | [bob-cli-kd.4.1.4](bob-cli-kd.4.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.4.1.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.4/README.md

<!-- sase:referenced-by:end -->
