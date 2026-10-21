# Bead: bob-cli-ab.5 — Band view inside the preview card

[Bead Pages](../README.md) / [bob-cli-ab](README.md) / bob-cli-ab.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.27.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.27.linker.w0.md) · **Assignee:** `bob-cli-ab.5` · **Size:** medium
**Created:** 2026-10-20 17:44:13 EDT · **Closed:** 2026-10-20 21:09:22 EDT
**Plan:** [202610/capture\_similar\_tasks\_band.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_similar_tasks_band.md)

## Description

mac_band: render the band at the foot of each task-creating card (header, rows, capsules, bulk rows, folded line), fold before scrolling, cross-fade, VoiceOver announcements, render fixtures, and capture-previews docs.

## Notes

[2026-10-21T01:09:08Z · bob-cli-ab.5] PROPOSED FOLLOW-UP: Mac scratch typecheck skipped — mac host was offline; Sources/BobMacCapture* and Tests/BobMacCapture* remain unverified on macOS until a later agent can rsync a scratch copy and run just typecheck-tests.

[2026-10-21T01:09:22Z · bob-cli-ab.5] Similar-tasks band at the foot of each task-creating preview card (standardPreviewItem, including project-note cards). Render gate hides on parse mode/item-count change and keeps held rows when parseItems is empty. Fold-before-scroll uses measuredAuxiliary − currentBand + fullBand vs available auxiliary. 120ms opacity cross-fade / Reduce Motion identity. One VoiceOver announcement per settled non-empty visible-key change at PreviewPane. CaptureCoreTests: SimilarTasksBandPolicyTests (10) and SimilarTasksBandPresentationTests (6) passed on Athena portable-check (1511 tests, 0 failures). docs-check passed. No leftover --epic-symbol entries. Mac scratch typecheck skipped (host offline); recorded as PROPOSED FOLLOW-UP. Did not write decisions:similar-tasks-are-a-settled-heads-up.

## Dependencies

- **Depends on:** [bob-cli-ab.4](bob-cli-ab.4.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ab.6](bob-cli-ab.6.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ab.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ab.5/README.md) | [bob-cli-ab.5](bob-cli-ab.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@59068d3`](https://github.com/bobs-org/bob-mac-capture/commit/59068d31390349a8529e59b90360dc9ab55be903) | feat(capture): add similar-tasks band at the foot of preview cards | [bob-cli-ab.5](bob-cli-ab.5.md) | 2026-10-20 21:10:47 EDT |
