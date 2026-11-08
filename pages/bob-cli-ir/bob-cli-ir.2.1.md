# Bead: bob-cli-ir.2.1 — Records engine schema, indexing, rendering, and planning

[Bead Pages](../README.md) / [bob-cli-ir.2](bob-cli-ir.2.md) / bob-cli-ir.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.2.md) · **Assignee:** `bob-cli-ir.2.1.land`
**Created:** 2026-11-08 11:17:51 EST
**Plan:** [202611/records\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/records_engine.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/records_engine.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:0463132eb6eafca3abae823e | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/records_engine.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ir.2 with one validated records engine for later CLI and capture consumers, safe byte-preserving updates, real-note fixtures, and a published contract.

## Notes

[2026-11-08T18:37:34Z · bob-cli-ir.2.1.land] LANDING REVIEW at 86af3d5e (origin/master fetched and identical): read this epic, all four child beads and every note, plan:202611/records_engine.md, binding plan:202611/record_notes.md, parent phase bob-cli-ir.2 and outer DECISIONS. Reviewed cd8a031f (schema/fixtures), 93c7c114 (render/update), b9db7007 (catalog), a8ccf5ed (planner/docs) and the actual modules/tests. The 107-title fixture, four raw fixtures, config isolation, typed validators, lazy catalog and timing evidence are present. The claimed update safety and complete planner contract are not yet satisfied; keep this epic and bob-cli-ir.2 open pending a medium tale repair.
FOLLOW-UP TRIAGE: the only PROPOSED FOLLOW-UP is bob-cli-ir.2.1.3 note #1 (schema.rs clippy derivable_impls and needless_borrows_for_generic_args), repeated in its close note. Declined a separate task: it was caused by this epic, and b9db7007 already derived RecordsConfig::Default and removed the needless mapping.get borrow. No genuinely distinct unrelated proposal remains, so no new task or corroboration is needed. Carry this outcome into the eventual close note.
INTEGRATION: reviewed all five non-epic commits after cd8a031f: 984f8196 signed-start diagnostics, 126958b2 mail display contracts, 23217c1d close typing aliases, b4147b0b Gmail hold/lift, 86af3d5e Gmail watch preparation. The engine has no capture or Gmail callers yet; their domain-specific behavior should not be routed through records. Shared docs registry/nav/snapshot already compose mail order 43 and records order 44 (44 entries). No integration edit needed at this base. Both epic-symbol inventories (bob-cli-ir.2.1 and bob-cli-ir.2) are empty; no just symvision recipe exists at review time.
BLOCKERS: catalog markdown_stem panics on one/two-byte non-Markdown filenames due to eager then_some slicing; folder enumeration hides occupied .md paths for external symlinks/nonregular entries and planner treats folder-read diagnostics as nonblocking; catalog list extraction drops null/unsupported members. Render span parsing treats nested keys as top-level and does not decode escaped YAML keys, accepts root flow/nonmapping YAML before inserting fields, checks required-empty only after finding a span, unconditionally adds EOF newline, and its heading scan ignores only triple-backtick fences. Planner lacks stem source, agreed set/default/missing/invalid/none states, optional supplied ranges, unknown-field nearest/allowed-key structured context, and resolves dynamic defaults only for display/render rather than the returned value. docs/records.md has no update-preservation section. Repair within the existing engine contract, with actual API regressions and just check/docs-check, then finish nested landing in the same coder turn.
EVIDENCE: file:explicit:0463132eb6eafca3abae823e contains a compiled probe of verbatim std-only production functions: short-name panics, nested status span, escaped key mismatch, and tilde-fence heading misclassification. This is focused source evidence, not a full engine test run. No just check or check-full was run by this landing review.

[2026-11-08T19:23:18Z · bob-cli-ir.2.1.land] LANDING BLOCKER at origin/master 9e0bcdd81aa8f39b4d0559df440a839e38fd582d. Implementation repairs are complete; this workspace was rebased from 86af3d5e after a non-overlapping Gmail sync commit landed. Focused cargo test --lib native::records:: passes (64 passed, 1 ignored); just docs-gen and just docs-check passed. Required sase tool run check ToolRun 4dbaae8977c2e80294c41a26c9844e73 fails: eight denied clippy::collapsible_if findings in the new Gmail sync files src/native/gmail/sync/file.rs (lines 1117, 1961, 2116) and src/native/gmail/sync/watch_apply.rs (591, 600, 613, 625, 633). The one records test needless-borrow lint was fixed and the focused records suite rerun successfully. These upstream Gmail changes are outside the records tale scope; keep this epic open until the required check is green. Therefore the approved landing sequence cannot close bob-cli-ir.2.1 or mark plan:202611/records_engine.md done yet. Empty epic-symbol inventory; no symvision recipe. FOLLOW-UP TRIAGE: child bob-cli-ir.2.1.3 note number 1 schema clippy proposal remains resolved by b9db7007; no duplicate task was filed. No unrelated proposal from this tale.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.2.1.land.md) | [bob-cli-ir.2.1](bob-cli-ir.2.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8ff0d8e`](https://github.com/bobs-org/bob-cli/commit/8ff0d8ed5a43b34977a6acaf4473159fe977e600) | feat(records): harden planning and byte-preserving updates | [bob-cli-ir.2.1](bob-cli-ir.2.1.md) | 2026-11-08 14:25:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.2.1.1][1] | Need the records-engine epic decisions and phase design context | 1 |
| read-by | [agent:bob-cli-ir.2.1.2][2] | Need DECISIONS and any interface notes from schema phase | 2 |
| read-by | [agent:bob-cli-ir.2.1.3][3] | Need sibling phase status to check prior work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.2.1.3/README.md

<!-- sase:referenced-by:end -->
