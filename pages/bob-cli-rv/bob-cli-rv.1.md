# Bead: bob-cli-rv.1 — bob-cli readers, recall, and snapshot accept stamps

[Bead Pages](../README.md) / [bob-cli-rv](README.md) / bob-cli-rv.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ho](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ho.md) · **Assignee:** `bob-cli-rv.1` · **Size:** medium
**Created:** 2026-11-28 08:22:27 EST · **Closed:** 2026-11-28 09:03:36 EST
**Plan:** [202611/task\_log\_datetime\_stamps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_log_datetime_stamps.md)

## Description

cli-readers: add the shared Rust stamp formatter and parser. Teach `bob logs` (parse, score, precision, cache) and the highlights note snapshot to read stamped entries in every log. Publish the canonical reader grammar, and mark the JSON change with `!`.

## Notes

[2026-11-28T14:03:36Z · bob-cli-rv.1--1] Verified focused log-history and snapshot tests, docs-check, and just check.

## Dependencies

- **Blocks:** [bob-cli-rv.3](bob-cli-rv.3.md) ✓ · ⧖ 2026-11-28
- **Blocks:** [bob-cli-rv.4](bob-cli-rv.4.md) ◐ · ⧖ 2026-11-28
- **Blocks:** [bob-cli-rv.5](bob-cli-rv.5.md) ◐ · ⧖ 2026-11-28
- **Blocks:** [bob-cli-rv.8](bob-cli-rv.8.md) ✓ · ⧖ 2026-11-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rv.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rv.1.md) | [bob-cli-rv.1](bob-cli-rv.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`08165ed`](https://github.com/bobs-org/bob-cli/commit/08165ed9cafa838a079eb5ca18acead319f9fcc8) | feat(logs)!: accept stamped task-log readers | [bob-cli-rv.1](bob-cli-rv.1.md) | 2026-11-28 08:51:29 EST |
