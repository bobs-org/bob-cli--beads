# Bead: bob-cli-on.10.1 — Obsidian requirement guards, toggle, drop, and typing assist

[Bead Pages](../README.md) / [bob-cli-on.10](bob-cli-on.10.md) / bob-cli-on.10.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) · **Assignee:** `bob-cli-on.10.1.land`
**Created:** 2026-11-21 14:10:17 EST
**Plan:** [202611/obsidian\_req\_gestures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/obsidian_req_gestures.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md

<!-- sase:links:end -->

## Description

Complete bob-cli-on.10 (the obsidian-gestures phase of plan:202611/task_requirements.md). The cycler, nav, and Block ID Prompt recognize requirement lines through byte-identical JS twins that pass bob-cli's RQ/RL/RW vectors. Every task gesture refuses or redirects on a req line with the contract copy. Ctrl+] toggles note and req with zone placement and the first-req scoop, Alt+[ drops with a reason and Alt+] restores, Ctrl+Shift+P opens the owner's Task Card, the offer-close scope note never counts reqs, and typing `- [` then space expands to `- [ ] ` with overtype absorption, atomic Backspace, Vim insert support, and a clean Undo. Each write is one undo step.

## Notes

[2026-11-22T02:11:52Z · bob-cli-oj.land] FROM bob-cli-oj.land (deploy coordination): the vault's task-status-cycler is still stuck behind a clean stamp from 726f9a5, bob-cli-oj.1's lost local commit, so 'bob plugins sync -p task-status-cycler' refuses without -F (bug bob-cli-or). The deployed 1.52.0 bytes equal landed ancestor 6e0d764, so forcing drops nothing unlanded. bob-cli-oj.land staged a Bryan-approval gate that rechecks the stamp and those bytes, then force-deploys origin/master task-status-cycler from a temporary detached worktree. If the gate already ran, sync normally after fetching and merging origin/master; if your lander already resolved the stamp, the gate reports 'skipped' and does nothing.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.land/README.md) | [bob-cli-on.10.1](bob-cli-on.10.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.10.1.1][1] | Need epic decisions and notes | 1 |
| read-by | [agent:bob-cli-on.10.1.2][2] | Need the epic decisions | 1 |
| read-by | [agent:bob-cli-on.10.1.5][3] | Need parent epic DECISIONS before implementing nav guards | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.5/README.md

<!-- sase:referenced-by:end -->
