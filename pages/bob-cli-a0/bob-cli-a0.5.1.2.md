# Bead: bob-cli-a0.5.1.2 — Gated reusable publication and recovery

[Bead Pages](../README.md) / [bob-cli-a0.5.1](bob-cli-a0.5.1.md) / bob-cli-a0.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.2` · **Size:** medium
**Created:** 2026-10-19 23:18:33 EDT · **Closed:** 2026-10-20 00:06:51 EDT
**Plan:** [202610/docs\_gated\_publication.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md)

## Description

publish-workflow: implement the workflow_call-only Pages publisher, staged broken-link drill, publication recording, live verification, and one blocked-issue lifecycle with focused failure-path tests.

## Notes

[2026-10-20T04:06:51Z · bob-cli-a0.5.1.2] Implemented gated reusable publisher: docs-publish.yml (workflow_call-only, force/drill/pinned, pages concurrency, caller+branch guard, plan/gate/deploy/record/verify/report jobs, pinned action tags), bob-docs check --drill with staged-only bogus-fragment probe, publish-record/publish-verify/publish-report subcommands, YAML-aware workflow tests + focused failure-path tests. Verified: 325 passed 2 skipped (docs suite) and just docs-check exit 0 with all gates green. No clean-base failures. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-a0.5.1.1](bob-cli-a0.5.1.1.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.5.1.3](bob-cli-a0.5.1.3.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.2/README.md) | [bob-cli-a0.5.1.2](bob-cli-a0.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9ea12d2`](https://github.com/bobs-org/bob-cli/commit/9ea12d2d90c332d801a96cad4a9c88c009fb3afe) | feat(docs): add reusable docs-publish workflow with record, verify, drill | [bob-cli-a0.5.1.2](bob-cli-a0.5.1.2.md) | 2026-10-20 00:08:06 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.5.1.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.2/README.md

<!-- sase:referenced-by:end -->
