# Bead: bob-cli-ji.7.1.6 — Document the shipped mode and assemble completion evidence

[Bead Pages](../README.md) / [bob-cli-ji.7.1](bob-cli-ji.7.1.md) / bob-cli-ji.7.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) · **Assignee:** `bob-cli-ji.7.1.6` · **Size:** small
**Created:** 2026-11-10 10:29:46 EST · **Closed:** 2026-11-10 17:07:49 EST
**Plan:** [202611/mac\_event\_note\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md)

## Description

docs: add the Mac event-notes page and nav entry, short keyboard/protocol/ idle-agenda links, and On your Mac in the bob-cli guide. Correct the mode's pending wording, run mounted docs gates, and collect phase and exact-SHA CI evidence for the child epic's land agent. Do not close bob-cli-ji.7 or any ancestor from this phase. Read Documentation and Landing.

## Notes

[2026-11-10T22:07:34Z · bob-cli-ji.7.1.6] PROPOSED FOLLOW-UP: docs-check word budgets already over cap on clean base (capture-panel 6036, capture-previews 6088, keyboard 6065, protocol 6149, bob-navigation-hotkeys 6132 vs 6000 cap); this phase adds ~100 words to keyboard/protocol and trims entries to stay minimal -r Recording pre-existing docs gate failure per phase instructions

[2026-11-10T22:07:49Z · bob-cli-ji.7.1.6] Docs phase done. Mac: new docs/event-notes.md + nav entry, short keyboard/protocol/idle-agenda links (trimmed to minimal). bob-cli: gcal-notes pending wording replaced with shipped link, guide gains On your Mac. Mounted docs gate run both directions: only failures are 5 pre-existing word-budget overages identical on clean base (recorded as PROPOSED FOLLOW-UP). No Swift/Rust changes; Mac HEAD 62a7b70, bob-cli HEAD 991e270e; changes uncommitted for finalizer.

## Dependencies

- **Depends on:** [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.7.1.6/README.md) | [bob-cli-ji.7.1.6](bob-cli-ji.7.1.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`23e7f90`](https://github.com/bobs-org/bob-cli/commit/23e7f90df5be9b52b5600c82a6b9104c6324d924) | docs(gcal): mark Mac event-note mode shipped and point at Mac guide | [bob-cli-ji.7.1.6](bob-cli-ji.7.1.6.md) | 2026-11-10 17:10:50 EST |
| bob-mac-capture | [`bob-mac-capture@1498f34`](https://github.com/bobs-org/bob-mac-capture/commit/1498f348f9095daacfe02a8fda9f07e8012030ef) | docs(capture): add event-notes page and nav entry with key/protocol/agenda links | [bob-cli-ji.7.1.6](bob-cli-ji.7.1.6.md) | 2026-11-10 17:11:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.7.1.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.7.1.6/README.md

<!-- sase:referenced-by:end -->
