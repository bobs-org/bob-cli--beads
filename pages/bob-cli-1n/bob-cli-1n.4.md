# Bead: bob-cli-1n.4 — Add a configurable pre-scan command to \`bob highlights\`

[Bead Pages](../README.md) / [bob-cli-1n](README.md) / bob-cli-1n.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ez](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ez.md) · **Assignee:** `bob-cli-1n.4` · **Size:** medium
**Created:** 2026-08-27 12:48:58 EDT · **Closed:** 2026-08-27 13:02:48 EDT
**Plan:** [202608/vault\_git\_sync.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/vault_git_sync.md)

## Description

highlights: teach `bob highlights scan` to run a configured command before it inspects the library, wired through `~/.config/bob/config.yml` and an environment override, so an off-band PDF bridge can deliver `xlib/` intake.

## Notes

[2026-08-27T17:02:48Z · bob-cli-1n.4] Implemented configurable bob highlights scan pre-scan command via config/env, doctor reporting, docs, and tests; verified with cargo test pre_scan, cargo test native::config::tests, cargo test highlights_ref_scan, and just all.

## Dependencies

- **Blocks:** [bob-cli-1n.5](bob-cli-1n.5.md) ◐ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1n.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.4/README.md) | [bob-cli-1n.4](bob-cli-1n.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`86bff41`](https://github.com/bobs-org/bob-cli/commit/86bff4105b7ac7de2d8b60d4b2241ff3204db9b9) | feat(highlights): add scan pre-scan hook | [bob-cli-1n.4](bob-cli-1n.4.md) | 2026-08-27 13:04:01 EDT |
