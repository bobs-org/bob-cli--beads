# Bead: bob-cli-9k.2 — Area and project parts in bob stats

[Bead Pages](../README.md) / [bob-cli-9k](README.md) / bob-cli-9k.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4t.linker.w0.md) · **Assignee:** `bob-cli-9k.2` · **Size:** medium
**Created:** 2026-10-18 16:35:49 EDT · **Closed:** 2026-10-18 18:28:48 EDT
**Plan:** [202610/pomodoro\_homes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes.md)

## Description

stats-parts: index closed-session links in the stats pass and add area and project parts to the pomodoro and task metrics, with buckets, a homes catalog, apportioned minutes, and health. Print every parts dimension in the CLI. Add an H-vector fixture vault and update docs/stats.md.

## Notes

[2026-10-18T21:34:30Z · bob-cli-9k.2] --list

[2026-10-18T22:28:44Z · bob-cli-9k.2] PROPOSED FOLLOW-UP: tests/cli/highlights/scan_hooks.rs rustfmt --check fails on clean master (write_file pre_scan_command line needs wrapping); identical on base tree, not caused by stats-parts

[2026-10-18T22:28:48Z · bob-cli-9k.2] H-vectors 167m with area/project/theme summing to total, buckets, apportioned, sase_time theme filter, byte-identical recompute. CLI prints pomodoro area/project/theme and task kind/area/project/note; project top-5 plus always-shown buckets and split line. Real vault BOB_NOW=2026-10-18T12:00:00 -r 2026-09-20..2026-10-17 major rows within 1pp of research (dev 45%, gtd 41%, sase 43%, GTD review 21%, bob 18%). Release 4w JSON median 200ms vs 174ms baseline (within 15%). cargo clippy gate and cargo test pass; just install done. just check fmt still fails on tests/cli/highlights/scan_hooks.rs identically on clean master (PROPOSED FOLLOW-UP).

## Dependencies

- **Depends on:** [bob-cli-9k.1](bob-cli-9k.1.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9k.3](bob-cli-9k.3.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.2/README.md) | [bob-cli-9k.2](bob-cli-9k.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`81103c2`](https://github.com/bobs-org/bob-cli/commit/81103c2e2b053e6107473b81f8952966e599023c) | feat(stats): add area and project parts to bob stats | [bob-cli-9k.2](bob-cli-9k.2.md) | 2026-10-18 18:29:50 EDT |
