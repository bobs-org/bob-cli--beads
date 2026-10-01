# Bead: bob-cli-31.2 — bob freshness list and seed

[Bead Pages](../README.md) / [bob-cli-31](README.md) / bob-cli-31.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md) · **Assignee:** `bob-cli-31.2` · **Size:** medium
**Created:** 2026-09-30 19:32:05 EDT · **Closed:** 2026-09-30 20:38:33 EDT
**Plan:** [202609/task\_freshness\_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)

## Description

fresh-cli: headless review queue (bob freshness list, human and JSON) and a guarded, idempotent, staggered cutover seed (bob freshness seed) that aborts on any parse change, plus help, README, and CLI tests.

## Notes

[2026-10-01T00:38:33Z · bob-cli-31.2] fresh-cli landed: bob freshness list (human+JSON review queue, NEW then DUE, whole-vault counts, lints last, --limit rows-only) and bob freshness seed (bin-packed 7-bucket stagger, today bucket for other lanes, second-seed guard with --force, dual-parser invariance abort, re-read refusal, temp+rename writes, idempotent same-day rerun). Verified: cargo fmt clean, clippy no errors, full cargo test green (1402 unit + 677 CLI incl 15 new freshness CLI tests, 4 seed unit tests, freshness help tests), manual dry-run/apply/rerun/guard cycle on fixture vaults. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-31.1](bob-cli-31.1.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-31.4](bob-cli-31.4.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-31.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-31.2/README.md) | [bob-cli-31.2](bob-cli-31.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f103979`](https://github.com/bobs-org/bob-cli/commit/f103979594c7a1b471ddb6a9f291befce6c3db2a) | feat(freshness): add bob freshness list and seed review queue | [bob-cli-31.2](bob-cli-31.2.md) | 2026-09-30 20:41:17 EDT |
