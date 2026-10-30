# Bead: bob-cli-ep.1 — bob-cli \`#\<type\>\` grammar, refusal, completion, and docs

[Bead Pages](../README.md) / [bob-cli-ep](README.md) / bob-cli-ep.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.be.md) · **Assignee:** `bob-cli-ep.1` · **Size:** large
**Created:** 2026-10-30 15:04:29 EDT
**Plan:** [202610/capture\_hash\_type\_marker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_hash_type_marker.md)

## Description

cli: switch the shared type-marker lexer to `#`, add the attached `@route^id#` and marker-only `@route+id#` forms, refuse unconfigured types, retire `t:` and the legacy `#tag` check, move `task_type` completion to `#`, and update docs, help, fixtures, and tests in one coherent change.

## Notes

[2026-10-30T23:04:02Z · bob-cli-ep.1--i] docs-check, check, and all passed. Apollo debug timings for Fix the parser #f (20 samples after one warmup, nearest-rank p95): capture-complete 41.7 ms (limit 60.6), capture-parse 53.6 ms (limit 49.7, miss +3.9 ms over 44.7+5), zsh protocol 59.9 ms (limit 73.6). Phase kept open because capture-parse exceeds its limit. sase bead epic-symbols bob-cli-ep.1 reported no --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-ep.2](bob-cli-ep.2.md) ◐ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ep.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ep.1.md) | [bob-cli-ep.1](bob-cli-ep.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4a95e5b`](https://github.com/bobs-org/bob-cli/commit/4a95e5b78cba78d2b1c13201ccda8736087b7f4a) | feat(capture)!: replace t: type markers with #\<type\> | [bob-cli-ep.1](bob-cli-ep.1.md) | 2026-10-30 19:05:00 EDT |
