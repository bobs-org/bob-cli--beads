# Bead: bob-cli-ii.4.1.5 — Apply the same watch effect after a confirmed send

[Bead Pages](../README.md) / [bob-cli-ii.4.1](bob-cli-ii.4.1.md) / bob-cli-ii.4.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ii.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.4.md) · **Assignee:** `bob-cli-ii.4.1.5` · **Size:** medium
**Created:** 2026-11-08 12:01:29 EST · **Closed:** 2026-11-08 15:41:02 EST
**Plan:** [202611/gmail\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_reply_watch.md)

## Description

send_hook: extend acknowledged-send finalization and completion recovery to apply the shared watcher plan under the send lock without resending or losing deferred markers.

## Notes

[2026-11-08T20:40:48Z · bob-cli-ii.4.1.5] PROPOSED FOLLOW-UP: just lint fails on clean master 457153f0 with 8 clippy::collapsible_if errors in src/native/gmail/sync/file.rs and watch_apply.rs — identical on the send_hook tree; no open task bead tracks this.

[2026-11-08T20:41:02Z · bob-cli-ii.4.1.5] Confirmed send holds enrolled watchers, skips unwatched sends, defers running holds until the next sync, blocks hold when sibling metadata is missing, lifts when a sibling incoming move wins, and retries the watch marker from complete state without a second Gmail send. cargo test --test gmail_send (11), gmail_sync (27), compose/watch lib tests (79), plus gmail_draft/compose_contract/turns/shell. just fmt clean. just lint still fails on clean 457153f0 with 8 clippy::collapsible_if in gmail/sync/file.rs and watch_apply.rs. epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-ii.4.1.4](bob-cli-ii.4.1.4.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ii.4.1.6](bob-cli-ii.4.1.6.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.4.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.5/README.md) | [bob-cli-ii.4.1.5](bob-cli-ii.4.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5a63e9a`](https://github.com/bobs-org/bob-cli/commit/5a63e9a2ccc4f4376da6c54df0ed07a01caa9660) | feat(gmail): apply reply-watch effects after a confirmed send | [bob-cli-ii.4.1.5](bob-cli-ii.4.1.5.md) | 2026-11-08 15:42:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.4.1.5][1] | Need remaining notes, decisions, and design file | 2 |
| read-by | [agent:bob-cli-ii.4.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.4.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.4.1.land.md

<!-- sase:referenced-by:end -->
