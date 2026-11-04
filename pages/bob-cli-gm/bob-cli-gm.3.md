# Bead: bob-cli-gm.3 — Completion, rewrite, and @@ absorption inside target runs

[Bead Pages](../README.md) / [bob-cli-gm](README.md) / bob-cli-gm.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.17k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.17k.md) · **Assignee:** `bob-cli-gm.3` · **Size:** medium
**Created:** 2026-11-03 13:55:33 EST · **Closed:** 2026-11-03 21:58:25 EST
**Plan:** [202611/capture\_multi\_target.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_multi_target.md)

## Description

assist: make capture-complete and capture-rewrite treat every member of a target run (and the `@` token extending one) as a marker position, give a run the non-absorbable `@@` notice, and update the editor-command docs and help.

## Notes

[2026-11-04T02:58:10Z · bob-cli-gm.3] PROPOSED FOLLOW-UP: Repair task-split fallout blocking just check — catalog leaf task/split, kinds decisions for task split:owner/match/nth/bullet-ref, 2 help snapshots, and 6 clippy errors in task_move/task_split/articles (untouched by this phase; owned by active bob-cli-go)

[2026-11-04T02:58:15Z · bob-cli-gm.3] PROPOSED FOLLOW-UP: Repair docs-tool memory strand front matter — just docs-check/docs-gen fail at sase/memory/glossary/task-merge.md, already tracked in bob-cli-go.8 notes

[2026-11-04T02:58:25Z · bob-cli-gm.3] Assist done: completion completes any run member plus inner-edge @-fragments (7-row table green), rewrite separator switch accepts tokens that become run members (3 rows green), @ on a run reports the non-absorbable notice instead of silent A6, bullet drawer menu keeps first member's drawers, docs/capture.md and capture-complete help updated with docs-gen run. Verified: lib capture_language 577 pass, CLI capture 1482 pass, fmt clean, own clippy clean, live capture-complete/rewrite tables reproduce. Pre-existing task-split fallout (4 test, 6 lint) and memory-strand docs-check failure recorded as PROPOSED FOLLOW-UPs; epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-gm.1](bob-cli-gm.1.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gm.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.3/README.md) | [bob-cli-gm.3](bob-cli-gm.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d19a8d9`](https://github.com/bobs-org/bob-cli/commit/d19a8d92f9641416d936697445deb19086af851c) | feat(capture): complete and rewrite inside target runs | [bob-cli-gm.3](bob-cli-gm.3.md) | 2026-11-03 21:59:49 EST |
