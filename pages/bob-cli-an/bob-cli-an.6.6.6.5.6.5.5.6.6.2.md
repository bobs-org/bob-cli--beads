# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.2 — Correct capture TEXT help to match the unknown-flag guard

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.2` · **Size:** xsmall
**Created:** 2026-10-25 10:04:06 EDT · **Closed:** 2026-10-25 10:15:51 EDT
**Plan:** [202610/backlog\_batch10\_port\_help\_doctor\_mermaid\_startpending.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch10_port_help_doctor_mermaid_startpending.md)

## Description

capture-help-accuracy: resolve bob-cli-c4 by wording TEXT help to say only the flag where TEXT begins is rejected, with docs-check green.

## Notes

[2026-10-25T14:15:51Z · bob-cli-an.6.6.6.5.6.5.5.6.6.2] Reworded TEXT help in all 5 capture-style commands (capture, capture-parse, capture-rewrite, capture-complete, capture-templates save) to say an unknown --flag where TEXT would begin is rejected and later tokens stay literal; regenerated CLI reference docs via just docs-gen. Verified: just docs-check green, capture_flag_guard lib tests 9/9 pass, just check green. Guard behavior unchanged; target task bob-cli-c4 left open for lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`633bc3f`](https://github.com/bobs-org/bob-cli/commit/633bc3f6045b5d80e252c7d1f31780d2f438030d) | docs(capture): clarify unknown-flag guard in TEXT help | [bob-cli-an.6.6.6.5.6.5.5.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.2.md) | 2026-10-25 10:16:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.2/README.md

<!-- sase:referenced-by:end -->
