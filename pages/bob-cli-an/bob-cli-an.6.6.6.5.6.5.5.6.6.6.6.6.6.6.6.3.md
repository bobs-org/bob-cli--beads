# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3 — Verify and coordinate the annotated-overwrite archive move under an open PDF

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3` · **Size:** large
**Created:** 2026-10-27 03:08:27 EDT · **Closed:** 2026-10-27 03:58:01 EDT
**Plan:** [202610/backlog\_batch16\_mac\_build\_orphan\_refs\_archive\_moves\_plugin\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md)

## Description

archive-move-presenter: resolve bob-cli-d0 by reproducing the archive move with the NSDocument presenter fixture on macOS CI, then sending the right move notifications or recording why merging-only access is correct.

## Notes

[2026-10-27T07:57:47Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3] Baseline 2f004d77. Annotated overwrite now uses one outer coordinate_explicit_pdf_move_with (live PDF -> preflighted archive PDF, ForMerging|ForMoving). Unannotated overwrites stay on merging write. move_annotated_bundle uses MoveContext::move_forward; immediate rollback uses InAccessorMoveReverseCoordinator (move_back, no-op before the forward move). Independent PlatformReverseCoordinator recovery uses a fresh coordinate_moving_write from archive to live, rechecks hashes inside the accessor, then deletes only a verified owned replacement. Feature enablement unchanged (default off). Never .forReplacing, never uncoordinated fallback.

Linux fake tests: 92 overwrite/file_coordination lib tests passed, including annotated success (one outer call, forward will/did), failpoint sweep (empty events before move; forward+inverse after), presenter-save abort before mutation, and platform reverse present/absent/changed-archive.

Native NSDocument tests added in macos_tests.rs (prefix archive_move_presenter_): merging+raw-rename unsafe control; notified forward follows archive and keeps replacement; in-accessor rollback restores live save target; merging-only reverse unsafe control; notified reverse restores live save target. They panic on CI if swiftc/login/presenter is missing; skip locally. Not executed on athena (Linux). Lander must check macOS CI job on the landed SHA, step "Run archive-move presenter cases": cargo test --locked --lib archive_move_presenter -- --nocapture --test-threads=1.

aarch64-apple-darwin clippy with stub CC/AR and CRATE_CC_NO_DEFAULTS=1 finished (type-check only, not a native build or runtime). just check, just docs-check, just check-scripts, and highlights_coordination_acceptance --self-test (13/13) passed. Real Highlights guided run remains unrun. bob-cli-d0 and ancestors left open.

[2026-10-27T07:58:01Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3] Annotated overwrite archive moves and recovery now use one bounded ForMerging|ForMoving scope with will/did notifications. Linux: 92 overwrite/file_coordination lib tests, just check, docs-check, and acceptance --self-test 13/13 passed; aarch64-apple-darwin clippy with stub CC/AR is type-check only. Native archive_move_presenter_* NSDocument cases are in macos_tests.rs and CI (--nocapture) but were not run on athena; lander must confirm the macOS job on the landed SHA. Real Highlights guided run remains unrun. bob-cli-d0 left open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e557b02`](https://github.com/bobs-org/bob-cli/commit/e557b021244a5aef656cbef0fcb14f6aea71aa53) | feat(ref): coordinate annotated-overwrite archive moves under open PDFs | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.3.md) | 2026-10-27 03:59:02 EDT |
