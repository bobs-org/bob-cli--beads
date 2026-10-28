# Bead: bob-cli-dd.3 — Preserve every byte outside renamed theme spans

[Bead Pages](../README.md) / [bob-cli-dd](README.md) / bob-cli-dd.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-da.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.land.md) · **Assignee:** `bob-cli-dd.3` · **Size:** small
**Created:** 2026-10-27 18:53:11 EDT · **Closed:** 2026-10-27 19:11:05 EDT
**Plan:** [202610/backlog\_batch\_b3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b3.md)

## Description

theme-rename-bytes: resolve bob-cli-dc in bob-cli by preserving CRLF, mixed terminators, trailing spaces, and missing final newline in global theme rename; verify exact unchanged bytes and retain transaction/journal semantics.

## Notes

[2026-10-27T23:10:57Z · bob-cli-dd.3] PROPOSED FOLLOW-UP: catalog protocol-1 entry count drifted to 55 vs pinned 54 — tests/cli/catalog.rs protocol_1_parses_with_schema_version_one fails identically on the clean base tree (git stash verified), unrelated to the rename byte-preservation change; needs its own triage bead

[2026-10-27T23:11:05Z · bob-cli-dd.3] theme-rename-bytes done: rewrite_file_contents now splices NAME tails on raw lines preserving CRLF/mixed/LF terminators, trailing spaces, and missing final newline (concat, never lines()/join); verify_renamed adds raw-byte checks rejecting collateral rewrites plus the existing prefix check; 5 new lib tests (CRLF, mixed/blank/trailing-space, no-final-newline, heading/child/multi-entry, verify-rejects-malformed) and 1 new CLI offline CRLF test (core.autocrlf=false, exact committed bytes, one commit, journal event). Verified: lib rename 11/11, cli themes_rename 11/11, cli themes_split 7/7, cargo fmt clean, just check green except pre-existing catalog protocol count 55-vs-54 which fails identically on the clean base tree (recorded as PROPOSED FOLLOW-UP). No vault rename performed; no db split or journal semantics changed. epic-symbols empty.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dd.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dd.3/README.md) | [bob-cli-dd.3](bob-cli-dd.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dd.3][1] | Need phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dd.3/README.md

<!-- sase:referenced-by:end -->
