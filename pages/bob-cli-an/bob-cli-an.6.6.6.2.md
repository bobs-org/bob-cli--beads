# Bead: bob-cli-an.6.6.6.2 — Stop bob capture filing unknown flags as task text

[Bead Pages](../README.md) / [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) / bob-cli-an.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.land.md) · **Size:** medium
**Created:** 2026-10-24 05:39:22 EDT · **Closed:** 2026-10-24 06:26:32 EDT
**Plan:** [202610/backlog\_batch4\_ci\_identity\_capture\_flags\_plugin\_tests\_relation\_race.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch4_ci_identity_capture_flags_plugin_tests_relation_race.md)

## Description

capture-flag-guard: resolve bob-cli-8a by applying the capture_flag_guard decision in bob capture and gating Bob Mac Capture's --require-pull-in-choice on a positive capability.

## Notes

[2026-10-24T10:26:32Z · bob-cli-an.6.6.6.2--1] capture_flag_guard=refuse implemented in bob capture, capture-complete, capture-parse, capture-rewrite, and capture-templates save with exit 2 plus JSON envelope under -f json and nothing written; --2/--1, bare --, post--- literal text, and trailing flag-words unchanged; Mac sends --require-pull-in-choice only after a pull_in.supported preview from the same executable and the dead pull-in fallback/note is removed; verified by just check (fmt, clippy, full cargo suite incl. 6 flag_guard integration + 4 unit tests + docs_reference goldens), just docs-check, mac portable-check 1555 tests 0 failures, and mac scratch bundle plus typecheck-tests (monitor dn0e10j1b073 exit 0); epic-symbols clean.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.2.md) | [bob-cli-an.6.6.6.2](bob-cli-an.6.6.6.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0afeb2f`](https://github.com/bobs-org/bob-cli/commit/0afeb2f3e744ee2ee775172d5c161eadd45e247b) | feat(capture)!: refuse unknown flags via capture\_flag\_guard | [bob-cli-an.6.6.6.2](bob-cli-an.6.6.6.2.md) | 2026-10-24 06:27:36 EDT |
| bob-mac-capture | [`bob-mac-capture@8400bd3`](https://github.com/bobs-org/bob-mac-capture/commit/8400bd3e1cd4afd0a29ad4a7ea83f33b7557311a) | feat(capture): gate pull-in flag on preview support | [bob-cli-an.6.6.6.2](bob-cli-an.6.6.6.2.md) | 2026-10-24 06:28:16 EDT |
