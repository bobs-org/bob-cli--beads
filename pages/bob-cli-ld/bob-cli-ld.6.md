# Bead: bob-cli-ld.6 — bob projects list -f json report

[Bead Pages](../README.md) / [bob-cli-ld](README.md) / bob-cli-ld.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c6.md) · **Assignee:** `bob-cli-ld.6` · **Size:** medium
**Created:** 2026-11-13 10:58:46 EST · **Closed:** 2026-11-13 13:50:19 EST
**Plan:** [202611/subprojects\_catalog\_section.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subprojects_catalog_section.md)

## Description

projects-list-json: add the versioned JSON report (projects, catalogs, findings) that the card consumes, plus a human catalog footer.

## Notes

[2026-11-13T18:32:43Z · bob-cli-ld.6] PROPOSED FOLLOW-UP: Restore docs-check headroom on the unchanged mounted references: the 2026-11-13 run flags bob-ledger-tools at 6136/6000 (existing tracker bob-cli-il) and bob-navigation-hotkeys at 6082/6000 (closed tracker bob-cli-jz now has post-close +1 evidence). The report page edited by this phase passes; the two unrelated source pages are untouched.

[2026-11-13T18:50:05Z · bob-cli-ld.6--1] PROPOSED FOLLOW-UP: just check is blocked by the same five deny-level Clippy diagnostics in unchanged src/native/gmail/unarchive.rs: needless_borrow at 283 (two), 313, and 330, plus useless_conversion at 464. Clean-base reproduction is already recorded by bob-cli-kx.3.1.4 and independently by bob-cli-ld.4 and bob-cli-ld.5; project-list changes do not touch this file. The repair is tracked under the Gmail archive work (bob-cli-kx).

[2026-11-13T18:50:19Z · bob-cli-ld.6--1] Implemented the versioned projects list JSON report and human catalog footer; focused project-list and help tests passed. Full just check fails only on five existing Clippy diagnostics in unchanged src/native/gmail/unarchive.rs; the same clean-base failure is already tracked under bob-cli-kx.3.1.4 and recorded as a proposed follow-up on this phase. Epic-symbol inventory is empty.

## Dependencies

- **Depends on:** [bob-cli-ld.4](bob-cli-ld.4.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.9](bob-cli-ld.9.md) ◐ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ld.6.md) | [bob-cli-ld.6](bob-cli-ld.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4570a7e`](https://github.com/bobs-org/bob-cli/commit/4570a7ea9e9866c84a8c1a8e2a55ea7a8f870203) | feat(projects): add versioned projects list report | [bob-cli-ld.6](bob-cli-ld.6.md) | 2026-11-13 13:52:49 EST |
