# Bead: bob-cli-pw.8.1.3 — Meeting Notes sheet and agenda entry points

[Bead Pages](../README.md) / [bob-cli-pw.8.1](bob-cli-pw.8.1.md) / bob-cli-pw.8.1.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pw.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.8.md) · **Assignee:** `bob-cli-pw.8.1.3` · **Size:** medium
**Created:** 2026-11-24 23:55:02 EST
**Plan:** [202611/mac\_meeting\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_meeting_notes.md)

## Description

meet-panel: integrate the portable session into a native Meeting Notes mode, Command-M, the status menu, and focusable agenda Notes actions; preserve the capture draft, implement choice and receipt states, and finish UI tests and user docs.

## Notes

[2026-11-25T07:42:21Z · bob-cli-pw.8.1.3] PROPOSED FOLLOW-UP: Reduce docs word-budget overruns — just docs-check fails on protocol.md (6308/6000), keyboard.md (6019/6000), plugin-apis.md (9287/8000), bob-navigation-hotkeys.md (6029/6000); keyboard was already 6022/6000 at clean base, protocol 6015/6000 at clean base 7d369ae8; no matching documentation-budget bead was found.

[2026-11-25T07:42:28Z · bob-cli-pw.8.1.3] Verification evidence (2026-11-25): portable build+tests pass on athena isolated copy /tmp/bob-meet-panel-check — swift build OK, swift test 2730 passed 1 skipped 0 failed including 13 new MeetingNotesAgendaTests; swift format lint exits 0 (warnings only). Mac docs-check nav fixed; 3 remaining budget errors are pre-existing base overruns. macOS CI staged via Scripts/macos-ci-check.

## Dependencies

- **Depends on:** [bob-cli-pw.8.1.1](bob-cli-pw.8.1.1.md) ✓ · ⧖ 2026-11-24
- **Depends on:** [bob-cli-pw.8.1.2](bob-cli-pw.8.1.2.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.8.1.3.md) | [bob-cli-pw.8.1.3](bob-cli-pw.8.1.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bcf0566`](https://github.com/bobs-org/bob-cli/commit/bcf0566ba90212b9198d38c69da96a00cba9ce78) | docs(guides): link Mac Capture meeting notes flow from filing guide | [bob-cli-pw.8.1.3](bob-cli-pw.8.1.3.md) | 2026-11-25 02:45:27 EST |
| bob-mac-capture | [`bob-mac-capture@3b443fe`](https://github.com/bobs-org/bob-mac-capture/commit/3b443fe6cdb6849d01787041ba17a23dadc7c9e2) | feat(meetings): add Meeting Notes sheet and agenda entry points | [bob-cli-pw.8.1.3](bob-cli-pw.8.1.3.md) | 2026-11-25 02:46:21 EST |
