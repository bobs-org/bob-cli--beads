# Bead: bob-cli-pf.1.1 — Card foot row, properties drawer, and equals-minus entry points

[Bead Pages](../README.md) / [bob-cli-pf.1](bob-cli-pf.1.md) / bob-cli-pf.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.md) · **Assignee:** `bob-cli-pf.1.1.land`
**Created:** 2026-11-22 14:45:08 EST · **Closed:** 2026-11-22 21:37:59 EST
**Plan:** [202611/card\_foot\_drawer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_foot_drawer.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/card_foot_drawer.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_foot_drawer.md

<!-- sase:links:end -->

## Description

Every property card exposes its complete frontmatter and created stamp through a read-only foot and drawer, with preserved card editing and verified real-Obsidian behavior, completing bob-cli-pf.1.

## Notes

[2026-11-23T02:07:49Z · bob-cli-pf.1.1.land] LANDING TRIAGE of PROPOSED FOLLOW-UPs (bob-cli-pf.1.1 lander, 2026-11-23): (1) pf.1.1.2 #1, pf.1.1.4 #1, pf.1.1.5 #1 full-suite timing failures -> existing node tasks bob-cli-km (event-link-times 25 ms), bob-cli-io (frees-marks 25 ms), bob-cli-pg (taskLinks keystroke p95 12 ms); attributed phase evidence recorded as notes, no +1 (no lander reproduction), no new task. (2) pf.1.1.5 #1 period-notes 'ensure -d cascade' failure -> NEW task bob-cli-pm (ci, small): deterministic real-clock dependence via navGroupsTodayText; fails 16/17 on 2026-11-23, passes 17/17 with Date pinned to 2026-11-18; not caused by this epic. (3) pf.1.1.5 #2 docs:check 'refusing to overwrite authored docs/reference/plugins/albums.md' -> +1 on bob-cli-it (same root cause: missing target/docs/mount-manifest.json with stale gitignored copies; reproduced by lander; noted the per-file branch mounts.py:869 also needs the fix). Not caused by this epic; none declined.

[2026-11-23T02:37:59Z · bob-cli-pf.1.1.land] Landing verification: child phases bob-cli-pf.1.1.1–.5 were closed and their delivered formatter, inventory, shared foot/drawer, adapters, record migration, =- arm, palette/Command Mode, tests, and docs were reviewed. No conflicting integration changes found. This landing fixed tag search queries through the shared API helper with command fallback, plain alias chips, and per-view two-pane mount healing. Focused suites pass 117/117; build, build:check, validate (12/12), docs inventory, and docs:check pass. Full npm test reports the pre-triaged event-link-times and frees-marks timing nodes plus bob-cli-pm period-notes; isolated event-link-times and frees-marks pass, taskLinks p95 passes, and period-notes reproduces bob-cli-pm. Real Obsidian was unavailable at the documented snap path; runner confirmed Bob 0.6.0 then stopped before screenshots, with unit and offline runner tests passing. bob plugins sync deployed bob-ledger-tools and also synchronized the already-present task-status-cycler build; no protected-deploy refusal. Docs check required temporarily moving ignored stale plugin and mac-capture mount copies aside; no tracked files moved. Follow-up triage stands: bob-cli-km, bob-cli-io, bob-cli-pg, and bob-cli-it noted/corroborated; bob-cli-pm created; none declined.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.1.land.md) | [bob-cli-pf.1.1](bob-cli-pf.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@bb57281`](https://github.com/bobs-org/bob-plugins/commit/bb57281a9e155df3a9771758f930b23b4408db92) | fix(property-cards): repair drawer tag search and pane fallback | [bob-cli-pf.1.1](bob-cli-pf.1.1.md) | 2026-11-22 21:44:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.1.1.2][1] | Need parent epic plan and DECISIONS | 1 |
| read-by | [agent:bob-cli-pf.1.1.3][2] | Need epic DECISIONS and phase list for adapter work | 1 |
| read-by | [agent:bob-cli-pf.1.1.5][3] | Need child epic scope and plan for acceptance phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.5/README.md

<!-- sase:referenced-by:end -->
