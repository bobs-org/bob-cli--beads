# Bead: bob-cli-ii.4.1 — Gmail reply holds, reply lifts, and send finalization

[Bead Pages](../README.md) / [bob-cli-ii.4](bob-cli-ii.4.md) / bob-cli-ii.4.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ii.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.4.md) · **Assignee:** `bob-cli-ii.4.1.land`
**Created:** 2026-11-08 12:01:29 EST
**Plan:** [202611/gmail\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_reply_watch.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_reply_watch.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_reply_watch.md

<!-- sase:links:end -->

## Description

Watched Gmail tasks react once to new outgoing or incoming messages, preserve manual edits between messages, and recover safely after deferrals or failures.

## Notes

[2026-11-08T21:42:26Z · bob-cli-ii.4.1.land] LAND TRIAGE (bob-cli-ii.4.1 land): (1) records/schema.rs clippy failures (from 4.1.1 #1 and 4.1.2 #2): DECLINED, no longer reproduce; 'just lint' passes on b252669b plus the land edits, and the records landing 8ff0d8ed changed schema.rs. (2) 8 clippy::collapsible_if errors in gmail/sync/file.rs and watch_apply.rs (4.1.5 #1): CAUSED BY THIS EPIC (phases 4.1.3/4.1.4), fixed in this landing; 'just lint' now passes. (3) guard real_lock_contention_and_release flake (4.1.2 #1): not caused by this epic. It reproduces on the pre-watch base 23217c1d (3 of 6 gmail:: lib runs). The test came from 39122cb2 (bob-cli-ii.3.1.2), so it is recorded as a DISCOVERED ISSUE note on active ancestor epic bob-cli-ii, not as a task. Other land edits: removed stale watch dead-code allowances and deleted the now-dead EnrollmentMembership::watched, WatchScan::watcher_count, WatchingTask::watches, and hold::configured_nudge_for_send; tests now call watch::watched_keys and watchers().count(). Integration: the only commits interleaved since b4147b0b are the records-engine commits 93c7c114, b9db7007, a8ccf5ed, and 8ff0d8ed. None touch Gmail, freshness, or task-status code, so nothing needed rewiring.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.land/README.md) | [bob-cli-ii.4.1](bob-cli-ii.4.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`25c0223`](https://github.com/bobs-org/bob-cli/commit/25c02232a5820c6625c8cf99f2e2eabeace421eb) | fix(gmail): clear reply-watch lint and stale dead-code allowances | [bob-cli-ii.4.1](bob-cli-ii.4.1.md) | 2026-11-08 16:45:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.4.1.2][1] | Need epic decisions that govern the assigned phase | 1 |
| read-by | [agent:bob-cli-ii.4.1.3][2] | need parent epic decisions | 1 |
| read-by | [agent:bob-cli-ii.4.1.4][3] | Need the parent epic decisions and phase contract | 1 |
| read-by | [agent:bob-cli-ii.4.1.5][4] | Need epic DECISIONS and remaining phase scope | 1 |
| read-by | [agent:bob-cli-ii.4.1.6][5] | Need epic DECISIONS and phase list for 4.1.6 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.5/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.6/README.md

<!-- sase:referenced-by:end -->
