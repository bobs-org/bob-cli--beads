# Bead: bob-cli-53.2 — Date marks in Tasks query results

[Bead Pages](../README.md) / [bob-cli-53](README.md) / bob-cli-53.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0xq](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0xq.md) · **Assignee:** `bob-cli-53.2` · **Size:** small
**Created:** 2026-10-07 08:19:07 EDT · **Closed:** 2026-10-07 09:11:21 EDT
**Plan:** [202610/task\_date\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_date_marks.md)

## Description

tasks-results: in full-mode Tasks query results, add the same mark to each date component through a bounded per-row frame pass. The date-mark post-processor triggers the pass, and it falls back to Tasks' native emoji dates. In short-mode results, CSS swaps the emoji for the glyph. Extend the tests, contract, README, and manifest, then deploy.

## Notes

[2026-10-07T13:11:21Z · bob-cli-53.2] Tasks-results date marks shipped: 267 frame-pass mixin (schedule/run/decorate, rAF+16ms fallback, 3-frame detached / 60-frame pending retries, WeakSet dedup, idempotent, Tasks listeners preserved), 266 hook (266 at 999 lines), 310+fragments registration, full/short-mode CSS, 12 new T-vector tests green, full suite 2040/2040, validate 6/6, deployed bob-ledger-tools 1.32.0 to vault via plugins sync -r workspace. Contract extended in docs/date-marks.md (Tasks subsection, T1-T9, 4 checklist items). Live checklist pending for Bryan.

## Dependencies

- **Depends on:** [bob-cli-53.1](bob-cli-53.1.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-53.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-53.2/README.md) | [bob-cli-53.2](bob-cli-53.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b5a0258`](https://github.com/bobs-org/bob-cli/commit/b5a0258de16d872bb69eea968f50478f0f6909f6) | docs(date-marks): document Tasks query results date marks (T1-T9) | [bob-cli-53.2](bob-cli-53.2.md) | 2026-10-07 09:12:44 EDT |
