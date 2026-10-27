# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2 — Coordinate the complete rename and id-repair transaction

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2` · **Size:** medium
**Created:** 2026-10-26 22:51:28 EDT · **Closed:** 2026-10-26 23:56:44 EDT
**Plan:** [202610/remaining\_pdf\_write\_coordination.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/remaining_pdf_write_coordination.md)

## Description

rename-transaction: put ref rename, same-stem id repair, verification, scoped commit, and rollback inside one explicit coordination scope. Revalidate after presenter saves, preserve the post-save rollback baseline, notify PDF moves, and return truthful retryable errors without claiming success on a hold.

## Notes

[2026-10-27T03:56:44Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2] Coordinated rename transaction landed in src/native/highlights_ref/rename/plan.rs. One explicit MarkerWriteSession (Exempt) drives full moves via coordinate_explicit_pdf_move_with and same-stem id repair via coordinate_explicit_pdf_write_with; unchanged needs no scope. Revalidates presenter saves (marker_changed vs preimage_changed, conservative full-rename hold), absent destinations, and touched preimages inside access; marker sync runs via for_external_coordination with saved-bytes rollback baseline and digest guard; moves/verification/commit/rollback all inside the same scope with forward/reverse notifications. Verified: lib highlights_ref::rename 31 passed, cli ref_library::rename 15 passed, 13 new coordinated tests (grant/hold/fail/save/marker/renumbered/idless/occupied/verify/commit/rollback/reported-as-error/human+JSON) passed, cargo fmt --check clean, cargo clippy gate clean, full just check exit 0. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.1.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.5.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1e92359`](https://github.com/bobs-org/bob-cli/commit/1e923594f18e7150fc50fd641d3016e177e58235) | feat(highlights-ref): coordinate complete rename and id-repair transaction | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2.md) | 2026-10-26 23:57:51 EDT |
