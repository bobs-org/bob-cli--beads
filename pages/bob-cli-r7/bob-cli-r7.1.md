# Bead: bob-cli-r7.1 — Whitespace-insensitive WISPr dossier kicker assertion

[Bead Pages](../README.md) / [bob-cli-r7](README.md) / bob-cli-r7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1h4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1h4.md) · **Assignee:** `bob-cli-r7.1` · **Size:** small
**Created:** 2026-11-27 10:16:12 EST · **Closed:** 2026-11-27 10:34:05 EST
**Plan:** [202611/task\_bead\_burndown\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_1.md)

## Description

wispr-kicker: make the wispr_summary lib test check the letter-spaced MEETING NOTES kicker without depending on pdftotext's spacing, then close bob-cli-q9.

## Notes

[2026-11-27T15:33:42Z · bob-cli-r7.1] PROPOSED FOLLOW-UP: just check still red on clean base from clippy_gate errors unrelated to wispr-kicker: clippy::question_mark at src/native/prose/section_model.rs:924 (already reported on bob-cli-qj.5.1 note #1 by bob-cli-qp.land) and clippy::items_after_test_module at src/native/prose/relocate.rs:813 (lib test target). Both reproduce identically with this phase change stashed; just check runs no tests until they are fixed.

[2026-11-27T15:34:05Z · bob-cli-r7.1] Wispr-kicker fix applied in src/native/meetings/profile.rs (7 insertions, 1 deletion, uncommitted for the land agent): kicker assertion compares whitespace-stripped text against MEETINGNOTES and still prints raw text on failure; all other assertions unchanged; only letter-spaced string in the module. Verified: cargo test --lib -- wispr_summary ok (1 passed), cargo test --lib -- native::meetings:: ok (41 passed), cargo fmt --check ok, epic-symbols clean. Task bead bob-cli-q9 closed. just check remains blocked by two pre-existing clippy_gate errors recorded as PROPOSED FOLLOW-UP (reproduce identically on clean base).

## Dependencies

- **Blocks:** [bob-cli-r7.2](bob-cli-r7.2.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r7.1/README.md) | [bob-cli-r7.1](bob-cli-r7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2671238`](https://github.com/bobs-org/bob-cli/commit/26712382e5f1e6a38e9b819c0e4e1dc1470aa111) | fix(meetings): whitespace-insensitive WISPr dossier kicker assertion | [bob-cli-r7.1](bob-cli-r7.1.md) | 2026-11-27 10:34:57 EST |
