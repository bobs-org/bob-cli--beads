# Bead: bob-cli-5s.1 — bob-cli exposes Blocked on ref rows

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.5z` · **Assignee:** `bob-cli-5s.1` · **Size:** small
**Created:** 2026-10-08 19:32:40 EDT · **Closed:** 2026-10-08 20:16:59 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

cli-blocked: add an always-present `blocked` boolean to `bob ref list/show/find` rows (true when the note's single ^ref tracker is Blocked [?]), document it in docs/ref.md as an overlay on the reading lane, and test it.

## Notes

[2026-10-09T00:16:45Z · bob-cli-5s.1] PROPOSED FOLLOW-UP: `just check` lib suite has 9 pre-existing failures in native::highlights_ref::return_links::tests (filter_* link-tagging tests); they fail identically on the clean base tree with this phase stashed, so they are unrelated to the blocked boolean change

[2026-10-09T00:16:51Z · bob-cli-5s.1] PROPOSED FOLLOW-UP: epic plan decision refs_decision_memory=no skipped the decision record extending the thin-client rule to Bob Refs (opening never mutates the vault); file it as a memory task bead at land time

[2026-10-09T00:16:59Z · bob-cli-5s.1] Added always-present blocked boolean to bob ref list/show/find rows (true only for a single [?] tracker); documented as reading-lane overlay in docs/ref.md. Verified: 61 ref_library lib tests, 73 ref_library CLI tests incl. 3 new blocked tests pass; live list/show/find JSON carry boolean blocked with schema_version 1; cargo fmt+clippy clean; full integration suite green. 9 return_links lib failures reproduce identically on clean base (recorded as follow-up).

## Dependencies

- **Blocks:** [bob-cli-5s.3](bob-cli-5s.3.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.9](bob-cli-5s.9.md) ✓ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.1/README.md) | [bob-cli-5s.1](bob-cli-5s.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4c9cdbe`](https://github.com/bobs-org/bob-cli/commit/4c9cdbe583770f6fa487be18af6615f259e3bf01) | feat(refs): expose Blocked as always-present boolean on ref rows | [bob-cli-5s.1](bob-cli-5s.1.md) | 2026-10-08 20:18:06 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.1/README.md

<!-- sase:referenced-by:end -->
