# Bead: bob-cli-e7.3 — Mac Task Wikilink Picker

[Bead Pages](../README.md) / [bob-cli-e7](README.md) / bob-cli-e7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b3.md) · **Assignee:** `bob-cli-e7.3` · **Size:** medium
**Created:** 2026-10-29 17:02:45 EDT · **Closed:** 2026-10-29 19:02:37 EDT
**Plan:** [202610/wikilink\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/wikilink_task_picker.md)

## Description

mac-picker: in bob-mac-capture, add the `.wikilinkTask` picker source that decodes `wikilink_task`, auto-opens on typed `((`, filters locally, inserts Bob's link, runs the Add block ID prompt in wikilink mode against `capture-task-id`, and covers it with presentation, panel, and fake-bob tests.

## Notes

[2026-10-29T23:02:37Z · bob-cli-e7.3] Implemented wikilinkTask picker in bob-mac-capture: decoding (wikilink_task/link_target/wikilink_replacement), .wikilinkTask source/index/routing/ID prompt/views, fixtures + fake-bob routes, 1765 portable tests pass (7 new presentation + 2 decoding). Mac targets unverified: mac offline, Linux cannot build BobMacCapture.

## Dependencies

- **Depends on:** [bob-cli-e7.1](bob-cli-e7.1.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e7.2](bob-cli-e7.2.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e7.4](bob-cli-e7.4.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e7.3/README.md) | [bob-cli-e7.3](bob-cli-e7.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@031f100`](https://github.com/bobs-org/bob-mac-capture/commit/031f100f52fbb2bfc758d28b5334886e4a9d02e0) | feat(mac-capture): add (( task wikilink picker | [bob-cli-e7.3](bob-cli-e7.3.md) | 2026-10-29 19:03:51 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e7.3][1] | check full description and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e7.3/README.md

<!-- sase:referenced-by:end -->
