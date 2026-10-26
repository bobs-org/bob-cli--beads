# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5 — Fix the two links to the nonexistent /bob-command-mode/ page

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5` · **Size:** small
**Created:** 2026-10-26 15:53:09 EDT · **Closed:** 2026-10-26 16:12:17 EDT
**Plan:** [202610/backlog\_batch15\_vault\_safety\_pdf\_moves\_and\_red\_gates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md)

## Description

command-mode-doc-links: resolve bob-cli-cs by pointing both command-mode links at /reference/plugins/bob-command-mode/ and running just docs-check to completion.

## Notes

[2026-10-26T20:12:17Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5] Updated both Bob Command Mode links to /reference/plugins/bob-command-mode/. Verified just docs-check passes all gates; npm run docs:check passes with BOB_CLI_DIR set to this checkout (447 passed, 1 skipped); bob plugins sync --dry-run reports 0 to copy. epic-symbols reports no leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b65bff1`](https://github.com/bobs-org/bob-cli/commit/b65bff1bd5a11c29b99c0e7263035de44520a089) | docs(guides): fix Bob Command Mode reference link | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5.md) | 2026-10-26 16:12:57 EDT |
| bob-plugins | [`bob-plugins@1621bd6`](https://github.com/bobs-org/bob-plugins/commit/1621bd6b3c84ed5f5ea8bc404d4b740073aa484f) | docs(plugins): fix Bob Command Mode reference link | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5.md) | 2026-10-26 16:14:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.5/README.md

<!-- sase:referenced-by:end -->
