# Bead: bob-cli-on — Task requirements (reqs)

[Bead Pages](../README.md) / bob-cli-on

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.land`
**Created:** 2026-11-21 11:13:26 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/task_requirements.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md

<!-- sase:links:end -->

## Description

A task can carry requirements: checkbox children without `#task`, nested as deep as the work needs, drawn as a quiet ⌗⌗ run in the task's ink. They are met when the task closes and can never be ticked early. They can be dropped with a reason or carried into their own task, and the close card audits them once. They sit in one canonical block order beside a NOTES drawer, and they promote one level at a time into project tasks. bob-cli, bob-plugins, Bob Mac Capture, and the vault agree byte for byte through shared vectors, and every legacy REQUIREMENTS drawer becomes NOTES.

## Notes

[2026-11-21T19:54:07Z · bob-cli-o6.6.1.land] DISCOVERED ISSUE: bob-cli a0961435 (bob-cli-on.1, req-contract) registered docs/task-requirements.md as a contract without updating the bob-docs contract tests, so tools/docs/tests/test_contracts.py fails 3/8 on master dfe20ca3: test_current_registry_and_generated_nav_are_complete_and_unique (registry has 55 entries, test expects 54), test_llmstxt_contracts_section_lists_exactly_registry_stems (index 46 'task-split.md' != 'task-requirements.md'), and test_readme_table_matches_original_contract_index_snapshot (README table sha f23b0e44... != pinned 34f4f8a4...). Repro: uv run --project tools/docs pytest -q tools/docs/tests/test_contracts.py. It is masked today only because just docs-check stops earlier at the reference word-budget lint. Proposed by bob-cli-o6.6.1.5 note #2 (also reproduced on clean base 250c3053 with that phase's docs stashed; evidence file:explicit:282423e57c9f033d6cf61ecc, bobcli-docs-postlint.log); re-verified on dfe20ca3 by the bob-cli-o6.6.1 land agent. Fix belongs with this epic: bump the expected count, the llms.txt list, and the README snapshot, following the precedent of bob-cli-hs.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-on.1](bob-cli-on.1.md) | Requirement recognizer, shared vectors, and the contract page | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.10](bob-cli-on.10.md) | Obsidian requirement guards, toggle, drop, and typing assist | ◐ in_progress | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.11](bob-cli-on.11.md) | Requirements on the Obsidian successor card and carry-now | ◐ in_progress | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.12](bob-cli-on.12.md) | Promotion maps requirements to tasks and notes to notes | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-on.13](bob-cli-on.13.md) | Mac requirement typing and glyph overlay | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-on.14](bob-cli-on.14.md) | Mac bullet indentation beyond two levels | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-on.15](bob-cli-on.15.md) | Requirements on the Mac Pull-In card | ◐ in_progress | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.16](bob-cli-on.16.md) | Reviewed vault migration | ◐ in_progress | small | 2026-11-21 | 1 | 0 |
| [bob-cli-on.17](bob-cli-on.17.md) | Memory records for task requirements | ◐ in_progress | small | 2026-11-21 | 1 | 0 |
| [bob-cli-on.2](bob-cli-on.2.md) | Keep every task reader and outside-text writer off requirement lines | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.3](bob-cli-on.3.md) | The task block layout module and requirement line writers | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.4](bob-cli-on.4.md) | The bob task tidy command | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.5](bob-cli-on.5.md) | The bob task rename-drawer command | ◐ in_progress | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-on.6](bob-cli-on.6.md) | Capture grammar, spans, typing rewrite, and NOTES routing for requirements | ◐ in_progress | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.7](bob-cli-on.7.md) | Carry a requirement branch into its own task | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.8](bob-cli-on.8.md) | Requirements on the capture successor card | ◐ in_progress | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.9](bob-cli-on.9.md) | Render requirements in Obsidian | ◐ in_progress | medium | 2026-11-21 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-on: Task requirements (reqs) [in_progress]"]
    n1["bob-cli-on.1: Requirement recognizer, shared vectors, and the contract page [closed]"]
    n2["bob-cli-on.10: Obsidian requirement guards, toggle, drop, and typing assist [in_progress]"]
    n3["bob-cli-on.10.1: Obsidian requirement guards, toggle, drop, and typing assist [in_progress]"]
    n4["bob-cli-on.10.1.1: Recognizer and layout twins in the cycler [closed]"]
    n5["bob-cli-on.10.1.2: Writer twin, cross-plugin copies, and the offer-close scope fix [in_progress]"]
    n6["bob-cli-on.10.1.3: Cycler requirement guards, Alt+[ drop, and Alt+] restore [in_progress]"]
    n7["bob-cli-on.10.1.4: Ctrl+] note/req toggle, `- [` typing assist, and o/O continuation [in_progress]"]
    n8["bob-cli-on.10.1.5: Nav and Block ID Prompt requirement guards and the owner Task Card [in_progress]"]
    n9["bob-cli-on.10.1.6: Contract section, cross-plugin e2e, and ship [in_progress]"]
    n10["bob-cli-on.11: Requirements on the Obsidian successor card and carry-now [in_progress]"]
    n11["bob-cli-on.12: Promotion maps requirements to tasks and notes to notes [in_progress]"]
    n12["bob-cli-on.13: Mac requirement typing and glyph overlay [in_progress]"]
    n13["bob-cli-on.14: Mac bullet indentation beyond two levels [in_progress]"]
    n14["bob-cli-on.15: Requirements on the Mac Pull-In card [in_progress]"]
    n15["bob-cli-on.16: Reviewed vault migration [in_progress]"]
    n16["bob-cli-on.17: Memory records for task requirements [in_progress]"]
    n17["bob-cli-on.2: Keep every task reader and outside-text writer off requirement lines [closed]"]
    n18["bob-cli-on.3: The task block layout module and requirement line writers [closed]"]
    n19["bob-cli-on.4: The bob task tidy command [closed]"]
    n20["bob-cli-on.5: The bob task rename-drawer command [in_progress]"]
    n21["bob-cli-on.6: Capture grammar, spans, typing rewrite, and NOTES routing for requirements [in_progress]"]
    n22["bob-cli-on.6.1: Requirement bullets in capture (grammar 29) [in_progress]"]
    n23["bob-cli-on.6.1.1: Numeric authored depth with today's behavior kept [closed]"]
    n24["bob-cli-on.6.1.2: Shared requirement position resolver, refusals, req_marker span, grammar 29 [in_progress]"]
    n25["bob-cli-on.6.1.3: Requirements in the blocks capture creates [in_progress]"]
    n26["bob-cli-on.6.1.4: Requirements added to existing tasks, the scoop, and req_link [in_progress]"]
    n27["bob-cli-on.6.1.5: The expand_req_marker typing rewrite [in_progress]"]
    n28["bob-cli-on.7: Carry a requirement branch into its own task [closed]"]
    n29["bob-cli-on.8: Requirements on the capture successor card [in_progress]"]
    n30["bob-cli-on.9: Render requirements in Obsidian [in_progress]"]
    n0 --> n1
    n0 --> n2
    n2 --> n3
    n3 --> n4
    n3 --> n5
    n3 --> n6
    n3 --> n7
    n3 --> n8
    n3 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n0 --> n15
    n0 --> n16
    n0 --> n17
    n0 --> n18
    n0 --> n19
    n0 --> n20
    n0 --> n21
    n21 --> n22
    n22 --> n23
    n22 --> n24
    n22 --> n25
    n22 --> n26
    n22 --> n27
    n0 --> n28
    n0 --> n29
    n0 --> n30
    n1 -.-> n17
    n1 -.-> n18
    n1 -.-> n30
    n2 -.-> n10
    n2 -.-> n15
    n4 -.-> n5
    n5 -.-> n6
    n5 -.-> n8
    n6 -.-> n7
    n7 -.-> n9
    n8 -.-> n9
    n10 -.-> n11
    n11 -.-> n16
    n12 -.-> n13
    n13 -.-> n14
    n15 -.-> n16
    n17 -.-> n2
    n17 -.-> n29
    n18 -.-> n2
    n18 -.-> n19
    n18 -.-> n21
    n18 -.-> n28
    n19 -.-> n20
    n20 -.-> n15
    n21 -.-> n12
    n21 -.-> n29
    n23 -.-> n24
    n24 -.-> n25
    n24 -.-> n27
    n25 -.-> n26
    n28 -.-> n29
    n29 -.-> n10
    n29 -.-> n14
    n29 -.-> n16
    n30 -.-> n15
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.1/README.md) | [bob-cli-on.1](bob-cli-on.1.md) | 1 |
| [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) | [bob-cli-on.10](bob-cli-on.10.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.1/README.md) | [bob-cli-on.10.1.1](bob-cli-on.10.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.2/README.md) | [bob-cli-on.10.1.2](bob-cli-on.10.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.3/README.md) | [bob-cli-on.10.1.3](bob-cli-on.10.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.4/README.md) | [bob-cli-on.10.1.4](bob-cli-on.10.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.5/README.md) | [bob-cli-on.10.1.5](bob-cli-on.10.1.5.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.6/README.md) | [bob-cli-on.10.1.6](bob-cli-on.10.1.6.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.land/README.md) | [bob-cli-on.10.1](bob-cli-on.10.1.md) | 0 |
| [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11/README.md) | [bob-cli-on.11](bob-cli-on.11.md) | 0 |
| [bbugyi200.athena.bob-cli-on.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.12/README.md) | [bob-cli-on.12](bob-cli-on.12.md) | 0 |
| [bbugyi200.athena.bob-cli-on.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.13/README.md) | [bob-cli-on.13](bob-cli-on.13.md) | 0 |
| [bbugyi200.athena.bob-cli-on.14](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.14/README.md) | [bob-cli-on.14](bob-cli-on.14.md) | 0 |
| [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15/README.md) | [bob-cli-on.15](bob-cli-on.15.md) | 0 |
| [bbugyi200.athena.bob-cli-on.16](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.16/README.md) | [bob-cli-on.16](bob-cli-on.16.md) | 0 |
| [bbugyi200.athena.bob-cli-on.17](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.17/README.md) | [bob-cli-on.17](bob-cli-on.17.md) | 0 |
| [bbugyi200.athena.bob-cli-on.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.2.md) | [bob-cli-on.2](bob-cli-on.2.md) | 1 |
| [bbugyi200.athena.bob-cli-on.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.3/README.md) | [bob-cli-on.3](bob-cli-on.3.md) | 1 |
| [bbugyi200.athena.bob-cli-on.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.4/README.md) | [bob-cli-on.4](bob-cli-on.4.md) | 1 |
| [bbugyi200.athena.bob-cli-on.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.5/README.md) | [bob-cli-on.5](bob-cli-on.5.md) | 0 |
| [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) | [bob-cli-on.6](bob-cli-on.6.md) | 0 |
| [bbugyi200.athena.bob-cli-on.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.1/README.md) | [bob-cli-on.6.1.1](bob-cli-on.6.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-on.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md) | [bob-cli-on.6.1.2](bob-cli-on.6.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-on.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.3/README.md) | [bob-cli-on.6.1.3](bob-cli-on.6.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-on.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.4/README.md) | [bob-cli-on.6.1.4](bob-cli-on.6.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-on.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.5/README.md) | [bob-cli-on.6.1.5](bob-cli-on.6.1.5.md) | 0 |
| [bbugyi200.athena.bob-cli-on.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.land/README.md) | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 0 |
| [bbugyi200.athena.bob-cli-on.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.7/README.md) | [bob-cli-on.7](bob-cli-on.7.md) | 1 |
| [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8/README.md) | [bob-cli-on.8](bob-cli-on.8.md) | 0 |
| [bbugyi200.athena.bob-cli-on.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.9.md) | [bob-cli-on.9](bob-cli-on.9.md) | 1 |
| [bbugyi200.athena.bob-cli-on.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.land/README.md) | [bob-cli-on](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a096143`](https://github.com/bobs-org/bob-cli/commit/a0961435506e4810841527ecd0b81505cb6d0632) | feat(task-reqs): add req forest recognizer contract | [bob-cli-on.1](bob-cli-on.1.md) | 2026-11-21 12:16:31 EST |
| bob-cli | [`ca07094`](https://github.com/bobs-org/bob-cli/commit/ca070941c05b42840a40d87f0e4f6a6e0aab6090) | feat(task-reqs): add task block layout and req line writers | [bob-cli-on.3](bob-cli-on.3.md) | 2026-11-21 13:32:20 EST |
| bob-cli | [`250c305`](https://github.com/bobs-org/bob-cli/commit/250c3053d652d1d6b48299557fc8272a809bab88) | docs(tasks): document requirement marks | [bob-cli-on.9](bob-cli-on.9.md) | 2026-11-21 13:37:40 EST |
| bob-cli | [`532df82`](https://github.com/bobs-org/bob-cli/commit/532df8259187f65b6f66864669eb80b133fcb35e) | feat(task-reqs): keep readers and writers off requirement lines | [bob-cli-on.2](bob-cli-on.2.md) | 2026-11-21 13:50:46 EST |
| bob-cli | [`f888213`](https://github.com/bobs-org/bob-cli/commit/f888213a22650dd6e33b38e9f77e7a65ca8e24e6) | feat(task): add bob task tidy to repair open task blocks | [bob-cli-on.4](bob-cli-on.4.md) | 2026-11-21 14:12:31 EST |
| bob-cli | [`2239120`](https://github.com/bobs-org/bob-cli/commit/2239120810ed5867eefc66a468cee04972aa6b45) | feat(task-split)!: carry a requirement branch into its own task | [bob-cli-on.7](bob-cli-on.7.md) | 2026-11-21 14:25:11 EST |
| bob-cli | [`1d89d95`](https://github.com/bobs-org/bob-cli/commit/1d89d95f3b2288601111965abad896eff5fd0195) | refactor(capture): make authored bullet depth a numeric level | [bob-cli-on.6.1.1](bob-cli-on.6.1.1.md) | 2026-11-21 15:12:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.6.1.5][1] | Look for existing DISCOVERED ISSUE notes about plugin fixture drift | 2 |
| read-by | [agent:bob-cli-on.7][2] | Check epic notes and sibling phase status for req-split | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.7/README.md

<!-- sase:referenced-by:end -->
