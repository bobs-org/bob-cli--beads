# Bead: bob-cli-ep.1 — bob-cli \`#\<type\>\` grammar, refusal, completion, and docs

[Bead Pages](../README.md) / [bob-cli-ep](README.md) / bob-cli-ep.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.be.md) · **Assignee:** `bob-cli-ep.1` · **Size:** large
**Created:** 2026-10-30 15:04:29 EDT · **Closed:** 2026-10-31 09:13:08 EDT
**Plan:** [202610/capture\_hash\_type\_marker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_hash_type_marker.md)

## Description

cli: switch the shared type-marker lexer to `#`, add the attached `@route^id#` and marker-only `@route+id#` forms, refuse unconfigured types, retire `t:` and the legacy `#tag` check, move `task_type` completion to `#`, and update docs, help, fixtures, and tests in one coherent change.

## Notes

[2026-10-30T23:04:02Z · bob-cli-ep.1--i] docs-check, check, and all passed. Apollo debug timings for Fix the parser #f (20 samples after one warmup, nearest-rank p95): capture-complete 41.7 ms (limit 60.6), capture-parse 53.6 ms (limit 49.7, miss +3.9 ms over 44.7+5), zsh protocol 59.9 ms (limit 73.6). Phase kept open because capture-parse exceeds its limit. sase bead epic-symbols bob-cli-ep.1 reported no --epic-symbol entries.

[2026-10-31T13:13:08Z · bob-cli-ep.1--3] Completed attached #<type> forms, refusal hints, completion, and docs. Paired apollo debug benchmark: 200 interleaved rounds; base 00ca6d0c with t:f, HEAD with #f; HEAD-minus-base p50/p95: capture-parse -13.7/-20.4 ms, capture-complete -21.2/-31.9 ms, zsh protocol -21.1/-30.6 ms. Verification: just check, just docs-check, just all all passed; CLI and lexer conformance coverage passed. Stale-doc sweep had no matches; t: sweep contained only intentional prose/retirement examples and unrelated duration/relation/fixture text. sase bead epic-symbols bob-cli-ep.1 reported no entries.

## Dependencies

- **Blocks:** [bob-cli-ep.2](bob-cli-ep.2.md) ◐ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ep.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ep.1.md) | [bob-cli-ep.1](bob-cli-ep.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4a95e5b`](https://github.com/bobs-org/bob-cli/commit/4a95e5b78cba78d2b1c13201ccda8736087b7f4a) | feat(capture)!: replace t: type markers with #\<type\> | [bob-cli-ep.1](bob-cli-ep.1.md) | 2026-10-30 19:05:00 EDT |
| bob-cli | [`d1dd23e`](https://github.com/bobs-org/bob-cli/commit/d1dd23e26711a9d80d9591c9ae6c1fd0eeaa5ec8) | fix(capture): finish attached #\<type\> forms, refusal hints, and docs | [bob-cli-ep.1](bob-cli-ep.1.md) | 2026-10-31 09:13:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ep.1--i][1] | Need current phase status before deciding close vs keep after latency miss | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ep.1.md

<!-- sase:referenced-by:end -->
