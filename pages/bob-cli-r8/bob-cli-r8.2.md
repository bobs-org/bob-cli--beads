# Bead: bob-cli-r8.2 — Deploy guard runs the inclusion proof in both stamp arms

[Bead Pages](../README.md) / [bob-cli-r8](README.md) / bob-cli-r8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.land.md) · **Assignee:** `bob-cli-r8.2` · **Size:** medium
**Created:** 2026-11-27 13:01:15 EST · **Closed:** 2026-11-27 13:41:40 EST
**Plan:** [202611/task\_bead\_burndown\_2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_2.md)

## Description

deploy-inclusion-proof: make evaluate_guard in src/native/plugins/deploy.rs try find_inclusion_proof for clean stamps with an unknown source_head, and stop a dirty incoming checkout from getting a false "no single commit holds the bundle" refusal, then close bob-cli-or and bob-cli-pb.

## Notes

[2026-11-27T18:41:40Z · bob-cli-r8.2] deploy-inclusion-proof done. evaluate_guard: clean-stamp arm tries find_inclusion_proof when ancestor_of is not Yes and incoming is clean (permits with proving_commit); dirty-stamp arm runs the proof regardless of incoming cleanliness (permits with proving_commit; refusal kept when no proving commit exists). Chose permit-over-reword for pb: proof is about vault bytes having landed, so overwriting cannot erase unlanded work even from a dirty checkout. Docs/help updated in same change (cli.rs long helps, docs/plugins.md guard bullets + recovery para, bob-plugins docs/develop/deployment.md, CLI reference via just docs-gen). Tests: 4 new unit tests in src/native/plugins/tests.rs + 1 new CLI test (clean unknown head via rewritten stamp); cargo test --lib -- native::plugins 65/65, --test cli plugins:: 36/36, docs_reference ok, just docs-check 449 passed, live dry-run from linked bob-plugins checkout exit 0 no refusals. just-check stays red only on pre-existing HEAD failures in untouched prose files (clippy + lib kinds + cli root_help), owned by epic bob-cli-qj.5.1; full lib otherwise 8278 passed. Closed bob-cli-or and bob-cli-pb with verification notes.

## Dependencies

- **Depends on:** [bob-cli-r8.1](bob-cli-r8.1.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-r8.3](bob-cli-r8.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.2/README.md) | [bob-cli-r8.2](bob-cli-r8.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dbdc7d2`](https://github.com/bobs-org/bob-cli/commit/dbdc7d24b28b2e72b2a3119155800738d4ad16ec) | feat(plugins): run deploy inclusion proof in both stamp arms | [bob-cli-r8.2](bob-cli-r8.2.md) | 2026-11-27 13:42:45 EST |
| bob-plugins | [`bob-plugins@ce4cb69`](https://github.com/bobs-org/bob-plugins/commit/ce4cb692999ad7db70015af5baaa11e85a079da6) | docs(deployment): sync guard rule covers clean stamps and dirty incoming | [bob-cli-r8.2](bob-cli-r8.2.md) | 2026-11-27 13:43:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-r8.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.2/README.md

<!-- sase:referenced-by:end -->
