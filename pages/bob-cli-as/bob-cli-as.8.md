# Bead: bob-cli-as.8 — Mac agenda renders Rotten Logs with a 🥀 chip

[Bead Pages](../README.md) / [bob-cli-as](README.md) / bob-cli-as.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.55.linker.w2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.55.linker.w2.md) · **Assignee:** `bob-cli-as.8` · **Size:** small
**Created:** 2026-10-23 08:24:13 EDT · **Closed:** 2026-10-23 09:00:40 EDT
**Plan:** [202610/rotten\_log.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_log.md)

## Description

mac-agenda: decode the agenda "rotten" log kind in Bob Mac Capture, render its header and entries like the other logs, and add a 🥀 N count chip.

## Notes

[2026-10-23T13:00:40Z · bob-cli-as.8] Mac agenda renders Rotten Logs: CaptureAgendaLog.rotten decodes 'rotten' (.other fallback kept), header '🥀 Rotten log', entries fold as .logEntry, chips '🥀 N' after ⚒/🗓 with 'Show rotten log, N entries' label. Tests: 4 new (decode, header/chip, chip order, .other fallback) — portable-check 1536 passed, docs-check passed. macOS BobMacCapture targets not compiled (Linux host); no Sources/BobMacCapture* changed.

## Dependencies

- **Depends on:** [bob-cli-as.2](bob-cli-as.2.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-as.9](bob-cli-as.9.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-as.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.8/README.md) | [bob-cli-as.8](bob-cli-as.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@73202c8`](https://github.com/bobs-org/bob-mac-capture/commit/73202c8142ca2fd4b3335d524df6153bc9ed3ef0) | feat(agenda): render Rotten Logs with a rotten chip | [bob-cli-as.8](bob-cli-as.8.md) | 2026-10-23 09:01:31 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-as.8][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.8/README.md

<!-- sase:referenced-by:end -->
