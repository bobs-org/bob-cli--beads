# Bead: bob-cli-go.13 — Live verification, cross-links, and accepted memory

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.13` · **Size:** small
**Created:** 2026-11-03 16:11:32 EST · **Closed:** 2026-11-04 12:23:03 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

closeout: verify every gesture end to end in a scratch vault, fix cross-links and stale docs, apply only the accepted memory decisions, and record follow-ups.

## Notes

[2026-11-04T17:22:41Z · bob-cli-go.13] PROPOSED FOLLOW-UP: capture still swallows unknown short flags as task text — `bob capture --dry-run -o -- ...` files `-o` as text while long flags error; cites closed bob-cli-8a (fixed long-flag guard only)

[2026-11-04T17:23:03Z · bob-cli-go.13] Closeout verified: 21/21 live scratch-vault checks green (move -t, merge into task/drawer/section, split, capture ~ merge, capture > transfer move+merge, rerun unchanged, reconcile converges to no-op, archive sweeps tombstone, move_to_task teaching refusal). Docs: removed stale sibling-phase admonitions in task-merge.md, delinked tests.rs path (lychee), added missing #transfer Shapes fence + target-run prose so 5 smoke queries resolve, added exact @route+id @route+id query for token coverage, kept capture-syntax under 6000-word budget (5993). Memory: added front matter to glossary task-merge/task-split strands (accepted memory_glossary_strands + memory_relation_effects already in body text); sase memory init clean. Gates: just fmt/lint/test/docs-gen/docs-check all pass. No epic-symbol leftovers. One PROPOSED FOLLOW-UP noted (short-flag swallow gap vs closed bob-cli-8a). Obsidian Ctrl+Shift+T/L and Mac-band manual checks left for Bryan.

## Dependencies

- **Depends on:** [bob-cli-go.12](bob-cli-go.12.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.9](bob-cli-go.9.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.13/README.md) | [bob-cli-go.13](bob-cli-go.13.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a6c55cb`](https://github.com/bobs-org/bob-cli/commit/a6c55cbbd22823a96a24b5b057dccb3f998a0992) | docs(closeout): verify move/merge/split end to end, fix cross-links and accepted memory | [bob-cli-go.13](bob-cli-go.13.md) | 2026-11-04 12:24:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h0.1][1] | Need to cite the phase that owns the known docs-check memory-format blocker | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.1/README.md

<!-- sase:referenced-by:end -->
