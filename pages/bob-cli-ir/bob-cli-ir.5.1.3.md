# Bead: bob-cli-ir.5.1.3 — Create records through the capture transaction

[Bead Pages](../README.md) / [bob-cli-ir.5.1](bob-cli-ir.5.1.md) / bob-cli-ir.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.5.md) · **Assignee:** `bob-cli-ir.5.1.3` · **Size:** medium
**Created:** 2026-11-08 18:25:56 EST · **Closed:** 2026-11-08 21:47:46 EST
**Plan:** [202611/capture\_record\_creation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_record_creation.md)

## Description

record-writes: wire the shared resolver into batch planning, install records through the existing no-replace path, and expose note_files plus human preview, refusal, and success output.

## Notes

[2026-11-09T02:47:32Z · bob-cli-ir.5.1.3] JSON/contract for bob-cli-ir.5.1.4 and bob-cli-ir.11: capture success adds top-level note_files (skip_serializing_if empty) with path, action="create", record_type, properties[{key,label,value,display,source}], body, markdown. Item record_note is serde skip and collected into note_files. value/display are Option<String> (display copied into value so CaptureResult stays Eq; choice displays use labels like "Liked"). source is "typed"|"default". Dry-run and commit share exact markdown bytes. Incomplete records exit 2 with extra.draft (ready-to-copy, title @dir/ or @dir/^stem, typed fields, omitted required as key:: … plus choice/date hints), extra.missing, extra.invalid[{field,code,message}]. Collisions use code record_exists and copy "record already exists: {path} (open it; adding to it with `@{dir}/{stem}` comes later)". schema_version stays 1; GRAMMAR_REVISION stays 20. No new capture subcommand or public flag. Planner: capture/record_note.rs stages via CaptureBatchPlanner with target_existed false; reserved_paths from planner.staged_snapshot() (records, projects, templates). Missing parent dirs created only at commit (ensure_new_file_parents) and rolled back when empty; PLANT_BEFORE_INSTALL race keeps foreign bytes. Human dry-run: "{prefix} would create  {ordinal}{emoji}new {kind}  {target}"; then exact markdown. Success: "{prefix} {emoji}new {kind}  {ordinal}{target}" plus field displays and "{n} note(s)". Record items skip Gmail rewrite, task-block, freshness, ledger, relations.

[2026-11-09T02:47:32Z · bob-cli-ir.5.1.3] PROPOSED FOLLOW-UP: just check on this tree is red from bob-cli-ir.3 records CLI leftovers that reproduce on clean HEAD 4c97ed41 — native::catalog::tests::document_shape (catalog.entries 83 vs expected 79), native::completion::kinds::tests::every_value_arg_has_a_decision (missing records new:set and records new:stem), and help::root_help_matches_sectioned_short_and_long_snapshots (Vault section lacks the records line). This phase did not change clap help, catalog ENTRIES, or completion kinds; 13 capture::record CLI tests and 6 new_note commit tests passed, and clippy/fmt were green.

[2026-11-09T02:47:46Z · bob-cli-ir.5.1.3] Wired record writes through capture/record_note.rs: shared resolver plans each item, stages Markdown with target_existed false, installs via the existing no-replace path, and emits additive note_files plus human preview/refusal/success. RECORD_EXECUTION_UNWIRED_MESSAGE is gone. Verified: cargo fmt --check green; clippy with just-check gates green; 13/13 tests/cli/capture::record and 6/6 capture::tests::commit::new_note* passed (dry-run/commit markdown equality, mixed task+record, later-item zero writes, same-draft and on-disk/case collisions, explicit stem, missing folder at commit, required/none/list YAML, %t later-row fail, @inbox local record route, Gmail URL opacity, grammar 20 parse wire, parent-dir create and PLANT_BEFORE_INSTALL foreign-byte preserve). epic-symbols empty. schema_version 1 / GRAMMAR_REVISION 20 unchanged. just check still red on three bob-cli-ir.3 leftovers recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-ir.5.1.2](bob-cli-ir.5.1.2.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.5.1.4](bob-cli-ir.5.1.4.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.5.1.3/README.md) | [bob-cli-ir.5.1.3](bob-cli-ir.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2561f9`](https://github.com/bobs-org/bob-cli/commit/f2561f962f5f91392d9721e094ac71f31e6832b3) | feat(capture): create record notes through the capture transaction | [bob-cli-ir.5.1.3](bob-cli-ir.5.1.3.md) | 2026-11-08 21:49:05 EST |
