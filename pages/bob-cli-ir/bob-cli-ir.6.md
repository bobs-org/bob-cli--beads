# Bead: bob-cli-ir.6 — Guided field entry in capture-complete

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.6` · **Size:** large
**Created:** 2026-11-08 11:06:12 EST · **Closed:** 2026-11-09 02:34:48 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

capture-record-assist: add the record_field and record_value completion contexts with continuations, the next-missing-field request, ranked folder values, record route rows, and the heading-menu New restaurant row that defuses the slash-to-hash rewrite.

## Notes

[2026-11-09T06:52:17Z · bob-cli-ir.6] Implemented capture-record-assist (`plan:202611/record_capture_guided_fields.md`).

Contract
- `-n/--next-missing-field` on `bob capture-complete`; `schema_version: 1`, `grammar: 20` (already current).
- Contexts `record_field` / `record_value`; record route rows carry emoji/type/count, `eat/ ` insertion, and candidate `continuation: {cursor, next_missing_field}` (separate from `picker.continuation`).
- Fresh `- ` offers required keys first; caret-in-value opens that field; last required omits continuation.
- Mixed `@eat#` JSON menu prepends `kind: "record_create"` on empty query and expands replacement to the whole token; shell keeps the established prefix protocol.
- Shared `record_value_near` warning (distance 2, greater folder frequency, no rewrite). Parse: code+message; complete: also authored/proposed.
- Opaque field values own `% # @ ~ URL ((` before task pickers. Template argument rows are not record items. Ordinary drafts skip the catalog (`last_catalog_files_opened()==0`).

Validation
- Unit `native::capture_complete::tests::records`: 19 passed (route label, field/value menus, status→category→location chain, Westfield collapse, Cheeseteaks near hint, section create, `@@` skip, opacity, empty URL, dates, CRLF, list splice, leftover notes, templates, human, shell).
- CLI `capture::complete_records`: 6 passed. `help_options::capture_complete_help_lists_options_alphabetically` passed.
- `just fmt` (`cargo fmt --all -- --check`) passed. `just docs-gen` regenerated `docs/reference/cli/capture-complete.md`. `just docs-check` passed.

Performance (debug profile, temp vault `inbox: inbox`, warmup 20, n=100)
- `capture-parse -f json -- 'Buy milk'`: HEAD `80c93209` p95 18.39ms → current 15.28ms (Δ −3.12ms).
- `capture-complete -c 8 -f json -- 'Buy milk'`: HEAD p95 16.16ms → current 15.30ms (Δ −0.85ms).
- Noise on the order of a few ms; no added record-catalog I/O on ordinary drafts.

[2026-11-09T07:32:52Z · bob-cli-ir.6--2] PROPOSED FOLLOW-UP: Flaky timing test native::ref_library::tests::extra_pass_and_additive_id_resolution_agree_on_the_fixture failed once during just check (extra 125.6ms vs additive 5.5ms; budget extra <= additive * 20) then passed in isolation (0.04s) and on a full re-run. Unrelated to capture-complete; load-sensitive comparison at src/native/ref_library/tests.rs:969.

[2026-11-09T07:34:48Z · bob-cli-ir.6--2] Closed by explicit `sase stitch create -B close` after create_commit landed 07ff3bf0 ("feat(capture): add guided record field completion"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-ir.6` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-ir.10](bob-cli-ir.10.md) ◐ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-ir.5](bob-cli-ir.5.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.7](bob-cli-ir.7.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.6.md) | [bob-cli-ir.6](bob-cli-ir.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`07ff3bf`](https://github.com/bobs-org/bob-cli/commit/07ff3bf01fd4dad8d8ebf287035877bfd43df90b) | feat(capture): add guided record field completion | [bob-cli-ir.6](bob-cli-ir.6.md) | 2026-11-09 02:34:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.6--2][1] | Need assigned phase scope before host-completion commit and close | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.6.md

<!-- sase:referenced-by:end -->
