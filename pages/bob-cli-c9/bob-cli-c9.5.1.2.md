# Bead: bob-cli-c9.5.1.2 — Hold scans that encounter a replaced annotated PDF

[Bead Pages](../README.md) / [bob-cli-c9.5.1](bob-cli-c9.5.1.md) / bob-cli-c9.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.md) · **Assignee:** `bob-cli-c9.5.1.2` · **Size:** medium
**Created:** 2026-10-26 07:41:50 EDT · **Closed:** 2026-10-26 08:59:42 EDT
**Plan:** [202610/annotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/annotated_reference_overwrite.md)

## Description

guard: Use the archived PDF evidence to hold a restored old PDF before sync can import annotations, change tasks, or repair its marker. Cover human and JSON scan, explicit sync, dry-run behavior, and a race before execution; keep ordinary scans unchanged.

## Notes

[2026-10-26T12:59:42Z · bob-cli-c9.5.1.2--1] Implemented replaced-capture holds across human/JSON scans and explicit sync, including dry-run preview and execution/coordinated-save race rechecks. Verified: replaced_capture tests (3), execution race unit (1), ref_scan tests (55), ref_sync tests (33), cargo fmt check, git diff check, and just docs-check passed.

## Dependencies

- **Depends on:** [bob-cli-c9.5.1.1](bob-cli-c9.5.1.1.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-c9.5.1.4](bob-cli-c9.5.1.4.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.1.2.md) | [bob-cli-c9.5.1.2](bob-cli-c9.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`af41608`](https://github.com/bobs-org/bob-cli/commit/af416080dc14480e6ad9cf1a19e3b043fd8dd22b) | fix(highlights): hold replaced annotated captures | [bob-cli-c9.5.1.2](bob-cli-c9.5.1.2.md) | 2026-10-26 09:00:39 EDT |
