# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5 — Pin bob-mac-capture's Swift format and re-indent the minority files once

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5` · **Size:** small
**Created:** 2026-10-27 06:23:59 EDT · **Closed:** 2026-10-27 07:03:16 EDT
**Plan:** [202610/backlog\_batch17\_macos\_gate\_source\_backfill\_hook\_dedupe\_dirty\_scans\_swift\_format.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md)

## Description

swift-format-config: resolve bob-cli-8k by adding a majority-style .swift-format, re-indenting the minority files in one whitespace-only commit, and compiling it on macOS CI before landing.

## Notes

[2026-10-27T10:46:29Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5] BASELINE: bob-mac-capture master 0e7eba4 had no .swift-format. First-body indent split (after matching final/public/private/class/struct/enum): 80 two-space files, 352 four-space files. Majority p99 line length in 4-space Sources is 96. Linux portable-check on master was not re-run; this phase measured the split then formatted.

FIX: added .swift-format (indent 4, tabWidth 4, lineLength 100, remaining keys from `swift format dump-configuration`). Re-indented the 80 two-space files by doubling leading spaces and adding the closer indent inside multiline string literals. git diff -w on Swift files empty (53090/53090). Did not edit AGENTS.md.

TESTS: just portable-check on athena passed (lint warnings only; 1695 tests, 0 failures). Mac ssh timed out. macos-precommit-gate has not landed. Draft PR https://github.com/bobs-org/bob-mac-capture/pull/9 SHA aab0211 CI run 40490755429 in progress; land only when Build and Test pass.

LIMITATIONS: Lint still warns on 4-space files (Package.swift #if indent, line length, rewrite rules). Those warnings existed against the 2-space default too. BobMacCapture* still needs the macOS CI job. Target task bob-cli-8k left open for the lander.

[2026-10-27T11:03:05Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5--1] PROPOSED FOLLOW-UP: mention .swift-format in bob-mac-capture AGENTS.md — the phase forbade editing AGENTS.md; agents that format Swift need the 4-space pin documented there.

[2026-10-27T11:03:16Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5--1] macOS CI run 40490755429 succeeded (Lint, Build, Test, Bundle, install gates). Merged PR #9 SHA aab0211 (merge dfd4e7b). Linux portable-check 1695 tests, 0 failures. Linked bob-mac-capture fast-forwarded to origin/master. bob-cli-8k left for the lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.5.md

<!-- sase:referenced-by:end -->
