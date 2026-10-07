# Bead: bob-cli-52.2 — uv resolution, URL safety, and doctor rows

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.2` · **Size:** small
**Created:** 2026-10-07 08:11:16 EDT · **Closed:** 2026-10-07 08:37:40 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

hardening: one shared `resolve_uv()` for the clip adapter, the Keep adapter, and gkeep doctor, with uv rows in both doctors. Also the bob-cli-4v IPv4-mapped IPv6 fix, a resolved-address check that pins every curl hop, and the `--max-time` doc drift fix.

## Notes

[2026-10-07T12:37:10Z · bob-cli-52.2] PROPOSED FOLLOW-UP: lib failures every_value_arg_has_a_decision and listen_filter_renders_card fail identically on clean base tree (verified via stash); triage against known bob-cli-4j/4u backlog

[2026-10-07T12:37:14Z · bob-cli-52.2] PROPOSED FOLLOW-UP: just check-web-clip-adapter self-test fails in sandbox at Playwright BrowserType.launch (TargetClosedError), unrelated to hardening Rust changes; needs athena/real-machine run

[2026-10-07T12:37:19Z · bob-cli-52.2] PROPOSED FOLLOW-UP: capture_pomodoros missing_note_and_missing_section_are_warning_successes flaked once under full parallel run but passes alone; matches known parallel flake bob-cli-40 pattern

[2026-10-07T12:37:31Z · bob-cli-52.2] RESOLVES: bob-cli-4v — is_non_global_literal now judges IPv4-mapped/compatible IPv6 literals by embedded IPv4; unit + CLI (BOB_HIGHLIGHTS_CURL=/bin/false) reproductions added

[2026-10-07T12:37:40Z · bob-cli-52.2] hardening done: shared env::resolve_uv (PATH+~/.local/bin+~/.cargo/bin+homebrew+/usr/local) used by clip adapter, Keep adapter, gkeep doctor uv row (new, 8-check JSON) and ref doctor web-clip-uv row with (outside PATH) markers; bob-cli-4v mapped-literal fix with unit+CLI tests; per-hop resolved-address check with --resolve pin + BOB_HIGHLIGHTS_RESOLVE seam (support.rs defaults *=203.0.113.1) + 2 new fetch tests; docs --max-time 300 + pinning scope. Verified: cargo fmt clean, clippy no new warns, cargo test all suites green except 2 lib failures proven pre-existing on clean base (noted as follow-ups) and 1 parallel flake passing alone; just check-adapter ok, check-web-clip-adapter fails at sandbox browser launch (noted). epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-52.6](bob-cli-52.6.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.9](bob-cli-52.9.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.2/README.md) | [bob-cli-52.2](bob-cli-52.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3232214`](https://github.com/bobs-org/bob-cli/commit/32322146c23cdd625f1b84b9250bb163f8d34296) | feat(hardening): shared uv resolution, URL safety, and doctor rows | [bob-cli-52.2](bob-cli-52.2.md) | 2026-10-07 08:39:11 EDT |
