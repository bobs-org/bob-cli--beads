# Bead: bob-cli-kx.3.1.3 — Restore recorded messages through an explicit undo command

[Bead Pages](../README.md) / [bob-cli-kx.3.1](bob-cli-kx.3.1.md) / bob-cli-kx.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.md) · **Assignee:** `bob-cli-kx.3.1.3` · **Size:** medium
**Created:** 2026-11-13 08:02:47 EST · **Closed:** 2026-11-13 10:21:56 EST
**Plan:** [202611/gmail\_archive\_receipts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_receipts.md)

## Description

unarchive: ship bob gmail unarchive with exact recorded IDs and receipt labels, live writer and modify gates, lock-free dry-run, journal releases, receipt clearing, and fault-tested idempotency.

## Notes

[2026-11-13T15:21:28Z · bob-cli-kx.3.1.3] PROPOSED FOLLOW-UP: Bring the pre-existing docs-check word budgets into range for docs/reference/plugins/bob-ledger-tools.md (6,136/6,000) and docs/reference/plugins/bob-navigation-hotkeys.md (6,055/6,000); both files are unchanged in this phase, and docs-check reports no other failures.

[2026-11-13T15:21:56Z · bob-cli-kx.3.1.3] Implemented receipt-scoped bob gmail unarchive with exact frozen-message restoration, idempotency, dry-run behavior, recorded-label recovery, journal release, and note projection repair. Verified: six unarchive integration tests, CLI parser test, CLI help test, docs-gen, and git diff --check pass. docs-check is blocked only by the two unchanged plugin reference pages recorded in the proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-kx.3.1.2](bob-cli-kx.3.1.2.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-kx.3.1.4](bob-cli-kx.3.1.4.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.3/README.md) | [bob-cli-kx.3.1.3](bob-cli-kx.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2ddfc94`](https://github.com/bobs-org/bob-cli/commit/2ddfc9444b523367ff70541524302b3cb923ae69) | feat(gmail): add receipt-scoped unarchive command | [bob-cli-kx.3.1.3](bob-cli-kx.3.1.3.md) | 2026-11-13 10:23:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.3.1.3][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-ld.2][2] | Need to check whether the unarchive commit's strict-clippy failure already has a phase proposal before recording it | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.2/README.md

<!-- sase:referenced-by:end -->
