# Bead: bob-cli-f6.3 — bob-cli: capture = starts a MEET on its next event run

[Bead Pages](../README.md) / [bob-cli-f6](README.md) / bob-cli-f6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bv](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bv.md) · **Assignee:** `bob-cli-f6.3` · **Size:** medium
**Created:** 2026-11-01 11:24:13 EST · **Closed:** 2026-11-01 15:05:05 EST
**Plan:** [202611/untracked\_calendar\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/untracked_calendar_events.md)

## Description

meet-event-run: default MEET starts to the next contiguous event run, apply the [t::] rule to every MEET start, add JSON and vectors.

## Notes

[2026-11-01T20:05:05Z · bob-cli-f6.3] MEET event-run starts landed: new capture/meet_event_run.rs engine (event run = earliest open unended lineup Event Task + contiguous same-trackedness successors, late-join clamp to latest closed session, future-start, pomodoro_event_run_later warning at >25m) applied after every start write (plain =, =meet, restart, counted suffix, kept-ledger swap incl. restoring [t::], link starts incl. queued-link sites); close_timing clamps a not-yet-started close to a zero-length session and warns about x0; JSON additive pomodoro_start.tracked/event_run and pomodoro_blocks[].tracked; human output '(60m · untracked) … from your calendar: T'; shared vectors tests/fixtures/meet_event_run (18 cases + README) consumed by tests/cli/capture/meet_event_run.rs; docs/capture.md, capture-syntax.md, vault-format.md, json-outputs.md updated. Verified: just lint clean, cargo fmt --check, cargo test --test cli (2634 pass), lib (4295 pass), all other workspace test targets pass, just docs-check passes. 5 legacy blocks-JSON tests had untracked [t::]-less fixtures; moved them to [t:: 30m] to keep their intent. No epic-symbols, no memory edits needed in this phase.

## Dependencies

- **Depends on:** [bob-cli-f6.1](bob-cli-f6.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.4](bob-cli-f6.4.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.6](bob-cli-f6.6.md) ◐ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.8](bob-cli-f6.8.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.3/README.md) | [bob-cli-f6.3](bob-cli-f6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`eda4dfc`](https://github.com/bobs-org/bob-cli/commit/eda4dfc30245469287f17b796531e7cc98893a17) | feat(capture): start a MEET on its next event run | [bob-cli-f6.3](bob-cli-f6.3.md) | 2026-11-01 15:06:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f6.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.3/README.md

<!-- sase:referenced-by:end -->
