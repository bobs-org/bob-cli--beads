# Bead: bob-cli-e6.9 — #TYPE identity, ledger agreement marks, and Ledger Tools words

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.9` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-29 22:57:57 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

type-tag-rendering: render explicit types as a colored #TYPE in the #task slot, retire the trailing pill, mark disagreeing ledger links, and rename Ledger Tools copy to type.

## Notes

[2026-10-30T02:57:57Z · bob-cli-e6.9] D11 landed in bob-plugins Ledger Tools plus bob-cli task-tag-marks contract. Explicit [type::]/[theme::] renders as colored #TYPE in the #task slot (identity ::after, field folded, no trailing pill); inherited stays a hash until Toggle inherited task types (off default); disagreeing Task Links get dashed #TYPE prefix; Day strip/Stats copy Time by type / Types; JSON theme unchanged. Verified: node --test identity+theme-rendered+theme-marks+tag-marks+manager+day-strip+stats 123/123; D11 8x4x2 contrast >=4.5:1; fragments all <=1000; npm run build + docs:inventory:check + build:check; just docs-gen + just docs-check green; epic-symbols none; vault ledger-tools deployed from this checkout. Glossary rename left for closeout (memory_glossary=yes).

## Dependencies

- **Blocks:** [bob-cli-e6.14](bob-cli-e6.14.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.16](bob-cli-e6.16.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.8](bob-cli-e6.8.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.9/README.md) | [bob-cli-e6.9](bob-cli-e6.9.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dfc08c1`](https://github.com/bobs-org/bob-cli/commit/dfc08c19d08a94581cba5e5070498b2f3fdac738) | docs(task-tag-marks): #TYPE identity contract | [bob-cli-e6.9](bob-cli-e6.9.md) | 2026-10-29 22:59:42 EDT |
| bob-plugins | [`bob-plugins@eb71f95`](https://github.com/bobs-org/bob-plugins/commit/eb71f95aa8ab038091e799252f02be8dcb90e624) | feat(ledger-tools): render explicit task types as colored #TYPE | [bob-cli-e6.9](bob-cli-e6.9.md) | 2026-10-29 23:11:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.9][1] | Need the phase scope, notes, and design file before finishing remaining docs/close work | 9 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.9/README.md

<!-- sase:referenced-by:end -->
