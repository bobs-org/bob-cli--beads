# Bead: bob-cli-7d.3 — CaptureCore Go To source, goto-mode index, URL builder

[Bead Pages](../README.md) / [bob-cli-7d](README.md) / bob-cli-7d.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4b.linker.w0.md) · **Assignee:** `bob-cli-7d.3` · **Size:** medium
**Created:** 2026-10-13 09:50:29 EDT · **Closed:** 2026-10-13 10:35:08 EDT
**Plan:** [202610/slash\_task\_goto.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/slash_task_goto.md)

## Description

mac-goto-core: add `.taskGoto` source/need strings, decode `target`, give `TaskLinkPickerIndex` a goto mode (ID-less rows selectable, destinations, action lines), add `ObsidianOpenURL.taskGotoURL`, picker-view strings, compile-only switch arms, fixtures, and CaptureCore tests; green macOS CI.

## Notes

[2026-10-13T14:35:03Z · bob-cli-7d.3] PROPOSED FOLLOW-UP: Repair existing bob-mac-capture Swift CI compile failures. The clean base reproduces the reserved local named guard in CaptureLinkGuardPresentation.swift; after a scratch-only rename, test compilation reaches malformed multiline literals in CaptureTogglePresentationTests.swift, and CaptureModelTests.swift also has a reserved guard local. CI for this phase commit reports these same base errors. The isolated Go To CaptureCore tests pass.

[2026-10-13T14:35:08Z · bob-cli-7d.3] Implemented and committed CaptureCore Go To picker support in bob-mac-capture (a86eddb7fd523607d9330842d791efb3a4021719). Verified git diff check and all five new TaskGotoPickerPresentationTests in an isolated CaptureCore package. The full CI run is red on Swift compile errors reproduced on the clean base; recorded the repair as a PROPOSED FOLLOW-UP. Confirmed epic-symbols has no remaining entries.

## Dependencies

- **Depends on:** [bob-cli-7d.1](bob-cli-7d.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7d.4](bob-cli-7d.4.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7d.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7d.3/README.md) | [bob-cli-7d.3](bob-cli-7d.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a86eddb`](https://github.com/bobs-org/bob-mac-capture/commit/a86eddb7fd523607d9330842d791efb3a4021719) | feat(capture): add Go To picker core | [bob-cli-7d.3](bob-cli-7d.3.md) | 2026-10-13 10:31:53 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7d.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7d.3/README.md

<!-- sase:referenced-by:end -->
