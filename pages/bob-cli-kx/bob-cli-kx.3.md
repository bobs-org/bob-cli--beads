# Bead: bob-cli-kx.3 — Undo command and receipt surfaces

[Bead Pages](../README.md) / [bob-cli-kx](README.md) / bob-cli-kx.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bt](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bt.md) · **Assignee:** `bob-cli-kx.3` · **Size:** large
**Created:** 2026-11-12 11:11:53 EST · **Closed:** 2026-11-13 16:42:04 EST
**Plan:** [202611/gmail\_archive\_on\_task\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_on_task_close.md)

## Previously Closed

> ↺ Closed 2026-11-13T21:36:08Z · done
>
> delegated work landed
>
> Reopened 2026-11-13T21:38:23Z by `sase bead open`

## Description

receipts: Make every archive legible and undoable. In bob-cli the bob gmail unarchive command, the gmail_archived frontmatter and mail-note banner lifecycle, the desktop notification, and the recent_archive JSON. In bob-plugins the display-only task chip, the banner's Move-back button, the mail.base Archived-by-Bob view, and the morning notice line.

## Notes

[2026-11-13T21:42:04Z · bob-cli-kx.3.1.land--5] Integrated receipts surfaces verified: bob gmail unarchive, receipt/banner projection, desktop notification, recent_archive, task chip, Move-back button, Archived by Bob mail.base view, and morning notice. Current just check has 6,954 lib tests pass, 1 failure, 3 ignored; the only failure is the deterministic gcal sync_args test tracked by bob-cli-l2, and bob-cli-kl did not reproduce. gmail_archive_apply passed 56/56; report.rs 22/22; targeted multi-generation archive projection 1/1; isolated capture timing 1/1; plugin banner/chip suites 56/56; morning archive notice 1/1; mail.base archived-view test passed in the lib run. just docs-gen passed; docs-check reports only the existing tracked word budgets bob-cli-il and bob-cli-jz. bob plugins sync deployment is complete. No just symvision recipe; epic-symbols returned no entries.

## Dependencies

- **Depends on:** [bob-cli-kx.2](bob-cli-kx.2.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.4](bob-cli-kx.4.md) ✓ · ⧖ 2026-11-12

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
| read-by | [agent:bob-cli-kx.3.1.land][3] | Need the parent link and phase scope for the tale closeout | 1 |
| read-by | [agent:bob-cli-kx.3.1.land--5][3] | Check whether the requested receipt phase was also closed by the preceding 3.1.1 close operation | 3 |
| read-by | [agent:bob-cli-ld.2][4] | Need to determine whether the clean-base clippy failures in gmail/unarchive.rs are caused by this active epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.1.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.2/README.md

<!-- sase:referenced-by:end -->
