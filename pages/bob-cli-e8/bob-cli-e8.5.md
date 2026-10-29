# Bead: bob-cli-e8.5 — Live mention index and relationIndex v2

[Bead Pages](../README.md) / [bob-cli-e8](README.md) / bob-cli-e8.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2v.linker.w0.md) · **Assignee:** `bob-cli-e8.5` · **Size:** medium
**Created:** 2026-10-29 17:20:22 EDT · **Closed:** 2026-10-29 18:40:38 EDT
**Plan:** [202610/inline\_task\_mentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inline_task_mentions.md)

## Description

plugin-index: teach bob-ledger-tools' live index the mention rules from the copied vectors, publish typed linkedFrom rows under relationIndex v2, and expose a pure scanMentions helper.

## Notes

[2026-10-29T22:40:09Z · bob-cli-e8.5] PROPOSED FOLLOW-UP: nav theme tests red on master — commit 68db3fb changed task-theme notices/pills without updating 5 tests (theme notices x3, stage rows, theme menu grey); full npm test also shows one load-flaky perf-bound test (freshness-mark-surfaces large-child-block, passes solo). All unrelated to mentions; base npm test is red via build:check on stale nav main.js

[2026-10-29T22:40:20Z · bob-cli-e8.5] Phase notes: fixture vectors.json copied byte-for-byte (v1, 16 vectors MN1-M12/MN21-23/MN25); scanner matches all 16 occurrence sets incl MN22 Unicode ch=13; reserved-label + typed-kind parsers (MN15/MN16); relationIndex v2 with linkedFrom/scanMentions, M7 precedence, alsoMentioned (MN8), dependency omit (MN9); switch linked_from_mentions default false with stat-key cache; perf apollo cold 1322.85ms/3256 prefilter over 6795 notes, warm 23.36ms/292989B (chunked 24/turn); npm test 4271/4277 green — only pre-existing nav-theme reds (see follow-up); docs:gen + docs:check passed; bob plugins sync deployed bob-ledger-tools (nav refused: foreign uncommitted build, not mine)

[2026-10-29T22:40:38Z · bob-cli-e8.5] relationIndex v2 live: MN fixture byte-identical (16 vectors, all occurrence/display/site/excerpt sets match incl MN22 Unicode); reserved-label + typed-kind parsers; linkedFrom/scanMentions with M7 + overlay; switch-gated (default false); 8 new + all relation tests green; docs:gen/check passed; ledger-tools synced. Only reds are 5 pre-existing nav-theme tests (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-e8.1](bob-cli-e8.1.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.6](bob-cli-e8.6.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.8](bob-cli-e8.8.md) ◐ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e8.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.5/README.md) | [bob-cli-e8.5](bob-cli-e8.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@13ac4dc`](https://github.com/bobs-org/bob-plugins/commit/13ac4dcc70e66cbf80d7e8c1aa1532e6d37350b3) | feat(ledger-tools): live mention index and relationIndex v2 | [bob-cli-e8.5](bob-cli-e8.5.md) | 2026-10-29 18:41:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e8.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.5/README.md

<!-- sase:referenced-by:end -->
