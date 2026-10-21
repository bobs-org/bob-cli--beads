# Bead: bob-cli-ac.5 — GitHub setup and first rehearsal release

[Bead Pages](../README.md) / [bob-cli-ac](README.md) / bob-cli-ac.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.w1.md) · **Assignee:** `bob-cli-ac.5` · **Size:** small
**Created:** 2026-10-20 18:36:53 EDT · **Closed:** 2026-10-20 23:34:49 EDT
**Plan:** [202610/crates\_io\_release\_train.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/crates_io_release_train.md)

## Description

github: dry-run the train on master, then (per github_apply) create the release environment and rulesets, arm the train, dispatch the first rehearsal release, and verify the same-day guard.

## Notes

[2026-10-21T03:34:28Z · bob-cli-ac.5] GitHub setup (github_apply=yes) and first-rehearsal attempt.

CI on master HEAD 104cee99: green https://github.com/bobs-org/bob-cli/actions/runs/39535709783 (lint 1m2s, package 1m28s, ubuntu 4m42s, macos 8m24s).

Unarmed dry-run dispatch: https://github.com/bobs-org/bob-cli/actions/runs/39536531820 success. RELEASES_PAUSED unset. plan SKIP unarmed, full CI green, preview initial bob-obsidian 0.2.0 with seeded notes (release-plz: already up-to-date, no bump), release/binaries skipped.

release environment created (id 24878621423) with custom branch policy master only; no required reviewers. First PUT with prevent_self_review failed HTTP 422; retried without that field. Branch ruleset 25521281 (~DEFAULT_BRANCH: deletion + non_fast_forward, no bypass). Tag ruleset 25521282 (refs/tags/v*: deletion + update, no bypass). Armed: gh variable set RELEASES_PAUSED --body false.

First real rehearsal dispatch: https://github.com/bobs-org/bob-cli/actions/runs/39537743529 FAILED in plan (exit 1, silent). Root cause: armed path looks up GitHub Releases via `gh release list`, and Actions does not export GITHUB_TOKEN unless passed; unarmed dry-run never reached that lookup.

Fix: pass GH_TOKEN/GITHUB_TOKEN in the plan job; prefer REST Releases API with stdlib urllib, fall back to gh; echo the verdict to stdout. Proven on ci/release/github-guard-token (deleted after): https://github.com/bobs-org/bob-cli/actions/runs/39538031188 success. Armed dry-run verdict: "dry run: no previous GitHub Release found; the next scheduled run would ship." Preview GO, initial 0.2.0, already up-to-date, release/binaries skipped.

PENDING REDISPATCH: after this guard-token fix lands on master, re-run github phase steps 6 and 7 (dispatch the first real rehearsal, then a same-day skip). No tag or Release was created. Train remains armed (RELEASES_PAUSED=false). Environment and both rulesets are in place.

[2026-10-21T03:34:49Z · bob-cli-ac.5] Verified: CI green on master 104cee99 (run 39535709783); unarmed dry-run SKIP+preview v0.2.0 (run 39536531820); release env+master policy, branch ruleset 25521281, tag ruleset 25521282, RELEASES_PAUSED=false; first rehearsal failed unauthenticated gh lookup (run 39537743529); fix proven armed dry-run GO+preview 0.2.0 (run 39538031188); scratch branch deleted; PENDING REDISPATCH for steps 6-7 after this lands. epic-symbols none.

## Dependencies

- **Depends on:** [bob-cli-ac.4](bob-cli-ac.4.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ac.8](bob-cli-ac.8.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ac.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ac.5/README.md) | [bob-cli-ac.5](bob-cli-ac.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ea7f5f0`](https://github.com/bobs-org/bob-cli/commit/ea7f5f0b7aaa371c98dd6d3ea368edb4d583d808) | fix(release): authenticate the train guard's GitHub Release lookup | [bob-cli-ac.5](bob-cli-ac.5.md) | 2026-10-20 23:43:35 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ac.6][1] | Check whether the GitHub phase recorded setup details needed for current maintainer documentation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ac.6/README.md

<!-- sase:referenced-by:end -->
