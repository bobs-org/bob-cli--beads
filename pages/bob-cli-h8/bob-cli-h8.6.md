# Bead: bob-cli-h8.6 — Make the highlights overwrite tests timezone-independent

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.6` · **Size:** small
**Created:** 2026-11-04 16:39:09 EST · **Closed:** 2026-11-04 17:11:43 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

highlights-tz-tests: the two highlights::overwrite_local failures (bob-cli-h6) assert a hardcoded -0400 offset, while CI stamps in UTC. Pin the zone for those bob subprocesses, sweep sibling assertions, and confirm the overwrite-refreshes-captured rule in docs. Then close h6 and the no-longer-reproducing bob-cli-fh.

## Notes

[2026-11-04T22:11:29Z · bob-cli-h8.6] PROPOSED FOLLOW-UP: Fix the eight clean-base Clippy errors in the h2-owned past-Pomodoro code — reproduced identically by just lint on this phase tree and detached base; already tracked on bob-cli-h2 note #3, so the h2 lander should carry it forward.

[2026-11-04T22:11:43Z · bob-cli-h8.6] Pinned reread and overwrite subprocess TZ to UTC, updated both captured assertions, and documented that overwrite refreshes captured. All 36 overwrite_local tests pass under UTC and America/New_York; just docs-check passes (447 passed, one skipped). just check reaches Clippy but fails on eight h2-owned errors reproduced identically on detached clean base; recorded proposed follow-up citing bob-cli-h2 note #3. epic-symbols reports none.

## Dependencies

- **Blocks:** [bob-cli-h8.11](bob-cli-h8.11.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.6/README.md) | [bob-cli-h8.6](bob-cli-h8.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`53bf947`](https://github.com/bobs-org/bob-cli/commit/53bf94721d638a02106ff7a142b216a4b80e2b7f) | test(highlights): pin overwrite timezone and document recapture stamp | [bob-cli-h8.6](bob-cli-h8.6.md) | 2026-11-04 17:12:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h8.11][1] | Check whether this clean-base Clippy failure already has a tracked follow-up | 1 |
| read-by | [agent:bob-cli-h8.6][2] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.11/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.6/README.md

<!-- sase:referenced-by:end -->
