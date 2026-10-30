# Bead: bob-cli-e6.13 — Task Card type edits relocate the live Task Link

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.13` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-29 23:42:17 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

task-card-relocate: rename the Task Card stage to Type, allow every type including PLAN, and relocate the task's live link with a consequence line, strict refusal, and one gesture.

## Notes

[2026-10-30T03:41:41Z · bob-cli-e6.13] PROPOSED FOLLOW-UP: view test "theme menu stays grey when hueFor is missing or throws" fails identically on clean HEAD (header pill lacks is-muted class); pre-existing, unrelated to e6.13

[2026-10-30T03:41:50Z · bob-cli-e6.13] PROPOSED FOLLOW-UP: plugins docs-check reports generated drift in docs/reference/glossary.md and docs/develop/decisions.md on a tree this phase did not touch; leave regen to e6.16 closeout

[2026-10-30T03:41:59Z · bob-cli-e6.13] PROPOSED FOLLOW-UP: bob-ledger-tools deploy refused (sibling bob-cli_14 checkout holds uncommitted ledger-tools changes); e6.13 strict-refusal message numbers need the additive routing fields once that syncs — refusal behavior itself is correct

[2026-10-30T03:42:17Z · bob-cli-e6.13] Task Card Type stage relocates the live Task Link per D8 absorb: Type rename, PLAN allowed, consequence line + strict refusal in stage, field-first then checked ledger write, D10 toasts, docs updated. Verified: theme-edit suite 22/22, model 16/16+theme-edit 39/0 combined, ledger routing 31/0, bullet-move 30/0, link-picker 16/16, build:check clean. Committed f3e566d in bob-plugins and deployed navigation-hotkeys to vault. Pre-existing failures recorded as follow-ups (grey-pill view test, docs generated drift); ledger-tools deploy blocked by sibling checkout.

## Dependencies

- **Depends on:** [bob-cli-e6.10](bob-cli-e6.10.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.14](bob-cli-e6.14.md) ◐ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.13/README.md) | [bob-cli-e6.13](bob-cli-e6.13.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.13][1] | Need full bead including notes for implementation | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.13/README.md

<!-- sase:referenced-by:end -->
