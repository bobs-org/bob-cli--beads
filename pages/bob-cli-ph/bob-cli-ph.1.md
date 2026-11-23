# Bead: bob-cli-ph.1 — Dual-read drawer recognizer, readers, and outside-text escape

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.1` · **Size:** large
**Created:** 2026-11-22 17:36:48 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

drawer-contract: one recognizer that reads `- **Title**` and legacy ALL-CAPS drawers, the true-case drawer model and Unicode key, every bob-cli vault reader retargeted, the `__…__` escape for imported text, DV/DH vectors, and the task-drawers contract page, with every writer left unchanged.

## Notes

[2026-11-22T22:42:10Z · bob-cli-ph.1] PRECONDITION WAIT: The approved true_case_drawers plan, drawer-contract step 0, requires bob-cli-on CLOSED before changes. Audited read on 2026-11-22 shows bob-cli-on in_progress with phases .11, .12, .15, and .17 still in_progress. No implementation or plan file was authored, and no unfinished coding attempt occurred. Checkout e98c7fe9 is clean; current capture_drawers still has the legacy-only model, ASCII drawer_key, and catalog v2. Added the explicit prerequisite edge and will stage a zero-weight monitor to resume planning after bob-cli-on closes. Epic symbols check found none.

[2026-11-22T22:42:17Z · bob-cli-ph.1] PROPOSED FOLLOW-UP: Repair the required research artifact reference in the true-case drawers epic — sase artifact read research:202611/true_case_drawers/true_case_drawers.md resolved status missing on 2026-11-22. The plan requires every phase to read this report; locate its canonical published reference before implementation.

[2026-11-23T08:42:42Z · bob-cli-ph.1--1] PLANNING RESUMED: Verified bob-cli-on closed with resolution done at 2026-11-23T08:31:17Z. Fast-forwarded the clean checkout to landing commit 7703011d. The ^prj Notes home and RL53-RL60/RW54-RW57 are landed; tools/docs contract tests pass 8/8. No earlier phase implementation exists. Note #2 is resolved: refreshing bob-cli--research through sase repo open restored research:202611/true_case_drawers/true_case_drawers.md at its original canonical reference, and an audited read succeeded. Preparing one medium tale for the remaining Rust recognizer/readers, escaping, vectors, and contract page; draft grammar and header writers stay unchanged.

## Dependencies

- **Depends on:** [bob-cli-on](../bob-cli-on/README.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-ph.2](bob-cli-ph.2.md) ◐ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.3](bob-cli-ph.3.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.1.md) | [bob-cli-ph.1](bob-cli-ph.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`37b2080`](https://github.com/bobs-org/bob-cli/commit/37b2080e9efca170f542954f088ce4169d430cfa) | feat(drawers): add dual-read task drawer readers | [bob-cli-ph.1](bob-cli-ph.1.md) | 2026-11-23 08:06:21 EST |
