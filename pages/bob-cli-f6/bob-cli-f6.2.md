# Bead: bob-cli-f6.2 — bob-cli: #untracked in Google Calendar and bob gcal sync

[Bead Pages](../README.md) / [bob-cli-f6](README.md) / bob-cli-f6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bv](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bv.md) · **Assignee:** `bob-cli-f6.2` · **Size:** medium
**Created:** 2026-11-01 11:24:13 EST · **Closed:** 2026-11-01 14:03:03 EST
**Plan:** [202611/untracked\_calendar\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/untracked_calendar_events.md)

## Description

gcal-untracked-tag: parse the Google token, render the row tag, split past MEET clusters by trackedness, report it in list/sync.

## Notes

[2026-11-01T19:03:03Z · bob-cli-f6.2] Implemented gcal #untracked: Google token parsing (title anywhere + description line), row tag at end of badge run, past MEET clusters split by trackedness with [t::] omitted for untracked, all-untracked running MEET, list VAULT/JSON + sync JSON reporting, kept_untracked once for worked flips, pre-existing title migration. Verified: new sync test (title/desc/route/clusters/running/list) + 3 lifecycle tests (untouched flip, worked kept-once, migration) pass; full gcal suites pass (sync 30, lifecycle 22, list 6); lib gcal unit 122 pass; cargo fmt clean; just lint gate pass; just docs-check pass (after docs-gen); full workspace cargo test pass with 0 failures.

## Dependencies

- **Depends on:** [bob-cli-f6.1](bob-cli-f6.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f6.6](bob-cli-f6.6.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.2/README.md) | [bob-cli-f6.2](bob-cli-f6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a6671b2`](https://github.com/bobs-org/bob-cli/commit/a6671b249fb2ec50c58f1b8fb6b6a0e1d7402a78) | feat(gcal)!: support #untracked calendar events end to end | [bob-cli-f6.2](bob-cli-f6.2.md) | 2026-11-01 14:04:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f6.2][1] | Need the phase scope and design file | 4 |
| read-by | [agent:research.2z.grk][2] | Need closed phase details for untracked ledger rows and gcal sync to understand current implementation | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f6.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.2z.grk/README.md

<!-- sase:referenced-by:end -->
