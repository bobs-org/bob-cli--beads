# Bead: bob-cli-hg.12.1.5 — Confirmed send command and sent-note finalization

[Bead Pages](../README.md) / [bob-cli-hg.12.1](bob-cli-hg.12.1.md) / bob-cli-hg.12.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.md) · **Assignee:** `bob-cli-hg.12.1.5` · **Size:** medium
**Created:** 2026-11-06 07:12:29 EST · **Closed:** 2026-11-06 15:26:13 EST
**Plan:** [202611/gmail\_compose.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_compose.md)

## Description

send-finalize: expose confirmed send, integrate recovery and sent-card refresh, promote compose notes in place, and preserve authored edits as in section 4.5.

## Notes

[2026-11-06T20:26:13Z · bob-cli-hg.12.1.5--2] Closed by explicit `sase stitch create -B close` after create_commit landed 57af3ead ("feat(gmail): add confirmed send and note finalization"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-hg.12.1.5` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-hg.12.1.4](bob-cli-hg.12.1.4.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hg.12.1.6](bob-cli-hg.12.1.6.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.12.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.1.5.md) | [bob-cli-hg.12.1.5](bob-cli-hg.12.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`57af3ea`](https://github.com/bobs-org/bob-cli/commit/57af3ead752da458c1dcc8b66c71396e46b2092c) | feat(gmail): add confirmed send and note finalization | [bob-cli-hg.12.1.5](bob-cli-hg.12.1.5.md) | 2026-11-06 15:25:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.5--2][1] | Need current phase scope and notes before finalizing verified work | 1 |
| read-by | [agent:bob-cli-hg.12.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.1.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.land/README.md

<!-- sase:referenced-by:end -->
