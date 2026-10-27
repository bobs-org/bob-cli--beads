# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2 — Coordinate ref rename/move, id stamp, and create --force PDF writes

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2` · **Size:** large
**Created:** 2026-10-26 15:53:09 EDT · **Closed:** 2026-10-27 02:18:58 EDT
**Plan:** [202610/backlog\_batch15\_vault\_safety\_pdf\_moves\_and\_red\_gates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md)

## Description

open-pdf-move-coordination: resolve bob-cli-az by routing rename/move, the id stamp, and create --force through bounded Highlights file coordination, then retiring the Bob Refs rename card's close-the-PDF hint.

## Notes

[2026-10-27T02:50:04Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2] Planning audit at dc040b02: no prior-worker notes and no phase epic-symbol entries; wrong-vault prerequisite has landed. Rename still moves and rewrites its id without coordination, while filed overwrite already owns an outer coordinated transaction. Private pdf_target scratch stamping is safe; remaining public stamp/copy and early audio publication paths need the guard. Prepared a five-phase child epic (move coordinator, rename transaction, guarded install, remaining capture writers, Mac UI/docs/acceptance), validated and revalidated with zero warnings. No product or memory files changed. The child lander is instructed to verify and close this phase only; bob-cli-az and batch-15 ancestor closure remain with the batch lander.

[2026-10-27T02:50:09Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2] PROPOSED FOLLOW-UP: Verify annotated-overwrite archive move presenter tracking — overwrite/execute.rs archive_pdf uses rename_no_replace inside merging access, and overwrite/recovery.rs PlatformReverseCoordinator uses coordinate_merging_write for the inverse; neither path currently issues didMoveToURL. This is a separate existing archive transaction from ref rename. The batch lander should check native presenter behavior and existing ownership before expanding bob-cli-az or filing follow-up work; no live or native reproduction was attempted during planning.

[2026-10-27T06:19:18Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.land] Tale cleanup landed everything this phase requires (auto-closed with the child epic at 2026-10-27). Rename/move and the id stamp are coordinated (execute_rename_with_session -> rename_move_accessor/rename_merge_accessor -> write_id_marker_with_saved); create --force and the other public PDF writers go through the guarded publish boundary; the Bob Refs close-the-PDF hint is gone. The dead uncoordinated rename path (apply_and_verify/apply_transaction/rollback_applied/write_id_marker) is deleted, both dead-code allows removed, uncoordinated() now test-only. Verified on this tree: clippy gate exit 0; lib tests rename 30 / marker_write 20 / publish 30 passed; cli ref_library::rename 15 passed; just check exit 0. Native limitations: Mac offline (ssh mac timed out), so no NSDocument move-fixture run, Mac bundle/typecheck, or real Highlights acceptance; Linux portable tests and the acceptance kit self-test passed during the phases.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.1.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.md) | 0 |
