# Bead: bob-cli-2p.2 — Named starts in \`bob capture-parse\`

[Bead Pages](../README.md) / [bob-cli-2p](README.md) / bob-cli-2p.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.36.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.36.w0.md) · **Assignee:** `bob-cli-2p.2` · **Size:** medium
**Created:** 2026-09-29 19:17:57 EDT · **Closed:** 2026-09-29 19:47:19 EDT
**Plan:** [202609/named\_pomodoro\_start.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/named_pomodoro_start.md)

## Description

editor: mirror the named start in the live-editor parser. Report mode, `section`, spans, the `=<X>#` incomplete state, and every near-miss diagnostic with precise ranges. Keep `@@` away from named starts and extend the editor/execution parity tests.

## Notes

[2026-09-29T23:47:07Z · bob-cli-2p.2] PROPOSED FOLLOW-UP: clippy --all-targets --all-features fails on untouched tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr, `|| true`); pre-existing on clean base, blocks `just lint`/`just all`

[2026-09-29T23:47:19Z · bob-cli-2p.2] Editor mirrors named starts: exact (=#bugs/=3#bugs, section+spec+two spans, # in no span), =<X># incomplete (needs pomodoro_name, partial spec, placeholder over #), E2/E3 over name, E4/nospace over extra text, child-line ranges, overflow over =<X>, =x#name close near miss; @@ never inherits incomplete named starts; human start line shows whole token; help sentence added. Verified: cargo test 1971 passed/0 failed, cargo fmt clean, new parity/chain/JSON-unit/CLI-protocol tests green; pre-existing clippy error in untouched pomodoro_name.rs:808 recorded as follow-up; no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-2p.1](bob-cli-2p.1.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2p.3](bob-cli-2p.3.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2p.4](bob-cli-2p.4.md) ◐ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2p.5](bob-cli-2p.5.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2p.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2p.2/README.md) | [bob-cli-2p.2](bob-cli-2p.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4a480bf`](https://github.com/bobs-org/bob-cli/commit/4a480bf014d8c4448442da8e869dccbcdc624589) | feat(capture): support named pomodoro starts in editor parse | [bob-cli-2p.2](bob-cli-2p.2.md) | 2026-09-29 19:49:07 EDT |
