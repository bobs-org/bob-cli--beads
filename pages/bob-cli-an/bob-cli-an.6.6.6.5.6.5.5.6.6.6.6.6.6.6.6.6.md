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

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md

<!-- sase:links:end -->

## Description

Close five existing tasks by giving Linux-launched agents a bounded precommit macOS check, attaching saved sources to the skipped agent-report references, stopping the research hook from creating duplicate references, refusing dirty ref-scan targets per PDF, and pinning bob-mac-capture's Swift format.

## Notes

[2026-10-27T13:19:50Z · bob-cli-d2.land] DISCOVERED ISSUE / d2 landing integration: your attach-source-skips phase .2 added JSON in 69b7d962, but commit_batch still prints committed <sha> (N references) to stdout. Reproduced on d38bef59 in an isolated Git vault: successful bob ref attach-source report -f json adoption exits 0 but json.loads(stdout) fails at line 1. Existing tests only cover dry-run JSON. bob-cli-d2 will include the shared commit-output repair and write-mode adoption/search JSON regressions in its remaining-work tale, avoiding duplicate edits. Also recorded bob-cli-d2.3 proposed overlap #2 on bob-cli-co: 17 hook-time attachments independently confirmed, historical membership in the old ambiguous/title-mismatch sets unproven; co stays open. Evidence: file:explicit:c61a26370b705cae1446a6ed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 0 |
