# Bead: bob-cli-ey.1.1.4 — A bare edge

[Bead Pages](../README.md) / [bob-cli-ey.1.1](bob-cli-ey.1.1.md) / bob-cli-ey.1.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Assignee:** `bob-cli-ey.1.1.4` · **Size:** small
**Created:** 2026-10-31 12:58:15 EDT · **Closed:** 2026-10-31 20:49:11 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

## Description

bare-hash-type-marker: a free-standing bare `#` at an item edge becomes an incomplete `task_type` marker (span on the `#`, need `task_type` mode `incomplete`, execution refuses with copy that teaches `#fix` and `\#`); delete the "bare hash stays the Pomodoro note" branch in `type_marker.rs` and the bare `#` in `is_trailing_transparent`; leave `#`+digit, `##…`, `#-…`, mid-line, and glued `#` unchanged. Commit as `feat(capture)!:`.

## Notes

[2026-11-01T00:49:11Z · bob-cli-ey.1.1.4--2] Bare edge # is an incomplete task_type marker (span on #, need task_type, mode incomplete) with teaching copy for #fix and \#. Deleted the Pomodoro-note branch in type_marker.rs and bare # from is_trailing_transparent. Digit, ##, #-, mid-line, and glued hashes stay prose. just check (monitor 0vkfp5pj5g96, exit 0) and just docs-check passed; no leftover epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-ey.1.1.3](bob-cli-ey.1.1.3.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.1.1.6](bob-cli-ey.1.1.6.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.4.md) | [bob-cli-ey.1.1.4](bob-cli-ey.1.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d7f683a`](https://github.com/bobs-org/bob-cli/commit/d7f683a1e59da7391384d5d46559ba09d056d3dd) | feat(capture)!: treat a bare edge # as an incomplete type marker | [bob-cli-ey.1.1.4](bob-cli-ey.1.1.4.md) | 2026-10-31 20:50:29 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.1.1.4--2][1] | Need notes, remaining work, and epic DECISIONS | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.4.md

<!-- sase:referenced-by:end -->
