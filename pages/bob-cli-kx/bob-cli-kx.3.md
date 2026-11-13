# Bead: bob-cli-kx.3 — Undo command and receipt surfaces

[Bead Pages](../README.md) / [bob-cli-kx](README.md) / bob-cli-kx.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bt](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bt.md) · **Assignee:** `bob-cli-kx.3` · **Size:** large
**Created:** 2026-11-12 11:11:53 EST
**Plan:** [202611/gmail\_archive\_on\_task\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_on_task_close.md)

## Description

receipts: Make every archive legible and undoable. In bob-cli the bob gmail unarchive command, the gmail_archived frontmatter and mail-note banner lifecycle, the desktop notification, and the recent_archive JSON. In bob-plugins the display-only task chip, the banner's Move-back button, the mail.base Archived-by-Bob view, and the morning notice line.

## Dependencies

- **Depends on:** [bob-cli-kx.2](bob-cli-kx.2.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.4](bob-cli-kx.4.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.md) | [bob-cli-kx.3](bob-cli-kx.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.3.1.1][1] | Need parent epic decisions and boundaries governing this phase | 1 |
| read-by | [agent:bob-cli-kx.3.1.2][2] | Need epic DECISIONS for receipt_lifecycle work | 1 |
| read-by | [agent:bob-cli-ld.2][3] | Need to determine whether the clean-base clippy failures in gmail/unarchive.rs are caused by this active epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.2/README.md

<!-- sase:referenced-by:end -->
