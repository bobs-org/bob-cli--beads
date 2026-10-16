# Bead: bob-cli-8b.1 — Template shelf store and auto-save in bob capture

[Bead Pages](../README.md) / [bob-cli-8b](README.md) / bob-cli-8b.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1n.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1n.linker.w0.md) · **Assignee:** `bob-cli-8b.1` · **Size:** medium
**Created:** 2026-10-16 08:18:36 EDT · **Closed:** 2026-10-16 08:47:28 EDT
**Plan:** [202610/saved\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/saved_capture_templates.md)

## Description

store: add the bob-owned template shelf (canonical block text, content-hash ids, locked atomic JSON at $XDG_STATE_HOME/bob-cli/capture/templates.json), save after every successful real template capture, the hidden --template-origin replace, the capture.max_saved_templates config key, additive JSON and human output, the A10 missing-rows wording, and docs.

## Notes

[2026-10-16T12:47:28Z · bob-cli-8b.1] Store phase done: shelf store with canonical text, hash ids, locked atomic JSON, origin replace, cap trim, quarantine, newer-schema guard; capture.max_saved_templates (0-36, default 36); post-commit auto-save with hidden --template-origin, saved/not_saved JSON, human segment, stderr warning; A10 missing-rows wording; docs in capture.md and README; just check green (fmt, clippy -D unused, 2656 lib + 1650 cli tests pass, incl. new store unit and shelf CLI tests)

## Dependencies

- **Blocks:** [bob-cli-8b.2](bob-cli-8b.2.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8b.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8b.1/README.md) | [bob-cli-8b.1](bob-cli-8b.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c1b1cef`](https://github.com/bobs-org/bob-cli/commit/c1b1cef9f2749c8a94b0290c4d728fc1797e7e4e) | feat(capture): add bob-owned template shelf with auto-save | [bob-cli-8b.1](bob-cli-8b.1.md) | 2026-10-16 08:48:55 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8b.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8b.1/README.md

<!-- sase:referenced-by:end -->
