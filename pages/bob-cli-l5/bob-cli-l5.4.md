# Bead: bob-cli-l5.4 — Docs, decision record, and glossary

[Bead Pages](../README.md) / [bob-cli-l5](README.md) / bob-cli-l5.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c2.md) · **Assignee:** `bob-cli-l5.4` · **Size:** medium
**Created:** 2026-11-12 16:39:08 EST · **Closed:** 2026-11-13 03:55:36 EST
**Plan:** [202611/gcal\_external\_event\_ack.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_external_event_ack.md)

## Description

docs: author docs/gcal-acks.md, update docs/gcal.md (commands, row-ownership table, JSON, known limits) and docs/gcal-notes.md cross-links, keep docs-gen/docs-check green, and file the decision record and glossary strand through /sase_memory_write.

## Notes

[2026-11-13T08:53:32Z · bob-cli-l5.4] PROPOSED FOLLOW-UP: Repair the unchanged docs/gcal-notes.md link to ../reference/mac-capture/event-notes.md — just docs-check reproduces the offline lychee failure already tracked by bob-cli-l7; this phase only added cross-links and did not introduce the broken path.

[2026-11-13T08:55:36Z · bob-cli-l5.4] Added and indexed docs/gcal-acks.md; updated gcal command, ownership, JSON, and known-limit docs plus note cross-links; expanded the authorized Event Ack glossary strand. just docs-gen and git diff --check pass. just docs-check passes lint, generated drift, strict build, and published URL checks, then fails only on the pre-existing offline lychee link tracked by bob-cli-l7 and recorded as a proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-l5.3](bob-cli-l5.3.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.4/README.md) | [bob-cli-l5.4](bob-cli-l5.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b68af01`](https://github.com/bobs-org/bob-cli/commit/b68af013d1fc403460d988c92b72fe4265767c43) | docs(gcal): document external event acknowledgements | [bob-cli-l5.4](bob-cli-l5.4.md) | 2026-11-13 03:57:41 EST |
