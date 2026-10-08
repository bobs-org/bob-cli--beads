# Bead: bob-cli-5p.1 — Contract, Rust evaluator, and bob freshness CLI

[Bead Pages](../README.md) / [bob-cli-5p](README.md) / bob-cli-5p.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0yb](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0yb.md) · **Assignee:** `bob-cli-5p.1` · **Size:** medium
**Created:** 2026-10-08 11:03:15 EDT · **Closed:** 2026-10-08 11:22:26 EDT
**Plan:** [202610/recurring\_review\_tier.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/recurring_review_tier.md)

## Description

rust: write the RECURRING contract and RC vectors into docs/freshness.md, add due/start to the Rust rows, apply the recurring overlay, queue order, counts, schema 11 CLI output, the recurring_undated lint, and tests.

## Notes

[2026-10-08T15:22:14Z · bob-cli-5p.1] PROPOSED FOLLOW-UP: Add RECURRING-tier decision record, mark decisions:review-walk-is-tiered superseded in part, and edit glossary:task-freshness (memory_records=no in this phase; land agent to triage)

[2026-10-08T15:22:26Z · bob-cli-5p.1] RECURRING tier landed in Rust: Tier::Recurring between Next/Tickler, occurs_on=min(scheduled,due,start), overlay_recurring after checklist overlay, queue due_on/path/line order, ByTier.recurring+Counts.recurring_due, recurring_undated lint, schema 11 JSON+human CLI, docs/freshness.md contract+RC1-RC12, README order. Verified: cargo fmt clean, clippy exit 0 (no new warnings), cargo test --no-fail-fast all green (1971 lib + 1189 cli incl. 12 new RC unit tests and list_json_and_human_cover_recurring_tier). epic-symbols clean, no leftovers.

## Dependencies

- **Blocks:** [bob-cli-5p.2](bob-cli-5p.2.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5p.4](bob-cli-5p.4.md) ◐ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5p.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5p.1/README.md) | [bob-cli-5p.1](bob-cli-5p.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`56a5e68`](https://github.com/bobs-org/bob-cli/commit/56a5e68811203a90e2b774fb9ad20dcdfd27ba07) | feat(freshness): add RECURRING walk tier for due recurring tasks | [bob-cli-5p.1](bob-cli-5p.1.md) | 2026-10-08 11:23:29 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5p.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5p.1/README.md

<!-- sase:referenced-by:end -->
