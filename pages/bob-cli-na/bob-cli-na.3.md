# Bead: bob-cli-na.3 — Records show/check/tidy learn the walk line

[Bead Pages](../README.md) / [bob-cli-na](README.md) / bob-cli-na.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5b.linker.w0.md) · **Assignee:** `bob-cli-na.3` · **Size:** small
**Created:** 2026-11-18 11:07:19 EST · **Closed:** 2026-11-18 12:53:19 EST
**Plan:** [202611/record\_walk\_ring.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_walk_ring.md)

## Description

walk-records: add record.walk to records show (JSON + human card), record_walk_* findings to records check, teach tidy's probes to see past the walk line, and pin Notes-insertion goldens with a walk line present.

## Notes

[2026-11-18T17:52:58Z · bob-cli-na.3] PROPOSED FOLLOW-UP: just docs-check fails on clean base too (bob-plugins reference/plugins mount collides with committed landing page in ephemeral workspace without the linked sidecar); needs land-agent or workspace fix, not a walk-records change

[2026-11-18T17:53:19Z · bob-cli-na.3] walk-records done: record.walk in show JSON+human card (N of M, 1 of 1, held=null, muted hint when not current), record_walk_damaged per record + record_walk_stale per album warnings in check (exit codes unchanged), tidy H1 probe skips walk/nav lines with CRLF/BOM goldens, update Notes goldens pin walk-first insertion with no walk edits staged; docs/records.md + json-outputs updated; glossary Record Note already carries the walk sentence (na.1). Verified: cargo test --workspace all green (lib 7372, cli 3793 incl. 3 new walk tests + 3 notes_section unit tests), just check fmt+clippy gates pass (fixed 4 mechanical clippy lints in walk.rs incl. 1 pre-existing useless_format; 1-line rustfmt normalization in untouched albums_create.rs kept), docs-check fails identically on clean base (recorded as PROPOSED FOLLOW-UP)

## Dependencies

- **Depends on:** [bob-cli-na.1](bob-cli-na.1.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-na.8](bob-cli-na.8.md) ✓ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-na.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-na.3/README.md) | [bob-cli-na.3](bob-cli-na.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3b5490c`](https://github.com/bobs-org/bob-cli/commit/3b5490c1ad415f61b710f3fe4eea500378c1210d) | feat(records): show, check, and tidy learn the record walk line | [bob-cli-na.3](bob-cli-na.3.md) | 2026-11-18 13:45:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-na.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-na.3/README.md

<!-- sase:referenced-by:end -->
