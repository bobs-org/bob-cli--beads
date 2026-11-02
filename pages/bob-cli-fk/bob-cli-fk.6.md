# Bead: bob-cli-fk.6 — bob-mac-capture: buffer wings on the Calendar rail and buffer-aware cards

[Bead Pages](../README.md) / [bob-cli-fk](README.md) / bob-cli-fk.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c5.md) · **Assignee:** `bob-cli-fk.6` · **Size:** medium
**Created:** 2026-11-01 21:42:32 EST · **Closed:** 2026-11-02 00:13:47 EST
**Plan:** [202611/gcal\_event\_buffers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_event_buffers.md)

## Description

mac-buffers: tolerant buffer decoding, hatched rail wings and buffer-aware firstGap, a row buffer capsule with accessibility text, buffer-aware event-run and conflict cards, fixtures, renders, and docs.

## Notes

[2026-11-02T05:13:15Z · bob-cli-fk.6] PROPOSED FOLLOW-UP: add one sentence to the Event Task glossary strand that [buffer:: -30m +15m] widens the span the event occupies (epic decision memory_event_task_glossary answered no, so the strand was left untouched)

[2026-11-02T05:13:21Z · bob-cli-fk.6] PROPOSED FOLLOW-UP: bob-cli HEAD does not compile its bob-obsidian lib (capture_pomodoros_agenda.rs:1205 calls BufferPart::as_str which has no impl), so docs-check fails after lint/build/URLs pass and just check is red — needs a bob-cli fix, no task bead tracks it yet

[2026-11-02T05:13:27Z · bob-cli-fk.6] PROPOSED FOLLOW-UP: macOS targets unverified (mac offline, SSH timed out) — still needed: typecheck-tests for the BobMacCapture wing/capsule view and CaptureAgendaDesignTests buffered renders once the mac is back

[2026-11-02T05:13:47Z · bob-cli-fk.6] mac-buffers landed in bob-mac-capture: tolerant CaptureEventBuffer/CaptureBufferPart on agenda rows, items[].event, event_run.events[], event_conflict.event plus buffer_part; rail capsules span the meeting with hatched low-opacity wings (dashed when untracked, hue outline while active), domain and firstGap over buffered spans; row buffer capsule (−30m +15m, hue-tinted while in progress) with holds+spoken a11y text; MEET chips append the label; event-run caption and both conflict headlines use buffer_part. Verified: swift build + full swift test on athena (1961 tests, 0 failures incl. 19 new CaptureAgendaBufferTests), format lint clean for touched lines, docs-check lint/drift/strict-build/URLs pass with budgets at 5999/6000. Unverified: macOS view compile + design renders (mac offline); docs-check cargo stage blocked by pre-existing bob-cli lib break (recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-fk.3](bob-cli-fk.3.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-fk.4](bob-cli-fk.4.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fk.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fk.6/README.md) | [bob-cli-fk.6](bob-cli-fk.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4f35460`](https://github.com/bobs-org/bob-mac-capture/commit/4f35460a94e2b52de1f8d8b1d3f52988796f91da) | feat(capture): render buffered event spans on mac agenda | [bob-cli-fk.6](bob-cli-fk.6.md) | 2026-11-02 00:15:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fk.6][1] | Need full phase detail including notes | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fk.6/README.md

<!-- sase:referenced-by:end -->
