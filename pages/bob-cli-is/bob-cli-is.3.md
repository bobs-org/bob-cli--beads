# Bead: bob-cli-is.3 — Mac forwards x/s to Bob's close-outcome alias

[Bead Pages](../README.md) / [bob-cli-is](README.md) / bob-cli-is.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3r.linker.w0.md) · **Assignee:** `bob-cli-is.3` · **Size:** medium
**Created:** 2026-11-08 11:42:41 EST
**Plan:** [202611/close\_outcome\_x\_s\_typing\_aliases.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/close_outcome_x_s_typing_aliases.md)

## Description

mac-close-alias: forward lowercase non-repeat x/s keys through a lexical send prefilter into the rewrite lane, mark them meaning-changing so the hold and Return deferral cover them, and add a one-time old-bob probe. Adds recorded fixtures, tests, Mac docs, the optional decision record, and an end-to-end check.

## Notes

[2026-11-08T21:05:00Z · bob-cli-is.3] Progress: implemented Mac x/s forwarding (prefilter, meaning-changing, old-bob probe), fixtures + generator + fake-bob, 9 new tests, docs (keyboard/capture-panel/protocol) within budget. Verified: portable-check 2268 passed/1 skipped on athena, docs-check green, Bob binding-contract rows green (xx->x!, xs->x*, past/link/lead/numbered fire; prose/uppercase/retired unchanged). Mac precommit CI failed Build on String.Index(utf8:within:) label (fixed, commit 3e95510); full macOS CI re-run still needed before close. No memory edits (decision declined). -r Record phase progress and remaining CI verification for next agent

## Dependencies

- **Depends on:** [bob-cli-is.1](bob-cli-is.1.md) ✓ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-is.2](bob-cli-is.2.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-is.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-is.3/README.md) | [bob-cli-is.3](bob-cli-is.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@2a39c2f`](https://github.com/bobs-org/bob-mac-capture/commit/2a39c2ffac859a2d1594171ef835b8d6a7b9c6f3) | feat(mac-capture): alias x and s to close outcomes | [bob-cli-is.3](bob-cli-is.3.md) | 2026-11-08 16:07:25 EST |
