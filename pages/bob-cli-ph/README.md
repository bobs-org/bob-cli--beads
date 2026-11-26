# Bead: bob-cli-ph — True-case drawers: bold headers that keep their real names

[Bead Pages](../README.md) / bob-cli-ph

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.land`
**Created:** 2026-11-22 17:36:48 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/true_case_drawers.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-pp][2] | True-case drawers' Mac phase (ph.8) adds drawer rendering in the same editor; it deliberately never hides drawer markers to avoid the req caret defect |

_Plus 12 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-pp/README.md

<!-- sase:links:end -->

## Description

A task drawer is a `- **Title**` bullet whose title keeps its authored capitalization everywhere: on disk, in capture, in Obsidian and Bob Mac Capture, and through promotion, reversal, and rename. Every surface draws it as a quiet, recognizable drawer, and ALL-CAPS stops being structure after a gated, multi-host-safe migration.

## Notes

[2026-11-23T16:27:53Z · bob-cli-pf.4.1.7.land] DISCOVERED ISSUE: Triaged bob-cli-pf.4.1.7.4 PROPOSED FOLLOW-UP #5. On bob-plugins b2c37102 against bob-cli f6cf62cf, node --test scripts/test-task-reqs-twin-copies.cjs fails its canonical README.md equality assertion (6 pass, 1 fail). git diff shows canonical tests/fixtures/task_reqs/README.md advanced in drawer-reader commit 37b2080e to RQ22/RL61 and bold drawer cases, while cycler/nav/block-id copies retain RQ21/RL60. This is causally owned by active drawer rollout, especially plugin-readers bob-cli-ph.2; synchronize semantic fixtures with the reader rollout, not README alone. No separate task created. The other proposal (#4, missing task-drawers navigation) is already repaired by f6cf62cf mkdocs.yml:375. Corroborates bob-cli-pq.3 notes #5/#7.

[2026-11-23T20:42:29Z · bob-cli-pq.land] HANDOFF from bob-cli-pq.land: Bryan waived the pq↔ph sequencing gate (bob-cli-pq note #1: 'Keep drawer words untouched; the later lander does the taste pass'). bob-cli-pq (criterion diamond) has landed first, so the joint drawer-tray/diamond taste pass belongs to this epic's lander once ph.7 (Obsidian drawer rendering) and ph.8 (Mac drawer rendering) land. Tune the tray's stroke weight beside the requirement diamond (16x16 viewBox, stroke-width 1.75, 0.92em mask in a 1em slot; the single size knob is 0.92em -> 1em, docs/task-requirements.md §4). Diamond-only baselines: notes file:explicit:6ceb733e2949af5516d84d19 (light) / ca9bfcba02f2502cd9513085 (dark); successor card file:explicit:3ba83de21213ca5060841b1a / 4a6962df7831b9d463b4f6b6; Mac preview/agenda file:explicit:a8c8984598169d92da8e1a46 / 3ca540750e2c9d40d78e6510. pq never changed a drawer word (NOTES / **Notes**) in any string.

[2026-11-25T10:57:19Z · bryanbugyi34@gmail.com] This epic should not need to wait for a release. See the drawer_reader_gate_without_release.md file in the research sidecar repo for context.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ph.1](bob-cli-ph.1.md) | Dual-read drawer recognizer, readers, and outside-text escape | ✓ closed | large | 2026-11-22 | 1 | 2 |
| [bob-cli-ph.10](bob-cli-ph.10.md) | Retire ALL-CAPS drawer recognition | ◐ in_progress | medium | 2026-11-22 | 1 | 0 |
| [bob-cli-ph.11](bob-cli-ph.11.md) | Memory records for true-case drawers | ◐ in_progress | small | 2026-11-22 | 1 | 0 |
| [bob-cli-ph.2](bob-cli-ph.2.md) | One plugin recognizer twin and dual-read plugin readers | ✓ closed | large | 2026-11-22 | 1 | 1 |
| [bob-cli-ph.3](bob-cli-ph.3.md) | Every host reads bold drawers before any writer flips | ✓ closed | small | 2026-11-22 | 1 | 2 |
| [bob-cli-ph.4](bob-cli-ph.4.md) | Every bob-cli writer emits bold drawer headers | ✓ closed | medium | 2026-11-22 | 1 | 1 |
| [bob-cli-ph.5](bob-cli-ph.5.md) | Drawer rename respells and inventories legacy drawers | ✓ closed | medium | 2026-11-22 | 1 | 1 |
| [bob-cli-ph.6](bob-cli-ph.6.md) | One place resolver and bold drawer drafts in capture | ✓ closed | large | 2026-11-22 | 1 | 0 |
| [bob-cli-ph.7](bob-cli-ph.7.md) | Obsidian drawer rendering, typing, and bold writers | ✓ closed | large | 2026-11-22 | 1 | 0 |
| [bob-cli-ph.8](bob-cli-ph.8.md) | Bob Mac Capture drawer rendering and typing | ◐ in_progress | large | 2026-11-22 | 1 | 3 |
| [bob-cli-ph.9](bob-cli-ph.9.md) | Reviewed migration of legacy ALL-CAPS drawers | ✓ closed | small | 2026-11-22 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ph: True-case drawers: bold headers that keep their real names [in_progress]"]
    n1["bob-cli-ph.1: Dual-read drawer recognizer, readers, and outside-text escape [closed]"]
    n2["bob-cli-ph.10: Retire ALL-CAPS drawer recognition [in_progress]"]
    n3["bob-cli-ph.11: Memory records for true-case drawers [in_progress]"]
    n4["bob-cli-ph.2: One plugin recognizer twin and dual-read plugin readers [closed]"]
    n5["bob-cli-ph.3: Every host reads bold drawers before any writer flips [closed]"]
    n6["bob-cli-ph.4: Every bob-cli writer emits bold drawer headers [closed]"]
    n7["bob-cli-ph.5: Drawer rename respells and inventories legacy drawers [closed]"]
    n8["bob-cli-ph.6: One place resolver and bold drawer drafts in capture [closed]"]
    n9["bob-cli-ph.6.1: True-case capture drawers and one place resolver [closed]"]
    n10["bob-cli-ph.6.1.1: Extract the shared place lexer and resolver without changing behavior [closed]"]
    n11["bob-cli-ph.6.1.2: Admit bold container drafts across all four contexts [closed]"]
    n12["bob-cli-ph.6.1.3: Preserve selected titles and prefer explicit catalog spellings [closed]"]
    n13["bob-cli-ph.6.1.4: Add drawer typing expansion and semantic preview annotations [closed]"]
    n14["bob-cli-ph.6.1.5: Verify the complete capture contract and publish its documentation [closed]"]
    n15["bob-cli-ph.7: Obsidian drawer rendering, typing, and bold writers [closed]"]
    n16["bob-cli-ph.7.1: Complete Obsidian true-case task drawers [closed]"]
    n17["bob-cli-ph.7.1.1: Bold plugin writers and verbatim project conversion [closed]"]
    n18["bob-cli-ph.7.1.2: Task drawer marks in Live Preview and reading view [closed]"]
    n19["bob-cli-ph.7.1.3: Drawer marker typing and Toggle Drawer [closed]"]
    n20["bob-cli-ph.7.1.4: Real Obsidian acceptance, screenshots, and documentation [closed]"]
    n21["bob-cli-ph.8: Bob Mac Capture drawer rendering and typing [in_progress]"]
    n22["bob-cli-ph.8.1: Finish Bob Mac Capture true-case drawers [in_progress]"]
    n23["bob-cli-ph.8.1.1: Repair the drawer annotation build and cover the landed decoding [in_progress]"]
    n24["bob-cli-ph.8.1.2: Tray and verbatim title on annotated preview drawer headers [in_progress]"]
    n25["bob-cli-ph.8.1.3: Semibold drawer titles and dimmed delimiters in the draft editor [in_progress]"]
    n26["bob-cli-ph.8.1.4: Bob-driven star expansion and atomic Backspace [in_progress]"]
    n27["bob-cli-ph.8.1.5: Drawer title newline and closing-star overtype [in_progress]"]
    n28["bob-cli-ph.8.1.6: Mac drawer acceptance, screenshots, and documentation [in_progress]"]
    n29["bob-cli-ph.9: Reviewed migration of legacy ALL-CAPS drawers [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n8 --> n9
    n9 --> n10
    n9 --> n11
    n9 --> n12
    n9 --> n13
    n9 --> n14
    n0 --> n15
    n15 --> n16
    n16 --> n17
    n16 --> n18
    n16 --> n19
    n16 --> n20
    n0 --> n21
    n21 --> n22
    n22 --> n23
    n22 --> n24
    n22 --> n25
    n22 --> n26
    n22 --> n27
    n22 --> n28
    n0 --> n29
    n1 -.-> n4
    n1 -.-> n5
    n2 -.-> n3
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
    n6 -.-> n8
    n6 -.-> n15
    n7 -.-> n29
    n8 -.-> n21
    n8 -.-> n29
    n10 -.-> n11
    n11 -.-> n12
    n12 -.-> n13
    n13 -.-> n14
    n15 -.-> n29
    n17 -.-> n18
    n17 -.-> n20
    n18 -.-> n19
    n18 -.-> n20
    n19 -.-> n20
    n21 -.-> n3
    n23 -.-> n24
    n23 -.-> n25
    n23 -.-> n28
    n24 -.-> n28
    n25 -.-> n26
    n25 -.-> n28
    n26 -.-> n27
    n26 -.-> n28
    n27 -.-> n28
    n29 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.1.md) | [bob-cli-ph.1](bob-cli-ph.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-ph.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.10/README.md) | [bob-cli-ph.10](bob-cli-ph.10.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.11/README.md) | [bob-cli-ph.11](bob-cli-ph.11.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.2.md) | [bob-cli-ph.2](bob-cli-ph.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.3/README.md) | [bob-cli-ph.3](bob-cli-ph.3.md) | 2 |
| [bbugyi200.apollo.bob-cli-ph.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.4/README.md) | [bob-cli-ph.4](bob-cli-ph.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.5.md) | [bob-cli-ph.5](bob-cli-ph.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.md) | [bob-cli-ph.6](bob-cli-ph.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.1/README.md) | [bob-cli-ph.6.1.1](bob-cli-ph.6.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.2/README.md) | [bob-cli-ph.6.1.2](bob-cli-ph.6.1.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.3/README.md) | [bob-cli-ph.6.1.3](bob-cli-ph.6.1.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.4/README.md) | [bob-cli-ph.6.1.4](bob-cli-ph.6.1.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.1.5.md) | [bob-cli-ph.6.1.5](bob-cli-ph.6.1.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.land/README.md) | [bob-cli-ph.6.1](bob-cli-ph.6.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-ph.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.md) | [bob-cli-ph.7](bob-cli-ph.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.7.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.1/README.md) | [bob-cli-ph.7.1.1](bob-cli-ph.7.1.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.2.md) | [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.3/README.md) | [bob-cli-ph.7.1.3](bob-cli-ph.7.1.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.7.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.4/README.md) | [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.land.md) | [bob-cli-ph.7.1](bob-cli-ph.7.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) | [bob-cli-ph.8](bob-cli-ph.8.md) | 3 |
| [bbugyi200.apollo.bob-cli-ph.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.1.md) | [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-ph.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.8.1.2/README.md) | [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.8.1.3/README.md) | [bob-cli-ph.8.1.3](bob-cli-ph.8.1.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.8.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.8.1.4/README.md) | [bob-cli-ph.8.1.4](bob-cli-ph.8.1.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.8.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.8.1.5/README.md) | [bob-cli-ph.8.1.5](bob-cli-ph.8.1.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.8.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.8.1.6/README.md) | [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.8.1.land/README.md) | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.9.md) | [bob-cli-ph.9](bob-cli-ph.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-ph.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.land/README.md) | [bob-cli-ph](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`37b2080`](https://github.com/bobs-org/bob-cli/commit/37b2080e9efca170f542954f088ce4169d430cfa) | feat(drawers): add dual-read task drawer readers | [bob-cli-ph.1](bob-cli-ph.1.md) | 2026-11-23 08:06:21 EST |
| bob-cli | [`c25d92f`](https://github.com/bobs-org/bob-cli/commit/c25d92fdd4e2c4073ec1a24bda34251fae8eded9) | feat(capture): add task drawer contracts and docs | [bob-cli-ph.1](bob-cli-ph.1.md) | 2026-11-23 12:14:15 EST |
| bob-cli | [`b1fa8ad`](https://github.com/bobs-org/bob-cli/commit/b1fa8ad6de8c3818152296f7c9af7cb2ec21ed1e) | docs: document plugin task drawer reader parity | [bob-cli-ph.2](bob-cli-ph.2.md) | 2026-11-23 13:04:10 EST |
| bob-cli | [`fd99ebb`](https://github.com/bobs-org/bob-cli/commit/fd99ebb85dcf0555cc48570397c419f4dd8f3167) | chore: add Bob host reader currency gate | [bob-cli-ph.3](bob-cli-ph.3.md) | 2026-11-23 18:51:04 EST |
| bob-cli | [`5ab392a`](https://github.com/bobs-org/bob-cli/commit/5ab392a1ba087c6f87d8685035979498082079ed) | chore(dev): let bob-host-currency gate on a bold-drawer read probe | [bob-cli-ph.3](bob-cli-ph.3.md) | 2026-11-25 06:49:42 EST |
| bob-cli | [`8f88a52`](https://github.com/bobs-org/bob-cli/commit/8f88a52c1cfc59236d6ddc4bd36ee6f11de95afd) | feat(task-drawers): emit bold drawer headers from every writer | [bob-cli-ph.4](bob-cli-ph.4.md) | 2026-11-25 08:27:23 EST |
| bob-cli | [`ae42b3e`](https://github.com/bobs-org/bob-cli/commit/ae42b3ed2a48ddc218021262c0fdd3fc791d99a1) | feat(task-drawers): preserve rename spelling and inventory legacy drawers | [bob-cli-ph.5](bob-cli-ph.5.md) | 2026-11-25 09:29:31 EST |
| bob-cli | [`45a5434`](https://github.com/bobs-org/bob-cli/commit/45a54345f59c7cefec7121ac46f61fe34ba3fbf1) | refactor(capture): extract shared place lexer and resolver | [bob-cli-ph.6.1.1](bob-cli-ph.6.1.1.md) | 2026-11-25 09:41:35 EST |
| bob-cli | [`22fea30`](https://github.com/bobs-org/bob-cli/commit/22fea308101c894185bc29d494c1b5bdca6dff71) | feat(capture): admit whole-bold container drafts | [bob-cli-ph.6.1.2](bob-cli-ph.6.1.2.md) | 2026-11-25 12:14:41 EST |
| bob-cli | [`0742684`](https://github.com/bobs-org/bob-cli/commit/0742684de3390415ffb5dbb3423c0dbc841f4b3e) | docs(task-drawers): document Obsidian trays, typing, and conversion | [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) | 2026-11-25 12:51:09 EST |
| bob-cli | [`8a1d16a`](https://github.com/bobs-org/bob-cli/commit/8a1d16a621f7829bf94b3ccabf49c04ab9192fd5) | feat(capture): prefer catalog spellings and preserve authored drawer titles | [bob-cli-ph.6.1.3](bob-cli-ph.6.1.3.md) | 2026-11-25 13:27:40 EST |
| bob-cli | [`dfc7fac`](https://github.com/bobs-org/bob-cli/commit/dfc7facb18ded459c5471372a65731a543e5f1f7) | feat(capture): wire drawer editor rewrite markers through JSON and previews | [bob-cli-ph.6.1.4](bob-cli-ph.6.1.4.md) | 2026-11-25 15:51:26 EST |
| bob-cli | [`d67a5b7`](https://github.com/bobs-org/bob-cli/commit/d67a5b7b8135af40ba8f345e90cb9a12f3fe0812) | docs(capture): complete drawer contract references | [bob-cli-ph.6.1.5](bob-cli-ph.6.1.5.md) | 2026-11-25 16:19:55 EST |
| bob-cli | [`2d2f200`](https://github.com/bobs-org/bob-cli/commit/2d2f200dfdbdce64c6ff685b0df5366e510e32f0) | feat(capture)!: land true-case drawers with one reserved-name rule | [bob-cli-ph.6.1](bob-cli-ph.6.1.md) | 2026-11-25 18:25:58 EST |
| bob-cli--plans | [`bob-cli--plans@5d3da5e`](https://github.com/bobs-org/bob-cli--plans/commit/5d3da5e0e76637aea0e969935c58ed7da97e1192) | chore(plans): mark capture\_true\_case\_drawers done | [bob-cli-ph.6.1](bob-cli-ph.6.1.md) | 2026-11-25 18:27:16 EST |
| bob-cli--plans | [`bob-cli--plans@c15fb27`](https://github.com/bobs-org/bob-cli--plans/commit/c15fb27b034f4413371b9deaed50ff4bae33f7bb) | docs(plan): mark true-case drawer epic complete | [bob-cli-ph.7.1](bob-cli-ph.7.1.md) | 2026-11-25 18:59:29 EST |
| bob-mac-capture | [`bob-mac-capture@4eb9b2e`](https://github.com/bobs-org/bob-mac-capture/commit/4eb9b2e977dc8275a5849d5ac7f8bc8fabb617b2) | fix(mac): require grammar 30 for drawer fixtures | [bob-cli-ph.8](bob-cli-ph.8.md) | 2026-11-25 19:18:09 EST |
| bob-cli | [`f4da72f`](https://github.com/bobs-org/bob-cli/commit/f4da72ff5dd08b9827eb8b13a9f2bce04c47d9f6) | docs(task-drawers): describe Mac thin-client drawer contract | [bob-cli-ph.8](bob-cli-ph.8.md) | 2026-11-25 19:51:53 EST |
| bob-mac-capture | [`bob-mac-capture@b45b195`](https://github.com/bobs-org/bob-mac-capture/commit/b45b1951b0f983edc4d8e9deae5ad92e96bb00ab) | feat(mac): carry true-case drawer annotations from Bob | [bob-cli-ph.8](bob-cli-ph.8.md) | 2026-11-25 19:53:07 EST |
| bob-mac-capture | [`bob-mac-capture@b0062be`](https://github.com/bobs-org/bob-mac-capture/commit/b0062be1749f388a849c5bf0251c7fb3f914bf94) | fix(mac-capture): decode drawer summary markers safely | [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) | 2026-11-25 21:11:04 EST |
| bob-mac-capture | [`bob-mac-capture@5073564`](https://github.com/bobs-org/bob-mac-capture/commit/5073564e3ce639eca04bd05659b1a5e6fd04a0f8) | test(mac-capture): align drawer assertions with true-case output | [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) | 2026-11-25 21:37:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-ph.4][2] | need epic decisions and notes | 1 |
| read-by | [agent:bob-cli-ph.6.1.2][3] | Need ancestor epic decisions that govern the capture-drawer phase | 1 |
| read-by | [agent:bob-cli-ph.7.1.land--3][4] | Confirm parent plan stays open during closeout | 1 |
| read-by | [agent:bob-cli-ph.7.1.land--7][4] | Confirm the containing Obsidian phase epic remains open after drawer closeout | 1 |
| read-by | [agent:bob-cli-pq.land][5] | Check drawer epic status for sequencing and taste pass ownership | 1 |
| read-by | [agent:g1][6] | Research how to progress the epic without waiting for a release | 1 |
| read-by | [agent:research.66.cdx][7] | Independent research into better-o and all-ops-reconcile-tasks; inspect referenced scope and completion | 1 |
| read-by | [agent:research.66.cld][8] | Context for better-o / all-ops-reconcile research | 1 |
| read-by | [agent:research.66.final][9] | Consolidating swarm research on better-o: verify drawer-epic phase states and the pn/po writer-gap beads the reports cite | 1 |
| read-by | [agent:research.66.gem][10] | Referenced in ^better-o for ongoing drawer changes | 1 |
| read-by | [agent:research.66.grk][11] | Need the true-case drawers epic that better-o says is still in progress | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.land.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.land/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.cdx/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.cld/README.md
[9]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.final/README.md
[10]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.gem/README.md
[11]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.grk/README.md

<!-- sase:referenced-by:end -->
