# Bead: bob-cli-nh.1 — Intention fields contract, typed reader, YAML writer, and readers

[Bead Pages](../README.md) / [bob-cli-nh](README.md) / bob-cli-nh.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ef](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ef.md) · **Assignee:** `bob-cli-nh.1` · **Size:** large
**Created:** 2026-11-19 09:35:21 EST
**Plan:** [202611/period\_intentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_intentions.md)

## Description

fields: add src/native/intentions/ with the day-or-period subject resolver, the typed frontmatter reader (intentions, summary, reflection, and stamps) with a legacy fallback to the old body shapes, a line-preserving YAML writer that verifies by re-parsing, and one review state machine for days and periods. Rewire every reader to it: capture-pomodoros, periods show, list, parts, strip, and brief. Document the contract in docs/periods.md.

## Notes

[2026-11-19T16:22:39Z · bob-cli-nh.1--1] Exported crate-level intentions API: fields::{FieldProvenance, Field<T>, Diagnostic, FrontmatterState, Fields, read, canonical_subject}; legacy::{IntentionsKind, intentions, parse_daily_headline, reflection, summary, period_sections, opening_headline}; state::{ReviewState, SummaryState, digest, summary_state, evaluate}; subject::{NoteSubject, SubjectInfo, ReadNoteError, read_existing}; write::{Patch<T>, OwnedPatch, WriteError, apply}.

## Dependencies

- **Blocks:** [bob-cli-nh.2](bob-cli-nh.2.md) ◐ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.3](bob-cli-nh.3.md) ◐ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.4](bob-cli-nh.4.md) ◐ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.5](bob-cli-nh.5.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.1.md) | [bob-cli-nh.1](bob-cli-nh.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e7aa392`](https://github.com/bobs-org/bob-cli/commit/e7aa392d688ea250ada1a6d732e3f27ed0e67c9c) | feat(intentions): add unified fields contract and readers | [bob-cli-nh.1](bob-cli-nh.1.md) | 2026-11-19 12:52:40 EST |
