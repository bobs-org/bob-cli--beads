# Bead: bob-cli-kx.3.1.2 — Materialize archive receipts in mail notes and Bases

[Bead Pages](../README.md) / [bob-cli-kx.3.1](bob-cli-kx.3.1.md) / bob-cli-kx.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.md) · **Assignee:** `bob-cli-kx.3.1.2` · **Size:** medium
**Created:** 2026-11-13 08:02:47 EST · **Closed:** 2026-11-13 09:31:53 EST
**Plan:** [202611/gmail\_archive\_receipts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_receipts.md)

## Description

receipt_lifecycle: reconcile gmail_archived and the managed banner after durable archive and release outcomes, repair interrupted local writes, and upgrade untouched mail.base templates.

## Notes

[2026-11-13T14:31:41Z · bob-cli-kx.3.1.2] PROPOSED FOLLOW-UP: docs-check reference word budgets (bob-ledger-tools.md 6136, bob-navigation-hotkeys.md 6055, cap 6000) fail identically on the clean base tree; tracked pattern matches bob-cli-l7

[2026-11-13T14:31:53Z · bob-cli-kx.3.1.2] receipt_lifecycle ships: pure note projection (gmail_archived + one banner span, idempotent zero-byte, refuses damaged/duplicate markers), live sweep in all six archive_apply exit paths (set after archive/recovery, clear after let-go, retain on reopen, repair journal-success/note-failure without remutation, skips unsafe folds, -d/-n write nothing, short per-note locks with re-read), mail.base Archived-by-Bob view with V1+V2 upgrades and customized files untouched, docs/gmail.md + vault-format.md updated. Verified: 7 receipt unit + 4 hub unit + 36 note-module lib tests, full gmail_archive_apply (34), gmail_sync (42), gmail lib (569), preview (4), shell (70); cargo fmt clean on touched files; just lint passes. Pre-existing only: docs-check word budgets (recorded as follow-up) and fmt drift in untouched plugins files (reverted).

## Dependencies

- **Depends on:** [bob-cli-kx.3.1.1](bob-cli-kx.3.1.1.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-kx.3.1.3](bob-cli-kx.3.1.3.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.2/README.md) | [bob-cli-kx.3.1.2](bob-cli-kx.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`59b6149`](https://github.com/bobs-org/bob-cli/commit/59b6149a41aa7f6f89ad715c4054aef4fe4302b8) | feat(gmail): materialize owned archive receipts into mail notes | [bob-cli-kx.3.1.2](bob-cli-kx.3.1.2.md) | 2026-11-13 09:34:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.3.1.2][1] | Need the phase scope and notes | 3 |
| read-by | [agent:bob-cli-kx.3.1.land][2] | Need the child scope and notes | 1 |
| read-by | [agent:bob-cli-kx.3.1.land--5][2] | Verify the receipt phase, child epic, and all six closed implementation phases before final integration close | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.1.land.md

<!-- sase:referenced-by:end -->
