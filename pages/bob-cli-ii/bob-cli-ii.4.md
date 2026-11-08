# Bead: bob-cli-ii.4 — The awaiting-reply hold and the reply lift

[Bead Pages](../README.md) / [bob-cli-ii](README.md) / bob-cli-ii.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19q.md) · **Assignee:** `bob-cli-ii.4` · **Size:** large
**Created:** 2026-11-07 17:21:21 EST · **Closed:** 2026-11-08 17:42:12 EST
**Plan:** [202611/gmail\_sync\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_reply_watch.md)

## Description

watch: fetch watched threads every run, refresh their mail notes, and apply each new turn to every open linking task, holding on your send and lifting with an [unblocked:: today] return on their reply, including the send finalize hook and the running-session guard.

## Notes

[2026-11-08T17:00:11Z · bob-cli-ii.4] Planning review: prerequisites ii.2/ii.3 and subsequent sync retry/recovery fixes are present at cd8a031f, but hold/lift, watch polling, and the send hook are not implemented. Prepared a six-phase child epic covering line rules, watch preparation, transaction/recovery, polling/reporting, send finalization, and contracts. The plan preserves inherited reply_hold_record=yes without re-asking it; the hermetic plan validator passes with only its memory-inheritance warning. Existing freshness vectors UB14/UB15 must be preserved; new reply vectors use the next free ids. No epic-symbol entries currently belong to ii.4. Child land must verify and close ii.4 only, leaving ii to its land agent.

## Dependencies

- **Depends on:** [bob-cli-ii.2](bob-cli-ii.2.md) ✓ · ⧖ 2026-11-07
- **Depends on:** [bob-cli-ii.3](bob-cli-ii.3.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.5](bob-cli-ii.5.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.8](bob-cli-ii.8.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.4.md) | [bob-cli-ii.4](bob-cli-ii.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.4.1.land][1] | Need the parent link | 1 |
| read-by | [agent:bob-cli-ii.4.1.land--1][1] | Verify the assigned phase bead and its child status before closeout | 2 |
| read-by | [agent:bob-cli-in.3][2] | Need to identify whether unused sync read APIs have a real consumer in the open reply-watch phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.4.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-in.3/README.md

<!-- sase:referenced-by:end -->
