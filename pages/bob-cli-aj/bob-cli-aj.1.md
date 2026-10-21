# Bead: bob-cli-aj.1 — bob-cli relation-label typing assist and completion contract

[Bead Pages](../README.md) / [bob-cli-aj](README.md) / bob-cli-aj.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12t](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12t.md) · **Assignee:** `bob-cli-aj.1` · **Size:** medium
**Created:** 2026-10-21 08:01:49 EDT · **Closed:** 2026-10-21 08:27:51 EDT
**Plan:** [202610/relation\_pipe\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_pipe_card.md)

## Description

bob: add the `attach_relation_label` capture-rewrite rule, add the `relation` object and `owner` to `relation_label` completions, and update tests, help, and docs.

## Notes

[2026-10-21T12:27:51Z · bob-cli-aj.1] bob phase done: attach_relation_label rewrite rule glues ' |' to relation tokens per completion grammar (all 14 behavior-table rows covered by tests, idempotent, no-cursor skip); relation_label completions now carry additive relation {direction to/from, range sigil-to-| with range.end==replacement.start} and owner (existing-task resolved or new-task text), omitted elsewhere. Verified: focused tests (7 relations incl. new contract test; 48 rewrite/rewrite-JSON incl. 3 new), just check exit 0 (fmt, clippy, 3153 lib + all integration binaries), just docs-gen refreshed capture-rewrite golden, just docs-check passed. epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-aj.2](bob-cli-aj.2.md) ◐ · ⧖ 2026-10-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-aj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aj.1/README.md) | [bob-cli-aj.1](bob-cli-aj.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bcc201f`](https://github.com/bobs-org/bob-cli/commit/bcc201feebc262f2b4f16569e959bd03cedecce4) | feat(capture): attach relation labels on typed pipe and expose relation in completions | [bob-cli-aj.1](bob-cli-aj.1.md) | 2026-10-21 08:28:52 EDT |
