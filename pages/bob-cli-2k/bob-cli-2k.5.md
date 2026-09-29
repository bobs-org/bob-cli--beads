# Bead: bob-cli-2k.5 — Bob Mac Capture numbered close card, span colors, and pending list state

[Bead Pages](../README.md) / [bob-cli-2k](README.md) / bob-cli-2k.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.34](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.34.md) · **Assignee:** `bob-cli-2k.5` · **Size:** medium
**Created:** 2026-09-29 13:45:03 EDT · **Closed:** 2026-09-29 14:58:37 EDT
**Plan:** [202609/close\_task\_selection.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_task_selection.md)

## Description

mac-selection-preview: in the bob-mac-capture linked repo, decode the new close
fields. Render SF Symbol number badges tinted by outcome on the close card, with
a teaching hint before a selection is typed and an outcome summary after. Color
the in-progress and complete list spans in the editor. Keep a live, dimmed card
with Close disabled while a list ends in `,` or `!`. Update status and
notifications, regenerate real-bob fixtures, add tests and README notes, and get
macOS CI green.

## Notes

[2026-09-29T18:58:37Z · bob-cli-2k.5] mac-selection-preview done in bob-mac-capture f6eae0b: decode in_progress/complete/task_links/index; numbered badges (filled when listed, capsule past 50) tinted orange/green/secondary with unlisted dimming; teaching hint and outcome summary incl. =x0 In progress none; numbered rows never overflow; orange/green list spans; pending dimmed card on trimmed draft with Close disabled and submit guard; status/notification completed count; real-bob fixtures (select-worked/complete/none/one/out-of-range, parse select/incomplete/invalid) plus regenerated worked.json; fake-bob branches; 13 new presentation/model tests plus span-mapping tests; README notes. Verified: macOS CI run 36615238978 green (lint/build/807 tests/bundle/smoke; 1 pre-existing skip). No Swift toolchain on Linux host; no epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-2k.3](bob-cli-2k.3.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2k.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2k.5/README.md) | [bob-cli-2k.5](bob-cli-2k.5.md) | 0 |
