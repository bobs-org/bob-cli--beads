# Bead: bob-cli-ji.8.3 — Write contract, validation warnings, human output, and missing tests

[Bead Pages](../README.md) / [bob-cli-ji.8](bob-cli-ji.8.md) / bob-cli-ji.8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.land.md) · **Assignee:** `bob-cli-ji.8.3` · **Size:** medium
**Created:** 2026-11-10 22:31:45 EST · **Closed:** 2026-11-11 00:39:34 EST
**Plan:** [202611/finish\_private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_private_gcal_event_notes.md)

## Description

write: fill `errors[].suggestions`, emit `clock` and `invalid` spans, add the missing directive-lookalike and reason option-like warnings, label the rail with the root, colour canonical lines and dim the lands-as block on a TTY, finish the docs, add the missing normalization vectors and tests, and regenerate the golden fixtures.

## Notes

[2026-11-11T05:31:13Z · bob-cli-ji.8.3] PROPOSED FOLLOW-UP: refresh Bob Mac Capture Tests/Fixtures/gcal-note copies from bob-cli tests/fixtures/gcal_note/json (changed across this epic: ambiguous.json, applied.json, both_scopes.json, cleared.json, google_reasons.json, inherited_reasons.json, invalid.json, list_all.json, preview.json, preview_match.json, saved.json, saved_elsewhere.json, saved_sync_failed.json, series_scope.json, show.json, show_preview_match.json, unchanged.json, waiting_states.json) and rerun its gcal-note tests.

[2026-11-11T05:31:22Z · bob-cli-ji.8.3] PROPOSED FOLLOW-UP: resolve the unchanged clean-base docs-check word-budget failures in docs/reference/mac-capture/capture-panel.md, capture-previews.md, keyboard.md, protocol.md, and docs/reference/plugins/bob-navigation-hotkeys.md; tracked by bob-cli-jz and bob-cli-h9.

[2026-11-11T05:39:34Z · bob-cli-ji.8.3] Implemented route suggestions, clock/invalid spans, validation warnings, TTY output styling and root rail labels, docs, normalization vectors, and golden fixtures. Verified: cargo test --lib native::gcal::note::write::tests (5 passed), cargo test --test gcal_note_cli (24 passed), and just check via SASE ToolRun (6,387 tests; format, clippy, and workspace tests passed). just docs-check still reports only unchanged mounted Mac/plugin word-budget failures tracked by bob-cli-jz and bob-cli-h9; follow-ups recorded. Epic symbols: none.

## Dependencies

- **Depends on:** [bob-cli-ji.8.2](bob-cli-ji.8.2.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.8.4](bob-cli-ji.8.4.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.3/README.md) | [bob-cli-ji.8.3](bob-cli-ji.8.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b706f55`](https://github.com/bobs-org/bob-cli/commit/b706f5592a5475a66e61f6b99cbbf5daef1a6f5c) | fix(gcal): complete private event note write contract | [bob-cli-ji.8.3](bob-cli-ji.8.3.md) | 2026-11-11 00:40:52 EST |
