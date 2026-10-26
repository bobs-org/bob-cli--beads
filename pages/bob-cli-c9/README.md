# Bead: bob-cli-c9 — bob ref create -f\|--force\[=reread\|overwrite\]: recapture a source you already have

[Bead Pages](../README.md) / bob-cli-c9

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14a.md) · **Assignee:** `bob-cli-c9.land`
**Created:** 2026-10-25 14:15:31 EDT
**Plan:** [202610/ref\_create\_force\_recapture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_force_recapture.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/ref_create_force_recapture.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_force_recapture.md

<!-- sase:links:end -->

## Description

A source that is already a reference can be captured again on purpose. Bare -f adds a new <root>__vN reading linked to the earlier ones. -f overwrite recaptures a reference in place and keeps its path, id, and reading task. Before that, anything you made in the old note is frozen into ref_history/. Without -f, a duplicate is refused before any fetch, with one clear message that names the existing copies and the exact fix.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-c9.1](bob-cli-c9.1.md) | Reading families in the library read model | ✓ closed | medium | 2026-10-25 | 1 | 1 |
| [bob-cli-c9.2](bob-cli-c9.2.md) | One already-captured refusal, before parent resolution | ✓ closed | medium | 2026-10-25 | 1 | 1 |
| [bob-cli-c9.3](bob-cli-c9.3.md) | The --force\[=MODE\] parser and bare -f reread | ✓ closed | large | 2026-10-25 | 1 | 0 |
| [bob-cli-c9.4](bob-cli-c9.4.md) | In-place overwrite of unannotated references | ✓ closed | large | 2026-10-25 | 1 | 0 |
| [bob-cli-c9.5](bob-cli-c9.5.md) | Annotated overwrite on the Mac | ◐ in_progress | large | 2026-10-25 | 1 | 0 |
| [bob-cli-c9.6](bob-cli-c9.6.md) | Decision record, glossary correction, and final docs pass | ◐ in_progress | small | 2026-10-25 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-c9: bob ref create -f|--force[=reread|overwrite]: recapture a source you already have [in_progress]"]
    n1["bob-cli-c9.1: Reading families in the library read model [closed]"]
    n2["bob-cli-c9.2: One already-captured refusal, before parent resolution [closed]"]
    n3["bob-cli-c9.3: The --force[=MODE] parser and bare -f reread [closed]"]
    n4["bob-cli-c9.3.1: Complete ref create force-mode parsing and rereads [closed]"]
    n5["bob-cli-c9.3.1.1: Parse recapture modes and preserve existing force behavior [closed]"]
    n6["bob-cli-c9.3.1.2: Resolve capture families and allocate complete reread bundles [closed]"]
    n7["bob-cli-c9.3.1.3: Derive lineage and preserve reading identity during intake [closed]"]
    n8["bob-cli-c9.3.1.4: Enable rereads for single files, URLs, and note snapshots [closed]"]
    n9["bob-cli-c9.3.1.5: Finish collection rereads and the public contract [closed]"]
    n10["bob-cli-c9.3.1.6: Finish ref create rereads - landing fixes for bob-cli-c9.3.1 [closed]"]
    n11["bob-cli-c9.3.1.6.1: Locked reread recheck for audio units, full scan, and previews [closed]"]
    n12["bob-cli-c9.3.1.6.2: Identity-correct family matching and attach targets [closed]"]
    n13["bob-cli-c9.3.1.6.3: Route guards, audio, vault ordering, redirects, and parser edges [closed]"]
    n14["bob-cli-c9.3.1.6.4: Docs, cleanup, test hardening, and acceptance evidence [closed]"]
    n15["bob-cli-c9.4: In-place overwrite of unannotated references [closed]"]
    n16["bob-cli-c9.4.1: In-place overwrite of unannotated references [closed]"]
    n17["bob-cli-c9.4.1.1: Share reference mutation safety primitives with rename [closed]"]
    n18["bob-cli-c9.4.1.2: Plan overwrite selection and inert prose archives [closed]"]
    n19["bob-cli-c9.4.1.3: Recover interrupted overwrites from host-local intents [closed]"]
    n20["bob-cli-c9.4.1.4: Apply and verify a staged overwrite in one scoped commit [closed]"]
    n21["bob-cli-c9.4.1.5: Enable local-file and vault-snapshot overwrite [closed]"]
    n22["bob-cli-c9.4.1.6: Enable single-URL overwrite across web capture routes [closed]"]
    n23["bob-cli-c9.4.1.7: Enable exact-set collection overwrite and complete remedies [closed]"]
    n24["bob-cli-c9.4.1.8: Verify overwrite preservation and crash recovery end to end [closed]"]
    n25["bob-cli-c9.4.1.9: Finish unannotated overwrite - contract fixes and transaction hardening [closed]"]
    n26["bob-cli-c9.4.1.9.1: Fix overwrite selection, refusals, and refusal coverage [closed]"]
    n27["bob-cli-c9.4.1.9.2: Preserve task alias, user fields, and audio; align output and docs [closed]"]
    n28["bob-cli-c9.4.1.9.3: Harden the overwrite transaction and prove it with failpoints [closed]"]
    n29["bob-cli-c9.5: Annotated overwrite on the Mac [in_progress]"]
    n30["bob-cli-c9.5.1: Annotated reference overwrite on the Mac [in_progress]"]
    n31["bob-cli-c9.5.1.1: Plan annotated archives and selective highlight links [closed]"]
    n32["bob-cli-c9.5.1.2: Hold scans that encounter a replaced annotated PDF [closed]"]
    n33["bob-cli-c9.5.1.3: Recover transactions that renamed annotated bundles [closed]"]
    n34["bob-cli-c9.5.1.4: Enable coordinated annotated overwrite [closed]"]
    n35["bob-cli-c9.5.1.5: Verify user behavior and extend Mac acceptance documentation [in_progress]"]
    n36["bob-cli-c9.6: Decision record, glossary correction, and final docs pass [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n3 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n4 --> n8
    n4 --> n9
    n4 --> n10
    n10 --> n11
    n10 --> n12
    n10 --> n13
    n10 --> n14
    n0 --> n15
    n15 --> n16
    n16 --> n17
    n16 --> n18
    n16 --> n19
    n16 --> n20
    n16 --> n21
    n16 --> n22
    n16 --> n23
    n16 --> n24
    n16 --> n25
    n25 --> n26
    n25 --> n27
    n25 --> n28
    n0 --> n29
    n29 --> n30
    n30 --> n31
    n30 --> n32
    n30 --> n33
    n30 --> n34
    n30 --> n35
    n0 --> n36
    n1 -.-> n3
    n2 -.-> n3
    n3 -.-> n15
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n8
    n8 -.-> n9
    n11 -.-> n12
    n12 -.-> n13
    n13 -.-> n14
    n15 -.-> n29
    n17 -.-> n18
    n17 -.-> n19
    n18 -.-> n20
    n19 -.-> n20
    n20 -.-> n21
    n21 -.-> n22
    n22 -.-> n23
    n23 -.-> n24
    n26 -.-> n27
    n27 -.-> n28
    n29 -.-> n36
    n31 -.-> n32
    n31 -.-> n33
    n31 -.-> n34
    n32 -.-> n34
    n33 -.-> n34
    n34 -.-> n35
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.1/README.md) | [bob-cli-c9.1](bob-cli-c9.1.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.2/README.md) | [bob-cli-c9.2](bob-cli-c9.2.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.md) | [bob-cli-c9.3](bob-cli-c9.3.md) | 0 |
| [bbugyi200.athena.bob-cli-c9.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.1/README.md) | [bob-cli-c9.3.1.1](bob-cli-c9.3.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.2/README.md) | [bob-cli-c9.3.1.2](bob-cli-c9.3.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.3/README.md) | [bob-cli-c9.3.1.3](bob-cli-c9.3.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.4/README.md) | [bob-cli-c9.3.1.4](bob-cli-c9.3.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.5/README.md) | [bob-cli-c9.3.1.5](bob-cli-c9.3.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.6.1/README.md) | [bob-cli-c9.3.1.6.1](bob-cli-c9.3.1.6.1.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.6.2.md) | [bob-cli-c9.3.1.6.2](bob-cli-c9.3.1.6.2.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.6.3/README.md) | [bob-cli-c9.3.1.6.3](bob-cli-c9.3.1.6.3.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.6.4/README.md) | [bob-cli-c9.3.1.6.4](bob-cli-c9.3.1.6.4.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.3.1.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.6.land.md) | [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) | 2 |
| [bbugyi200.athena.bob-cli-c9.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.land.md) | [bob-cli-c9.3.1](bob-cli-c9.3.1.md) | 0 |
| [bbugyi200.athena.bob-cli-c9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.md) | [bob-cli-c9.4](bob-cli-c9.4.md) | 0 |
| [bbugyi200.athena.bob-cli-c9.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.1/README.md) | [bob-cli-c9.4.1.1](bob-cli-c9.4.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.2.md) | [bob-cli-c9.4.1.2](bob-cli-c9.4.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.3/README.md) | [bob-cli-c9.4.1.3](bob-cli-c9.4.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.4/README.md) | [bob-cli-c9.4.1.4](bob-cli-c9.4.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.5/README.md) | [bob-cli-c9.4.1.5](bob-cli-c9.4.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.6/README.md) | [bob-cli-c9.4.1.6](bob-cli-c9.4.1.6.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.7.md) | [bob-cli-c9.4.1.7](bob-cli-c9.4.1.7.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.8/README.md) | [bob-cli-c9.4.1.8](bob-cli-c9.4.1.8.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.9.1/README.md) | [bob-cli-c9.4.1.9.1](bob-cli-c9.4.1.9.1.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.9.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.9.2/README.md) | [bob-cli-c9.4.1.9.2](bob-cli-c9.4.1.9.2.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.9.3/README.md) | [bob-cli-c9.4.1.9.3](bob-cli-c9.4.1.9.3.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.4.1.9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.9.land.md) | [bob-cli-c9.4.1.9](bob-cli-c9.4.1.9.md) | 2 |
| [bbugyi200.athena.bob-cli-c9.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.land.md) | [bob-cli-c9.4.1](bob-cli-c9.4.1.md) | 0 |
| [bbugyi200.athena.bob-cli-c9.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.md) | [bob-cli-c9.5](bob-cli-c9.5.md) | 0 |
| [bbugyi200.athena.bob-cli-c9.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.1/README.md) | [bob-cli-c9.5.1.1](bob-cli-c9.5.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.1.2.md) | [bob-cli-c9.5.1.2](bob-cli-c9.5.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.3/README.md) | [bob-cli-c9.5.1.3](bob-cli-c9.5.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.4/README.md) | [bob-cli-c9.5.1.4](bob-cli-c9.5.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-c9.5.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.5/README.md) | [bob-cli-c9.5.1.5](bob-cli-c9.5.1.5.md) | 0 |
| [bbugyi200.athena.bob-cli-c9.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.land/README.md) | [bob-cli-c9.5.1](bob-cli-c9.5.1.md) | 0 |
| [bbugyi200.athena.bob-cli-c9.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.6/README.md) | [bob-cli-c9.6](bob-cli-c9.6.md) | 0 |
| [bbugyi200.athena.bob-cli-c9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.land/README.md) | [bob-cli-c9](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e852198`](https://github.com/bobs-org/bob-cli/commit/e852198de298a5cc138c26c183f0f5597d2f9b13) | feat(ref): one already-captured refusal, before parent resolution | [bob-cli-c9.2](bob-cli-c9.2.md) | 2026-10-25 14:58:17 EDT |
| bob-cli | [`16f86b7`](https://github.com/bobs-org/bob-cli/commit/16f86b7df6d9e8ee69822404ada9092ba8220339) | feat(ref): reading families in the library read model | [bob-cli-c9.1](bob-cli-c9.1.md) | 2026-10-25 15:05:38 EDT |
| bob-cli | [`2e08351`](https://github.com/bobs-org/bob-cli/commit/2e08351e893b59f79aa6de7f3c663db1000f640f) | feat(highlights): add force parser with reread/overwrite modes | [bob-cli-c9.3.1.1](bob-cli-c9.3.1.1.md) | 2026-10-25 16:22:11 EDT |
| bob-cli | [`347c36b`](https://github.com/bobs-org/bob-cli/commit/347c36b1c7add475a8a3a739dc1f024db7d7aebd) | feat(highlights): read-only family planning recapture with no reread writes | [bob-cli-c9.3.1.2](bob-cli-c9.3.1.2.md) | 2026-10-25 17:00:04 EDT |
| bob-cli | [`291efa6`](https://github.com/bobs-org/bob-cli/commit/291efa6b374695cace353fab593504d5c0cc6600) | feat(highlights): derive birth earlier lineage and reading-aware ref task IDs | [bob-cli-c9.3.1.3](bob-cli-c9.3.1.3.md) | 2026-10-25 17:53:00 EDT |
| bob-cli | [`499294b`](https://github.com/bobs-org/bob-cli/commit/499294b3fa35a2a01a4b4173ed8bc9fea9764ae9) | feat(ref)!: enable rereads for single files, URLs, and note snapshots | [bob-cli-c9.3.1.4](bob-cli-c9.3.1.4.md) | 2026-10-25 18:45:24 EDT |
| bob-cli | [`9923063`](https://github.com/bobs-org/bob-cli/commit/9923063e3288b15380c6da99f3d877911d6b7944) | feat(highlights): collection rereads use shared recapture preflight | [bob-cli-c9.3.1.5](bob-cli-c9.3.1.5.md) | 2026-10-25 19:16:13 EDT |
| bob-cli | [`c192014`](https://github.com/bobs-org/bob-cli/commit/c192014eeede15b4a87079787ade257372ec575c) | fix(ref): recheck locked reread intake occupancy | [bob-cli-c9.3.1.6.1](bob-cli-c9.3.1.6.1.md) | 2026-10-25 20:00:58 EDT |
| bob-cli | [`e35773e`](https://github.com/bobs-org/bob-cli/commit/e35773e533dc567a5f45a6bc12bb01b96b21e0d0) | fix(ref): preserve family identity for rereads | [bob-cli-c9.3.1.6.2](bob-cli-c9.3.1.6.2.md) | 2026-10-25 20:30:46 EDT |
| bob-cli | [`d96ed41`](https://github.com/bobs-org/bob-cli/commit/d96ed412085581c4b49456c6672bd26db4fc9592) | feat(highlights-ref): add route guards for create/clip overwrite, redirect, and narrated hints | [bob-cli-c9.3.1.6.3](bob-cli-c9.3.1.6.3.md) | 2026-10-25 21:12:26 EDT |
| bob-cli | [`516d7b9`](https://github.com/bobs-org/bob-cli/commit/516d7b98fe31311470d6cce1bd61dc3d81ce0665) | fix(ref): contract docs, cleanup, and reread test hardening | [bob-cli-c9.3.1.6.4](bob-cli-c9.3.1.6.4.md) | 2026-10-25 21:39:53 EDT |
| bob-cli | [`b48bd93`](https://github.com/bobs-org/bob-cli/commit/b48bd939cb33a5c5a6e9afea690bc4bed06fc3f4) | fix(ref): name newest narrated reading and resolve exact-output overwrite paths | [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) | 2026-10-25 22:22:43 EDT |
| bob-cli--plans | [`bob-cli--plans@3afa34a`](https://github.com/bobs-org/bob-cli--plans/commit/3afa34ac5cfd9e7f1855199c272b51e99e4ddcad) | chore(plans): mark reread landing and create-reread plans done | [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) | 2026-10-25 22:23:40 EDT |
| bob-cli | [`6196cea`](https://github.com/bobs-org/bob-cli/commit/6196cea7b90f6648a80a9c5099611c1598b3cd40) | refactor(ref): extract shared reference mutation safety primitives | [bob-cli-c9.4.1.1](bob-cli-c9.4.1.1.md) | 2026-10-25 22:59:23 EDT |
| bob-cli | [`07d5a18`](https://github.com/bobs-org/bob-cli/commit/07d5a18d1057e337a969e71741bc756a964c519f) | feat(highlights-ref): durable overwrite-intent lifecycle with recovery | [bob-cli-c9.4.1.3](bob-cli-c9.4.1.3.md) | 2026-10-25 23:29:51 EDT |
| bob-cli | [`419e84f`](https://github.com/bobs-org/bob-cli/commit/419e84f31ab6519eed507dc04bbb33a086842450) | feat(ref): prepare safe in-place overwrite preflight | [bob-cli-c9.4.1.2](bob-cli-c9.4.1.2.md) | 2026-10-25 23:52:53 EDT |
| bob-cli | [`8e35872`](https://github.com/bobs-org/bob-cli/commit/8e35872b95c965abf2f45cef45fa3201c509435d) | feat(ref): apply staged overwrite in scoped transaction | [bob-cli-c9.4.1.4](bob-cli-c9.4.1.4.md) | 2026-10-26 00:29:41 EDT |
| bob-cli | [`00200a9`](https://github.com/bobs-org/bob-cli/commit/00200a967fa818fc0f2c40135bc7cc49d2ce927c) | feat(highlights): enable local-file and vault-snapshot overwrite | [bob-cli-c9.4.1.5](bob-cli-c9.4.1.5.md) | 2026-10-26 01:21:22 EDT |
| bob-cli | [`57e74dc`](https://github.com/bobs-org/bob-cli/commit/57e74dcab9aa1432aea4bb0322d65fa270935148) | feat(highlights): enable single-URL overwrite across web capture routes | [bob-cli-c9.4.1.6](bob-cli-c9.4.1.6.md) | 2026-10-26 01:50:59 EDT |
| bob-cli | [`c8a255b`](https://github.com/bobs-org/bob-cli/commit/c8a255b48d55d32f892e2a7f8ceb25fa7df626a1) | feat(highlights): enable collection overwrite | [bob-cli-c9.4.1.7](bob-cli-c9.4.1.7.md) | 2026-10-26 02:27:17 EDT |
| bob-cli | [`94abe3d`](https://github.com/bobs-org/bob-cli/commit/94abe3d98061c8642c7b91d9975999afeeed269e) | test(highlights): verify overwrite preservation and crash recovery | [bob-cli-c9.4.1.8](bob-cli-c9.4.1.8.md) | 2026-10-26 03:01:15 EDT |
| bob-cli | [`3e9da7c`](https://github.com/bobs-org/bob-cli/commit/3e9da7cc63731672dbe04794a2520b72ca7feb94) | fix(highlights): honor overwrite selection and refusal contracts | [bob-cli-c9.4.1.9.1](bob-cli-c9.4.1.9.1.md) | 2026-10-26 04:30:31 EDT |
| bob-cli | [`43f8aff`](https://github.com/bobs-org/bob-cli/commit/43f8aff5d0a39b8c982fe7048e6839d86406c0fe) | feat(highlights): overwrite local and web routes with alias preservation | [bob-cli-c9.4.1.9.2](bob-cli-c9.4.1.9.2.md) | 2026-10-26 05:26:32 EDT |
| bob-cli | [`66f9d67`](https://github.com/bobs-org/bob-cli/commit/66f9d67f6573048b76a1d34274a95e7fc4b438c2) | fix(highlights): harden overwrite recovery, selection recheck, and failpoints | [bob-cli-c9.4.1.9.3](bob-cli-c9.4.1.9.3.md) | 2026-10-26 06:26:32 EDT |
| bob-cli | [`4ee76d1`](https://github.com/bobs-org/bob-cli/commit/4ee76d114ab76a912350cf62bbe2acea29d87fd7) | fix(highlights): repair overwrite identity, narration, selection, and rollback proof | [bob-cli-c9.4.1.9](bob-cli-c9.4.1.9.md) | 2026-10-26 07:27:34 EDT |
| bob-cli--plans | [`bob-cli--plans@f749cce`](https://github.com/bobs-org/bob-cli--plans/commit/f749cce3c55cf2fdaa7e2b87d1396b2be628a783) | docs(plans): mark overwrite landing and unannotated plans done | [bob-cli-c9.4.1.9](bob-cli-c9.4.1.9.md) | 2026-10-26 07:28:17 EDT |
| bob-cli | [`e482520`](https://github.com/bobs-org/bob-cli/commit/e482520841bdc4939290066569d0972f41538287) | feat(ref): plan annotated overwrite archives and highlight links | [bob-cli-c9.5.1.1](bob-cli-c9.5.1.1.md) | 2026-10-26 08:11:04 EDT |
| bob-cli | [`564168f`](https://github.com/bobs-org/bob-cli/commit/564168f3a8c29d7bb55a5009d0906a27bf1a497c) | feat(ref): recover annotated overwrite transactions that renamed bundles | [bob-cli-c9.5.1.3](bob-cli-c9.5.1.3.md) | 2026-10-26 08:55:40 EDT |
| bob-cli | [`af41608`](https://github.com/bobs-org/bob-cli/commit/af416080dc14480e6ad9cf1a19e3b043fd8dd22b) | fix(highlights): hold replaced annotated captures | [bob-cli-c9.5.1.2](bob-cli-c9.5.1.2.md) | 2026-10-26 09:00:39 EDT |
| bob-cli | [`ca6065a`](https://github.com/bobs-org/bob-cli/commit/ca6065af5ac55b802793952d95459b0d29cbe622) | feat(highlights): support coordinated annotated overwrite | [bob-cli-c9.5.1.4](bob-cli-c9.5.1.4.md) | 2026-10-26 09:46:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.land][1] | Check plan ownership overlap with batch-12 candidates | 2 |
| read-by | [agent:bob-cli-c9.1][2] | Need epic scope for family phase | 1 |
| read-by | [agent:bob-cli-c9.2][3] | parent epic scope | 1 |
| read-by | [agent:bob-cli-c9.3.1.6.land--1][4] | Confirm parent epic stays open and later phases remain in progress | 1 |
| read-by | [agent:bob-cli-c9.5.1.3][5] | Need outer epic decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.6.land.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.3/README.md

<!-- sase:referenced-by:end -->
