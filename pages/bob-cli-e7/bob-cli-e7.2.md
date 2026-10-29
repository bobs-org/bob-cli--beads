# Bead: bob-cli-e7.2 — bob-cli wikilink\_task completion contract

[Bead Pages](../README.md) / [bob-cli-e7](README.md) / bob-cli-e7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b3.md) · **Assignee:** `bob-cli-e7.2` · **Size:** medium
**Created:** 2026-10-29 17:02:45 EDT · **Closed:** 2026-10-29 17:45:30 EDT
**Plan:** [202610/wikilink\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/wikilink_task_picker.md)

## Description

bob-contract: in bob-cli, detect the `((query` field, serve the vault-wide `wikilink_task` snapshot with backend-formatted `[[target#^id]]` replacements, groups, disabled reasons, and a picker descriptor, add `wikilink_replacement` to `capture-task-id`, keep shell completion out of it, and document the contract.

## Notes

[2026-10-29T21:45:30Z · bob-cli-e7.2] Implemented the wikilink_task contract: ((query field detection after [[ and before markers, vault-wide snapshot with backend-formatted [[target#^id]] replacements (shortest unique basename; done/ always path), groups, disabled reasons, picker descriptor, and capture-task-id wikilink_replacement in both --route and --note-path modes. Shell completion returns nothing. Documented in capture.md and generated CLI help. Verified capture_task_wikilinks unit tests, complete_wikilink_task CLI tests (triggers, ranges, groups, guards, link targets, cursor_after, splice-validity, task-id), rustfmt, and just docs-check. No leftover --epic-symbol entries.

[2026-10-29T21:57:19Z · bob-cli-e7.2--1] PROPOSED FOLLOW-UP: just check fails on 7 leftover bob-obsidian CLI tests from bob-cli-e6.1 types wording (themes vs types meters, catalog themes-split path) — already recorded as DISCOVERED ISSUE on bob-cli-e6; e6.16 is the likely owner. Reproduced on this monitor run 690ad151bbcd28c671eef300115568f3 / qrj1d21xm9sz identically to clean HEAD d0603a5d.

## Dependencies

- **Blocks:** [bob-cli-e7.3](bob-cli-e7.3.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e7.2.md) | [bob-cli-e7.2](bob-cli-e7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`53bf3df`](https://github.com/bobs-org/bob-cli/commit/53bf3dfaddc8d30aec4a0dd539dd1d3d281d2e9d) | feat(capture): add wikilink\_task (( completion contract | [bob-cli-e7.2](bob-cli-e7.2.md) | 2026-10-29 18:09:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e7.2--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e7.2.md

<!-- sase:referenced-by:end -->
