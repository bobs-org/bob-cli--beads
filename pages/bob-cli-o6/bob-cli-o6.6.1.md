# Bead: bob-cli-o6.6.1 — Finish the title-block proof, visual matrix, and guarded album rollout

[Bead Pages](../README.md) / [bob-cli-o6.6](bob-cli-o6.6.md) / bob-cli-o6.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-o6.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.6.md) · **Assignee:** `bob-cli-o6.6.1.land`
**Created:** 2026-11-21 08:22:47 EST · **Closed:** 2026-11-21 15:06:05 EST
**Plan:** [202611/title\_block\_final\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/title_block_final_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/title_block_final_proof.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:a32022c60d3fc54dd426ac59 | attached via sase artifact create --bead |

_Plus 8 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/title_block_final_proof.md

<!-- sase:links:end -->

## Description

The shipped title-block family is proven in real Obsidian and the full visual matrix, live albums are tidied only after every sync host proves compatible, and the verified merged plugin build is deployed with durable evidence for o6.6.

## Notes

[2026-11-21T20:06:05Z · bob-cli-o6.6.1.land] Land verification (bob-cli-o6.6.1). All 5 phases closed. Each child note was reviewed and its work checked against source and commits. DECISIONS honored: no memory files, Cargo version, or CHANGELOG edits; no day/period title bytes changed; bank Setup kept its heading.
- title-walkthrough: bob-plugins 3860513 adds scripts/obsidian-title-block-e2e{,-lib}.cjs and the offline wrapper, which is registered in test:unit.
- fail-open-proof: c803a4e extends the runner. Its 3 recovery failures were carried as follow-ups by o6.6.1.2/.3 and fixed in 238fa91 (240k sticky-fallback memory carries currentPath; unit regression; ledger-tools 1.152.1). I reviewed the diff.
- visual-matrix: 9a15d52 adds scripts/preview-title-block-matrix.cjs (o6.6.1.3 left it untracked; o6.6.1.5 committed it).
- album-rollout: live tidy applied in vault commit 3f9861acf863 (6 albums) after all three hosts passed a 29/29 probe. A relaunch confirmed it idempotent (tidy 0, sync current, check 0 errors).
- final-gates-deploy: bob-cli cb9f8fad brings vault-format.md to 5978/6000 words (bob-cli-oc repaired) and fixes the capture.md 12.24 anchor. Evidence manifest: file:explicit:6a34814f8b6f320845a11587.
Drift reconciliation: 3 bob-plugins commits landed after 238fa91 (d9fe19d bank row notes, da0737b intention [[, e6d7aed record card [[). They touch no 240*/242k/296* title-block fragments, but the bundle changed, so I reran on clean e6d7aed (ledger-tools 1.154.0, main.js fe0f2be3): build:check ok; title-block unit tests and offline wrapper 89/89; real-Obsidian walkthrough 65/65 (inventory complete, 0 console exceptions); matrix 77/77, all 77 PNGs byte-identical to the o6.6.1.5-inspected set, so their verdicts carry over. Evidence: file:explicit:a32022c60d3fc54dd426ac59.
Deployed bob-ledger-tools is another in-flight agent's dirty build (bob-cli_11 at da0737b, which contains 238fa91). The guard protects it; no -F was used.
bob-cli commits after cb9f8fad (task tidy, task-split, glossary) do not touch the epic's docs or album paths, so no integration edits were needed. epic-symbols: none for o6.6.1 or o6.6.
Follow-up triage:
(1) o6.6.1.2 #1 / o6.6.1.3 #1, title-slot recovery: declined; fixed in-epic by 238fa91 and re-verified 65/65.
(2) o6.6.1.5 #1, nav-hotkeys docs budget (now 6307/6000): already routed by o6.6.1.5 (+1 on bob-cli-ob, DISCOVERED ISSUE on bob-cli-om); nothing further.
(3) o6.6.1.5 #2, test_contracts.py 3 failures from a0961435: re-verified on dfe20ca3; routed as DISCOVERED ISSUE to active epic bob-cli-on (on.1 caused it).
(4) o6.6.1.5 #3, deploy guard skips inclusion proof for clean stamps: reproduced; confirmed ancestors 3956368/6e0d764 hold the deployed bundles byte for byte; new task bob-cli-or (bug, small), linked to mv, e4, and h8.2.
(5) o6.6.1.5 #4, 25 ms perf budgets: +1 on bob-cli-io (frees-marks) and bob-cli-km (event-link-times).
Also found while landing:
- bob-ledger-tools.md is at 6042/6000 because of d9fe19d: +1 on bob-cli-il, DISCOVERED ISSUE on bob-cli-oo.
- bob-cli-oq (capture.md anchor) was already fixed by cb9f8fad: closed with evidence.
- bob-cli-oc: repair evidence noted and left open for the outer land agent, per plan.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.land/README.md) | [bob-cli-o6.6.1](bob-cli-o6.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@7cd986d`](https://github.com/bobs-org/bob-cli--plans/commit/7cd986de0e91d646b1a3217401a97abdaf2feae7) | chore(plans): mark title\_block\_final\_proof done after bob-cli-o6.6.1 landed | [bob-cli-o6.6.1](bob-cli-o6.6.1.md) | 2026-11-21 15:08:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.6.1.1][1] | Need parent DECISIONS, notes, and whether earlier title-walkthrough work already landed | 1 |
| read-by | [agent:bob-cli-o6.6.1.3][2] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-o6.6.1.5][3] | Need epic decisions and notes for final gates phase | 1 |
| read-by | [agent:bob-cli-o6.6.1.land][4] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:bob-cli-oj.5.1.1][5] | Check which fragments the open o6.6.1 phases are changing | 2 |
| read-by | [agent:bob-cli-oj.5.1.2][6] | Check which fragments open o6.6.1 phases touch | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][7] | bob-cli-o6 precondition: which open o6.6.1 phases edit which fragments | 1 |
| read-by | [agent:bob-cli-oj.5.1.4][8] | Coordination: which o6.6.1 phases are open and the files they own | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.land/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md

<!-- sase:referenced-by:end -->
