# Bead: bob-cli-a2.12 — Task Card \`⇧L\` Linked from…, counted gestures, hand-edit mirror, and Ctrl+D

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.12` · **Size:** medium
**Created:** 2026-10-20 09:08:23 EDT · **Closed:** 2026-10-20 12:12:31 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

nav-linked-from: add the reverse stage (⇧L, Ctrl+Shift+Alt+L, and Ctrl+Shift+P on a LINKED FROM line) that writes other tasks' LINKS lines, counted N<Ctrl+Shift+L> sources, and the LINKS hand-edit mirror with undo re-arm. Ctrl+D on the Links to row removes every link, Ctrl+D on Linked from is refused, and LG vectors are tested.

## Notes

[2026-10-20T16:12:07Z · bob-cli-a2.12] PROPOSED FOLLOW-UP: Track existing clean-base check failures — npm test still has six known failures tracked by bob-cli-a2.9 note #2 and reverified against clean origin/master in bob-cli-a2.11 note #3; docs:check has the same two missing MkDocs Material environment failures recorded in bob-cli-a2.11 note #3.

[2026-10-20T16:12:31Z · bob-cli-a2.12] Implemented and deployed Linked from, relation mirror hand edits, counted Links to, Ctrl+D behavior, and nav relations v1. Build, validate (7/7), and 62 focused tests pass; full suite has the six clean-base failures and docs:check the two known MkDocs Material environment failures, recorded as a proposed follow-up. Epic-symbol check is clear.

## Dependencies

- **Depends on:** [bob-cli-a2.11](bob-cli-a2.11.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a2.15](bob-cli-a2.15.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.12/README.md) | [bob-cli-a2.12](bob-cli-a2.12.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3ba8bf9`](https://github.com/bobs-org/bob-plugins/commit/3ba8bf9a5c10db5eba871d186bf9818132e31414) | feat(navigation): add linked-from relation stage | [bob-cli-a2.12](bob-cli-a2.12.md) | 2026-10-20 12:13:16 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.12][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.12/README.md

<!-- sase:referenced-by:end -->
