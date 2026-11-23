# Bead: bob-cli-on.11 — Requirements on the Obsidian successor card and carry-now

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.11` · **Size:** large
**Created:** 2026-11-21 11:13:27 EST · **Closed:** 2026-11-23 00:54:15 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-p8][1] | Active obsidian-close-card phase edits the same cycler close card and offer-close verdicts |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-p8/README.md

<!-- sase:links:end -->

## Description

obsidian-close-card: mirror the requirement split in nav with api.taskSplit, bind Ctrl+Shift+T carry-now on requirement lines, render picker v6 requirement groups with their keys, and let the cycler plan and apply verdicts with guarded Undo.

## Notes

[2026-11-22T19:56:19Z · bob-cli-on.11] Planning audit: no prior implementation notes; prerequisites on.8 and on.10 are closed. At bob-cli 96a23f50 and bob-plugins 2b3b6b6, Rust carry/close contracts and plugin req guards are landed, but nav split remains SP1-SP31, successors is v5, and taskSplit API is absent. Authored and validated a six-phase child epic: carry API, snapshot/verdict model, picker v6, guarded carry/drop apply, placement/landing, and managed Done integration. No implementation changes made. Child land agent must verify deployment and close only on.11; no epic-symbol entries currently target this phase. Existing bob-cli-p8 remains separate scope.

[2026-11-23T05:54:54Z · bob-cli-on.11.1.7.land] PHASE CLOSEOUT from mixed-undo tale: carry-now and close-card scope fulfilled. Child epic on.11.1 and repair epic on.11.1.7 closed. 137 compose order closeRestores then reqRestores; public-path 25/25; live e2e 6/6; just check succeeded (ab245f33e7288778f9f38dd7e929f822). Cycler 1.58.1 deployed without -F, nav 2.107.0 synced. Follow-ups remain km/io/ob; p8 separate. Containing epic bob-cli-on left open for its land agent. No epic-symbols. justfile has no symvision recipe.

## Dependencies

- **Depends on:** [bob-cli-on.10](bob-cli-on.10.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.12](bob-cli-on.12.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.8](bob-cli-on.8.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) | [bob-cli-on.11](bob-cli-on.11.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.2][1] | Need parent phase DECISIONS that remain final for the child epic | 1 |
| read-by | [agent:research.5u.cld][2] | Check whether in-flight req card/memory phases render or record the hash run glyph, for display redesign timing | 1 |
| read-by | [agent:research.5u.gem][3] | Inspect display-related and remaining phases of bob-cli-on | 1 |
| read-by | [agent:research.5x.mus][4] | Drawer research: successor card conflict check | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.gem/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.mus/README.md

<!-- sase:referenced-by:end -->
