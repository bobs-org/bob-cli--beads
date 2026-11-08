# Bead: bob-cli-is.3 — Mac forwards x/s to Bob's close-outcome alias

[Bead Pages](../README.md) / [bob-cli-is](README.md) / bob-cli-is.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3r.linker.w0.md) · **Assignee:** `bob-cli-is.3` · **Size:** medium
**Created:** 2026-11-08 11:42:41 EST
**Plan:** [202611/close\_outcome\_x\_s\_typing\_aliases.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/close_outcome_x_s_typing_aliases.md)

## Description

mac-close-alias: forward lowercase non-repeat x/s keys through a lexical send prefilter into the rewrite lane, mark them meaning-changing so the hold and Return deferral cover them, and add a one-time old-bob probe. Adds recorded fixtures, tests, Mac docs, the optional decision record, and an end-to-end check.

## Notes

[2026-11-08T21:05:00Z · bob-cli-is.3] Progress: implemented Mac x/s forwarding (prefilter, meaning-changing, old-bob probe), fixtures + generator + fake-bob, 9 new tests, docs (keyboard/capture-panel/protocol) within budget. Verified: portable-check 2268 passed/1 skipped on athena, docs-check green, Bob binding-contract rows green (xx->x!, xs->x*, past/link/lead/numbered fire; prose/uppercase/retired unchanged). Mac precommit CI failed Build on String.Index(utf8:within:) label (fixed, commit 3e95510); full macOS CI re-run still needed before close. No memory edits (decision declined). -r Record phase progress and remaining CI verification for next agent

[2026-11-08T22:09:48Z · bob-cli-is.3] Resumed verification: prior Mac commit 2a39c2ffac859a2d1594171ef835b8d6a7b9c6f3 landed; its CI 42523594058 builds but has 24 test assertion failures. Earlier hold phase 03392a55eb87577ac8bd1b69c381949cc9e2024b is green in CI 42519302906. Repaired probe lifecycle (startup, same-client retry, replacement, cancellation, separate process lane), direct-client hold flush, chained-alias replay routing, and comma-assist parse ordering. Updated legacy call-count/agenda assertions to distinguish the capability probe; replaced new fixed-sleep checks; added bounded-release burst/probe tests and recorded emoji/chained fixtures. Verified this turn: primary just check passed (ToolRun cb2b2b563e9a1f27678567162722aa49, 643 seconds); current Bob binary passes 23 alias cases with cursor/edit/summary/idempotence/no-cursor assertions plus 25 literal cases; fixture generation, changed Swift parsing, shell syntax, and git diff --check pass. No memory edits. epic-symbols reports none. Remaining: execute prepared verification script for Athena portable-check, Mac scratch bundle/typecheck-tests, and Scripts/macos-ci-check; repair any failures, then land and watch the exact pushed SHA before closing only this phase. Verification script and per-stage logs: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261108_164606/bob-cli-is.3-verify.ckrjx6tk/verify.py.

[2026-11-08T22:22:29Z · bob-cli-is.3--1] Verification continuation: monitor 0yyp6tg1jxh1 passed Athena portable-check (2269 tests, 1 skipped, 0 failures) and Mac app bundle compilation, then failed typecheck-tests solely on missing main-actor isolation of the new nested CaptureCloseAliasTests.Editor helper. Added @MainActor to that helper; git diff --check and fixture/generator shell syntax pass. No production or portable code changed this turn, so those passing gates need no repeat. Prepared verify_mac.py beside prior per-stage logs to rerun scratch Mac bundle/typecheck-tests and full Scripts/macos-ci-check, preserving original logs. Bead remains in progress pending precommit CI, finalization, and exact pushed-SHA CI. No memory edits or new beads.

[2026-11-08T22:50:38Z · bob-cli-is.3--2] Verification continuation: macOS scratch compilation/typecheck passed in monitor refjenfv9z18. Precommit CI 42530462345 (snapshot 968fe92716d284919352148d7587bc70c10b34a0) passed lint/build but failed three tests: agenda clear test accepted the startup probe as its in-flight request; close-digit harness used plainDraft setter, clearing the pending comma-assist parse; old-Bob literal Return ran before normal parse/preview readiness. Fixed only the tests: await the exact live-preview argv, mirror editor attributedDraft binding and assert digit parse/replay count, and await ordinary grammar/preview readiness before unsupported-alias Return. No production changes this turn. git diff --check passes. Prior Rust just check, contract/fixtures and 2269 portable tests remain valid. Prepared verify_mac_assertions.py beside earlier logs to run changed Swift lint, scratch Mac typecheck and full precommit macOS CI; keep phase open until precommit passes, finalization lands the repair, and exact pushed-SHA CI is green. No memory edits or new beads.

[2026-11-08T23:17:28Z · bob-cli-is.3--3] Precommit verification is green: monitor rdq6yb396zeq / ToolRun 58ccf78cbfda74f5d221f92796ab32e0 passed changed Swift formatting, scratch Mac build and all test target typechecks, and full macOS CI run 42532454467 (snapshot 051d77bc8113377adc99b339a19ddf2f017f8e4c). Lint, Build, Test, Bundle, signature, launch smoke, and install/reinstall all passed. Confirmed the complete current working tree equals verified tree 1609ffac2fc9854d7f5cc26bc05c580f4477163f; no source changes this continuation. Prior primary just check cb2b2b563e9a1f27678567162722aa49, 48 contract cases/fixtures, docs check and 2269 portable tests (1 skipped) remain applicable. Preparing explicit sase_final commit for bob-mac-capture and a post-finalization exact-SHA CI watch. Keep this phase in progress until pushed-SHA CI is green; then check epic-symbols and close only bob-cli-is.3. No memory edits or new beads.

## Dependencies

- **Depends on:** [bob-cli-is.1](bob-cli-is.1.md) ✓ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-is.2](bob-cli-is.2.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-is.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-is.3.md) | [bob-cli-is.3](bob-cli-is.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@2a39c2f`](https://github.com/bobs-org/bob-mac-capture/commit/2a39c2ffac859a2d1594171ef835b8d6a7b9c6f3) | feat(mac-capture): alias x and s to close outcomes | [bob-cli-is.3](bob-cli-is.3.md) | 2026-11-08 16:07:25 EST |
| bob-mac-capture | [`bob-mac-capture@0f6753b`](https://github.com/bobs-org/bob-mac-capture/commit/0f6753bf429b9b1b86454fb8d95a17ce965a8f1c) | fix(mac-capture): verify close aliases and isolate probe and replay races | [bob-cli-is.3](bob-cli-is.3.md) | 2026-11-08 18:18:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.2.1.land][1] | Need the child scope to see whether it caused the mac-capture docs budget overage | 1 |
| read-by | [agent:bob-cli-is.3][2] | Need to add verification status note before handoff | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ir.2.1.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-is.3.md

<!-- sase:referenced-by:end -->
