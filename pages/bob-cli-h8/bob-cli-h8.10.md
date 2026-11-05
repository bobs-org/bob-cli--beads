# Bead: bob-cli-h8.10 — Make the brief's Still open lists honest for ended periods

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.10` · **Size:** medium
**Created:** 2026-11-04 16:39:10 EST · **Closed:** 2026-11-04 19:17:09 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

brief-still-open: apply the chosen bob-cli-gu semantics so a past period's Still open section stops reporting today's vault. By default, rebuild Kept 3+ and No linked minutes as of span end, and omit Blocked projects with a note.

## Notes

[2026-11-05T00:16:53Z · bob-cli-h8.10] PROPOSED FOLLOW-UP: docs-check lint fails on base too — docs/reference/mac-capture/protocol.md over budget at 6003 words (cap 6000). Reproduces identically with changes stashed.

[2026-11-05T00:16:59Z · bob-cli-h8.10] PROPOSED FOLLOW-UP: cargo clippy reports 4 pre-existing errors in capture_language (editor_pomodoro.rs needless_return x3, past.rs boolean logic) on files this phase did not touch; owned by h2/h4 per shared rules.

[2026-11-05T00:17:09Z · bob-cli-h8.10] Implemented still_open rebuild for ended periods in src/native/periods/brief.rs: zero_minute and kept rebuilt as of span end (created<=end, open at end, no linked minutes; kept counts dated Rotten Log entries), blocked omitted with as_of/omitted_reason, Markdown title as of span end. Updated docs/periods.md and tests (new rebuild test + closed-week expectations). Verified: 10/10 brief tests pass, cargo fmt clean, clippy/docs-check failures pre-existing on base (recorded as follow-ups).

## Dependencies

- **Depends on:** [bob-cli-h8.9](bob-cli-h8.9.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.10/README.md) | [bob-cli-h8.10](bob-cli-h8.10.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a3aa214`](https://github.com/bobs-org/bob-cli/commit/a3aa2149bced74d8e98090a89e5d5d954deb8411) | feat(periods): rebuild brief Still open for ended periods | [bob-cli-h8.10](bob-cli-h8.10.md) | 2026-11-04 19:18:19 EST |
