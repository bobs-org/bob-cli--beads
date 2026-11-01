# Bead: bob-cli-ey.1.1.3 — %n replaces the trailing # Pomodoro note; %l replaces URL %/URL @

[Bead Pages](../README.md) / [bob-cli-ey.1.1](bob-cli-ey.1.1.md) / bob-cli-ey.1.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Assignee:** `bob-cli-ey.1.1.3` · **Size:** medium
**Created:** 2026-10-31 12:58:15 EDT · **Closed:** 2026-10-31 19:46:16 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

## Description

note-and-listen-directives: teach the directive lexer `%n` and `%l`; route `%n` to the existing Pomodoro-note path with its refusals (routes, forced route, `s:`, `$`, `#type`; `@@route` does not apply) and delete the trailing-`#` marker; route `%l` to ref listen (bare-URL items only, else `directive_not_applicable`) and delete `is_standalone_listen_marker` everywhere, including `gkeep/plan.rs`; update help, docs, and tests. Commit as `feat(capture)!:`.

## Notes

[2026-10-31T23:46:16Z · bob-cli-ey.1.1.3] Implemented %n (Pomodoro note) and %l (listen) directives; deleted trailing-# marker and is_standalone_listen_marker (incl. gkeep). Verified: cargo test --workspace all green (4235 lib + 2590 cli), just docs-check passed, cargo fmt + clippy gates clean, no epic-symbols left. Covered %n fallback order/no-Pomodoro, %n refusals (routes/forced/s/priority/type), %l bare-URL-only with directive_not_applicable elsewhere.

## Dependencies

- **Depends on:** [bob-cli-ey.1.1.2](bob-cli-ey.1.1.2.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.1.1.4](bob-cli-ey.1.1.4.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.1.1.5](bob-cli-ey.1.1.5.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.1.1.3/README.md) | [bob-cli-ey.1.1.3](bob-cli-ey.1.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4c011cd`](https://github.com/bobs-org/bob-cli/commit/4c011cd788f3953a90e9251ee67a985a824871b6) | feat(capture)!: teach %n and %l directives, retire trailing # and URL %/@ | [bob-cli-ey.1.1.3](bob-cli-ey.1.1.3.md) | 2026-10-31 19:47:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.1.1.3][1] | Need phase scope and design | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.1.1.3/README.md

<!-- sase:referenced-by:end -->
