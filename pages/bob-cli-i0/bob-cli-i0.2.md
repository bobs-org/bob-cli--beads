# Bead: bob-cli-i0.2 — What's new digest engine

[Bead Pages](../README.md) / [bob-cli-i0](README.md) / bob-cli-i0.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.199](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.199.md) · **Assignee:** `bob-cli-i0.2` · **Size:** medium
**Created:** 2026-11-06 15:11:24 EST · **Closed:** 2026-11-06 15:54:48 EST
**Plan:** [202611/install\_all\_wait\_and\_whats\_new.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md)

## Description

digest-engine: implement `install_ui digest`. It resolves ranges from the install watermark, extracts commits, strips SASE trailers, groups by Conventional Commit type, chooses the richest of four levels that fits the screen, and renders the section plus a digest.json record. Tests use real temp Git repos.

## Notes

[2026-11-06T20:54:48Z · bob-cli-i0.2] digest-engine done: commits.py (ranges, parsing, trailer/Verified handling) + digest.py (budget, 4 levels, layout, record) + digest subcommand wired; 87 install_ui tests pass via just check-scripts (exit 0); verified TTY digest at 80/260 cols against this repo (rows fit 100-cell measure, SHAs right-aligned, breaking badges, folded Verified rows) and non-TTY plain mode with 60-commit cap

## Dependencies

- **Depends on:** [bob-cli-i0.1](bob-cli-i0.1.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-i0.4](bob-cli-i0.4.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-i0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.2/README.md) | [bob-cli-i0.2](bob-cli-i0.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4fd782a`](https://github.com/bobs-org/bob-cli/commit/4fd782a3c172e732244a7625b2c236bcbd1f3600) | feat(install): add What's new digest engine | [bob-cli-i0.2](bob-cli-i0.2.md) | 2026-11-06 15:56:29 EST |
