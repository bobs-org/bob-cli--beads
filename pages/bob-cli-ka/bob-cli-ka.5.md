# Bead: bob-cli-ka.5 — Bob Mac Capture place menu, highlighting, and grouped preview

[Bead Pages](../README.md) / [bob-cli-ka](README.md) / bob-cli-ka.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b9.md) · **Assignee:** `bob-cli-ka.5` · **Size:** large
**Created:** 2026-11-11 09:22:46 EST
**Plan:** [202611/notebook\_section\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_section_bullets.md)

## Description

mac: in bob-mac-capture, generalize the drawer menu into one place menu painted from Bob's chrome, open it for section bullets and glued notebook sections, keep the empty-notebook hint, group the notebook batch preview by section, regenerate fixtures, update protocol docs, and watch macOS CI to green.

## Notes

[2026-11-11T19:36:18Z · bob-cli-ka.5] PROPOSED FOLLOW-UP: Empty glued notebook section completion omits place_menu — source inspection at bob-cli 1a9b68289f65f57d0b4a1bc3d9f955f82ae0291a shows engine.rs place_menu_for requires is_notebook_section_menu(candidates) for context section, but that predicate uses rows.iter().any and is false with zero rows even when notebook_menu_target resolved the notebook. Thus a bare @nb# on a notebook without H2s cannot deliver Type a section name; bullet context does carry the hint. This is source-backed evidence, not a runtime reproduction. Land agent should confirm with a scratch-vault CLI regression and use the resolved notebook target to retain chrome for empty glued responses; the Mac must not infer notebook identity or invent the missing chrome.

## Dependencies

- **Depends on:** [bob-cli-ka.2](bob-cli-ka.2.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-ka.3](bob-cli-ka.3.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-ka.4](bob-cli-ka.4.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ka.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ka.5.md) | [bob-cli-ka.5](bob-cli-ka.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4a69ed2`](https://github.com/bobs-org/bob-mac-capture/commit/4a69ed25bec6a6398d64e1873eccb928d21af96a) | feat(capture): paint notebook section place menus from Bob chrome | [bob-cli-ka.5](bob-cli-ka.5.md) | 2026-11-11 16:10:15 EST |
