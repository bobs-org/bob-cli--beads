# Bead: bob-cli-kx.2.1.8.3 — Sync wiring, hydration capture, and preview parity

[Bead Pages](../README.md) / [bob-cli-kx.2.1.8](bob-cli-kx.2.1.8.md) / bob-cli-kx.2.1.8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.land.md) · **Assignee:** `bob-cli-kx.2.1.8.3` · **Size:** medium
**Created:** 2026-11-12 23:51:15 EST · **Closed:** 2026-11-13 05:59:25 EST
**Plan:** [202611/gmail\_archive\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_landing_repairs.md)

## Description

integration: Capture saved IDs before watch hydration, block archive writes after failed or incomplete filing, keep filing/watch report rows when the archive phase errors, simulate enablement in dry-run so a first preview confirms, and reject a supplied mismatched -c. Implement section 3.

## Notes

[2026-11-13T10:59:25Z · bob-cli-kx.2.1.8.3] Implemented the archive sync safeguards and preview/confirmation behavior for this phase. Verified with cargo fmt --check; focused saved-ID snapshot and digest-gate unit tests; gmail_archive_apply (25), gmail_archive_preview (4), gmail_sync (41), gmail_shell (69), and gmail_transport (4) integration tests; just lint; and git diff --check. All passed. Confirmed no remaining epic symbols before close.

## Dependencies

- **Depends on:** [bob-cli-kx.2.1.8.2](bob-cli-kx.2.1.8.2.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.2.1.8.4](bob-cli-kx.2.1.8.4.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.8.3/README.md) | [bob-cli-kx.2.1.8.3](bob-cli-kx.2.1.8.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6b9261a`](https://github.com/bobs-org/bob-cli/commit/6b9261a74b0c0f27548de4992501c52c549f4447) | fix(gmail): preserve archive preview and sync safety | [bob-cli-kx.2.1.8.3](bob-cli-kx.2.1.8.3.md) | 2026-11-13 06:01:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.8.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.8.3/README.md

<!-- sase:referenced-by:end -->
