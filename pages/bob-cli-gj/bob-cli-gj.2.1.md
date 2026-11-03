# Bead: bob-cli-gj.2.1 — Implement note-pull capture in bob-cli

[Bead Pages](../README.md) / [bob-cli-gj.2](bob-cli-gj.2.md) / bob-cli-gj.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.md) · **Assignee:** `bob-cli-gj.2.1.land`
**Created:** 2026-11-03 12:31:13 EST
**Plan:** [202611/note\_pull\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull_cli.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/note_pull_cli.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull_cli.md

<!-- sase:links:end -->

## Description

Complete bob-cli-gj.2 with atomic explicit note-pull selection, grammar 7, shared pull-in reporting, NP1–NP28 coverage, and real-bob fixtures for the Mac phase.

## Notes

[2026-11-03T20:17:27Z · 17p] DISCOVERED ISSUE: this epic's phases broke the bob-cli build (just install) twice on 2026-11-03. (1) c673d144 (bob-cli-gj.2.1.1) added the required CaptureItemResult.note_pull field but missed the sub-bullet literal that 3b1cf138 (agent 17i) had just added in plan_capture_item, which caused a missing-field compile error. Agent 17l fixed it in 9a606395 by putting note_pull: None first. (2) a95d5d8f (bob-cli-gj.2.1.2) added note_pull: None as the last field of the same literal on a base without 9a606395. The rebase applied cleanly because the hunks are about 80 lines apart, which left E0062 "field note_pull specified more than once". The fix commit drops the trailing copy and keeps the leading one, which matches every other literal. Both phases passed tests on their pre-rebase base, and nothing compiled the rebased tip. Land agent: run cargo check --all-targets --locked on the master tip after each phase lands. bob-cli-gh.8's PROPOSED FOLLOW-UP #1 is the same first breakage, already fixed by 9a606395.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gj.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gj.2.1.land/README.md) | [bob-cli-gj.2.1](bob-cli-gj.2.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.8][1] | Determine whether the existing note-pull phase tracks the clean-base compiler failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.8/README.md

<!-- sase:referenced-by:end -->
