# Bead: bob-cli-an.6.5 — Make new reference IDs follow stems and stay unique across ref/

[Bead Pages](../README.md) / [bob-cli-an.6](bob-cli-an.6.md) / bob-cli-an.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.land.md) · **Assignee:** `bob-cli-an.6.5` · **Size:** medium
**Created:** 2026-10-23 12:41:09 EDT · **Closed:** 2026-10-23 13:31:38 EDT
**Plan:** [202610/backlog\_batch2\_athena\_hardening\_and\_ref\_ids.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch2_athena_hardening_and_ref_ids.md)

## Description

ref-id-allocation: resolve bob-cli-8o so created references record their actual note stem and default collision walks cover every ref type directory.

## Notes

[2026-10-23T17:18:14Z · bob-cli-an.6.5] PROPOSED FOLLOW-UP: Document six PDF-write environment controls — just docs-check fails identically on clean base because BOB_REF_FRONTMOST_BUNDLE_ID, BOB_REF_HID_IDLE_SECONDS, BOB_REF_PDF_SCAN_BUDGET_SECONDS, BOB_REF_PDF_WRITE_BUDGET_SECONDS, BOB_REF_READING_PROBE, and BOB_REF_READING_WINDOW_SECONDS in src/native/highlights_ref/pdf_write_policy.rs are undocumented; no existing bead tracks this lint failure.

[2026-10-23T17:31:38Z · bob-cli-an.6.5--1] Implemented and checked ref ID allocation: created IDs follow the final output basename, and default target collision checks cover other ref types and recorded IDs across ref/. Added the allocation contract to docs/ref.md. Integrated just check passed (monitor 56c84nseqmad, exit 0); git diff --check passed. just docs-check still reports the six undocumented BOB_REF_* controls already recorded in this phase's PROPOSED FOLLOW-UP note. epic-symbols has no leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.5.md) | [bob-cli-an.6.5](bob-cli-an.6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9885bde`](https://github.com/bobs-org/bob-cli/commit/9885bde15100fcf41d5dcc99053c443a184d04d6) | fix(ref): allocate unique IDs from output stems | [bob-cli-an.6.5](bob-cli-an.6.5.md) | 2026-10-23 13:32:20 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.5--1][1] | Need the phase scope, design file, and prior work notes before completion | 1 |
| read-by | [agent:bob-cli-an.6.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.land/README.md

<!-- sase:referenced-by:end -->
