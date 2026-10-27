# Bead: bob-cli-d7.1 — Skip the snapshot store test when note-profile LaTeX packages are missing

[Bead Pages](../README.md) / [bob-cli-d7](README.md) / bob-cli-d7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14v.md) · **Assignee:** `bob-cli-d7.1` · **Size:** small
**Created:** 2026-10-27 14:54:31 EDT · **Closed:** 2026-10-27 15:17:31 EDT
**Plan:** [202610/backlog\_batch\_a1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_a1.md)

## Description

snapshot-test-gate: move the note-profile package skip helper into shared test support, gate store_snapshot_create_records_note_snapshot_route and any other ungated real snapshot render with it, and close bob-cli-d6.

## Notes

[2026-10-27T19:17:31Z · bob-cli-d7.1--1] Shared note-profile package gate; athena real-render route test and missing-package parser test passed; just check passed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-d7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d7.1.md) | [bob-cli-d7.1](bob-cli-d7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d208c59`](https://github.com/bobs-org/bob-cli/commit/d208c595c7483acb43a4407018a0171fd21df8fc) | fix(tests): gate note-profile snapshot renders by package availability | [bob-cli-d7.1](bob-cli-d7.1.md) | 2026-10-27 15:18:09 EDT |
