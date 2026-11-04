# Bead: bob-cli-h8 — Work the top-ten task bead bundles from the two-host audit

[Bead Pages](../README.md) / bob-cli-h8

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.land`
**Created:** 2026-11-04 16:39:09 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/top_ten_bead_bundles.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md

<!-- sase:links:end -->

## Description

Every work item ranked by the 2026-11-04 two-host bead audit is done. bob-plugins `npm test` is green under UTC and New York time. `bob plugins sync` accepts a dirty deploy once its exact bundle is committed, so the vault stops running stale plugins. Obsidian closes keep recorded Pomodoro time. `bob periods brief` attributes archived and multi-link minutes correctly before the 2026-11-09 weekly Review. Vault edits stop leaking SASE plans. bob-mac-capture and bob-cli master CI are green again for the failures nobody else owns. athena alerts on hostile CPU, exec, and egress. Every link-consuming writer keeps notes, and generic ref PDFs render emoji.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-h8.1](bob-cli-h8.1.md) | Make bob-plugins npm test green | ✓ closed | medium | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.10](bob-cli-h8.10.md) | Make the brief's Still open lists honest for ended periods | ◐ in_progress | medium | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.11](bob-cli-h8.11.md) | Render emoji and uncovered symbols in generic ref PDFs | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.12](bob-cli-h8.12.md) | Bring reconcile and task\_complete consumption to capture's rules | ◐ in_progress | medium | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.13](bob-cli-h8.13.md) | Bring bob-plugins Depends-On consumption to the same rules | ◐ in_progress | medium | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.2](bob-cli-h8.2.md) | Let bob plugins sync accept committed dirty deploys | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.3](bob-cli-h8.3.md) | Fix archived-task minutes and multi-link splitting in the periods brief | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.4](bob-cli-h8.4.md) | Stop vault edits from leaking SASE plans into ~/bob | ✓ closed | small | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.5](bob-cli-h8.5.md) | Turn bob-mac-capture master CI green and record the CI-watch rule | ✓ closed | medium | 2026-11-04 | 1 | 2 |
| [bob-cli-h8.6](bob-cli-h8.6.md) | Make the highlights overwrite tests timezone-independent | ✓ closed | small | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.7](bob-cli-h8.7.md) | Alert on hostile CPU, writable-dir execution, and mining egress on athena | ◐ in_progress | medium | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.8](bob-cli-h8.8.md) | Align task-status-cycler's deferred-only close with bob | ✓ closed | small | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.9](bob-cli-h8.9.md) | Brief truncation counts, Bryan's words, and Markdown glitches | ✓ closed | medium | 2026-11-04 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-h8: Work the top-ten task bead bundles from the two-host audit [in_progress]"]
    n1["bob-cli-h8.1: Make bob-plugins npm test green [closed]"]
    n2["bob-cli-h8.10: Make the brief's Still open lists honest for ended periods [in_progress]"]
    n3["bob-cli-h8.11: Render emoji and uncovered symbols in generic ref PDFs [closed]"]
    n4["bob-cli-h8.12: Bring reconcile and task_complete consumption to capture's rules [in_progress]"]
    n5["bob-cli-h8.13: Bring bob-plugins Depends-On consumption to the same rules [in_progress]"]
    n6["bob-cli-h8.2: Let bob plugins sync accept committed dirty deploys [closed]"]
    n7["bob-cli-h8.3: Fix archived-task minutes and multi-link splitting in the periods brief [closed]"]
    n8["bob-cli-h8.4: Stop vault edits from leaking SASE plans into ~/bob [closed]"]
    n9["bob-cli-h8.5: Turn bob-mac-capture master CI green and record the CI-watch rule [closed]"]
    n10["bob-cli-h8.6: Make the highlights overwrite tests timezone-independent [closed]"]
    n11["bob-cli-h8.7: Alert on hostile CPU, writable-dir execution, and mining egress on athena [in_progress]"]
    n12["bob-cli-h8.8: Align task-status-cycler's deferred-only close with bob [closed]"]
    n13["bob-cli-h8.9: Brief truncation counts, Bryan's words, and Markdown glitches [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n1 -.-> n12
    n4 -.-> n5
    n7 -.-> n13
    n10 -.-> n3
    n12 -.-> n5
    n13 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.1.md) | [bob-cli-h8.1](bob-cli-h8.1.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.10/README.md) | [bob-cli-h8.10](bob-cli-h8.10.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.11/README.md) | [bob-cli-h8.11](bob-cli-h8.11.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.12.md) | [bob-cli-h8.12](bob-cli-h8.12.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.13/README.md) | [bob-cli-h8.13](bob-cli-h8.13.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.2/README.md) | [bob-cli-h8.2](bob-cli-h8.2.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.3/README.md) | [bob-cli-h8.3](bob-cli-h8.3.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.4/README.md) | [bob-cli-h8.4](bob-cli-h8.4.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.5.md) | [bob-cli-h8.5](bob-cli-h8.5.md) | 2 |
| [bbugyi200.athena.bob-cli-h8.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.6/README.md) | [bob-cli-h8.6](bob-cli-h8.6.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.7.md) | [bob-cli-h8.7](bob-cli-h8.7.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.8/README.md) | [bob-cli-h8.8](bob-cli-h8.8.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.9.md) | [bob-cli-h8.9](bob-cli-h8.9.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.land/README.md) | [bob-cli-h8](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ea015b6`](https://github.com/bobs-org/bob-cli/commit/ea015b665311e384c0daa6ce451c7350e72a4aa0) | fix(periods): attribute archived tasks and split multi-link minutes in brief | [bob-cli-h8.3](bob-cli-h8.3.md) | 2026-11-04 17:05:30 EST |
| bob-cli | [`53bf947`](https://github.com/bobs-org/bob-cli/commit/53bf94721d638a02106ff7a142b216a4b80e2b7f) | test(highlights): pin overwrite timezone and document recapture stamp | [bob-cli-h8.6](bob-cli-h8.6.md) | 2026-11-04 17:12:34 EST |
| bob-cli | [`d32e858`](https://github.com/bobs-org/bob-cli/commit/d32e858d581e5d2a4b7699dd622d0fb9cd518582) | feat(plugins)!: accept committed dirty deploys via inclusion proof | [bob-cli-h8.2](bob-cli-h8.2.md) | 2026-11-04 17:14:19 EST |
| bob-cli | [`0e11f8b`](https://github.com/bobs-org/bob-cli/commit/0e11f8b0e8c3974da3113fe15fd19fa3839c2368) | fix(highlights): preserve fallback glyphs in generic ref PDFs | [bob-cli-h8.11](bob-cli-h8.11.md) | 2026-11-04 17:42:48 EST |
| bob-cli | [`75bb6c6`](https://github.com/bobs-org/bob-cli/commit/75bb6c62e82526445576872e5542de2ad53bd914) | feat(periods): report brief truncation totals and clean words and aliases | [bob-cli-h8.9](bob-cli-h8.9.md) | 2026-11-04 18:39:00 EST |
| bob-cli | [`20c58da`](https://github.com/bobs-org/bob-cli/commit/20c58da9d62d034036bd6cfb0c8ceb17cac0496c) | docs(agents): tell agents to watch exact-SHA macOS CI after pushes | [bob-cli-h8.5](bob-cli-h8.5.md) | 2026-11-04 18:49:38 EST |
| bob-mac-capture | [`bob-mac-capture@47fece2`](https://github.com/bobs-org/bob-mac-capture/commit/47fece243c16eee115fbcb1b763cd56d75561d33) | fix(capture): accept Go To refetch anchored at token start, report stderr on failure | [bob-cli-h8.5](bob-cli-h8.5.md) | 2026-11-04 18:50:03 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h0.land][1] | Check whether the new audit epic already covers h5/h6/clippy and the h0 lander scope | 1 |
| read-by | [agent:bob-cli-h8.8][2] | need epic context and g4 reference | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h0.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.8/README.md

<!-- sase:referenced-by:end -->
