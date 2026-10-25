# Bead: bob-cli-an.6.6.6.5.6.5.5.6 — Backlog batch 9: quiet EPIPE exits, explicit listen publish manifest state, and three recurring test flakes

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) / bob-cli-an.6.6.6.5.6.5.5.6

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.land`
**Created:** 2026-10-25 08:44:09 EDT
**Plan:** [202610/backlog\_batch9\_epipe\_listen\_publish\_refresh\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md

<!-- sase:links:end -->

## Description

Close five existing task beads by making bob exit quietly when its stdout reader closes early, marking explicitly published listen episodes in their source library, and removing the Mac hidden-refresh flake, the capture-related debug perf-gate flake, and the migrate-tasks snapshot race. Continue the bounded backlog campaign until all project task beads are resolved.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.2][1] | parent epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.2/README.md

<!-- sase:referenced-by:end -->
