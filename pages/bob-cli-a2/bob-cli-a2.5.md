# Bead: bob-cli-a2.5 — Capture \`~\` / \`~~\` lexer, guards, and capture-parse wire

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.5` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT · **Closed:** 2026-10-20 10:37:03 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

capture-parse: add a relation scanner in the `&` / `*` modifier runs with the digit, slash, strike, escape, and placement guards; labels after `|`; relation_* spans; relations[]; relation_target and relation_label needs; owner reuse; the relation_grammar signal; and a temporary execution refusal. Pinned by LP vectors.

## Notes

[2026-10-20T14:37:03Z · bob-cli-a2.5] capture-parse ~ wire landed: scanner in leading/trailing runs with digit/slash/strike/escape guards, labels after |, relation_* spans, relations[] + relation_grammar + RelationTarget/Label needs, owner reuse, temp unsupported guard. Verified: 19 parse_relation tests pass (LP1-LP18 + guard), 864 capture CLI tests pass, 3112 lib tests pass, 1881 CLI tests pass, clippy/fmt clean, docs-gen regenerated.

## Dependencies

- **Depends on:** [bob-cli-a2.2](bob-cli-a2.2.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a2.6](bob-cli-a2.6.md) ◐ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a2.7](bob-cli-a2.7.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.5/README.md) | [bob-cli-a2.5](bob-cli-a2.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.5/README.md

<!-- sase:referenced-by:end -->
