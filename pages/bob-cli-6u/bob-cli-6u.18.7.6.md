# Bead: bob-cli-6u.18.7.6 — Finish ^prj project blocking — fix what the bob-cli-6u.18.7 land audit found

[Bead Pages](../README.md) / [bob-cli-6u.18.7](bob-cli-6u.18.7.md) / bob-cli-6u.18.7.6

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.land.md) · **Assignee:** `bob-cli-6u.18.7.6.land`
**Created:** 2026-10-12 22:09:27 EDT
**Plan:** [202610/prj\_line\_blocking\_final\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_final_audit_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/prj_line_blocking_final_audit_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_final_audit_fixes.md

<!-- sase:links:end -->

## Description

Every defect the bob-cli-6u.18.7 land audit found in the ^prj project-blocking fixes is fixed in bob-cli and bob-plugins, each with a regression test that fails on the old code. bob-cli `just check` fails only the bob-cli-6m percent-listen tests. bob-plugins `npm test` fails only the known bob-cli-6v, bob-cli-6w and bob-cli-3w cases. The fixed bob and plugins are installed on this host and, when it is reachable, on the MacBook.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.land/README.md) | [bob-cli-6u.18.7.6](bob-cli-6u.18.7.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.7.6.3][1] | Need parent epic DECISIONS for cycler-fixes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.3/README.md

<!-- sase:referenced-by:end -->
