# Bead: bob-cli-kd.3 — Read the bank — list, report, ensure, and ack

[Bead Pages](../README.md) / [bob-cli-kd](README.md) / bob-cli-kd.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.3` · **Size:** medium
**Created:** 2026-11-11 11:24:16 EST · **Closed:** 2026-11-11 13:56:53 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

## Description

bank-cli: add the bare `bob bank` waiting queue, `report` with the totals semantics, and two capture-style guarded writes: `ensure` (month note and day heading) and `ack` (tick shown rows). Give each beautiful human output and `schema_version: 1` JSON, with account status stubbed as `unverified`.

## Notes

[2026-11-11T18:56:38Z · bob-cli-kd.3] PROPOSED FOLLOW-UP: pre-existing lib failure native::capture_link_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates (2 warnings vs 1) reproduces identically on clean base; unrelated to bank-cli

[2026-11-11T18:56:42Z · bob-cli-kd.3] PROPOSED FOLLOW-UP: just docs-check fails on 5 pre-existing word-budget overruns in untouched docs/reference/mac-capture/* and docs/reference/plugins/bob-navigation-hotkeys.md (6000-word cap); unrelated to bank-cli docs

[2026-11-11T18:56:53Z · bob-cli-kd.3] bank-cli ships: bare bob bank waiting queue, report with totals semantics, ensure + ack guarded writes, human output + schema_version:1 JSON with unverified/untracked stub. Verified: just lint ok, 31 bank lib tests ok, 3549 CLI integration tests ok, manual end-to-end (ensure/list/report/ack/JSON/teaching-empty/week/year/exits) ok, docs-gen current. One lib failure (capture_link_tasks unreadable-notes) and docs-check budget overruns reproduce on clean base; recorded as PROPOSED FOLLOW-UPs.

## Dependencies

- **Depends on:** [bob-cli-kd.2](bob-cli-kd.2.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.4](bob-cli-kd.4.md) ◐ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.6](bob-cli-kd.6.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.3/README.md) | [bob-cli-kd.3](bob-cli-kd.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`49218b3`](https://github.com/bobs-org/bob-cli/commit/49218b38ebf3372b44274fa94869ad7ccc58311c) | feat(bank): add list, report, ensure, and ack to bob bank | [bob-cli-kd.3](bob-cli-kd.3.md) | 2026-11-11 13:58:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.3/README.md

<!-- sase:referenced-by:end -->
