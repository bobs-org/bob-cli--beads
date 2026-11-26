# Bead: bob-cli-q8.10.2 — Counted absorption, batch ↵ absorption, chord block-ID prompts, and one-undo reversal

[Bead Pages](../README.md) / [bob-cli-q8.10](bob-cli-q8.10.md) / bob-cli-q8.10.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-q8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-q8.land.md) · **Assignee:** `bob-cli-q8.10.2` · **Size:** medium
**Created:** 2026-11-26 02:09:19 EST · **Closed:** 2026-11-26 02:39:48 EST
**Plan:** [202611/finish\_plain\_link\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_plain_link_ties.md)

## Description

nav-tie-writers: counted-session and counted-batch dependency adds absorb plain links. Marked and counted Depends-on/Blocks ↵ on a ⇄ row absorbs instead of refusing. Chord refusals name the pressed chord. Chords on ID-less rows or owners go through the block-ID prompt. A same-note reversal commits in one editor transaction. Audit the 218/665/667 writers.

## Notes

[2026-11-26T07:39:30Z · bob-cli-q8.10.2] Audit 218/665/667: 218 is subtree-only with no dependency writes; 665 conversion and 667 promotion preserve Depends-On onto fresh notes with no LINKS lines, so no new pair can carry a plain link. One-line tie-audit comments left at each writer.

[2026-11-26T07:39:37Z · bob-cli-q8.10.2] Verified: build clean; tie-chords (18), tie-change-writer (12), counted-tie-absorption (5), plain-link-ties all pass (57 total); bob-plugins docs lint+drift pass; bob plugins sync copied 1; cargo ties pass; bob-cli docs urls/links/edit/search pass.

[2026-11-26T07:39:48Z · bob-cli-q8.10.2] Counted session/batch absorb plain links with honest suffix; marked Depends/Blocks absorb via batch writers; chords name pressed chord and refuse with marks/counted; ID-less chords use +id prompt (Esc writes nothing); same-note reversal is one undo, cross-note reports incomplete; 218/665/667 audited; tests 57 pass; build clean; plugins synced.

## Dependencies

- **Blocks:** [bob-cli-q8.10.3](bob-cli-q8.10.3.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.10.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.10.2/README.md) | [bob-cli-q8.10.2](bob-cli-q8.10.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6e722fc`](https://github.com/bobs-org/bob-cli/commit/6e722fc6508f9bed5983917dc67416cfac404a60) | docs(task-dependencies): record tie-chord absorption, tie-change and reversal semantics | [bob-cli-q8.10.2](bob-cli-q8.10.2.md) | 2026-11-26 02:41:27 EST |
| bob-plugins | [`bob-plugins@6fb169b`](https://github.com/bobs-org/bob-plugins/commit/6fb169bb8641603b19ab9cbc98cfefae2fdb3731) | feat(nav-hotkeys): counted and vault tie absorption, tie-change flow, dependency reversal | [bob-cli-q8.10.2](bob-cli-q8.10.2.md) | 2026-11-26 02:42:19 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q8.10.2][1] | Need final scope before closing nav-tie-writers | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.10.2/README.md

<!-- sase:referenced-by:end -->
