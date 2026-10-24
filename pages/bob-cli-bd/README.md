# Bead: bob-cli-bd — Annotation sections for ref notes (\`# Name\` + \`@name\`)

[Bead Pages](../README.md) / bob-cli-bd

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2d.linker.w0.md) · **Assignee:** `bob-cli-bd.land`
**Created:** 2026-10-24 07:59:21 EDT
**Plan:** [202610/ref\_note\_annotation\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_note_annotation_sections.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/ref_note_annotation_sections.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_note_annotation_sections.md

<!-- sase:links:end -->

## Description

A Highlights sticky note whose first line is `# Name` declares a section, and every highlight, underline, image, or sticky note tagged `@name` renders grouped under it: real headings with a quiet section card in Obsidian, native section headers in the Bob Mac Capture Refs panel, and grouped output in every `bob ref show` format. Notes that never declare a section stay byte-identical, the grouping is re-derived from the annotations on every scan (nothing new is persisted), and adding, removing, or moving a tag never changes a `^h-` ID or re-creates a task.

## Notes

[2026-10-24T13:25:53Z · bob-cli-an.6.6.6.5.land] DISCOVERED ISSUE (from bob-cli-an.6.6.6.5 lander, 2026-10-24): bob-cli master CI is red on both test jobs because of bd.1 commit 6ec2f16a (level-aware sidecar page headings). Failing nodes: tests/cli/highlights/continuations.rs::continuation_scan_tucks_two_pages_and_is_idempotent (line 218) and ::continuation_scan_reports_dangling_marker (line 313). CI run 40095684849 on 94591ea6: test (ubuntu-latest) and test (macos-latest) fail exactly these two (1992/2 and 1990/2); lint and package pass. Bisect on athena: cargo test --test cli highlights::continuations passes 3/3 at bff7bc72 (6ec2f16a^) and fails 2/3 at 6ec2f16a. Root cause: parse_sidecar_markdown now takes page_heading_level from the FIRST page-shaped heading. These fixtures start with a simple-style marker page '## Page 1' and then use linked '#### [Page 11](highlights://...)' headings, so level=2 and the #### page headings no longer split the stream; every highlight renders under '### Page 1', continuations=0, and the dangling line names Page 1. bd.1 validated only lib highlights_ref tests (631), not the CLI suite. Read-only vault scan: 0 of the live sidecars mix page-heading levels, so live impact is nil today, but the first-heading rule is fragile (a level-1 '# P values' sticky before the first real page heading would disable all page splits). The fix belongs to this epic (choose the level from linked-style or most-common page headings, or accept any level for linked [Page N](highlights://) headings), then rerun cargo test --test cli highlights::. Not caused by bob-cli-an.6.6.6.5; no task created because this active epic owns the causal commit.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-bd.1](bob-cli-bd.1.md) | Sidecar parser gates | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bd.2](bob-cli-bd.2.md) | Section grammar and pure planner | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bd.3](bob-cli-bd.3.md) | Sectioned managed-region parser | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bd.4](bob-cli-bd.4.md) | Sectioned rendering and identity | ◐ in_progress | large | 2026-10-24 | 1 | 0 |
| [bob-cli-bd.5](bob-cli-bd.5.md) | Sections in bob ref show | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bd.6](bob-cli-bd.6.md) | Section stubs, diagnostics, and route hints | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bd.7](bob-cli-bd.7.md) | Docs, Obsidian styling, and cross-surface checks | ◐ in_progress | medium | 2026-10-24 | 1 | 0 |
| [bob-cli-bd.8](bob-cli-bd.8.md) | Section headers in the Bob Mac Capture Refs panel | ✓ closed | large | 2026-10-24 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-bd: Annotation sections for ref notes (`# Name` + `@name`) [in_progress]"]
    n1["bob-cli-bd.1: Sidecar parser gates [closed]"]
    n2["bob-cli-bd.2: Section grammar and pure planner [in_progress]"]
    n3["bob-cli-bd.3: Sectioned managed-region parser [closed]"]
    n4["bob-cli-bd.4: Sectioned rendering and identity [in_progress]"]
    n5["bob-cli-bd.5: Sections in bob ref show [closed]"]
    n6["bob-cli-bd.6: Section stubs, diagnostics, and route hints [in_progress]"]
    n7["bob-cli-bd.7: Docs, Obsidian styling, and cross-surface checks [in_progress]"]
    n8["bob-cli-bd.8: Section headers in the Bob Mac Capture Refs panel [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n1 -.-> n2
    n2 -.-> n4
    n3 -.-> n4
    n3 -.-> n5
    n4 -.-> n6
    n5 -.-> n7
    n5 -.-> n8
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.1/README.md) | [bob-cli-bd.1](bob-cli-bd.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-bd.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bd.2.md) | [bob-cli-bd.2](bob-cli-bd.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-bd.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.3/README.md) | [bob-cli-bd.3](bob-cli-bd.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-bd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.4/README.md) | [bob-cli-bd.4](bob-cli-bd.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-bd.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.5/README.md) | [bob-cli-bd.5](bob-cli-bd.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-bd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.6/README.md) | [bob-cli-bd.6](bob-cli-bd.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-bd.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.7/README.md) | [bob-cli-bd.7](bob-cli-bd.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-bd.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bd.8.md) | [bob-cli-bd.8](bob-cli-bd.8.md) | 1 |
| [bbugyi200.apollo.bob-cli-bd.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bd.land/README.md) | [bob-cli-bd](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b7645d1`](https://github.com/bobs-org/bob-cli/commit/b7645d17ba1a98caf43b8607e863e16c03bb5fc1) | feat(highlights-ref): parse sectioned managed regions | [bob-cli-bd.3](bob-cli-bd.3.md) | 2026-10-24 08:22:20 EDT |
| bob-cli | [`6ec2f16`](https://github.com/bobs-org/bob-cli/commit/6ec2f16a564fe99b5582b15daa52dfdb9e785e64) | feat(highlights): keep hard-wrapped hash lines in quotes and scope page headings by level | [bob-cli-bd.1](bob-cli-bd.1.md) | 2026-10-24 08:48:27 EDT |
| bob-cli | [`94591ea`](https://github.com/bobs-org/bob-cli/commit/94591ea66d48c89fba305344c40d0df5bfceecc6) | feat(ref): group bob ref show output by annotation sections | [bob-cli-bd.5](bob-cli-bd.5.md) | 2026-10-24 08:51:41 EDT |
| bob-mac-capture | [`bob-mac-capture@f9cd88a`](https://github.com/bobs-org/bob-mac-capture/commit/f9cd88add5f2b4bdb8ca5a0dffde9b42617b7253) | feat(refs): present annotation sections in the inspector and Copy card | [bob-cli-bd.8](bob-cli-bd.8.md) | 2026-10-24 09:48:43 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.land][1] | Active epic causally linked to master CI break (6ec2f16a level-aware page headings break continuations CLI tests); check scope and notes before DISCOVERED ISSUE note | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.land/README.md

<!-- sase:referenced-by:end -->
