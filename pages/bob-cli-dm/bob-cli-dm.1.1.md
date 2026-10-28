# Bead: bob-cli-dm.1.1 — Rust task theme suggestions and canonical task fields

[Bead Pages](../README.md) / [bob-cli-dm.1](bob-cli-dm.1.md) / bob-cli-dm.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-dm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.md) · **Assignee:** `bob-cli-dm.1.1.land`
**Created:** 2026-10-28 09:05:51 EDT · **Closed:** 2026-10-28 17:37:53 EDT
**Plan:** [202610/task\_theme\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_core.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/task_theme_core.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_core.md

<!-- sase:links:end -->

## Description

Complete bob-cli-dm.1 with pure suggestion and field rules, a read-only explanation CLI, unknown-default hints, shared vectors, preservation coverage, and the published contract.

## Notes

[2026-10-28T21:02:54Z · bob-cli-dm.1.1.land] LAND AUDIT at c6243477 (origin/master fetched and equal): read this epic, every child and every note, parent phase bob-cli-dm.1, parent epic DECISIONS, both linked plans, commits a1b8766b/9409bfa5/c6243477, and their actual source/tests/docs. Earlier .2 pending cache/help/timing notes are resolved by .2 notes 4-5; audited file:explicit:babfd9c7f9ecf3f6fe7fddcf confirms distinct same-profile release binaries, frozen snapshot, 10 warmups + 100 alternating samples each, p95 41.400022 -> 37.079298 ms (-4.320724 ms), canonical check exit 0. .3 adds actual writer-level preservation coverage including archive history and reading reinsert, and documents PT13 while preserving PT12. No epic commit edited memory, live vault, version, or changelog; schema stays 1. Reviewed non-epic commits since a1b8766b, including 8852f7bf configured-theme fixture fix (already integrated), cancel-label source closing, 0f1898ee ref-task selection diagnostics, complete-label policy, and 4c55a595 shared completion extraction. New close paths should gain distinctive-field preservation assertions in remaining work; no automatic theme writer should be added. Other drift is docs, vault-sync clobber protection, or capture-related timing and does not need task-theme integration. epic-symbols reports zero for both this epic and bob-cli-dm.1; current justfile has no symvision recipe. Remaining epic defects found in .1: duplicate trailing-field parser rejects shared-scanner-valid [created :: DATE], accepts nonfields such as [key with spaces:: value], and set_task_theme adds a space before LF/CRLF on field replacement; frontmatter parsing treats quoted padded off as the OFF theme, quoted whitespace as invalid, and unindented/blank-separated multiline lists as blank; config accepts explicit reading_theme null despite the non-string error contract. The new suggestion/field modules also carry forbidden blanket allow(dead_code), and copy canonical naming/normalization rather than reusing authorities. Proposing one medium tale for only these remaining fixes, regression vectors, integration preservation, checks, and final closeout; do not close yet.

[2026-10-28T21:03:02Z · bob-cli-dm.1.1.land] FOLLOW-UP TRIAGE BEFORE REPAIR TALE: All child notes were read; no literal PROPOSED FOLLOW-UP entries exist. The .2 invalid-identical-binary, full-scan, serial-cache, help-fixture and pending-verification reports are superseded by the verified final parallel-cache result and need no separate task. Under /sase_new_task, screened the non-epic shell/deadline flakes mentioned in bob-cli-dm.1.1.3 note 1: searched flake tasks, swept the last week, inspected active epics and read bob-cli-8q, bob-cli-b9, and bob-cli-3j. Declined a new task, +1, or reopening: the phase note omits exact failing test IDs and retained failure logs, the similar tasks are closed after f00854be fixes, and its final 6399-test check passed. There is insufficient evidence to identify a distinct defect, establish a semantic duplicate, or claim a post-close regression/credible active-epic cause. Preserve this attribution and limitation; a future exact-node recurrence can be triaged with evidence. All reproducible parsing/placement/allowance findings are caused by this epic and remain epic work in the repair tale. No unrelated task was created or silently deferred.

[2026-10-28T21:37:53Z · bob-cli-dm.1.1.land] Verified nested epic bob-cli-dm.1.1. Children .1.1.1/.1.1.2/.1.1.3 remain closed. Landing repairs: frontmatter_scalar trims after unquoting and classifies empty-value blocks (padded off, quoted blank, unindented/blank-then list as Invalid); canonical_theme_name reuses canonicalize_pomodoro_name with a no-+ guard; plan.reading_theme Null is ConfigError (absence defaults READ, off disables); shared all_inline_fields drives trailing_field_key; set/clear preserve LF/CRLF/CR/no-newline; module-wide dead_code allows removed; unused suggest re-exports deleted; narrow cfg_attr allowances name bob-cli-dm.4/.5/.7. Preservation: task_cancel::edit_source and complete_task_tree keep authored (theme::  WRITE) bytes. origin/master still c6243477; no later overlapping commits. sase tool run check 745957776dd0e3066ad0c0a8a5613093 exit 0: 6408 passed, 0 failed, 1 ignored (5m 26s). just docs-check all gates passed. Scratch-vault smoke: human/JSON suggest for override, inherit, off, closed; vault bytes unchanged. epic-symbols: none. justfile still has no symvision recipe. Timing: file:explicit:babfd9c7f9ecf3f6fe7fddcf p95 41.400022→37.079298 ms (−4.320724); no rebenchmark (warm cache path unchanged). Follow-up triage already recorded: no PROPOSED FOLLOW-UP; phase-3 flake notes declined without exact node IDs; no new task/+1/reopen. Memory files unedited (memory_decision_record=no, memory_glossary_term=no). ledger_theme_pills and seed_plex_chore remain later phases. Schema 1 additive.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.1.land.md) | [bob-cli-dm.1.1](bob-cli-dm.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fc59428`](https://github.com/bobs-org/bob-cli/commit/fc594281b1f623738b6ee0f71c8ff86df0285246) | fix(themes): repair task-theme scalars, placement, and unused-code gates | [bob-cli-dm.1.1](bob-cli-dm.1.1.md) | 2026-10-28 17:41:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.1.1.3][1] | check child epic phases status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.1.1.3/README.md

<!-- sase:referenced-by:end -->
