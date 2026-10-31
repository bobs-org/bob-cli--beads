# Bead: bob-cli-ey.1.1.3 — %n replaces the trailing # Pomodoro note; %l replaces URL %/URL @

[Bead Pages](../README.md) / [bob-cli-ey.1.1](bob-cli-ey.1.1.md) / bob-cli-ey.1.1.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Assignee:** `bob-cli-ey.1.1.3` · **Size:** medium
**Created:** 2026-10-31 12:58:15 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

## Description

note-and-listen-directives: teach the directive lexer `%n` and `%l`; route `%n` to the existing Pomodoro-note path with its refusals (routes, forced route, `s:`, `$`, `#type`; `@@route` does not apply) and delete the trailing-`#` marker; route `%l` to ref listen (bare-URL items only, else `directive_not_applicable`) and delete `is_standalone_listen_marker` everywhere, including `gkeep/plan.rs`; update help, docs, and tests. Commit as `feat(capture)!:`.

## Dependencies

- **Depends on:** [bob-cli-ey.1.1.2](bob-cli-ey.1.1.2.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.1.1.4](bob-cli-ey.1.1.4.md) ◐ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.1.1.5](bob-cli-ey.1.1.5.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.1.1.3/README.md) | [bob-cli-ey.1.1.3](bob-cli-ey.1.1.3.md) | 0 |
