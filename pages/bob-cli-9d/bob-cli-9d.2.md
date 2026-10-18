# Bead: bob-cli-9d.2 — RefsCore: Newest ordering, date groups, captions, refs-rank

[Bead Pages](../README.md) / [bob-cli-9d](README.md) / bob-cli-9d.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11j.md) · **Assignee:** `bob-cli-9d.2` · **Size:** medium
**Created:** 2026-10-18 15:40:20 EDT · **Closed:** 2026-10-18 15:57:44 EDT
**Plan:** [202610/refs\_newest\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_newest_mode.md)

## Description

refs-core-newest: decode `added_at`, keep git instants in the snapshot, and add the pure Newest listing (date groups, sort keys, captions, why-here, section jumps) plus `refs-rank --newest`.

## Notes

[2026-10-18T19:57:34Z · bob-cli-9d.2] PROPOSED FOLLOW-UP: RefsLibrary refresh must carry git_added_at forward — RefsLibrary.swift (~line 568) rebuilds the snapshot with `next.gitAddedDates = (snapshot?.gitAddedDates ?? [:]).filter{...}` and never copies `gitAddedAt`, so every plain refresh drops git instants and (because pathsNeedingGitDates now lists git-dated rows without an instant) re-triggers the -g lane; bob-cli-9d.3 must carry gitAddedAt through that filter in addition to switching runGitDatePass to RefsSnapshot.mergingGitDates.

[2026-10-18T19:57:44Z · bob-cli-9d.2] RefsCore Newest landed in bob-mac-capture: RefRecord.addedAt (decodeIfPresent), RefItem.addedAt parsed once in RefItem.make, RefsSnapshot.gitAddedAt/git_added_at (decode-if-present), pathsNeedingGitDates refill, pure RefsSnapshot.mergingGitDates; RefsListOrder + RefsListing.order, RefsSectionKind.added(RefsAddedGroup), RefsRanker.listing(order:), RefsNewest.swift timeline/groups, Newest captions/why-here/shortTime, moveSection in Newest, refs-rank --newest, README Data/Sorting/Tuning. Verified: just portable-check green (1368 tests, 0 failures, incl. 39 new RefsNewestTests); Mac scratch copy bundle.sh + just typecheck-tests PASS (scratch deleted); time formatting identical on Mac and Linux; live bob -g piped into refs-rank --newest works (installed bob predates bob-added-at so UNDATED still has 3 rows and no added_at). Decisions honored: newest_persistence=reset (panel phase), no decisions record edited. Follow-up recorded for bob-cli-9d.3: carry gitAddedAt through RefsLibrary refresh.

## Dependencies

- **Blocks:** [bob-cli-9d.3](bob-cli-9d.3.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9d.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9d.2/README.md) | [bob-cli-9d.2](bob-cli-9d.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@5a0bff5`](https://github.com/bobs-org/bob-mac-capture/commit/5a0bff53388edce1c3f12908bfd7f1f9565b6ea3) | feat(refs): add Newest ordering, date groups, and refs-rank --newest | [bob-cli-9d.2](bob-cli-9d.2.md) | 2026-10-18 15:58:15 EDT |
