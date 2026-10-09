# Bead: bob-cli-62.1 — Model located reading-task actions and v2 note projection

[Bead Pages](../README.md) / [bob-cli-62](README.md) / bob-cli-62.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z7.md) · **Assignee:** `bob-cli-62.1` · **Size:** medium
**Created:** 2026-10-09 15:45:02 EDT · **Closed:** 2026-10-09 16:09:30 EDT
**Plan:** [202610/finish\_ref\_sync\_parent\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/finish_ref_sync_parent_tasks.md)

## Description

v2-planning: add pure v1/v2/birth/reopen planning, parent-free sync snapshots, status conflict handling, and managed-embed rendering with focused tests.

## Notes

[2026-10-09T20:09:14Z · bob-cli-62.1] v2-planning implemented (pure seam, no scan wiring): new highlights_ref/reading_plan.rs with NoteBranch/classify_note_branch (missing note = v2 birth; outside task or managed embed = v2; in-note ^ref / trackerless legacy = v1), BirthParent/resolve_birth_parent (injected resolver; any ParentError falls back to mac_inbox + warning child), BirthTask/select_birth_task (unique orphan incl. newest-closed adopted, none = Insert, ambiguous/archive-open = Refused), missing_task_diagnostic (open_ref_without_task + git/abandoned guidance; terminal silent), status_mark, v2_task_status_signal (task-vs-base gesture detection, marker/fm-only changes drive LineEdit, incompatible inputs conflict via pdf_task_status_conflict_error shape, archived-terminal + open signal = reopen, live-terminal = line edit, [?] overlay via ref_task_mark_target_status, unknown marks quiet, no-base disagreement refuses), plan_reopen_destination (archive source route when open else inbox + warning), managed_embed_target (route for root, path-minus-md otherwise incl. done/), split/join_body_lines (CRLF-preserving), heal_managed_embed (exactly one ![[res#^id]] one blank below H1; H1-less bodies untouched), v2_birth_body (embed instead of tracker, audio after embed), plan_reading_task composer returning ReadingTaskPlan {branch, kind Birth/Existing/ClosedTerminal/Reopen/Missing/Refused/V1, action NoWrite/Insert{route,label,warning,mark,prefer_block_id}/LineEdit, residence, embed, status_target, task_changed, refuse_status_parent_writes, diagnostics}. projection.rs adds without_parent/normalize_v2_base/residence_parent_value/marker_projection_with_parent_hint. audio.rs adds maybe_insert_audio_embed_after_managed (v1 placement untouched). region.rs split_note_body drops the recognized managed line from own_notes (regionless legacy bodies verbatim). Public scan entrypoints unwired (for bob-cli-62.3); executor consumes the plan (bob-cli-62.2). 50 focused vault-free unit tests in highlights_ref/tests/reading_plan.rs. Verified: cargo test --lib 2110 passed; highlights_ref 292 passed; ref_tasks 24 passed; cargo test --test cli highlights 222 passed; cargo test --test cli ref_ 205 passed + 1 pre-existing doctor failure (see follow-up); cargo fmt --check clean; cargo clippy --all-targets --all-features exit 0 (only awaiting-wiring dead_code seam warnings, same as prior phase).

[2026-10-09T20:09:22Z · bob-cli-62.1] PROPOSED FOLLOW-UP: doctor_reports_ref_tasks_and_parents_rows fails on missing fixture lib/ dir — `bob ref doctor` exits 1 with `library directory does not exist or is not a directory` in the test vault; reproduces byte-identically (modulo PID/timing) on clean base HEAD 4cc1281 via separate worktree, so unrelated to v2-planning (see bob-cli-5y.7 note 3 which already records it as pre-existing).

[2026-10-09T20:09:30Z · bob-cli-62.1] v2-planning done and verified: pure reading-plan seam (classify/birth+adopt/reopen/status-vs-base/parent-free snapshots/embed heal + v2 birth bodies) with 50 vault-free unit tests; public scan paths untouched for later phases. cargo test --lib 2110 passed, cli highlights 222 passed, cli ref_ 205 passed, fmt clean, clippy exit 0. Only failure is doctor_reports_ref_tasks_and_parents_rows, proven byte-identical on clean base HEAD 4cc1281 (missing fixture lib/ dir; recorded as PROPOSED FOLLOW-UP, cf. bob-cli-5y.7 note 3). No epic-symbol entries remain.

## Dependencies

- **Blocks:** [bob-cli-62.2](bob-cli-62.2.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-62.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-62.1/README.md) | [bob-cli-62.1](bob-cli-62.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8c938cf`](https://github.com/bobs-org/bob-cli/commit/8c938cfb2a126e2bc92185f7d278153b2ef7dfab) | feat(highlights-ref): add vault-free v2 reading-plan seam | [bob-cli-62.1](bob-cli-62.1.md) | 2026-10-09 16:11:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-62.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-62.1/README.md

<!-- sase:referenced-by:end -->
