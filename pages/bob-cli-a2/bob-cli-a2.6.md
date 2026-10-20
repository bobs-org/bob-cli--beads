# Bead: bob-cli-a2.6 — Relation completion pools, label suggestions, and task-id replacements

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.6` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT · **Closed:** 2026-10-20 11:27:48 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

capture-complete: add contexts relation_to, relation_from, and relation_label; reuse the `&` catalog (open, closed, archived) with direction-specific eligibility, ranking, and badges. Label suggestions come from every LINKS line, and a typed-label row returns bob's canonical spelling. Add the relation_to_replacement and relation_from_replacement task-id fields, the owner-picker relations[], and shell groups.

## Notes

[2026-10-20T15:19:20Z · bob-cli-a2.6] PROPOSED FOLLOW-UP: Restore the optional github-callouts dependency for Material docs tests — docs-check fails both test_templates.py Material cases with ModuleNotFoundError, reproducing the clean-tree failure already recorded by bob-cli-a2.1.

[2026-10-20T15:27:48Z · bob-cli-a2.6] Closed by explicit `sase stitch create -B close` after create_commit landed fa9669dd ("feat(capture): implement task relation completion"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-a2.6` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-a2.13](bob-cli-a2.13.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.5](bob-cli-a2.5.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.6/README.md) | [bob-cli-a2.6](bob-cli-a2.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fa9669d`](https://github.com/bobs-org/bob-cli/commit/fa9669dd2a09caf4077ebdf9ef8bc7c39cc95a33) | feat(capture): implement task relation completion | [bob-cli-a2.6](bob-cli-a2.6.md) | 2026-10-20 11:26:44 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.6/README.md

<!-- sase:referenced-by:end -->
