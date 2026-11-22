# Bead: bob-cli-oz.1 — bob capture-complete --task-links: (( in plain prose, with shared prose vectors

[Bead Pages](../README.md) / [bob-cli-oz](README.md) / bob-cli-oz.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ff](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ff.md) · **Assignee:** `bob-cli-oz.1` · **Size:** small
**Created:** 2026-11-21 17:39:51 EST · **Closed:** 2026-11-21 23:24:56 EST
**Plan:** [202611/prompt\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prompt_task_links.md)

## Description

cli-task-links: add a prose (( detector without capture-grammar checks, the -T/--task-links option on capture-complete -L, byte-identical prose trigger vectors, tests, and capture-complete docs.

## Notes

[2026-11-22T04:24:46Z · bob-cli-oz.1] PROPOSED FOLLOW-UP: just docs-check fails 3 tools/docs/tests/test_contracts.py tests (registry/nav missing walks.md, llmstxt stems, README contract table sha) — reproduces identically on clean base 6b9139a6 with this phase stashed; already recorded in bob-cli-on notes, so no new bead needed unless that epic drops it. Every other docs-check stage (lint, generated drift, strict build, URLs, lychee, tutorial, media) passed with this change.

[2026-11-22T04:24:56Z · bob-cli-oz.1] Added capture_task_wikilinks::prose_completion_field_at (capture token rules minus close-log/editor-item/whole-item checks; capture completion_field_at and wikilink_task_spans unchanged, sharing one tokens_where scanner), -T/--task-links (.requires(links-only), sorted, flag guard spec updated) threaded through CompleteRequest, and a shared engine wikilink_task_result helper used by both the capture branch and links_only_result ([[ first, then (( with owner = --source-note or ""). New tests/fixtures/task_wikilinks/prose_trigger_vectors.json (version 1, source, 45 string-only cases covering every plan bullet) replayed by prose_trigger_vectors_match. New tests/cli/capture/complete_links_only_tasks.rs (7 tests: -T without -L exit 2; wikilink_task with guards/cursor_after/picker; -S this-note group present/absent; [[ wins; plain -L leaves (( empty; prose opens where capture does not; capture path rows identical to prose rows). Docs: capture.md -L paragraph + usage line, just docs-gen regenerated reference. Verified: cargo fmt --check, just lint (exit 0), just test (exit 0: 7704 lib + 3933 cli + all other binaries), acceptance command returns context wikilink_task replacement {14,22}. docs-check: only the 3 pre-existing test_contracts failures (reproduced on clean base; see PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-oz.2](bob-cli-oz.2.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oz.6](bob-cli-oz.6.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oz.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oz.1/README.md) | [bob-cli-oz.1](bob-cli-oz.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`145b00d`](https://github.com/bobs-org/bob-cli/commit/145b00d50e56a47c2a288a9405d044956b2e0ced) | feat(capture): complete (( task links in plain prose with capture-complete -L -T | [bob-cli-oz.1](bob-cli-oz.1.md) | 2026-11-21 23:26:26 EST |
