# Bead: bob-cli-nb.3 — Pin cadences in chezmoi

[Bead Pages](../README.md) / [bob-cli-nb](README.md) / bob-cli-nb.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1e2.md) · **Assignee:** `bob-cli-nb.3` · **Size:** xsmall
**Created:** 2026-11-18 13:06:51 EST · **Closed:** 2026-11-18 16:16:13 EST
**Plan:** [202611/bob\_tick.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_tick.md)

## Description

chezmoi_config: add the commented tick: block (gcal 1h, gmail 1h, gkeep manual, refs, projects, tasks 15m) to the chezmoi Bob config, update the gcal comment, and validate it against the engine build and an older bob.

## Notes

[2026-11-18T21:16:13Z · bob-cli-nb.3] Added the documented tick: block with explicit gcal/gmail hourly, gkeep manual, and refs/projects/tasks 15m cadences; updated the gcal scheduling comment. Verified BOB_CONFIG_FILE=... cargo run -q -- tick -d shows all six cadences, installed bob 0.5.0 runs bob plan with the config, git diff --check passes, and epic-symbols reports no leftovers.

## Dependencies

- **Depends on:** [bob-cli-nb.1](bob-cli-nb.1.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-nb.5](bob-cli-nb.5.md) ✓ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nb.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nb.3/README.md) | [bob-cli-nb.3](bob-cli-nb.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@5c68b1f`](https://github.com/bbugyi200/dotfiles/commit/5c68b1f1ac303fc26d2dd816043e7aef7b3941d2) | feat(bob): pin bob tick cadences in chezmoi | [bob-cli-nb.3](bob-cli-nb.3.md) | 2026-11-18 16:17:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nb.3][1] | Need the phase scope, design file, prior work, and epic decisions before implementing this assigned phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nb.3/README.md

<!-- sase:referenced-by:end -->
