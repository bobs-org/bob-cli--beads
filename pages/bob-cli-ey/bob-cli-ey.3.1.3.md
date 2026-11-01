# Bead: bob-cli-ey.3.1.3 — Implement unselected menus, directive rows, and the grammar gate

[Bead Pages](../README.md) / [bob-cli-ey.3.1](bob-cli-ey.3.1.md) / bob-cli-ey.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.md) · **Assignee:** `bob-cli-ey.3.1.3` · **Size:** medium
**Created:** 2026-10-31 23:33:00 EDT · **Closed:** 2026-11-01 01:16:07 EST
**Plan:** [202610/mac\_directives.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_directives.md)

## Description

menus-gate: honor initial_selection across completion contexts, render Bob-authored directive rows and bare-hash type menus, style directive spans, and require grammar at least 2 for capture without losing the draft.

## Notes

[2026-11-01T06:16:07Z · bob-cli-ey.3.1.3] menus-gate landed in bob-mac-capture: unselected completion (Int? selectedCompletionIndex; initial_selection none wins over suggested-row; Tab takes first, Down/Ctrl-N select first, Return submits the typed draft, Command-Return is submitAndOpen, disabled rows consume including mouse, File-under and chip reopen stay first-row), Bob-authored directive rows (token/name/summary/detail/disabled_reason, CAPTURE AS header, teal directive spans, shouldRequestCompletion includes directive, bare # opens the type menu unselected), and capture-parse grammar ≥ 2 (missing/1 show exactly "Update bob to use drawers and % directives", disable Capture, keep the draft; 2/3 submit; pending parse disables without that message; Recheck Bob/client identity invalidates; older generations cannot overwrite). Hosted submit tests that skip analysis call installCompatibleCaptureGrammarForTests(). athena `just portable-check`: 1866 tests, 0 failures. `just docs-check` passed. `just check-scripts` passed; fake-bob `bash -n` ok. macOS targets unverified (ssh to mac timed out). Clip-preview remains bob-cli-ey.3.1.4.

## Dependencies

- **Depends on:** [bob-cli-ey.3.1.2](bob-cli-ey.3.1.2.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.3.1.4](bob-cli-ey.3.1.4.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.3.1.3/README.md) | [bob-cli-ey.3.1.3](bob-cli-ey.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@cea18c1`](https://github.com/bobs-org/bob-mac-capture/commit/cea18c1f0e3d340d270353c2b557e523e6428a36) | feat(mac-capture)!: open unselected directive menus and gate capture on grammar 2 | [bob-cli-ey.3.1.3](bob-cli-ey.3.1.3.md) | 2026-11-01 01:17:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.3.1.3][1] | Need notes and full phase body | 10 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.3.1.3/README.md

<!-- sase:referenced-by:end -->
