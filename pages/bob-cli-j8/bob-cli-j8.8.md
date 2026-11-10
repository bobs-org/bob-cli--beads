# Bead: bob-cli-j8.8 — Bob Mac Capture presents notebooks

[Bead Pages](../README.md) / [bob-cli-j8](README.md) / bob-cli-j8.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3x.linker.w0.md) · **Assignee:** `bob-cli-j8.8` · **Size:** large
**Created:** 2026-11-09 12:11:28 EST
**Plan:** [202611/bob\_notebooks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_notebooks.md)

## Description

mac-notebook-capture: decode unknown block-ID intents as unsupported instead of link, show `kind: "notebook"` targets with a book icon and summary, keep notebooks out of File-under, render notebook note, sub-note, and creation previews and success lines, and present note-bullet rows in the `+` picker.

## Notes

[2026-11-10T09:58:04Z · bob-cli-j8.8--4] Mac Capture CI diagnostic: exact-SHA run 42793097983 (snapshot d2c784daf300b458013e763a672b712cfb3b58d7) passed formatting and Build but failed Test with SwiftPM fatalError during test-target compilation; no xctest process or hang-sample artifact was produced. The base SHA 9a0bb25c4b55b547a6d92c35c93017471e74feff run 42735343020 shows the same test-step failure and empty hang artifact. No notebook-specific failure was exposed. Keep this phase in progress pending a green exact-SHA gate; the separate bob-cli docs mount collision remains unresolved.

[2026-11-10T09:59:05Z · bob-cli-j8.8--4] PROPOSED FOLLOW-UP: Diagnose why Mac Capture exact-SHA CI emits SwiftPM fatalError during test-target compilation without an xctest process or hang sample, including a baseline run, and determine whether the runner or test watchdog needs a separate fix. Seen in runs 42793097983 and 42735343020.

## Dependencies

- **Blocks:** [bob-cli-j8.10](bob-cli-j8.10.md) ◐ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j8.5](bob-cli-j8.5.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.8.md) | [bob-cli-j8.8](bob-cli-j8.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2882ea`](https://github.com/bobs-org/bob-cli/commit/f2882ea6fc30894c848bafa4a68e4f81b7c148ed) | fix(ci): select Mac Capture workflow for exact-SHA checks | [bob-cli-j8.8](bob-cli-j8.8.md) | 2026-11-10 05:02:21 EST |
| bob-mac-capture | [`bob-mac-capture@b20ceca`](https://github.com/bobs-org/bob-mac-capture/commit/b20ceca5526c6f379f8d2983e70115f150a9ae48) | feat(capture): present notebook capture targets and previews | [bob-cli-j8.8](bob-cli-j8.8.md) | 2026-11-10 05:02:56 EST |
