# Bead: bob-cli-7v.7 — Docs, live verification, and follow-ups

[Bead Pages](../README.md) / [bob-cli-7v](README.md) / bob-cli-7v.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10k.md) · **Assignee:** `bob-cli-7v.7` · **Size:** small
**Created:** 2026-10-15 12:30:28 EDT · **Closed:** 2026-10-15 15:06:41 EDT
**Plan:** [202610/ref\_create\_multi\_url\_collections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_multi_url_collections.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-7y][1] | bob-cli-7v.7's live Squarespace collection verification timed out in the browser with no -H replay fallback |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-7y/README.md

<!-- sase:links:end -->

## Description

docs: document several-URL collections in the create, clip, and ref docs, run a live end-to-end check in a scratch vault on athena, and record follow-ups (plus the optional decisions strand).

## Notes

[2026-10-15T19:06:33Z · bob-cli-7v.7--2] PROPOSED FOLLOW-UP: Retry the live Squarespace two-part collection end-to-end when browser navigation is reliable — the scratch-vault dry run timed out on part 2 and the real capture timed out on part 1 (45 s); curl fetched both URLs, collection --html replay is unsupported, and no files were written.

[2026-10-15T19:06:41Z · bob-cli-7v.7--2] Documented multi-URL collections in highlights-create, highlights-clip, and ref docs. TMPDIR=/tmp just check passed (cargo fmt, clippy, 2597 unit tests, 1603 CLI tests, 27 Dataview parity, 32 task tests, 1 real-vault parity). Live Squarespace verification could not complete: dry run timed out on part 2 and retry timed out on part 1 after 45 s; scratch vault remained unchanged, and the failure plus retry proposal is recorded on this bead. epic-symbols reported no leftovers. Decisions honored: no -O and no memory edit.

## Dependencies

- **Depends on:** [bob-cli-7v.6](bob-cli-7v.6.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7v.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7v.7.md) | [bob-cli-7v.7](bob-cli-7v.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dad02a2`](https://github.com/bobs-org/bob-cli/commit/dad02a2f6e308ca8492759a967e17658d140f6b4) | docs(ref): document multi-url collections | [bob-cli-7v.7](bob-cli-7v.7.md) | 2026-10-15 15:07:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7v.7--2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7v.7.md

<!-- sase:referenced-by:end -->
