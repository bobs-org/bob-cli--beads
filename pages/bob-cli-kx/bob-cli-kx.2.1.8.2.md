# Bead: bob-cli-kx.2.1.8.2 — Mutation boundary, let-go, and failure isolation

[Bead Pages](../README.md) / [bob-cli-kx.2.1.8](bob-cli-kx.2.1.8.md) / bob-cli-kx.2.1.8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.land.md) · **Assignee:** `bob-cli-kx.2.1.8.2` · **Size:** medium
**Created:** 2026-11-12 23:51:15 EST · **Closed:** 2026-11-13 05:20:00 EST
**Plan:** [202611/gmail\_archive\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_landing_repairs.md)

## Description

boundary: Plan every terminal journal event before its Gmail write, revalidate local evidence per thread under the maintenance lock, honor the planned decision set, fix recovery ordering, scope let-go to recorded IDs and run it independently of the gate, and add the missing end-to-end fault tests. Implement section 2.

## Notes

[2026-11-13T10:20:00Z · bob-cli-kx.2.1.8.2] Implemented section 2: journal-before-mutate with pre-planned terminal events, per-thread vault maintenance lock with fresh revalidation (frozen IDs never expanded, growth becomes unsaved), planned-decision gating (Kept-to-Archive held, downgrades honored, receipt resolved only when Archive planned), recovery-before-consent ordering with invalid_grant abort, let-go scoped to recorded IDs with thread identity checks running on paused/unresolvable runs, and HOLD_UNRESOLVABLE accounting. Verified: cargo fmt --check clean; clippy gates pass (only pre-existing unrelated warnings); cargo test --lib archive_ 137 passed; gmail_archive_apply 23 passed (15 existing + 8 new boundary fault tests asserting exact argv and journal); gmail_archive_preview 3, gmail_transport 4, gmail_sync 41, gmail_shell 69 passed. epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-kx.2.1.8.1](bob-cli-kx.2.1.8.1.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.2.1.8.3](bob-cli-kx.2.1.8.3.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.8.2/README.md) | [bob-cli-kx.2.1.8.2](bob-cli-kx.2.1.8.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`642e158`](https://github.com/bobs-org/bob-cli/commit/642e1580872c74acc2ce3d30b02ff2cfe510841e) | feat(gmail)!: apply mutation boundary, let-go isolation, and fault tests \[bob-cli-kx.2.1.8.2\] | [bob-cli-kx.2.1.8.2](bob-cli-kx.2.1.8.2.md) | 2026-11-13 05:22:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.8.2][1] | Need full details | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.8.2/README.md

<!-- sase:referenced-by:end -->
