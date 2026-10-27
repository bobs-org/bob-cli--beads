# Bead: bob-cli-da.3 — Correct the vault-format walk order and check the page

[Bead Pages](../README.md) / [bob-cli-da](README.md) / bob-cli-da.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-d7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d7.land.md) · **Assignee:** `bob-cli-da.3` · **Size:** small
**Created:** 2026-10-27 16:30:19 EDT · **Closed:** 2026-10-27 16:39:20 EDT
**Plan:** [202610/backlog\_batch\_b2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b2.md)

## Description

vault-format-docs: read bob-cli-d8, fix docs/reference/vault-format.md lines 171-172 to PRE → NEW → PROJECTS → PENDING → NEXT → RECURRING → TICKLER → ROTTEN → POST per src/native/freshness/state.rs Tier and docs/freshness.md, check nearby explanations, run just docs-check, and close bob-cli-d8. Docs only, no behavior or memory changes.

## Notes

[2026-10-27T20:39:20Z · bob-cli-da.3] Updated docs/reference/vault-format.md to the PRE → NEW → PROJECTS → PENDING → NEXT → RECURRING → TICKLER → ROTTEN → POST walk order; checked nearby explanations against docs/freshness.md and src/native/freshness/state.rs. just docs-check passed (447 passed, 1 skipped); git diff --check passed. epic-symbols reported no leftovers. Closed this assigned phase only; bob-cli-d8 remains untouched.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-da.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.3/README.md) | [bob-cli-da.3](bob-cli-da.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4fd8291`](https://github.com/bobs-org/bob-cli/commit/4fd82919009fa061ced90434f8033528c9eb6f85) | docs(freshness): correct vault walk order | [bob-cli-da.3](bob-cli-da.3.md) | 2026-10-27 16:40:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-da.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.3/README.md

<!-- sase:referenced-by:end -->
