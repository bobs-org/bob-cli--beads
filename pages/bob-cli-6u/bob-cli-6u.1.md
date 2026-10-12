# Bead: bob-cli-6u.1 — Line-model project contract, PDT tag vectors, and UB unblock vectors

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.1` · **Size:** medium
**Created:** 2026-10-12 10:25:45 EDT · **Closed:** 2026-10-12 10:50:51 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

contract: rewrite docs/task-dependencies.md §13 for the ^prj line model (drop the YAML storage, R0 hoist, property R-rules, PDP/PDW), repair the other sections 75e323b made false, and add the #prj_is_blocked and [unblocked::] contracts with PDT and UB vectors.

## Notes

[2026-10-12T14:45:22Z · 72] COORDINATION — docs/task-dependencies.md §12.10 "Project pull-in" and §12.11 PP1–PP24 landed in ec7251e (bob-cli-6t.1) just before this phase started. This plan's §12/§13 repair tables do not list them. While rewriting §13, §12.5 and §12.2:
(a) Keep the §13.4 sentence naming §12.10 as the one close-gesture path that makes ^prj Next.
(b) Port §12.10's YAML-model wording:
- Rule step 3 "N has project reasons (§13.3)" is vacuous under Design §2, because ^prj reports only its own reasons. Fold it into steps 1–2.
- PP7: a future project date is now R's own inline [scheduled::], so the result is still_blocked{reason: scheduled}, not reason project.
- PP8: "or project depends_on" becomes R's own Depends-On line.
- Drop the Gate's "or N has a non-empty depends_on key".
- Drop Trigger (b)'s "including the derived field for a depends_on property".
- PP17's "legacy internal Depends-On line": internal ^prj targets are kept on the line but never projected, so R qualifies through trigger (a) only and there is no project_task row to beat.
(c) §12.10 Writes says "Nothing else changes". The recover-rank path (R ? → space; PP10/PP11/PP18 when R was [?]) is an automatic Blocked→Ready recovery, so it writes [unblocked::] per the new freshness §5. The linked ? → * path lands in Next and is skipped.
If this is out of scope, record a PROPOSED FOLLOW-UP so 6u.17 picks it up. See research:202610/bob_cli_6t_6u_epic_conflict.md.

[2026-10-12T14:49:14Z · bob-cli-6u.1] PROPOSED FOLLOW-UP: percent-listen CLI tests still fail on master — same two capture::r#ref panics at tests/cli/capture/ref.rs:942 (NotFound) and :991 (listen runner was invoked); tracked by bob-cli-6m; docs-only contract did not touch capture.

[2026-10-12T14:50:51Z · bob-cli-6u.1] Rewrote docs/task-dependencies.md §13 to the ^prj line model (Depends-On + inline [scheduled::]; dropped YAML storage, R0 hoist, property R-rules, PDP/PDW); added PDT1–12 (#prj_is_blocked every_resident) and pointed freshness.md at UB1–15 ([unblocked::] WRITE/CLEAR/READ, schema 14 / namespace v12, unblock_keeps). Repaired 75e323b sections (intro/§1/§2.1/§3/§4.2/§4.3/§5/§6.4/§8/§10/§11/§12.2/§12.5/PP8; PP7 reason scheduled). Pointers in docs/projects.md and docs/task-status-hooks.md. Memory left for publish. just all: fmt+clippy pass; 1365 passed / 2 failed in --test cli = bob-cli-6m percent-listen (cited as PROPOSED FOLLOW-UP). epic-symbols: none leftover. Did not close bob-cli-6u.

## Dependencies

- **Blocks:** [bob-cli-6u.10](bob-cli-6u.10.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.11](bob-cli-6u.11.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.15](bob-cli-6u.15.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.2](bob-cli-6u.2.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.3](bob-cli-6u.3.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.1/README.md) | [bob-cli-6u.1](bob-cli-6u.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`37c100f`](https://github.com/bobs-org/bob-cli/commit/37c100fa50d94c3038eec1e4f966dc48caab1616) | docs(task-deps): rewrite §13 for the ^prj line-model contract | [bob-cli-6u.1](bob-cli-6u.1.md) | 2026-10-12 10:52:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.1][2] | Need notes, design path, and remaining work details | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.1/README.md

<!-- sase:referenced-by:end -->
