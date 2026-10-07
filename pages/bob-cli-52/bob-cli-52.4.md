# Bead: bob-cli-52.4 — Capture grammar for reference items and URL lists

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.4` · **Size:** small
**Created:** 2026-10-07 08:11:17 EDT · **Closed:** 2026-10-07 09:27:57 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

grammar: the whole-item bare-URL claim and `CaptureKind::Ref`, the lexical URL-list split in shared draft splitting, the editor `ref` mode and `ref_url` span, and routing-option plumbing. Every production caller keeps routing off until phase capture.

## Notes

[2026-10-07T13:27:45Z · bob-cli-52.4] PROPOSED FOLLOW-UP: pre-existing failures reproduce identically on clean base (tracked): every_value_arg_has_a_decision by bob-cli-4j, capture_pomodoros parallel flake by bob-cli-40, listen-card render by bob-cli-4u

[2026-10-07T13:27:49Z · bob-cli-52.4] PROPOSED FOLLOW-UP: highlights::create::ingest_characterizes_url_failure_modes fails on clean base too (sandbox DNS resolves the fixture host to a private address); no tracking bead found

[2026-10-07T13:27:57Z · bob-cli-52.4] Grammar phase done: CaptureKind::Ref claim with routing-off plumbing, lexical URL-list split, editor ref mode/ref_url span, planner usage-error arms. Verified: 12 new lib tests + 2 new CLI tests pass; cargo check/clippy/fmt clean; full lib 1852 pass + full CLI 1118 pass except failures reproducing identically on base (4j/4u/40 + sandbox-DNS ingest test, recorded as follow-ups); epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-52.3](bob-cli-52.3.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.7](bob-cli-52.7.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.4/README.md) | [bob-cli-52.4](bob-cli-52.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`98fd8ae`](https://github.com/bobs-org/bob-cli/commit/98fd8ae492c59ed08e843e713e023595246febea) | feat(capture): add reference item grammar with routing-gated Ref kind | [bob-cli-52.4](bob-cli-52.4.md) | 2026-10-07 09:29:14 EDT |
