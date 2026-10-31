# Bead: bob-cli-ez.2 — Host-local Keep status cache and its writers

[Bead Pages](../README.md) / [bob-cli-ez](README.md) / bob-cli-ez.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2y.linker.w0.md) · **Assignee:** `bob-cli-ez.2` · **Size:** medium
**Created:** 2026-10-31 13:32:41 EDT · **Closed:** 2026-10-31 14:26:19 EDT
**Plan:** [202610/gkeep\_footer\_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gkeep_footer_indicator.md)

## Description

keep-status-cache: add the 0600 status.json cache under bob's state dir with a default-pull observation helper, and make list, pull (dry and real), doctor, and login record observations, failures, and pull invalidation.

## Notes

[2026-10-31T17:57:11Z · bob-cli-ez.2] PROPOSED FOLLOW-UP: skipped decisions-web record (decision_record=no) for keep-status-cache — epic asked whether to add a decisions-web record that bob owns the Keep count, its cache, and its check budget; auto-decided false, so no memory edit. Land agent: no record unless Bryan reopens that ask.

[2026-10-31T18:26:19Z · bob-cli-ez.2--1] Verified keep-status-cache: 0600 status.json writers on list/pull/doctor/login; vault-only list writes nothing; -n records pending; archive failure stays invalidated; -l/-i still record the default count; parity fixture counts 5; just check passed; no leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-ez.3](bob-cli-ez.3.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ez.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ez.2.md) | [bob-cli-ez.2](bob-cli-ez.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ecffd6f`](https://github.com/bobs-org/bob-cli/commit/ecffd6fa8fa8fbc444d276a434cac43b3b4df75b) | feat(gkeep): persist host-local Keep status cache | [bob-cli-ez.2](bob-cli-ez.2.md) | 2026-10-31 14:28:03 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ez.2--1][1] | Need the phase scope, design file, notes, and DECISIONS after monitor verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ez.2.md

<!-- sase:referenced-by:end -->
