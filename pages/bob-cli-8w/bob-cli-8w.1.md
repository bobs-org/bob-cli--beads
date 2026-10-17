# Bead: bob-cli-8w.1 — bob reports which notes a capture should open

[Bead Pages](../README.md) / [bob-cli-8w](README.md) / bob-cli-8w.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8q.md) · **Assignee:** `bob-cli-8w.1` · **Size:** medium
**Created:** 2026-10-17 15:54:14 EDT · **Closed:** 2026-10-17 16:33:10 EDT
**Plan:** [202610/ctrl\_enter\_capture\_and\_open.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_enter_capture_and_open.md)

## Description

bob-open-notes: add the always-present, batch-level `open_notes` array to `bob capture --format json` (dry-run and real runs alike). Each entry carries an absolute path, a role, a label, and a landing line and ref taken from the final staged text. Document the field in docs/capture.md and test every capture kind.

## Notes

[2026-10-17T20:25:49Z · bob-cli-8w.1] PROPOSED FOLLOW-UP: lib test native::highlights_ref::note_snapshot::profile::tests::pandoc_maps_every_contract_construct_to_tex fails identically on the clean base tree (panic: lifted link at src/native/highlights_ref/note_snapshot/profile.rs:946). Out of scope for bob-open-notes; close this phase anyway.

[2026-10-17T20:32:44Z · bob-cli-8w.1] PROPOSED FOLLOW-UP: cite bob-cli-87 / closed bob-cli-8g.6 notes — pandoc_maps_every_contract_construct_to_tex still panics lifted link on clean HEAD; already tracked, out of scope here.

[2026-10-17T20:33:10Z · bob-cli-8w.1] bob capture --format json now always emits batch-level open_notes (dry-run and real) from staged text before commit: absolute path, role, label, landing line, and ref; day last when changed; first-touch path dedupe. Documented in docs/capture.md. CLI suite tests/cli/capture/open_notes.rs covers task, bullet, sub_bullet, toggle, link, pomodoro session/link/task, complete, dependency, project_note, library-hit and queued ref. cargo fmt --check and clippy gate green. cargo test --test cli 1752 passed including the 17 open_notes tests and task_blocks dry/real after nulling open_notes.path. just check still fails only the clean-base lib test pandoc_maps_every_contract_construct_to_tex (lifted link; tracked by bob-cli-87). No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-8w.3](bob-cli-8w.3.md) ◐ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8w.1/README.md) | [bob-cli-8w.1](bob-cli-8w.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8b6ca21`](https://github.com/bobs-org/bob-cli/commit/8b6ca217377c327843e28285bce7d7b93a360005) | feat(capture): emit batch-level open\_notes in JSON | [bob-cli-8w.1](bob-cli-8w.1.md) | 2026-10-17 16:34:30 EDT |
