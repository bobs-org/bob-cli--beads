# Bead: bob-cli-a0.5.1 — Launch Bob documentation with gated hourly GitHub Pages publishing

[Bead Pages](../README.md) / [bob-cli-a0.5](bob-cli-a0.5.md) / bob-cli-a0.5.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.land`
**Created:** 2026-10-19 23:18:30 EDT
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

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.land/README.md) | [bob-cli-a0.5.1](bob-cli-a0.5.1.md) | 0 |

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
