# Bead: bob-cli-q5.2.1.2 — Exclude planned-today tasks from freshness and walks

[Bead Pages](../README.md) / [bob-cli-q5.2.1](bob-cli-q5.2.1.md) / bob-cli-q5.2.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.md) · **Assignee:** `bob-cli-q5.2.1.2` · **Size:** medium
**Created:** 2026-11-25 19:37:40 EST
**Plan:** [202611/snoozed\_planned\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_planned_today.md)

## Description

review-exclusions: thread is_snoozed_today through freshness scan, evaluation, placement, and seed, and use planned-today at review and lane-walk exclusion sites. Preserve ledger-only Today and whole-lane plan meters. Add executable freshness and walks vectors and publish their contracts for the plugin phase.

## Notes

[2026-11-26T08:22:55Z · bob-cli-q5.2.1.2] PROPOSED FOLLOW-UP: Recover the missing reader-recovery phase implementation — bob-cli-q5.2.1.1 is closed but origin/master at 1c23bce7 has no snooze/read.rs or reconciliation snoozed recovery. The original transcript reports passing focused tests; saved completion file:explicit:37516ddfbf84314980ed8752 lists 14 uncommitted paths at base 19e7fe54. This phase will extract the shared reader needed for review exclusions; the land agent must recover or finish the missing direct recovery, preservation tests, and predecessor docs before closing the child epic.

[2026-11-26T08:34:14Z · bob-cli-q5.2.1.2] Implementation contract for consumers: src/native/snooze/read.rs now exposes read(day_text, vault_relative_day_path, note_date, &SnoozeClock, &NoteIndex, &NoteTaskSettings, lookup) -> ReadView {rows: Vec<RowDetail {parsed, identity, title}>, classified: ClassifiedRows, identities: IdentityMap}. lookup returns cached Option<&str> by vault-relative path; parsed task notes are cached once per call. state::live_targets(&view.classified) supplies planned/blocked; planned_from_snapshot is a membership-only adapter with explicit Bob-zone today/note dates (membership does not depend on time-of-day). CLI evaluation uses this same reader. RowCtx/FreshnessRow/UnblockScope keep is_snoozed_today separate from is_today. Shared executable SP1-SP12/SP15 vectors are tests/fixtures/walks/planned-today.json; SP13 wake, SP14 placement, SP16 excess, SP17 seed are named Rust/CLI tests. docs/freshness.md and docs/walks.md publish the input/output contract. cargo check --tests passed before the final small cache/date-adapter refinements; focused executable tests and full gates still pending. No epic-symbol entries.

[2026-11-26T08:36:36Z · bob-cli-q5.2.1.2] Verification update: just docs-check passed all implemented gates (lint, generated drift, strict build, URLs/links/tutorial and 447 documentation unit tests; 1 optional font-dependency test skipped). cargo check --tests passed; final formatting and diff checks pass. Full executable regression verification is being handed to a monitor, with implementation complete and only test/gate triage remaining. Baseline for clean-base comparisons is 1c23bce7. Do not infer the predecessor direct-recovery changes landed: the earlier proposed follow-up remains for the land agent; this phase owns the reader extraction and exclusions only.

## Dependencies

- **Depends on:** [bob-cli-q5.2.1.1](bob-cli-q5.2.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.2.1.3](bob-cli-q5.2.1.3.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.1.2.md) | [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b867865`](https://github.com/bobs-org/bob-cli/commit/b8678657640747b58ab418ef2206c86786b240db) | feat(freshness): exclude planned-today tasks from review and walks | [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) | 2026-11-26 03:38:14 EST |
