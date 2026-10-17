# Bead: bob-cli-87.13 — Finish note snapshots so real area and project notes match the spec

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.13

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.land.md) · **Assignee:** `bob-cli-87.13.land`
**Created:** 2026-10-17 10:11:18 EDT
**Plan:** [202610/note\_snapshot\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshot_landing_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/note_snapshot_landing_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshot_landing_repairs.md

<!-- sase:links:end -->

## Description

Every `bob ref create <area or project note>` snapshot matches the bob-cli-87 visual spec and content policy on the real vault: status glyphs sit on the first line of their task text, no stale status-chip row or raw `^block-id` labels appear, links to existing vault files resolve, images are framed, earlier-snapshot hints follow the plan, and the docs record what was verified on athena and the Mac.

## Notes

[2026-10-17T22:00:05Z · bob-cli-8w.land] DISCOVERED ISSUE (from bob-cli-8w.land, triaging bob-cli-8w.1 PROPOSED FOLLOW-UP #1/#2): cargo test --lib pandoc_maps_every_contract_construct_to_tex fails on bob-cli master 30bdfb89 — panic 'lifted link' at src/native/highlights_ref/note_snapshot/profile.rs:946 (the expected \hyperref[t-next]{visible link\BobTag{ᵇ}} is missing from the emitted TeX). bob-cli-87.land note #5 recorded this test passing at 5af6521; the only note_snapshot commits since are 9ef336cc (bob-cli-87.13.1) and 2ae12515 (bob-cli-87.13.2, hang-indent task rows), so this child epic's work most likely changed the emitted TeX and the expectation or projection now needs repair. Impact: just check fails for every agent at the lib-test step. Not caused by bob-cli-8w; no new task filed because it belongs to this active epic.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.13.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.13.land/README.md) | [bob-cli-87.13](bob-cli-87.13.md) | 0 |
