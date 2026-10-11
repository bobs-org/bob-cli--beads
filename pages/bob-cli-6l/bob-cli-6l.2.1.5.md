# Bead: bob-cli-6l.2.1.5 — Evaluate review answers and formulas

[Bead Pages](../README.md) / [bob-cli-6l.2.1](bob-cli-6l.2.1.md) / bob-cli-6l.2.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.md) · **Assignee:** `bob-cli-6l.2.1.5` · **Size:** medium
**Created:** 2026-10-11 07:36:42 EDT · **Closed:** 2026-10-11 09:47:11 EDT
**Plan:** [202610/daily\_stats\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats_engine.md)

## Description

journal_formulas: implement journal distinct-row and last-answer selectors, recorded-writer compatibility, review-close gap detection, and checked formula evaluation with null and quality propagation. Test multi-host reader vectors and the existing R1-R19 writer vectors without changing the journal writer.

## Notes

[2026-10-11T13:46:59Z · bob-cli-6l.2.1.5] PROPOSED FOLLOW-UP: cli tests capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance and percent_listen_reference_runs_existing_worker_and_installs_audio fail identically on the clean base (missing listen runner binary); unrelated to journal_formulas

[2026-10-11T13:47:11Z · bob-cli-6l.2.1.5] journal_formulas done: evaluate_journal (distinct-key reviewed, last-answer keep_rate with pooled bp, tier/outcome parts, shipped+normalized decay spellings recognized, gap detection from registry review_closed incl. redefined defs) and evaluate_formula (checked arithmetic, half-away division, null/worst-quality propagation, latest-dep since) in src/native/stats; 10-case reader fixture plus R1-R19 loader prove recorded vectors feed the reader; review_answers.json untouched. Verified: cargo fmt clean, clippy clean for touched files, 68 stats lib tests pass, just check green except 2 listen-runner cli failures that reproduce identically on the clean base (recorded as PROPOSED FOLLOW-UP). epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-6l.2.1.4](bob-cli-6l.2.1.4.md) ✓ · ⧖ 2026-10-11
- **Blocks:** [bob-cli-6l.2.1.6](bob-cli-6l.2.1.6.md) ✓ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.2.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.5/README.md) | [bob-cli-6l.2.1.5](bob-cli-6l.2.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0d014c0`](https://github.com/bobs-org/bob-cli/commit/0d014c0299c25a5f13ca2947a155f0af8562e1c7) | feat(stats): evaluate review answers and checked formulas | [bob-cli-6l.2.1.5](bob-cli-6l.2.1.5.md) | 2026-10-11 09:48:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6l.2.1.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.5/README.md

<!-- sase:referenced-by:end -->
