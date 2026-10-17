# Bead: bob-cli-87.13.2 — Print profile fixes for task-row layout and image frames

[Bead Pages](../README.md) / [bob-cli-87.13](bob-cli-87.13.md) / bob-cli-87.13.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.land.md) · **Assignee:** `bob-cli-87.13.2` · **Size:** medium
**Created:** 2026-10-17 10:11:19 EDT · **Closed:** 2026-10-17 11:28:47 EDT
**Plan:** [202610/note\_snapshot\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshot_landing_repairs.md)

## Description

profile-fixes: put each status glyph on the first line of its task text with a hanging indent, frame images with a hairline using no new packages, and make the real-render tests skip cleanly when the note-profile TeX packages are missing.

## Notes

[2026-10-17T15:20:58Z · bob-cli-87.13.2--3] PROPOSED FOLLOW-UP: CLI completion PTY tests flake under high load — monitor 1p75wv4yv9cr failed completion::zsh_adapter::real_zsh_first_tab_completes and completion::bash::bash_readline_inserts_what_bob_returned after 60s (zpty/readline driver SETUP OK, empty stderr) at load1=81; the same tests passed on this dirty tree in monitors hpb5esvxspt0 and mxeyezj9ypb0 and passed in isolation this turn in 21s. Phase files do not touch completion.

[2026-10-17T15:21:01Z · bob-cli-87.13.2--3] PROPOSED FOLLOW-UP: native::highlights_ref::fetch::tests::curl_pins_the_checked_address_with_resolve flakes with Text file busy (os error 26) — monitor mxeyezj9ypb0; later monitor 1p75wv4yv9cr passed it. Phase files do not touch fetch.

[2026-10-17T15:28:47Z · bob-cli-87.13.2--4] Print-profile task-row hanging indent, hairline image frames, and missing-TeX skip are in; just check passed on monitor gk2299fq22g7 (exit 0). No --epic-symbol leftovers. Completion/fetch flakes already recorded as PROPOSED FOLLOW-UP notes.

## Dependencies

- **Blocks:** [bob-cli-87.13.4](bob-cli-87.13.4.md) ◐ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.13.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.13.2.md) | [bob-cli-87.13.2](bob-cli-87.13.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2ae1251`](https://github.com/bobs-org/bob-cli/commit/2ae1251512e06db6fb0a2c9a1360ac48ec80aa5e) | fix(note-snapshot): hang-indent task rows and hairline image frames | [bob-cli-87.13.2](bob-cli-87.13.2.md) | 2026-10-17 11:29:49 EDT |
