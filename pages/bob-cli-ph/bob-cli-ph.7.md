# Bead: bob-cli-ph.7 — Obsidian drawer rendering, typing, and bold writers

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.7` · **Size:** large
**Created:** 2026-11-22 17:36:49 EST · **Closed:** 2026-11-25 18:56:13 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

obsidian-drawers: the drawer glyph and true-case title in Live Preview and reading view, the `*` typing assists and Toggle Drawer, bold plugin writers, and verbatim promotion and reversal.

## Notes

[2026-11-25T13:56:30Z · bob-cli-q4.2] Coordination note from bob-cli-q4.2 (open-lines / upcoming notes-key) for o / O / Ctrl+Shift+O in task-status-cycler:

1. Keep taskBlockEnsureNotesDrawer and the insert planners callable as pure functions that report whether they created the drawer, so Ctrl+Shift+O on a req-owning task can reuse them and auto-prune an empty newly materialized Notes drawer if the user exits insert mode without typing.
2. Make the * assist work on a freshly opened drawer-indent sibling (which o on an existing drawer header will emit).
3. Keep Smart Enter as "child inside the drawer". o opens a sibling after the drawer's subtree; Ctrl+Shift+O / Smart Enter open a child. The three stay orthogonal.
4. notes-key (bob-cli-q4.12, Ctrl+Shift+O) lands after ph.7 so it inherits drawer spelling from the shared helpers rather than hard-coding NOTES or **Notes** bytes.

[2026-11-25T18:16:09Z · bob-cli-ph.7.1.land] Historical deployment source SHAs resolved by ph.7.1 land audit after finalizers: bob-plugins f2e8c62a29464701cb097233579c156964cb4996 implements bold-writes marker in task-status-cycler/navigation; 2796d63dc79b3c5e44d113a5b2aae4bbc2ee4ad8 plus export fix 5ed3bd22 implement ledger drawer-render marker; 8d3c555c61041065281b74259086b82633719c47 plus 8254caa48938b49b73cd4187c216406d1e3f5fea implement drawer-typing marker and Prec.highest. Phase acceptance reports prior non-forcing deploys and durable report e9988819 plus four screenshot refs already attached here. Not declaring rollout-ready: nested epic has confirmed title-whitespace, stale assertions and tray/strike/folded-count acceptance gaps. A single medium repair tale will update deploy evidence, close ph.7.1 and then only this phase; no future SHA/CI wait is required for that same-turn close.

[2026-11-25T23:56:49Z · bob-cli-ph.7.1.land--7] Deployment verification: plugin id bob-ledger-tools at exact revision ea3bc6a42500cb93ea77f69f4e50fbd7adf44261, deployed to Apollo by bob plugins sync --repo ... --no-pull -p bob-ledger-tools. Apollo stamp reports dirty=clean and complete; deployed bundle contains bob-task-drawer-render-v1. Exact-SHA npm test rerun 0vkpsfthmhye passed (9685 main pass, 5 skipped, performance 26/26); build and validate passed. Docs:check's four word-budget errors are clean-baseline overages corroborated by bob-cli-q6.4 and bob-cli-q7.2; plugin-apis is warning-only. Report and all four screenshots are attached.

## References

- file:explicit:e9988819b2a7e52753c34291
- file:explicit:99c1ffea61076da96225acc2
- file:explicit:a95e8a34e6fb850dac4ed7ce
- file:explicit:d0f7de1722a08229a8ef40a4
- file:explicit:e51daf687f9c74c956f3709f
- file:explicit:7d1382945a7925b0c31918ec
- file:explicit:e5eff65dbb95130799331a0d
- file:explicit:dd053632f1ae33b646f71e15
- file:explicit:e66c8c4d308eb70022271092
- file:explicit:feac1be20bb6aa1d6571c489
- file:explicit:22401646d913918cad305ac5
- file:explicit:42000cab6117ad14d45cbcd9
- file:explicit:c9eb02d67786acc3f37bc5d3
- file:explicit:b4eb9c7bdacd8f1c4adca9fa
- file:explicit:d3609bf8b5367af587438fe8
- file:explicit:264a2179214d204058bfe90b
- file:explicit:9305afba3e03592417e35d5c
- file:explicit:b1271577a9fd765671e79e8e
- file:explicit:4c03d1781aa3b399c23209ee
- file:explicit:ec391b9d72e4e35769fde38f

## Dependencies

- **Depends on:** [bob-cli-ph.4](bob-cli-ph.4.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.9](bob-cli-ph.9.md) ◐ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pq.5](../bob-cli-pq/bob-cli-pq.5.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.md) | [bob-cli-ph.7](bob-cli-ph.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-ph.7.1.4][2] | Need prior phase notes, markers, deploy evidence, and remaining work | 1 |
| read-by | [agent:bob-cli-ph.7.1.land--1][3] | Need parent phase status and coordination notes | 1 |
| read-by | [agent:bob-cli-ph.7.1.land--2][3] | Review epic scope and closeout requirements for drawer landing repairs | 2 |
| read-by | [agent:bob-cli-ph.7.1.land--3][3] | Need current drawer epic status and phase children for closeout | 1 |
| read-by | [agent:bob-cli-ph.7.1.land--7][3] | Verify drawer epic bead status and scope before attaching evidence and closing | 3 |
| read-by | [agent:bob-cli-pq.1][4] | sequencing check for glyph-contract | 2 |
| read-by | [agent:bob-cli-pq.3][5] | Check prerequisite drawer implementation and remaining integration | 1 |
| read-by | [agent:bob-cli-q4.2][6] | Need ph.7 status before leaving the open-lines coordination note | 1 |
| read-by | [agent:g1][7] | Check whether phase is blocked on the release gate | 1 |
| read-by | [agent:research.66.cld][8] | Check overlap of drawer typing/writers with better-o Ctrl+Shift+O design | 2 |
| read-by | [agent:research.66.grk][9] | Need drawer-writer sequencing so better-o can leave the right note on bob-cli-ph | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.1/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.3/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q4.2/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.cld/README.md
[9]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.grk/README.md

<!-- sase:referenced-by:end -->
