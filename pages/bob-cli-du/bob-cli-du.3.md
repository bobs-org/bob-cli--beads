# Bead: bob-cli-du.3 — Completion, parse, relations list, rename warnings, and zsh show complete labels

[Bead Pages](../README.md) / [bob-cli-du](README.md) / bob-cli-du.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.aw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.aw.md) · **Assignee:** `bob-cli-du.3` · **Size:** medium
**Created:** 2026-10-28 14:49:53 EDT · **Closed:** 2026-10-28 20:02:53 EDT
**Plan:** [202610/relation\_complete\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md)

## Description

complete-surfaces: add completes_source flags, the configured overlay, relation_complete verdicts and hints to capture-complete and capture-parse, the ✓ column and counts to bob relations list and zsh, and the complete-label rename warning.

## Notes

[2026-10-29T00:02:53Z · bob-cli-du.3] Implemented complete-label completion metadata, source cues and inverse hints; parse-span flags; list overlays/counts and zsh descriptions; and rename warnings. Verified 38 matching library tests, focused CLI list/parse/zsh/rename tests, cargo check, formatting, docs generation, and docs-check (447 passed, 1 optional font test skipped). Updated the authorized task-relation glossary strand.

## Dependencies

- **Depends on:** [bob-cli-du.2](bob-cli-du.2.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-du.4](bob-cli-du.4.md) ◐ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-du.8](bob-cli-du.8.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.3/README.md) | [bob-cli-du.3](bob-cli-du.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`387a4fc`](https://github.com/bobs-org/bob-cli/commit/387a4fc2fad35d330754f4fca53dce08a78d7f67) | feat(relations): add complete-label CLI surfaces | [bob-cli-du.3](bob-cli-du.3.md) | 2026-10-28 20:03:55 EDT |
