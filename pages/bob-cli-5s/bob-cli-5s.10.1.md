# Bead: bob-cli-5s.10.1 — bob-cli blocked-field polish and stray .build cleanup

[Bead Pages](../README.md) / [bob-cli-5s.10](bob-cli-5s.10.md) / bob-cli-5s.10.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.bob-cli-5s.land` · **Assignee:** `bob-cli-5s.10.1` · **Size:** small
**Created:** 2026-10-09 08:04:27 EDT · **Closed:** 2026-10-09 08:36:05 EDT
**Plan:** [202610/bob\_refs\_land\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md)

## Description

cli-blocked-polish: untrack the stray `.build/` files and ignore `/.build/`, serialize `blocked` directly after `reading_state_source`, add a several-trackers-with-one-[?] fixture test, and finish the docs/ref.md contract (client note, additive under schema_version 1).

## Notes

[2026-10-09T12:35:34Z · bob-cli-5s.10.1] PROPOSED FOLLOW-UP: completion CLI tests flake run-to-run (bash/readline/protocol/vault subsets fail with disjoint sets on base and on this phase tree; zero references to ref_library) — consider quarantine or retry for tests/cli/completion

[2026-10-09T12:36:05Z · bob-cli-5s.10.1] Done: untracked .build/ (.buildSystem_debug, CACHEDIR.TAG) and added /.build/ to .gitignore; moved RefRow.blocked directly after reading_state_source (verified list/show/find JSON key order); added two_trackers_blocked.md fixture (two ^ref trackers, one [?]) asserting blocked==false in src/native/ref_library/tests.rs and tests/cli/ref_library/list.rs with count updates (34 rows/33 library, -R all 33, unknown/-s unknown vecs, find 34/33); docs/ref.md gains Refs-panel client note and schema_version-1 additive note plus corrected field list. Verified: git ls-files .build empty; ref_library focused tests 61 lib + 73 cli pass; cargo fmt+clippy clean; full just check passes except 9 known return_links Pandoc failures (task bob-cli-5t, plan-authorized) and flaky completion tests that fail disjointly on base too (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-5s.10.4](bob-cli-5s.10.4.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.10.1/README.md) | [bob-cli-5s.10.1](bob-cli-5s.10.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b566ba4`](https://github.com/bobs-org/bob-cli/commit/b566ba4431b97df6405a75babe9d17899bae7eea) | fix(refs): polish blocked field, drop stray .build, finish ref.md contract | [bob-cli-5s.10.1](bob-cli-5s.10.1.md) | 2026-10-09 08:37:58 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.10.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.1/README.md

<!-- sase:referenced-by:end -->
