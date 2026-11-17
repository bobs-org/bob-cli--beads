# Bead: bob-cli-mn.2 — Mac Capture opens the record list on a bare @album/ draft

[Bead Pages](../README.md) / [bob-cli-mn](README.md) / bob-cli-mn.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1d8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1d8.md) · **Assignee:** `bob-cli-mn.2` · **Size:** small
**Created:** 2026-11-17 06:44:44 EST · **Closed:** 2026-11-17 08:11:39 EST
**Plan:** [202611/album\_slash\_record\_list.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_slash_record_list.md)

## Description

mac_record_list: in bob-mac-capture, skip the cached route list when the caret's record_route span is the whole draft so bob's record_target rows show; add real-bob fixtures, fake-bob cases, hosted tests, and docs; verify on macOS CI.

## Notes

[2026-11-17T13:11:39Z · bob-cli-mn.2] cachedRouteCompletion defers a whole-draft record_route with caret at end to capture-complete; fake-bob + generated eat-bare fixtures; hosted tests cover @eat/ record_target vs title-bearing cache; just portable-check, just docs-check, Mac scratch typecheck-tests, and Scripts/macos-ci-check SHA 31542f19 run 44086243927 all passed.

## Dependencies

- **Depends on:** [bob-cli-mn.1](bob-cli-mn.1.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mn.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mn.2.md) | [bob-cli-mn.2](bob-cli-mn.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@19a23f4`](https://github.com/bobs-org/bob-mac-capture/commit/19a23f40db527d6db0d1992aa24a45d13a5909b0) | feat(capture): list album records after a typed @album/ | [bob-cli-mn.2](bob-cli-mn.2.md) | 2026-11-17 08:13:30 EST |
