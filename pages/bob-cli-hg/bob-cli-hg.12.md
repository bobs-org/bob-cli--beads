# Bead: bob-cli-hg.12 — Compose, reply, draft, and confirmed send

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.12

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.12` · **Size:** large
**Created:** 2026-11-05 12:37:50 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

gmail-compose: compose notes and Reply sections, Markdown-to-email rendering with refusals, Gmail drafts recorded by id, an exact digest-bound preview, send by draft id with crash recovery, the compose scope, and the sent card.

## Notes

[2026-11-06T12:10:31Z · bob-cli-hg.12] Planning audit: no prior phase-work notes; baseline fcc4efa5 has save/list and compose login but no new/reply/draft/send implementation. Validated a six-phase child epic covering source notes, rendering, draft/readback previews, send recovery, finalization, and docs/consumer fixtures. Verified gog v0.44.0 rejects simultaneous --thread-id and --reply-to-message-id; the plan preserves exact threading via message ID plus returned-thread verification. No epic-symbol entries for this phase. No product or memory files changed; phase remains in progress pending plan approval and implementation.

## Dependencies

- **Blocks:** [bob-cli-hg.13](bob-cli-hg.13.md) ◐ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.6](bob-cli-hg.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.md) | [bob-cli-hg.12](bob-cli-hg.12.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.4][1] | Need epic DECISIONS | 1 |
| read-by | [agent:cq][2] | Understand compose/reply/draft/confirmed-send phase status and UX | 1 |
| read-by | [agent:research.5s.grk][3] | Need remaining Gmail phase user-facing scopes for the guide | 1 |
| read-by | [agent:research.5s.mus][4] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.cq/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.grk/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
