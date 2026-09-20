# Bead: bob-cli-23.1 — Rename the pre-scan hook config surface and add \`--no-hooks\`

[Bead Pages](../README.md) / [bob-cli-23](README.md) / bob-cli-23.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.16](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.apollo.16.md) · **Assignee:** `bob-cli-23.1` · **Size:** medium
**Created:** 2026-09-20 15:38:36 EDT · **Closed:** 2026-09-20 15:48:13 EDT
**Plan:** [202609/highlights\_pre\_scan\_hook.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/highlights_pre_scan_hook.md)

## Description

cli: rename `highlights.pre_scan_command` to `highlights.pre_scan_hook` (config key, env override, report labels, docs), reject the legacy names loudly, add the `-n|--no-hooks` flag to `bob highlights`, and export a hook-marker env var to the hook child process.

## Notes

[2026-09-20T19:48:13Z · bob-cli-23.1] Renamed highlights.pre_scan_command to pre_scan_hook (config key, BOB_HIGHLIGHTS_PRE_SCAN_HOOK env, report labels), legacy key and legacy env now hard errors naming new spelling, added -n|--no-hooks on root+scan+doctor threading through scan_library and doctor_vault (doctor prints skipped), hook child gets BOB_HIGHLIGHTS_IN_PRE_SCAN_HOOK=1. Verified: cargo test full suite green (879 lib + 457 cli incl 7 new hook tests + existing pre-scan tests updated, config unit tests incl legacy rejection), cargo clippy clean (warnings only), help shows -n|--no-hooks alphabetically. Note: cargo fmt --check fails repo-wide on untouched files too (toolchain rustfmt 1.9 vs repo baseline), not introduced by this change.

## Dependencies

- **Blocks:** [bob-cli-23.2](bob-cli-23.2.md) ◐ · ⧖ 2026-09-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-23.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-23.1/README.md) | [bob-cli-23.1](bob-cli-23.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8d19926`](https://github.com/bobs-org/bob-cli/commit/8d19926d6fa6bb82d4ed7eea10c0f24939cd18c6) | feat(highlights): rename pre-scan hook config and add --no-hooks | [bob-cli-23.1](bob-cli-23.1.md) | 2026-09-20 15:48:59 EDT |
