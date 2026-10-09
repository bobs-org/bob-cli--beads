# Bead: bob-cli-5s.10 — Bob Refs landing fixes: make search, error recovery, refresh, ranking, and the inspector match the bob\_refs\_panel spec

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.10

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.bob-cli-5s.land` · **Assignee:** `bob-cli-5s.10.land`
**Created:** 2026-10-09 08:04:27 EDT
**Plan:** [202610/bob\_refs\_land\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/bob_refs_land_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md

<!-- sase:links:end -->

## Description

Finish epic bob-cli-5s. Close every gap its land audit found between the shipped Bob Refs panel and plan:202610/bob_refs_panel.md: typed queries reach the model, an open error re-shows the panel with its state and working buttons, unavailable rows stay in place dimmed, refresh fires on wake and every open, ranking follows the spec tables in local days, the inspector tells the truth, the ⌘K menu anchors at the row, and bob-cli drops stray Swift build files and finishes the blocked-field contract.

## Notes

[2026-10-09T12:58:48Z · bryanbugyi34@gmail.com] I think we've broken bob-mac-capture's 'just install' command. See 🔒 bob\_mac\_capture\_install\_error.txt for context.

## Attachments

- 🔒 bob\_mac\_capture\_install\_error.txt · text/plain · 8.21582 KiB (private attachment)

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5s.10.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.land/README.md) | [bob-cli-5s.10](bob-cli-5s.10.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.10.1][1] | epic decisions context | 1 |
| read-by | [agent:bob-cli-5s.10.2][2] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-5s.10.3][3] | epic decisions | 1 |
| read-by | [agent:bob-cli-5s.10.4][4] | Need epic decisions and plan scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.4/README.md

<!-- sase:referenced-by:end -->
