# Bead: bob-cli-q5.2.1.2 — Exclude planned-today tasks from freshness and walks

[Bead Pages](../README.md) / [bob-cli-q5.2.1](bob-cli-q5.2.1.md) / bob-cli-q5.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.md) · **Assignee:** `bob-cli-q5.2.1.2` · **Size:** medium
**Created:** 2026-11-25 19:37:40 EST · **Closed:** 2026-11-26 04:19:29 EST
**Plan:** [202611/snoozed\_planned\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_planned_today.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0bc82d5d4b7f7164deb53e4c | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

review-exclusions: thread is_snoozed_today through freshness scan, evaluation, placement, and seed, and use planned-today at review and lane-walk exclusion sites. Preserve ledger-only Today and whole-lane plan meters. Add executable freshness and walks vectors and publish their contracts for the plugin phase.

## Notes

[2026-11-26T08:22:55Z · bob-cli-q5.2.1.2] PROPOSED FOLLOW-UP: Recover the missing reader-recovery phase implementation — bob-cli-q5.2.1.1 is closed but origin/master at 1c23bce7 has no snooze/read.rs or reconciliation snoozed recovery. The original transcript reports passing focused tests; saved completion file:explicit:37516ddfbf84314980ed8752 lists 14 uncommitted paths at base 19e7fe54. This phase will extract the shared reader needed for review exclusions; the land agent must recover or finish the missing direct recovery, preservation tests, and predecessor docs before closing the child epic.

[2026-11-26T08:34:14Z · bob-cli-q5.2.1.2] Implementation contract for consumers: src/native/snooze/read.rs now exposes read(day_text, vault_relative_day_path, note_date, &SnoozeClock, &NoteIndex, &NoteTaskSettings, lookup) -> ReadView {rows: Vec<RowDetail {parsed, identity, title}>, classified: ClassifiedRows, identities: IdentityMap}. lookup returns cached Option<&str> by vault-relative path; parsed task notes are cached once per call. state::live_targets(&view.classified) supplies planned/blocked; planned_from_snapshot is a membership-only adapter with explicit Bob-zone today/note dates (membership does not depend on time-of-day). CLI evaluation uses this same reader. RowCtx/FreshnessRow/UnblockScope keep is_snoozed_today separate from is_today. Shared executable SP1-SP12/SP15 vectors are tests/fixtures/walks/planned-today.json; SP13 wake, SP14 placement, SP16 excess, SP17 seed are named Rust/CLI tests. docs/freshness.md and docs/walks.md publish the input/output contract. cargo check --tests passed before the final small cache/date-adapter refinements; focused executable tests and full gates still pending. No epic-symbol entries.

[2026-11-26T08:36:36Z · bob-cli-q5.2.1.2] Verification update: just docs-check passed all implemented gates (lint, generated drift, strict build, URLs/links/tutorial and 447 documentation unit tests; 1 optional font-dependency test skipped). cargo check --tests passed; final formatting and diff checks pass. Full executable regression verification is being handed to a monitor, with implementation complete and only test/gate triage remaining. Baseline for clean-base comparisons is 1c23bce7. Do not infer the predecessor direct-recovery changes landed: the earlier proposed follow-up remains for the land agent; this phase owns the reader extraction and exclusions only.

[2026-11-26T09:00:00Z · bob-cli-q5.2.1.2--1] Verification triage: implementation is committed as b8678657. Monitor 5rfve5sbzwpf passed freshness/snooze/task_complete/hooks unit tests and freshness CLI; just check passed format and Clippy but failed 43 lib tests and 56 CLI tests. The introduced SP vector assertion confused ignored-row reasons (ready/already_linked) with the CLI state ignored. Fixed SP4/SP5/SP9/SP15 fixtures to separate snooze_state and snooze_reason and added the reason assertion; all vector cases pass with the existing test binary after fixture correction. A fresh full gate plus clean-base 1c23bce7 lib/CLI comparison is next; no claim yet that the remaining 98 failures are unrelated. Existing leads are q9 (PDF kicker spacing), q4 (17 settle fixture failures), and ph.10/ph.8.1.6 (bold-only drawer fixture drift). No docs changed, so prior docs-check remains valid.

[2026-11-26T09:19:10Z · bob-cli-q5.2.1.2--2] PROPOSED FOLLOW-UP: Corroborate the 98 pre-existing full-gate failures for lander triage. Monitor n9xg2e0s5q80 (tool run ef46807f496a338f934940a1949e320b) ran just check on committed implementation bbcae8e03383b33cae1efc21856c00488fe68e16: fmt and gated Clippy passed; lib 8183 passed / 43 failed / 5 ignored; CLI 4160 passed / 55 failed; every other test binary and doctest passed. The same clean checkout was temporarily switched to clean base 1c23bce7a8a0024e7874f0955bee104f4207870c, where RUST_TEST_THREADS=16 cargo test --lib --test cli --no-fail-fast reproduced lib 8180 passed / 43 failed / 5 ignored and CLI 4156 passed / 55 failed. All 98 failure names AND assertion diagnostics match after normalizing only harness PIDs, TempDir nonces, and the optional backtrace hint; zero new, changed, or base-only failures. Independently checked that every FAILED test line has a compared diagnostic block. comparison_passed=true and regression_passed=true; all seven added lib/CLI tests pass, including the rebuilt SP vector reason assertions. Original master/HEAD was restored and git status is clean. Existing tracking: bob-cli-q9 covers the PDF kicker spacing failure; bob-cli-q4 covers the 17 settle-fixture CLI failures; bob-cli-ph.10 and bob-cli-ph.8.1.6 record the bold-only drawer fixture drift (remaining 42 lib and 38 CLI failures). No new beads created. The missing predecessor direct recovery work in note #1 remains outside this phase for the land agent. Evidence bundle (comparison script, JSON, raw current/base logs, retained monitor output, independent validation): file:explicit:0bc82d5d4b7f7164deb53e4c.

[2026-11-26T09:19:29Z · bob-cli-q5.2.1.2--2] Verified planned-today freshness/review/walk exclusions, shared snooze reader/CLI classification, placement callers, seed counters/idempotence, wake behavior, and unchanged ledger-only Today/whole-lane plan meters. Implementation b8678657 and conformance state/reason correction bbcae8e0 are committed. Rebuilt SP1-SP12/SP15 vectors plus named SP13/SP14/SP16/SP17 coverage pass; all seven added lib/CLI tests pass. Monitor n9xg2e0s5q80 completed successfully: fmt/Clippy pass; just check retains only 98 failures (43 lib, 55 CLI), all independently reproduced with identical normalized diagnostics on clean base 1c23bce7; no new or changed failures. All other test binaries/doctests pass. Prior just docs-check remains valid (447 passed, 1 optional skip); no docs edited or gates needlessly repeated. Baseline failures and evidence recorded as PROPOSED FOLLOW-UP; predecessor direct recovery remains the land agent's separate follow-up. epic-symbols reports no leftovers. Clean checkout restored to bbcae8e0; no further source fixes needed. Closing only bob-cli-q5.2.1.2; no ancestor closed.

## Dependencies

- **Depends on:** [bob-cli-q5.2.1.1](bob-cli-q5.2.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.2.1.3](bob-cli-q5.2.1.3.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.1.2.md) | [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b867865`](https://github.com/bobs-org/bob-cli/commit/b8678657640747b58ab418ef2206c86786b240db) | feat(freshness): exclude planned-today tasks from review and walks | [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) | 2026-11-26 03:38:14 EST |
| bob-cli | [`bbcae8e`](https://github.com/bobs-org/bob-cli/commit/bbcae8e03383b33cae1efc21856c00488fe68e16) | test(walks): distinguish ignored snooze states from reasons | [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) | 2026-11-26 04:01:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.2.1.2--1][1] | Need the phase scope, design file, and prior verification notes | 1 |
| read-by | [agent:bob-cli-q5.2.1.3][2] | Check prior phases implementation for shared reader | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.3/README.md

<!-- sase:referenced-by:end -->
