# Bead: bob-cli-qq — Property Card Cabinets

[Bead Pages](../README.md) / bob-cli-qq

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6m.linker.w0.md) · **Assignee:** `bob-cli-qq.land`
**Created:** 2026-11-26 16:09:02 EST
**Plan:** [202611/property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_cabinets.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/property_card_cabinets.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-r5][2] | Cabinets go-live (bob-cli-qq.9) still edits kit hunks near 240m/240q; land this after qq closes to avoid colliding |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_cabinets.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-r5/README.md

<!-- sase:links:end -->

## Description

Child areas, sub-projects, notebooks, albums, and album records open as collapsible cabinets at the bottom of their note's Property Card. Each cabinet shows exactly the data its H2 section showed. Album Schema and bank Setup move into the same chrome as a restyled Properties cabinet, and `_` becomes a numbered, cancel-safe cabinet pick. The stored catalogs stay bob-owned Markdown, and nothing in bob-cli, the release train, or Bob Mac Capture changes. The work lands dark beside bob-cli-qj, bob-cli-qm, and bob-cli-qp and switches on only after the sibling go-lives it would race.

## Notes

[2026-11-27T12:29:31Z · bob-cli-qm.land] DISCOVERED ISSUE (from the bob-cli-qm landing; proposed by bob-cli-qm.7--1 note #6): bob-cli-qm.7 (bob-plugins eca733c2) deleted the Notebook/Prose preview gate and its cardPreviewKinds key. The cabinets runner still seeds the dead key: bob-plugins scripts/obsidian-cabinets-e2e.cjs:20 GATE_DATA has cardPreviewKinds: ["notebook", "prose"], line 490 gateClosed has cardPreviewKinds: [], and the wrapper scripts/test-obsidian-cabinets-e2e.cjs:73 pins that seed with assert.match. ledger-tools ignores the key, so nothing breaks. Drop it from both objects and the wrapper assertion when bob-cli-qq.9 removes cabinetsPreview. Keep scripts/test-ledger-tools-cabinets-kit.cjs:102: it deliberately passes cardPreviewKinds as a foreign key to prove it never enables cabinets.

[2026-11-27T13:16:39Z · bob-cli-qp.land] DISCOVERED ISSUE (from the bob-cli-qp landing; proposed by bob-cli-qp.7 note #3 plus lander integration review): (1) The cabinets runner counts only uncaught exceptions. bob-plugins scripts/obsidian-cabinets-e2e.cjs:700 records Runtime.exceptionThrown and gates no-runtime-exceptions at :1483, but it never subscribes to Runtime.consoleAPICalled. CodeMirror reports extension and keymap failures through console.error, which is how the 240wg atomicRanges TypeError ('.between is not a function', introduced by a4bd99f2) hit every Live Preview Vim/arrow motion in the deployed vault without ever failing a cabinets run. bob-cli-qp.7 repaired the facet (propertyCardCabinetAbsorbAtomicRangeSet, unit-covered in scripts/test-ledger-tools-cabinets-absorption.cjs since 2bd92b19). Mirror the Ref Card runner (scripts/obsidian-ref-card-acceptance-e2e.cjs:523 consoleErrors plus flows.cjs:602) so console.error during cursor motions fails acceptance. (2) bob-cli-qp.8 (4410a5bf) deleted the Ref Card gate, so refCardPreview is a dead key like cardPreviewKinds (note #1). The runner still seeds it at obsidian-cabinets-e2e.cjs:20 (GATE_DATA refCardPreview: true) and :780 (gateClosed refCardPreview: false), and scripts/test-obsidian-cabinets-e2e.cjs:77 pins it with assert.match. ledger-tools ignores it, so nothing breaks. Drop it together with cardPreviewKinds when bob-cli-qq.9 removes cabinetsPreview, and keep scripts/test-ledger-tools-cabinets-kit.cjs:102 as the foreign-key negative test. Left to qq because qq.8 and qq.9 own and are actively changing these files.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-qq.1](bob-cli-qq.1.md) | Cabinet gate, model, session state, provider registry, and the view collector | ✓ closed | medium | 2026-11-26 | 1 | 1 |
| [bob-cli-qq.2](bob-cli-qq.2.md) | Walker-footer overlay push/pop API | ✓ closed | small | 2026-11-26 | 1 | 1 |
| [bob-cli-qq.3](bob-cli-qq.3.md) | Catalog recognition, ownership claims, render-time hiding, and the body renderer | ✓ closed | medium | 2026-11-26 | 1 | 1 |
| [bob-cli-qq.4](bob-cli-qq.4.md) | One cabinet chrome, delegation, the stack, and the CSS region | ✓ closed | medium | 2026-11-26 | 1 | 1 |
| [bob-cli-qq.5](bob-cli-qq.5.md) | The \`\_\` dispatch and numbered cabinet pick | ✓ closed | medium | 2026-11-26 | 1 | 1 |
| [bob-cli-qq.6](bob-cli-qq.6.md) | Areas, Projects, Notebooks, and Albums cabinets on area and project cards | ✓ closed | medium | 2026-11-26 | 1 | 1 |
| [bob-cli-qq.7](bob-cli-qq.7.md) | The album Records cabinet | ✓ closed | medium | 2026-11-26 | 1 | 1 |
| [bob-cli-qq.8](bob-cli-qq.8.md) | Real-Obsidian acceptance and screenshot review with the gate open | ◐ in_progress | medium | 2026-11-26 | 1 | 8 |
| [bob-cli-qq.9](bob-cli-qq.9.md) | Switch cabinets on, docs, approved memory, and clean deploy | ◐ in_progress | medium | 2026-11-26 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-qq: Property Card Cabinets [in_progress]"]
    n1["bob-cli-qq.1: Cabinet gate, model, session state, provider registry, and the view collector [closed]"]
    n2["bob-cli-qq.10: Finish Property Card Cabinets — acceptance GO, go-live, and close bob-cli-qq [in_progress]"]
    n3["bob-cli-qq.10.1: Bring the Reading cabinet paint within the 2x inline budget [in_progress]"]
    n4["bob-cli-qq.10.2: Fix the intermittent Reading card miss in the shared property-card host [closed]"]
    n5["bob-cli-qq.10.3: Footer overlay narrow clipping, Areas title row, and runner console errors [closed]"]
    n6["bob-cli-qq.10.4: Rerun real-Obsidian Cabinets acceptance to GO and close bob-cli-qq.8 [in_progress]"]
    n7["bob-cli-qq.10.5: Delete the cabinets gate, convert the tests, deploy, and smoke [in_progress]"]
    n8["bob-cli-qq.10.6: Cabinets docs in both repos, approved memory, and close bob-cli-qq.9 [in_progress]"]
    n9["bob-cli-qq.2: Walker-footer overlay push/pop API [closed]"]
    n10["bob-cli-qq.3: Catalog recognition, ownership claims, render-time hiding, and the body renderer [closed]"]
    n11["bob-cli-qq.4: One cabinet chrome, delegation, the stack, and the CSS region [closed]"]
    n12["bob-cli-qq.5: The `_` dispatch and numbered cabinet pick [closed]"]
    n13["bob-cli-qq.6: Areas, Projects, Notebooks, and Albums cabinets on area and project cards [closed]"]
    n14["bob-cli-qq.7: The album Records cabinet [closed]"]
    n15["bob-cli-qq.8: Real-Obsidian acceptance and screenshot review with the gate open [in_progress]"]
    n16["bob-cli-qq.9: Switch cabinets on, docs, approved memory, and clean deploy [in_progress]"]
    n0 --> n1
    n0 --> n2
    n2 --> n3
    n2 --> n4
    n2 --> n5
    n2 --> n6
    n2 --> n7
    n2 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n0 --> n15
    n0 --> n16
    n1 -.-> n11
    n3 -.-> n6
    n4 -.-> n6
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n8
    n9 -.-> n12
    n10 -.-> n13
    n10 -.-> n14
    n11 -.-> n12
    n11 -.-> n13
    n11 -.-> n14
    n12 -.-> n15
    n13 -.-> n15
    n14 -.-> n15
    n15 -.-> n16
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.1.md) | [bob-cli-qq.1](bob-cli-qq.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.10.1.md) | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.10.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.2/README.md) | [bob-cli-qq.10.2](bob-cli-qq.10.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.10.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.10.3.md) | [bob-cli-qq.10.3](bob-cli-qq.10.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.10.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.4/README.md) | [bob-cli-qq.10.4](bob-cli-qq.10.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-qq.10.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.5/README.md) | [bob-cli-qq.10.5](bob-cli-qq.10.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-qq.10.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.6/README.md) | [bob-cli-qq.10.6](bob-cli-qq.10.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-qq.10.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.land/README.md) | [bob-cli-qq.10](bob-cli-qq.10.md) | 0 |
| [bbugyi200.apollo.bob-cli-qq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.2.md) | [bob-cli-qq.2](bob-cli-qq.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.3/README.md) | [bob-cli-qq.3](bob-cli-qq.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.4.md) | [bob-cli-qq.4](bob-cli-qq.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.5/README.md) | [bob-cli-qq.5](bob-cli-qq.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.6/README.md) | [bob-cli-qq.6](bob-cli-qq.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.7/README.md) | [bob-cli-qq.7](bob-cli-qq.7.md) | 1 |
| [bbugyi200.apollo.bob-cli-qq.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.8/README.md) | [bob-cli-qq.8](bob-cli-qq.8.md) | 8 |
| [bbugyi200.apollo.bob-cli-qq.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.9/README.md) | [bob-cli-qq.9](bob-cli-qq.9.md) | 0 |
| [bbugyi200.apollo.bob-cli-qq.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.land/README.md) | [bob-cli-qq](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c0a5c4d`](https://github.com/bobs-org/bob-plugins/commit/c0a5c4dd4dfa21eebf778834c464ae8e58b9a47f) | feat(ledger): add walker-footer overlay API | [bob-cli-qq.2](bob-cli-qq.2.md) | 2026-11-26 16:21:24 EST |
| bob-plugins | [`bob-plugins@1e29d7c`](https://github.com/bobs-org/bob-plugins/commit/1e29d7ce681c5e83db4cccdd028d292153957815) | feat(cabinets): add catalog absorption kit (bob-cli-qq.3) | [bob-cli-qq.3](bob-cli-qq.3.md) | 2026-11-26 16:40:14 EST |
| bob-plugins | [`bob-plugins@9c1123b`](https://github.com/bobs-org/bob-plugins/commit/9c1123bdf6c224d1e5cefa54ad5e5135070a907e) | feat(cabinets): add gated cabinet kit and view state | [bob-cli-qq.1](bob-cli-qq.1.md) | 2026-11-26 17:08:09 EST |
| bob-plugins | [`bob-plugins@9527ee1`](https://github.com/bobs-org/bob-plugins/commit/9527ee14e2fa4193bdd3fbc9d85017094f39ef90) | feat(ledger-tools): add cabinet plugin features and refresh docs inventory | [bob-cli-qq.4](bob-cli-qq.4.md) | 2026-11-26 20:42:29 EST |
| bob-plugins | [`bob-plugins@5e2c0bd`](https://github.com/bobs-org/bob-plugins/commit/5e2c0bd54aaeb8c6fe4012f36277f0ace0fb0bde) | feat(cabinets): add numbered cabinet pick and \_ dispatch | [bob-cli-qq.5](bob-cli-qq.5.md) | 2026-11-26 20:54:14 EST |
| bob-plugins | [`bob-plugins@6cb79d7`](https://github.com/bobs-org/bob-plugins/commit/6cb79d73bc0602ea6d5f8902783c16b7e1683912) | feat(cabinets): add the album Records cabinet | [bob-cli-qq.7](bob-cli-qq.7.md) | 2026-11-26 21:05:14 EST |
| bob-plugins | [`bob-plugins@a4bd99f`](https://github.com/bobs-org/bob-plugins/commit/a4bd99f27b1980539e7ebedf87e39c4897670f26) | feat(cabinets): add host catalog providers | [bob-cli-qq.6](bob-cli-qq.6.md) | 2026-11-26 21:46:47 EST |
| bob-plugins | [`bob-plugins@7e0ba56`](https://github.com/bobs-org/bob-plugins/commit/7e0ba5695e86ea88c4f103e682c38e342f43a701) | test(cabinets): add real Obsidian acceptance runner | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 22:14:41 EST |
| bob-plugins | [`bob-plugins@18e6cb9`](https://github.com/bobs-org/bob-plugins/commit/18e6cb9980eb028d04f8841fea9f0cd2ac85d207) | test(cabinets): retain failed real-Obsidian acceptance evidence | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 22:48:25 EST |
| bob-plugins | [`bob-plugins@bd1af86`](https://github.com/bobs-org/bob-plugins/commit/bd1af8607014226cc86b75845c5739032295643a) | fix(cabinets): add report fixtures and record properties stack | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 23:24:11 EST |
| bob-plugins | [`bob-plugins@66667b1`](https://github.com/bobs-org/bob-plugins/commit/66667b1c224fd2403f0ac7ceb9d46850d091441e) | test(cabinets): preserve attempt 4 report and attempt 5 launcher | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 23:38:01 EST |
| bob-plugins | [`bob-plugins@f279186`](https://github.com/bobs-org/bob-plugins/commit/f279186d37b5cad0054cec52bfb1e9b85d0e5f4e) | fix(cabinets): preserve Obsidian startup diagnostics | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-26 23:50:30 EST |
| bob-plugins | [`bob-plugins@e9f0c07`](https://github.com/bobs-org/bob-plugins/commit/e9f0c0703a8b10576663374883e2bb4b0ad277c2) | fix(cabinets-e2e): isolate Xvfb temporary storage | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-27 00:16:24 EST |
| bob-plugins | [`bob-plugins@c476086`](https://github.com/bobs-org/bob-plugins/commit/c476086a9a7135ad944993ed9ea0d715ec3fcddd) | fix(cabinets): repair acceptance fixtures and narrow bank layout | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-27 00:57:29 EST |
| bob-plugins | [`bob-plugins@28e7573`](https://github.com/bobs-org/bob-plugins/commit/28e7573951895c58e1917815d96e08c646b873ae) | fix(cabinets): absorb every Live Preview catalog and keep cabinet bodies painted | [bob-cli-qq.8](bob-cli-qq.8.md) | 2026-11-27 08:08:11 EST |
| bob-plugins | [`bob-plugins@b6ae31d`](https://github.com/bobs-org/bob-plugins/commit/b6ae31d8f5b89bc7898cefc79a0f21000c25dd87) | fix(cabinets): polish footer overlay and acceptance checks | [bob-cli-qq.10.3](bob-cli-qq.10.3.md) | 2026-11-27 09:28:42 EST |
| bob-plugins | [`bob-plugins@1c4266e`](https://github.com/bobs-org/bob-plugins/commit/1c4266ed9bf938e83719e47f93175e1d0a3e1eae) | fix(ledger-tools): recover Reading property cards after plugin reload | [bob-cli-qq.10.2](bob-cli-qq.10.2.md) | 2026-11-27 10:27:41 EST |
| bob-plugins | [`bob-plugins@17a64fa`](https://github.com/bobs-org/bob-plugins/commit/17a64fabb6040db49d8fd77bec404d4f513913d7) | perf(ledger-tools): defer gate-open Reading inline paint for projects/records cabinets | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 2026-11-27 10:53:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.land][1] | Check whether cabinets already knows about the atomicRanges console-error gap and stale ref gate keys in its runner | 2 |
| read-by | [agent:bob-cli-qq.10.2][2] | Need parent plan path and design contract for reading-miss | 1 |
| read-by | [agent:bob-cli-qq.5][3] | Need epic scope for phase qq.5 | 1 |
| read-by | [agent:bob-cli-qq.7][4] | need epic scope and sibling repo info | 2 |
| read-by | [agent:bob-cli-qq.8--3][5] | Confirm the parent bead scope and preserve its status as requested | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.7/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.8.md

<!-- sase:referenced-by:end -->
