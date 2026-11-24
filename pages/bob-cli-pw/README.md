# Bead: bob-cli-pw — Meeting notes become event-linked references

[Bead Pages](../README.md) / bob-cli-pw

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.65.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.65.linker.w0.md) · **Assignee:** `bob-cli-pw.land`
**Created:** 2026-11-24 10:38:46 EST
**Plan:** [202611/meeting\_notes\_event\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/meeting_notes_event_refs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/meeting_notes_event_refs.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/meeting_notes_event_refs.md

<!-- sase:links:end -->

## Description

One deliberate gesture, from the CLI, Obsidian, or Bob Mac Capture, files AI meeting notes (Wispr Flow first, any producer) as a `meetings` reference. The reference is filed under the meeting's area or project, gets a searchable recap and a polished dossier PDF, and has a Next reading task related `notes from` its Event Task. The `~/tmp/bryan_derrick_meet_notes.txt` notes are filed onto `20261123#^bryan-bugyi-derrick` this way as the first use case.

## Notes

[2026-11-24T16:59:46Z · 1fq--code] DISCOVERED ISSUE (from fix_meetings_build plan step 7): render_recap output layout differs from the epic contract in plan:202611/meeting_notes_event_refs.md ('The recap region'). Contract specifies a '## Notes' heading, a '> [!summary] TL;DR' callout, and '###' sub-headings; current render_recap emits a meta line, a plain TL;DR paragraph, and '##' headings copying the notes' own levels. Left as-is in the committed goldens under tests/fixtures/meetings/golden/ (recap_wispr.md, recap_adversarial.md). A later meeting phase should align the recap layout with the epic contract before recap regions are written into vault notes.

[2026-11-24T17:06:33Z · bob-cli-pl.1--4] DISCOVERED ISSUE: Conflict-repair verification of main rebased onto dbf405e397b7081c5c5531590608637346e49dfc reproduced meeting-module build failures in sase tool run check (ToolRun f4df3fa669a8de2c5c803661f5c8db6c, exit 101). src/native/meetings/dossier.rs:348 class_fence lacks the returned borrow lifetime (E0106); normalize.rs:242 passes &str to parse_next_step(String) (E0308); mod.rs:19-26 reexports unused items denied by the canonical -D unused gate. git diff HEAD -- src/native/meetings is empty, so these are inherited from dbf405e3, not the props conflict repair. The gate stops before tests. Search across task types found no duplicate; causal owner is bob-cli-pw.1. The existing fix_meetings_build work mentioned in note 1 may already address these; record this as independent reproduction on the older integrated base, not a new request to duplicate that work.

[2026-11-24T17:22:00Z · bob-cli-pl.1--4] DISCOVERED ISSUE: Additional impact of note #2 during bob-plugins conflict repair. BOB_CLI_DIR pointing at clean bob-cli 31131fe2 npm run docs:check (from bob-plugins) passed mounted-doc lint, drift, strict Zensical build, published URLs, offline links, edit links and search smoke, then exited 2 at executable tutorial because cargo build --locked --bin bob exited 101: dossier.rs:348 class_fence E0106 and normalize.rs:242 parse_next_step E0308. No bob-cli files changed in this repair. This corroborates the older-base build blocker already owned by pw.1; no duplicate task or fix request.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-pw.1](bob-cli-pw.1.md) | Structural notes normalizer, dossier source, and recap renderer | ✓ closed | medium | 2026-11-24 | 1 | 2 |
| [bob-cli-pw.2](bob-cli-pw.2.md) | Event Task resolution, matching, recent-meetings listing, and agenda notes state | ✓ closed | medium | 2026-11-24 | 1 | 1 |
| [bob-cli-pw.3](bob-cli-pw.3.md) | Meeting dossier print profile | ◐ in_progress | medium | 2026-11-24 | 1 | 0 |
| [bob-cli-pw.4](bob-cli-pw.4.md) | Marker-carried meeting identity births the LINKS relation and recap | ✓ closed | medium | 2026-11-24 | 1 | 1 |
| [bob-cli-pw.5](bob-cli-pw.5.md) | The \`bob ref meet\` command | ◐ in_progress | large | 2026-11-24 | 1 | 0 |
| [bob-cli-pw.6](bob-cli-pw.6.md) | File the first meeting's notes | ◐ in_progress | small | 2026-11-24 | 1 | 0 |
| [bob-cli-pw.7](bob-cli-pw.7.md) | Obsidian surfaces for meeting notes | ◐ in_progress | medium | 2026-11-24 | 1 | 0 |
| [bob-cli-pw.8](bob-cli-pw.8.md) | Bob Mac Capture meeting-notes mode and Meetings kind | ◐ in_progress | large | 2026-11-24 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-pw: Meeting notes become event-linked references [in_progress]"]
    n1["bob-cli-pw.1: Structural notes normalizer, dossier source, and recap renderer [closed]"]
    n2["bob-cli-pw.2: Event Task resolution, matching, recent-meetings listing, and agenda notes state [closed]"]
    n3["bob-cli-pw.3: Meeting dossier print profile [in_progress]"]
    n4["bob-cli-pw.4: Marker-carried meeting identity births the LINKS relation and recap [closed]"]
    n5["bob-cli-pw.5: The `bob ref meet` command [in_progress]"]
    n6["bob-cli-pw.6: File the first meeting's notes [in_progress]"]
    n7["bob-cli-pw.7: Obsidian surfaces for meeting notes [in_progress]"]
    n8["bob-cli-pw.8: Bob Mac Capture meeting-notes mode and Meetings kind [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n1 -.-> n3
    n1 -.-> n4
    n2 -.-> n5
    n3 -.-> n5
    n4 -.-> n5
    n5 -.-> n6
    n5 -.-> n7
    n5 -.-> n8
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.1.md) | [bob-cli-pw.1](bob-cli-pw.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-pw.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.2/README.md) | [bob-cli-pw.2](bob-cli-pw.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-pw.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.3/README.md) | [bob-cli-pw.3](bob-cli-pw.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-pw.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.4/README.md) | [bob-cli-pw.4](bob-cli-pw.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-pw.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.5/README.md) | [bob-cli-pw.5](bob-cli-pw.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-pw.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.6/README.md) | [bob-cli-pw.6](bob-cli-pw.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-pw.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.7/README.md) | [bob-cli-pw.7](bob-cli-pw.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-pw.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.8/README.md) | [bob-cli-pw.8](bob-cli-pw.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-pw.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.land/README.md) | [bob-cli-pw](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dbf405e`](https://github.com/bobs-org/bob-cli/commit/dbf405e397b7081c5c5531590608637346e49dfc) | feat(meetings): add notes normalization and rendering | [bob-cli-pw.1](bob-cli-pw.1.md) | 2026-11-24 11:11:34 EST |
| bob-cli | [`b832e58`](https://github.com/bobs-org/bob-cli/commit/b832e58df449d9d422a488f1d8f3bf0828a93487) | feat(meetings): add read-only meeting resolver and agenda wiring | [bob-cli-pw.2](bob-cli-pw.2.md) | 2026-11-24 12:52:20 EST |
| bob-cli | [`e5169b8`](https://github.com/bobs-org/bob-cli/commit/e5169b814083d717ab3df15f4adf6ec61a446d01) | fix(meetings): satisfy strict lint checks | [bob-cli-pw.1](bob-cli-pw.1.md) | 2026-11-24 13:13:31 EST |
| bob-cli | [`923df1a`](https://github.com/bobs-org/bob-cli/commit/923df1a63e771bcaa13488b3e0bc64152b97cac4) | feat(meetings): marker-carried meeting identity births LINKS relation and recap | [bob-cli-pw.4](bob-cli-pw.4.md) | 2026-11-24 14:06:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.1--4][1] | Confirm the meeting epic owns the compile errors blocking mounted plugin docs checks | 2 |
| read-by | [agent:bob-cli-pw.2][2] | Need parent epic scope and plan pointer | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.2/README.md

<!-- sase:referenced-by:end -->
