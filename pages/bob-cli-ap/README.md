# Bead: bob-cli-ap — Tucked continuation groups — keep every \`\<\` highlight distinct inside its group

[Bead Pages](../README.md) / bob-cli-ap

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12y.md) · **Assignee:** `bob-cli-ap.land`
**Created:** 2026-10-23 05:11:20 EDT · **Closed:** 2026-10-23 07:17:15 EDT
**Plan:** [202610/tucked\_continuation\_groups.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/tucked_continuation_groups.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/tucked_continuation_groups.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/tucked_continuation_groups.md

<!-- sase:links:end -->

## Description

A `<` note groups a highlight with the one before it without erasing either: the group renders as one quote card under one heading and one `^h-` ID, and inside it every highlight keeps its own words, its own page, and its own images and comment, in reading order. Existing ref notes migrate on the next scan with no block-ID churn, no tombstones, and no change to any note that has no group. `bob ref show` (and, if approved, the Bob Mac Capture Refs inspector) shows the same pieces.

## Notes

[2026-10-23T10:49:23Z · bob-cli-ap.land] LANDING REVIEW: Read every note on bob-cli-ap and ap.1/ap.2/ap.3 and reviewed approved plan plus actual source and commits 5376dc6e, f2c24531, and bob-mac-capture da5faa8. All phases are closed. Follow-up triage: collected zero PROPOSED FOLLOW-UP entries; no distinct unrelated work was found, so no task was created, corroborated, or declined. Remaining findings are caused by this epic and stay epic work: Mac RefsInspectorFeed.hiddenNotedCount incorrectly sums piece note cards instead of hidden entries, and header VoiceOver uses an entry-based phrase for card counts. Executing the actual portable Swift model with one group containing two commented pieces produced total=1, noteCards=2, +1 more · 2 with notes · ⌃D shows it, 1 more highlight, 2 with notes, and Highlights, 1, 2 with notes. The legacy migration test uses an abbreviated quote instead of exact pre-epic renderer output, so it misses the legacy match path; add a real frozen fixture and a cross-piece hyphen case with a non-generated prior ID. Finish the required continuation wording sweep (docs/highlights-ref-sync.md lines 41 and 836) and document legacy-only fusion helpers. Integration: fetched bob-cli origin/master; it contains only the two epic commits since start. Mac commit 8160db3 landed during the epic and moves Refs reset to Ctrl-C; reviewed its router/model/docs diff, no conflict with group rendering or Copy, and da5faa8 already builds on it. Reviewer decisions were honored in committed scope: Mac inspector implemented; phase ap.1 records live CSS installation and four successful scratch-note migrations; no memory files changed. epic-symbols currently empty; neither repo defines a symvision recipe. No parent_bead is shown. Will propose a small tale for these corrections, full required verification, and same-turn epic closeout. This review has not yet rerun just check: sase tool run check returns unknown tool check, so use the documented SASE_TOOL_BYPASS raw gate or monitor fallback.

[2026-10-23T10:50:06Z · bob-cli-ap.land] CSS DECISION VERIFIED: Opened gh:bobs-org/bob with sase repo and compared the published .obsidian/snippets/ref-highlights.css to the complete documented CSS block byte-for-byte; they match (SHA256 1edafd1f155374c59f5499df7fa7ca5ac7c8bbffe8df13264fb30b5979bdf62a). Vault history includes installation commit 87191475. No vault files were changed.

[2026-10-23T11:17:15Z · bob-cli-ap.land] Landed tucked-group corrections. Mac RefsInspectorFeed.hiddenNotedCount now counts hidden entries with note cards (not card sum); header VoiceOver uses note-card phrasing when card count differs from entry count, preserving chip total. Added RefsInspectorTests.testGroupWithTwoNoteCardsCountsOneHiddenEntry (single+group hidden, solo group, clamped visibility). Rust legacy migration now uses exact pre-epic 5376dc6e^ fused gas-town block and asserts full ID set plus byte-identical rerender; added hyphen-seam case (inter-/national -> international) with non-generated head h-0123456789ab proving legacy_full_text path, no tombstones, tucked pieces separate. Documented assemble_group_quote/seam as legacy-only in continuation.rs. Docs sweep: grouping language at intro and first-write rule, dangling as could not form a group; underline merging untouched. Gates: cargo continuations 18 passed, RefsInspectorTests 61 passed, just check ok (3167 passed), just portable-check ok (1532 passed), just docs-check ok (447 passed, 1 skipped) in both repos, Mac docs-check via cached bob-cli ok. CSS already installed and verified (vault 87191475, SHA256 1edafd...bdf62a). Integration: bob-cli origin/master has only epic commits 5376dc6e/f2c24531; mac at da5faa8 on 8160db3, no new drift. Follow-up triage: no PROPOSED FOLLOW-UP in any child/epic notes, no new tasks.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ap.1](bob-cli-ap.1.md) | Render, parse, and identify tucked groups in bob-cli | ✓ closed | medium | 2026-10-23 | 1 | 1 |
| [bob-cli-ap.2](bob-cli-ap.2.md) | Expose group pieces in bob ref show | ✓ closed | small | 2026-10-23 | 1 | 1 |
| [bob-cli-ap.3](bob-cli-ap.3.md) | Render group pieces in the Bob Mac Capture Refs inspector | ✓ closed | medium | 2026-10-23 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ap: Tucked continuation groups — keep every `&lt;` highlight distinct inside its group [closed]"]
    n1["bob-cli-ap.1: Render, parse, and identify tucked groups in bob-cli [closed]"]
    n2["bob-cli-ap.2: Expose group pieces in bob ref show [closed]"]
    n3["bob-cli-ap.3: Render group pieces in the Bob Mac Capture Refs inspector [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ap.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ap.1.md) | [bob-cli-ap.1](bob-cli-ap.1.md) | 1 |
| [bbugyi200.athena.bob-cli-ap.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ap.2/README.md) | [bob-cli-ap.2](bob-cli-ap.2.md) | 1 |
| [bbugyi200.athena.bob-cli-ap.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ap.3/README.md) | [bob-cli-ap.3](bob-cli-ap.3.md) | 1 |
| [bbugyi200.athena.bob-cli-ap.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ap.land.md) | [bob-cli-ap](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5376dc6`](https://github.com/bobs-org/bob-cli/commit/5376dc6e7bf2511f7239820fa7e4f55e93772faf) | feat(highlights-ref): render continuation pieces as tucked groups | [bob-cli-ap.1](bob-cli-ap.1.md) | 2026-10-23 06:02:53 EDT |
| bob-cli | [`f2c2453`](https://github.com/bobs-org/bob-cli/commit/f2c24531b5796878af1bff47d984bccababec6bf) | feat(ref): expose annotation group pieces with seams in show | [bob-cli-ap.2](bob-cli-ap.2.md) | 2026-10-23 06:16:21 EDT |
| bob-mac-capture | [`bob-mac-capture@da5faa8`](https://github.com/bobs-org/bob-mac-capture/commit/da5faa8c54daa19444577564f36f068a1690e01b) | feat(refs): render tucked group pieces in the Refs inspector | [bob-cli-ap.3](bob-cli-ap.3.md) | 2026-10-23 06:37:17 EDT |
| bob-cli | [`510c8a4`](https://github.com/bobs-org/bob-cli/commit/510c8a4425ca8ff267f3852133f86e1cf64c5cec) | fix(highlights-ref): harden legacy migration coverage and grouping docs | [bob-cli-ap](README.md) | 2026-10-23 07:19:04 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ap.2][1] | Need epic context and decisions for phase ap.2 | 1 |
| read-by | [agent:bob-cli-ap.3][2] | epic context | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ap.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ap.3/README.md

<!-- sase:referenced-by:end -->
