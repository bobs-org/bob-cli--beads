# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6 — Backlog batch 17: a precommit macOS gate, the attach-source backfill skips, duplicate research references, scan-wide dirty refusals, and a Swift format config

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land`
**Created:** 2026-10-27 06:23:58 EDT
**Plan:** [202610/backlog\_batch17\_macos\_gate\_source\_backfill\_hook\_dedupe\_dirty\_scans\_swift\_format.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md

<!-- sase:links:end -->

## Description

Close five existing tasks by giving Linux-launched agents a bounded precommit macOS check, attaching saved sources to the skipped agent-report references, stopping the research hook from creating duplicate references, refusing dirty ref-scan targets per PDF, and pinning bob-mac-capture's Swift format.

## Notes

[2026-10-27T13:19:50Z · bob-cli-d2.land] DISCOVERED ISSUE / d2 landing integration: your attach-source-skips phase .2 added JSON in 69b7d962, but commit_batch still prints committed <sha> (N references) to stdout. Reproduced on d38bef59 in an isolated Git vault: successful bob ref attach-source report -f json adoption exits 0 but json.loads(stdout) fails at line 1. Existing tests only cover dry-run JSON. bob-cli-d2 will include the shared commit-output repair and write-mode adoption/search JSON regressions in its remaining-work tale, avoiding duplicate edits. Also recorded bob-cli-d2.3 proposed overlap #2 on bob-cli-co: 17 hook-time attachments independently confirmed, historical membership in the old ambiguous/title-mismatch sets unproven; co stays open. Evidence: file:explicit:c61a26370b705cae1446a6ed.

[2026-10-27T14:18:28Z · bob-cli-d2.land--1] The shared attach-source JSON write-mode repair is implemented in this working diff: commit diagnostics go to stderr in JSON mode so stdout stays one parseable envelope across batch and final commits. Verified by focused attach (25 passed) and full CLI checks (2,291 CLI tests passed; just check and just docs-check passed). Verification evidence: file:explicit:65cf00f6aef47b5c575e10e2 and file:explicit:0b7f8779ba750441f4469595. The broader saved-Markdown landing remains open on bob-cli-d2 because its approved attachment stop gate failed.

[2026-10-27T14:21:17Z · bob-cli-d2.land--1] Updated landing summary after the live vault fast-forward is file:explicit:a56b38495295a784e55ac0a0; it supersedes the earlier summary snapshot while preserving the JSON repair verification and stop-gate record.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e6296bc`](https://github.com/bobs-org/bob-mac-capture/commit/e6296bc9727a0f5e2533049b36212e6ea2e6d40b) | style(refs): re-indent per-PDF dirty-hold lines to the pinned 4-space format | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 2026-10-27 10:43:29 EDT |
| bob-mac-capture | [`bob-mac-capture@3f70d49`](https://github.com/bobs-org/bob-mac-capture/commit/3f70d498e156506599f67606defd1c014d9edeb0) | fix(ci): wait for lagging job status before judging a completed run | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 2026-10-27 10:45:31 EDT |
| bob-mac-capture | [`bob-mac-capture@ed8f3d3`](https://github.com/bobs-org/bob-mac-capture/commit/ed8f3d3a17b599ed6d3c81ed58a43a075f7fb529) | docs(agents): point Swift formatting at the pinned .swift-format | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 2026-10-27 10:47:03 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land][1] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:bob-cli-d2.land--1][2] | Confirm the named JSON repair epic after note append | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d2.land.md

<!-- sase:referenced-by:end -->
