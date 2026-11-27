# Bead: bob-cli-re.3 — Preserve task block identity when canceling an ID-less successor

[Bead Pages](../README.md) / [bob-cli-re](README.md) / bob-cli-re.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r8.land.md) · **Assignee:** `bob-cli-re.3` · **Size:** medium
**Created:** 2026-11-27 15:31:19 EST · **Closed:** 2026-11-27 17:32:07 EST
**Plan:** [202611/task\_bead\_burndown\_3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_3.md)

## Description

idless-cancel: fix the capture -X stale task-block reference, verify JSON and written bytes, and close bob-cli-oh.

## Notes

[2026-11-27T22:31:49Z · bob-cli-re.3] PROPOSED FOLLOW-UP: Triage clean-base `just check` failures (no matching task bead found): four capture type-lead unit tests, two prose unit tests and the prose extract CLI test, plus the themes and themes_rename CLI tests. A clean-HEAD rerun of type_leads_accept_multibyte_text_and_reject_non_string_keys reproduces the panic at src/native/config/capture.rs:802 (`no entry found for key`).

[2026-11-27T22:32:07Z · bob-cli-re.3] Forwarded task-block identities across successor verdict and recovery writes by same-indentation task order. Verified the original no-jump ID-less cancel case, duplicate-title jump case, and reversed-selection case with dry-run/real bytes against JSON; 23 successor-verdict tests pass. cargo fmt --check and git diff --check pass. just check exits 101 on unrelated config/prose/themes tests; the type-lead failure reproduces on clean HEAD and is recorded as a proposed follow-up. Epic symbols: none.

## Dependencies

- **Depends on:** [bob-cli-re.2](bob-cli-re.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-re.4](bob-cli-re.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-re.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.3/README.md) | [bob-cli-re.3](bob-cli-re.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d117d28`](https://github.com/bobs-org/bob-cli/commit/d117d28838ac4b75e7a3bb7b1de45b6117e0d4da) | fix(capture): preserve ID-less task blocks across successor closes | [bob-cli-re.3](bob-cli-re.3.md) | 2026-11-27 17:33:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-re.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.3/README.md

<!-- sase:referenced-by:end -->
