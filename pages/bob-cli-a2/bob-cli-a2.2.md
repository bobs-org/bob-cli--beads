# Bead: bob-cli-a2.2 — Rust relation grammar, planners, label rules, registry guards, and config

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.2` · **Size:** medium
**Created:** 2026-10-20 09:08:22 EDT · **Closed:** 2026-10-20 09:58:57 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

cli-core: add src/native/task_relations/ (LINKS and LINKED FROM parsers, label normalisation, formatters, canonical sort, slot rules, and edit planners pinned by LK/LW). Add an is_managed_link_line registry predicate at every Task Link guard site, the relations.linked_from_lines config, and MC tests. No writer emits lines yet.

## Notes

[2026-10-20T13:58:38Z · bob-cli-a2.2] PROPOSED FOLLOW-UP: just check --lib flake on highlights_ref::fetch fake-curl ETXTBSY (os error 26) — already tracked as bob-cli-5l; isolated rerun of curl_pins_the_checked_address_with_resolve and curl_passes_q_as_first_argument passed

[2026-10-20T13:58:57Z · bob-cli-a2.2] Landed src/native/task_relations/ (LK1–LK20, LW1–LW13, Rule 6, MC15) plus is_managed_link_line at the five scanner sites, relations.linked_from_lines config (default true), and MC10/MC16/MC17 tests. canonical_link now keeps the explicit done/ path (LW13). just check: rustfmt and clippy green; lib 3110 passed; two highlights_ref fetch fake-curl tests failed once with ETXTBSY then passed isolated (bob-cli-5l). No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-a2.1](bob-cli-a2.1.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a2.4](bob-cli-a2.4.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a2.5](bob-cli-a2.5.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.2/README.md) | [bob-cli-a2.2](bob-cli-a2.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6d1f0a9`](https://github.com/bobs-org/bob-cli/commit/6d1f0a9c110ab8cf3a3a5d3751f15692b8485252) | feat(task-relations): add parsers, planners, and managed-link guards | [bob-cli-a2.2](bob-cli-a2.2.md) | 2026-10-20 09:59:55 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.2/README.md

<!-- sase:referenced-by:end -->
