# Bead: bob-cli-o6.6.1.5 — Run final gates and deploy the verified merged tree

[Bead Pages](../README.md) / [bob-cli-o6.6.1](bob-cli-o6.6.1.md) / bob-cli-o6.6.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-o6.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.6.md) · **Assignee:** `bob-cli-o6.6.1.5` · **Size:** medium
**Created:** 2026-11-21 08:22:48 EST · **Closed:** 2026-11-21 14:07:04 EST
**Plan:** [202611/title\_block\_final\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/title_block_final_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:282423e57c9f033d6cf61ecc | attached via sase artifact create --bead |
| related | file:explicit:30a9b2aff9440b2256cfa96b | attached via sase artifact create --bead |
| related | file:explicit:6a34814f8b6f320845a11587 | attached via sase artifact create --bead |
| related | file:explicit:8964d8d2784e5b0f83457683 | attached via sase artifact create --bead |
| related | file:explicit:e17222ffc1c7fb003e5b3d6a | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

final-gates-deploy: integrate the completed phases, repair the epic-caused vault-format word-budget regression if still present, run both repositories' required gates and the final combined proof, deploy through bob plugins sync, and run deployed-vault smoke with matching managed-file hashes. Attach the final evidence manifest for the child land agent; close only this worker's own phase.

## Notes

[2026-11-21T19:06:01Z · bob-cli-o6.6.1.5] PROPOSED FOLLOW-UP: Restore docs lint headroom in bob-navigation-hotkeys.md — reference/plugins/bob-navigation-hotkeys.md is 6247 > 6000 lint words (error), which turns both `npm run docs:check` (bob-plugins) and `just docs-check` (bob-cli) red at lint. Introduced by bob-plugins 79fe2e1 (proseField LINK band; page 8631 -> 8918 wc words); fails identically on clean bob-cli baca8701 + bob-plugins c4953d3. Related: bob-cli-ob (headroom task, which states the page was 5995 when filed). Evidence: file:explicit:282423e57c9f033d6cf61ecc (bobcli-docs-check-pre.log, final-*-docs-check.log).

[2026-11-21T19:06:05Z · bob-cli-o6.6.1.5] PROPOSED FOLLOW-UP: Update bob-docs contract tests for the task-requirements contract — tools/docs/tests/test_contracts.py has 3 failures (registry 55 vs expected 54; llms.txt contracts list; README table snapshot sha). Introduced by bob-cli a0961435 (task-reqs contract, likely epic bob-cli-on) without a test update; reproduced on clean base 250c3053 with this phase docs stashed. Hidden today because docs-check stops at the nav-hotkeys lint error. Every other post-lint docs gate passes on the final tree. Evidence: file:explicit:282423e57c9f033d6cf61ecc (bobcli-docs-postlint.log).

[2026-11-21T19:06:10Z · bob-cli-o6.6.1.5] PROPOSED FOLLOW-UP: Plugin deploy guard should try the inclusion proof for clean stamps whose source_head is unknown — block-id-prompt (vault 1.39.0) and task-status-cycler (vault 1.52.0) are stuck behind a clean stamp for unpushed 726f9a5 (bob-cli_13, 13:11Z). Their exact bundles are in ancestor commits 3956368 / 6e0d764, and master has 1.40.0 / 1.52.2. src/native/plugins/deploy.rs accepts a clean stamp only via ancestor_of(source_head) and runs find_inclusion_proof only for dirty stamps, so even a clean tree is refused, contrary to docs/develop/deployment.md ("any clean checkout whose HEAD reaches a commit holding the deployed bundle byte for byte syncs without --force"). This also keeps the required deployed-vault smoke red at its pre-check. No -F used. Related: bob-cli-h8.2.

[2026-11-21T19:06:23Z · bob-cli-o6.6.1.5] PROPOSED FOLLOW-UP: Make the 25 ms ledger-tools perf budgets load-tolerant — test-ledger-tools-frees-marks.cjs ("200-link / 2000-task build", 37 ms) and test-ledger-tools-event-link-times.cjs ("one build over a 200-link ledger", 26.0 ms) each failed one full npm test run at load average 107-182 and pass 3/3 in isolation; a third full run on the same tree was 8246/0. event-link was already recorded by bob-cli-o6.4.1.2. Evidence: file:explicit:282423e57c9f033d6cf61ecc (final2-npm-test*.log).

[2026-11-21T19:07:04Z · bob-cli-o6.6.1.5] final-gates-deploy done. Fixed the 3 carried fail-open recovery failures in bob-plugins 240k: sticky insert-failed/unstable fallback memory now carries currentPath, and a preserveFallback release forgets it once the pane shows another note. New unit regression fails 16/17 on old code, 17/17 fixed. bob-ledger-tools bumped to 1.152.1. On the final integrated tree (plugins cdd9df7+fix, bob-cli 250c3053+docs): real-Obsidian title-block walkthrough 65/65 (inventory complete, 0 exceptions; pre-fix baseline 62/3); matrix 77/77, all images inspected (49 reused by exact hash from phase 3, 28 inspected here); build:check 0; npm test 8246/0 (two earlier runs each tripped a different 25 ms perf budget under load 107-182, both pass alone); just check 0. bob-cli-oc repaired: vault-format 6037 -> 5978 words; also fixed the capture.md section 12.24 anchor that broke the strict build. Docs gates still red at lint, only on the unrelated nav-hotkeys page (79fe2e1); post-lint gates pass except pre-existing test_contracts (a0961435). Deployed with bob plugins sync --repo --no-pull, no -F: bob-ledger-tools synced, manifest/main.js/styles.css sha256 23c4b886/229ff12e/0b68ad62 = source = walkthrough bundle. Isolated smoke pass. Deployed-vault smoke is red at its pre-check because block-id-prompt, task-status-cycler, and nav-hotkeys drift (not this epic; guard gap recorded). Evidence manifest file:explicit:6a34814f8b6f320845a11587; 4 PROPOSED FOLLOW-UPs recorded.

## Dependencies

- **Depends on:** [bob-cli-o6.6.1.1](bob-cli-o6.6.1.1.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-o6.6.1.2](bob-cli-o6.6.1.2.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-o6.6.1.3](bob-cli-o6.6.1.3.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-o6.6.1.4](bob-cli-o6.6.1.4.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.5/README.md) | [bob-cli-o6.6.1.5](bob-cli-o6.6.1.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cb9f8fa`](https://github.com/bobs-org/bob-cli/commit/cb9f8fadd227f1cac8b86047a150854e1ab908bd) | docs(reference): trim vault-format under the reference word cap and fix a capture anchor | [bob-cli-o6.6.1.5](bob-cli-o6.6.1.5.md) | 2026-11-21 14:08:18 EST |
| bob-plugins | [`bob-plugins@238fa91`](https://github.com/bobs-org/bob-plugins/commit/238fa91d45fbedf437c69b24eff13f040479dc32) | fix(ledger-tools): retry the title slot after the pane leaves a failed note | [bob-cli-o6.6.1.5](bob-cli-o6.6.1.5.md) | 2026-11-21 14:11:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.5.1.1][1] | Check which fragments the open o6.6.1 phases are changing | 1 |
| read-by | [agent:bob-cli-oj.5.1.2][2] | Check which fragments open o6.6.1 phases touch | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][3] | bob-cli-o6 precondition: which open o6.6.1 phases edit which fragments | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md

<!-- sase:referenced-by:end -->
