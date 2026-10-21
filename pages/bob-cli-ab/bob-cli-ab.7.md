# Bead: bob-cli-ab.7 — ID-less rows and the +N reveal

[Bead Pages](../README.md) / [bob-cli-ab](README.md) / bob-cli-ab.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.27.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.27.linker.w0.md) · **Assignee:** `bob-cli-ab.7` · **Size:** small
**Created:** 2026-10-20 17:44:13 EDT · **Closed:** 2026-10-20 21:58:39 EDT
**Plan:** [202610/capture\_similar\_tasks\_band.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_similar_tasks_band.md)

## Description

mac_idless: route link actions on ID-less rows through the existing Add block ID prompt, reveal hidden matches with ↓ while focused, and finish the docs, fixtures, and end-to-end checks.

## Notes

[2026-10-21T01:58:39Z · bob-cli-ab.7] mac_idless done in bob-mac-capture (uncommitted): ID-less rows route link actions through a new similarTask Add-block-ID prompt (prefilled suggestions, Tab cycling, writes ID before Return, Esc keeps band focus); +N reveal via policy revealed counts with unfocus collapse; docs + idless/revealed fixtures. Verified: portable-check 1526 tests 0 failures on athena, docs-check passed, real-bob e2e on scratch vault (requires_block_id row then capture-task-id --route returns all replacements, vault restored). macOS targets unverified: mac offline, no typecheck-tests/bundle run.

## Dependencies

- **Depends on:** [bob-cli-ab.6](bob-cli-ab.6.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ab.8](bob-cli-ab.8.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ab.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ab.7/README.md) | [bob-cli-ab.7](bob-cli-ab.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3653661`](https://github.com/bobs-org/bob-mac-capture/commit/365366127c0c8295f604488c6850511f453c7083) | feat(mac-capture): route ID-less similar-tasks rows through Add block ID and add +N reveal | [bob-cli-ab.7](bob-cli-ab.7.md) | 2026-10-20 21:59:46 EDT |
