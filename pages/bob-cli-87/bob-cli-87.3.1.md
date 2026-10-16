# Bead: bob-cli-87.3.1 — Bob area and project snapshot projection

[Bead Pages](../README.md) / [bob-cli-87.3](bob-cli-87.3.md) / bob-cli-87.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.3.md) · **Assignee:** `bob-cli-87.3.1.land`
**Created:** 2026-10-16 11:43:18 EDT · **Closed:** 2026-10-16 14:27:33 EDT
**Plan:** [202610/snapshot\_bob\_layer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_bob_layer.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/snapshot_bob_layer.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:d0d45785d14fd9cc8f6cbfc1 | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_bob_layer.md

<!-- sase:links:end -->

## Description

Area and project snapshots show a source-aware masthead, readable task rows and history, accurate omission counts, and an optional linked closed-task appendix.

## Notes

[2026-10-16T18:00:23Z · bob-cli-87.3.1.land] LAND AUDIT at 6c53e13: Read this epic, every child and every note, both linked plans, DECISIONS, source, and implementation commits 57c3df2/87bc784/6c53e13. All three phases are closed but seven synthetic probes expose remaining epic work: inline embeds bypass Bob policy and counts; relationship-row children receive duplicate chips; comment-hidden fields leak into chips; promoted canceled ^prj loses CANCEL LOG even with include_closed; preamble closed rows sort after body rows; nested self-snapshot descendants under closed ancestors count as closed instead of self; parent H1 wikilinks leak raw syntax. Exact probes and failures: file:explicit:d0d45785d14fd9cc8f6cbfc1. Existing 128 snapshot/profile tests pass; 54 every_ coverage tests pass; cargo fmt --check and git diff --check pass after removing temporary probes. No production edits retained. Follow-up triage via sase_new_task: sole proposal bob-cli-87.3.1.1 note 1 is resolved by f2ced0c (both capture-template registry tests pass), so declined a new task or reopening; searched tasks, swept recent tasks, reviewed active epic scopes and owning bob-cli-8b. Integration review: fetched origin/master equals 6c53e13; non-epic 8e96375, f2ced0c, a3e45a3, 280321a, ff97c62, 0e59ed0 are present. Article shared helpers already integrated; no other downstream caller needs this projection yet. No epic-symbol entries; current justfile has no symvision. Proposing one medium repair tale; its final step must run just check, close this epic normally, mark plan:202610/snapshot_bob_layer.md done, and close only parent phase bob-cli-87.3. No force and no own-commit dependency. Outer epic bob-cli-87 remains its land agent responsibility.

[2026-10-16T18:27:33Z · bob-cli-87.3.1.land] Landing repairs complete: all 7 probes now pass. Inline embeds apply Bob chips/visibility/counts with distinct anchors, prose intact, both modes, ordinary control kept. Relationship nested tasks transform once (priority/scheduled/repeat single chips). Comment-hidden fields (percent/HTML/multiline/ref/code) use effective spelling, no resurrection. Canceled/completed ^prj outcomes preserve status/date chips and full history in Outcome history without falsification. Appendix restores preamble/body/embedded order with no duplicates. Self vs closed omissions use provenance precedence with no overlap, bytes unchanged. Parent H1 uses syntax title-candidate (linked/emphasized/commented/fenced/alias). Verified: 135 note_snapshot tests, 54 every_ tests, just check green. Follow-up bob-cli-87.3.1.1 note 1 resolved by f2ced0c, no new task.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.3.1.land.md) | [bob-cli-87.3.1](bob-cli-87.3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`16c4640`](https://github.com/bobs-org/bob-cli/commit/16c4640a6135e193de504b83532b12ad1a933d00) | fix(snapshot): finish Bob projection landing repairs | [bob-cli-87.3.1](bob-cli-87.3.1.md) | 2026-10-16 14:29:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.3.1.1][1] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-87.3.1.2][2] | Need parent epic DECISIONS and remaining work notes | 1 |
| read-by | [agent:bob-cli-87.3.1.3--2][3] | Verify the enclosing epic remains untouched after closing the assigned phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.3.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.3.1.3.md

<!-- sase:referenced-by:end -->
