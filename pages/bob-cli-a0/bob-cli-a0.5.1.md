# Bead: bob-cli-a0.5.1 — Launch Bob documentation with gated hourly GitHub Pages publishing

[Bead Pages](../README.md) / [bob-cli-a0.5](bob-cli-a0.5.md) / bob-cli-a0.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.land`
**Created:** 2026-10-19 23:18:30 EDT · **Closed:** 2026-10-20 10:12:57 EDT
**Plan:** [202610/docs\_gated\_publication.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/docs_gated_publication.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md

<!-- sase:links:end -->

## Description

Complete the publish scope of bob-cli-a0.5: ship reusable publication and weekly workflows, bootstrap bobs-org/bobs-org.github.io, verify the live site, and demonstrate a broken-link drill followed by recovery without replacing the last good site. Record the run evidence for the assigned phase's land agent.

## Notes

[2026-10-20T05:20:59Z · bob-cli-a0.10.1.land] DISCOVERED ISSUE: (found by bob-cli-a0.10.1 land agent at bob-cli dadf0734) Every steps-bearing job in .github/workflows/docs-publish.yml (publish, deploy, record, verify, report) and .github/workflows/docs-weekly.yml (weekly, report) has no runs-on key (grep -c runs-on = 0 in both files). GitHub Actions rejects a called reusable workflow whose step jobs omit runs-on (Required property is missing: runs-on), so the first live publish/weekly run in bob-cli-a0.5.1.5 should fail at workflow validation. test_publish_workflow.py / test_weekly_workflow.py do not assert runs-on. Fix: add runs-on: ubuntu-latest (or the chosen runner) to each job and a test that every job with steps declares runs-on. Related: the bob-cli-a0.10.1 tale adds an actions/setup-node@v7 step before the publish job's production gate because bob-docs check --production now runs bob-plugins' Node inventory generator.

[2026-10-20T13:46:48Z · bob-cli-a0.5.1.land] LAND TRIAGE (bob-cli-a0.5.1.land, 2026-10-20). (1) Epic note #1, runs-on missing: RESOLVED by 110624b8. All five docs-publish jobs and both docs-weekly jobs declare ubuntu-latest, and test_every_job_declares_ubuntu_latest asserts it. (2) PROPOSED FOLLOW-UP from bob-cli-a0.5.1.5 notes #9 and #11, the Adobe HTTP 403 in docs/assets/fonts/OFL.txt that keeps weekly issue #2 open: routed through /sase_new_task. There is no duplicate task, and the causal home is the active parent epic, so it was recorded as a DISCOVERED ISSUE note on bob-cli-a0 for the a0.13 final sweep. It is not epic work, because the plan explicitly allows a clean-base external failure as a follow-up. (3) New land finding: the hourly schedule has fired only once (39405915133) since 05:03Z, and no 11:17, 12:17, or 13:17 runs exist. Routed through /sase_new_task to a DISCOVERED ISSUE note on bob-cli-a0. It looks like GitHub's best-effort scheduling, not a defect in bob-docs; the workflows are active and dispatch works. (4) DECLINED: the risk that pinned rollbacks run current master tooling rather than the pinned tools/docs. The plan requires 'compatible current orchestration' and clear rejection of unsupported rollbacks, so this is by design. (5) Epic-caused defects found in source review are remaining epic work, planned as a closeout tale: the documented rollback (edit SHAs plus hold, then --pinned) always fails the pinned fingerprint check; a run queued behind another pages run records on its stale trigger SHA, so its manifest push is rejected after deploy; host-bootstrap --deploy-dir commits the whole index rather than only the maintained files; the live /urls.txt precheck in publish-verify has no retry; both runbooks wrongly say a record failure keeps the previous site live, and the inactivity rule is worded as 'without a run'; the recovery issue count ignores the title; the publish-verify --expected help is stale; and there is dead code.

[2026-10-20T14:12:57Z · bob-cli-a0.5.1.land] Closeout of gated hourly GitHub Pages publishing. All five phases verified against source and commits d18b45de, 9ea12d2d, d5c318a9, dadf0734, 110624b8, 8783d498, 1b1758fd, d51c160e, 2f9ad5bd.

Live evidence: first publish 39422837056 with manifest 5910ffb; no-op 39423369898; drill 39423449416; recovery 39423607269 closing issue #1 with manifest 38773b6 and unchanged fingerprint 902aeea93583d0100052049ee1ccc04632034f7049b36fa9b5898a7b42817d7a; weekly 39427654125 with Material passing and issue #2 open on the Adobe HTTP 403.

Live /build.json provenance: bob-cli d51c160e60d200c830b620257944897934a42f89, bob-mac-capture 532c376c7e1844909315732f68b96d68cf72207d, bob-plugins ff369873dab5b34c853b4201c6816ef1f362d6b8; all dirty flags false.

Host templates match the bob-cli templates (bootstrap preview is a no-op after the README sync).

Closeout tale fixes: documented pinned rollback now restores a recorded published.json whole (hand-edited SHAs still fail the fingerprint check); record checks out the planned deploy SHA and pushes HEAD:refs/heads/<branch> so a queued run records instead of being rejected after deploy; host-bootstrap --deploy-dir commits only maintained paths; live /urls.txt precheck retries like page GETs; runbooks now state post-deploy failure boundaries and that GitHub inactivity is 60 days without repository activity; recovery counts only issues titled "Docs publish blocked"; publish-verify --expected help names the recorded published.json; unused timezone/DRILL_MARKER/_FRAGMENT_PATTERNS/REUSABLE_WORKFLOW/inspect_workflow_state/ensure_managed_label were removed.

Verification: uv run --project tools/docs pytest tools/docs/tests — 440 passed, 1 skipped (fonts); just docs-check — all implemented gates passed; just check — cargo fmt, clippy, and tests passed; git diff --check passed. just symvision is unavailable (no justfile recipe).

Host README sync commit 0e56d5254f7da425282ac5a785e278987bd8cf62 (README.md only; published.json byte-identical at HEAD and HEAD^).

Triage: runs-on resolved by 110624b8; Adobe 403 and hourly schedule routed to bob-cli-a0 as DISCOVERED ISSUE notes; pinned-tooling risk declined as by design.

Scheduled runs: 1 (39405915133 at 2026-10-20T10:09:26Z). None have appeared since 13:43Z on 2026-10-20. sase bead epic-symbols bob-cli-a0.5.1 had no entries.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.1.land.md) | [bob-cli-a0.5.1](bob-cli-a0.5.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`10019f6`](https://github.com/bobs-org/bob-cli/commit/10019f635d6b79ecaff5033c464dc7de0bf1a3ad) | fix(docs): close gated publication with rollback, record CAS, and runbook fixes | [bob-cli-a0.5.1](bob-cli-a0.5.1.md) | 2026-10-20 10:15:36 EDT |
| bob-cli--plans | [`bob-cli--plans@1c1765b`](https://github.com/bobs-org/bob-cli--plans/commit/1c1765bc6e72de7d2df39b90038489bac4f03f07) | chore(docs): mark gated publication epic plan done | [bob-cli-a0.5.1](bob-cli-a0.5.1.md) | 2026-10-20 10:16:50 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:12a][1] | Child epic status for docs launch; diagnosing 404 | 1 |
| read-by | [agent:bob-cli-a0.5.1.1][2] | Need binding decisions and prior phase notes for this implementation | 1 |
| read-by | [agent:bob-cli-a0.5.1.2][3] | need epic plan and decisions | 1 |
| read-by | [agent:bob-cli-a0.5.1.4][4] | Need parent epic scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.12a/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.4/README.md

<!-- sase:referenced-by:end -->
