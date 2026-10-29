# Bead: bob-cli-e7.4 — Mac picker design review and docs

[Bead Pages](../README.md) / [bob-cli-e7](README.md) / bob-cli-e7.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b3.md) · **Assignee:** `bob-cli-e7.4` · **Size:** small
**Created:** 2026-10-29 17:02:45 EDT · **Closed:** 2026-10-29 19:41:41 EDT
**Plan:** [202610/wikilink\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/wikilink_task_picker.md)

## Description

mac-design-docs: in bob-mac-capture, render light/dark design fixtures of the card and ID prompt, review and polish them, show Markdown links in task text by their label, and document the picker, keys, and capability row.

## Notes

[2026-10-29T23:41:41Z · bob-cli-e7.4] mac-design-docs done in bob-mac-capture: TaskDisplayText renders [label](url) as label (incl. titled Keep form, pinned by 6 new tests + updated Keep-source expectation); wikilink-task render fixtures (grouped/filtered/id-less-selected/history/id-prompt at 760+620, light+dark) added to CapturePickerDesignTests via RenderFixtureWriter; docs updated (wikilink-completion section, pickers index, keyboard line, protocol capability+compat row). Verified: just docs-check passed (447 passed); swift build+full portable suite on athena 1774 tests 0 failures. NOT verified: macOS-only targets ( incl. new design test compile + PNG review) — Mac offline, swift-format absent.

## Dependencies

- **Depends on:** [bob-cli-e7.3](bob-cli-e7.3.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e7.4/README.md) | [bob-cli-e7.4](bob-cli-e7.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@8f303e2`](https://github.com/bobs-org/bob-mac-capture/commit/8f303e256852449df00ad06e4aab91c5cf8b6ea2) | feat(mac-capture): review Task Wikilink picker design and document it | [bob-cli-e7.4](bob-cli-e7.4.md) | 2026-10-29 19:43:28 EDT |
