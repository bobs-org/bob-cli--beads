# Bead: bob-cli-8w.4 — Control-Return gesture and the open pipeline

[Bead Pages](../README.md) / [bob-cli-8w](README.md) / bob-cli-8w.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8q.md) · **Assignee:** `bob-cli-8w.4` · **Size:** medium
**Created:** 2026-10-17 15:54:14 EDT · **Closed:** 2026-10-17 17:05:40 EDT
**Plan:** [202610/ctrl\_enter\_capture\_and\_open.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_enter_capture_and_open.md)

## Description

mac-ctrl-return: handle Control-Return (with Command-Return as an alias in the editor) across the editor, completion, pickers, prompts, the successor card, the stash, and the template shelf. Open the plan through one Obsidian-activating NSWorkspace call that reports failures, and switch notifications over to the plan. Also update the README keyboard docs, add tests, and run the compile checks.

## Notes

[2026-10-17T21:05:40Z · bob-cli-8w.4--1] Implemented the Control-Return routing, capture/open pipeline, notification handling, tests, and keyboard docs in bob-mac-capture. git diff --check passed and athena just portable-check exited 0. Mac scratch typecheck was attempted but SSH timed out, so macOS targets remain unverified. epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-8w.3](bob-cli-8w.3.md) ✓ · ⧖ 2026-10-17
- **Blocks:** [bob-cli-8w.5](bob-cli-8w.5.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8w.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8w.4.md) | [bob-cli-8w.4](bob-cli-8w.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@57406f8`](https://github.com/bobs-org/bob-mac-capture/commit/57406f81d47b52cb5e22b9675a01aae98e0cf446) | feat(capture): add Control-Return open pipeline | [bob-cli-8w.4](bob-cli-8w.4.md) | 2026-10-17 17:06:24 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8w.4--1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8w.4.md

<!-- sase:referenced-by:end -->
