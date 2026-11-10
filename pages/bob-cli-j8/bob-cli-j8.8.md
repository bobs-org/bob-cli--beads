# Bead: bob-cli-j8.8 — Bob Mac Capture presents notebooks

[Bead Pages](../README.md) / [bob-cli-j8](README.md) / bob-cli-j8.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3x.linker.w0.md) · **Assignee:** `bob-cli-j8.8` · **Size:** large
**Created:** 2026-11-09 12:11:28 EST
**Plan:** [202611/bob\_notebooks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_notebooks.md)

## Description

mac-notebook-capture: decode unknown block-ID intents as unsupported instead of link, show `kind: "notebook"` targets with a book icon and summary, keep notebooks out of File-under, render notebook note, sub-note, and creation previews and success lines, and present note-bullet rows in the `+` picker.

## Notes

[2026-11-10T09:58:04Z · bob-cli-j8.8--4] Mac Capture CI diagnostic: exact-SHA run 42793097983 (snapshot d2c784daf300b458013e763a672b712cfb3b58d7) passed formatting and Build but failed Test with SwiftPM fatalError during test-target compilation; no xctest process or hang-sample artifact was produced. The base SHA 9a0bb25c4b55b547a6d92c35c93017471e74feff run 42735343020 shows the same test-step failure and empty hang artifact. No notebook-specific failure was exposed. Keep this phase in progress pending a green exact-SHA gate; the separate bob-cli docs mount collision remains unresolved.

[2026-11-10T09:59:05Z · bob-cli-j8.8--4] PROPOSED FOLLOW-UP: Diagnose why Mac Capture exact-SHA CI emits SwiftPM fatalError during test-target compilation without an xctest process or hang sample, including a baseline run, and determine whether the runner or test watchdog needs a separate fix. Seen in runs 42793097983 and 42735343020.

[2026-11-10T11:07:10Z · bob-cli-j8.8] RESUMPTION AUDIT: Prior work landed in bob-mac-capture b20ceca5526c6f379f8d2983e70115f150a9ae48 and bob-cli f2882ea6fc30894c848bafa4a68e4f81b7c148ed. Full GitHub job logs identify the Test failure precisely: CaptureListPanelTests.swift:443:37 cannot find fakeBobPath in scope, identically on clean base run 42735343020/job 129563084490, feature snapshot run 42793097983/job 129751277903, and landed feature run 42795804211/job 129760562111. Each passed Swift formatting and Build; test-target compilation failed before tests ran. A bounded completion plan corrects creationParentContext using the immediate parent in Bob-provided breadcrumbs, adds focused regressions, restores the missing test-local helper, and verifies this phase. No epic-symbol entries remain as of this audit.

[2026-11-10T11:07:16Z · bob-cli-j8.8] PROPOSED FOLLOW-UP: Preserve the landed notebook feature during the bob-cli-jf repository restoration — bob-mac-capture master now includes b20ceca5526c6f379f8d2983e70115f150a9ae48 above the incident SHA 9a0bb25c, so the existing restoration gate predicated on master still equaling 9a0bb25c is stale. The docs mount collision is already tracked by bob-cli-jf; its remediation must retain this feature and any subsequent phase completion fixes. This phase does not authorize rewriting remote history.

[2026-11-10T11:35:16Z · bob-cli-j8.8] COMPLETION PASS: Nested notebook creation now names the immediate parent (penultimate Bob breadcrumb), not the root owner. Landed in bob-mac-capture working tree on top of b20ceca5526c6f379f8d2983e70115f150a9ae48: CaptureNotebookPresentation.creationParentContext, generated notebook-capture-create-nested.json from host bob SHA f2882ea6fc30894c848bafa4a68e4f81b7c148ed (bob 0.5.0, isolated scratch vault), focused presentation regressions, missing test-local fakeBobPath() in CaptureListPanelTests.swift (the compiler diagnostic on base 9a0bb25c run 42735343020 / snapshot 42793097983 / feature 42795804211), and notebook ID-flow panel tests using decoded notebook-complete-parent-notes.json candidate dev_nvim|14:060f4792 through fake-bob capture-task-id. Offline: bash -n Scripts/generate-notebook-fixtures.sh, parsed generated JSON, python3 -B Scripts/test_macos_ci_check.py (42 tests OK). No local swift/swift-format. just docs-check still fails on unchanged host SHA f2882ea6 with the bob-mac-capture mount collision already tracked by bob-cli-jf. Exact-SHA macos-swift.yml gate is next via Scripts/macos-ci-check.

## Dependencies

- **Blocks:** [bob-cli-j8.10](bob-cli-j8.10.md) ◐ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j8.5](bob-cli-j8.5.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.8.md) | [bob-cli-j8.8](bob-cli-j8.8.md) | 4 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2882ea`](https://github.com/bobs-org/bob-cli/commit/f2882ea6fc30894c848bafa4a68e4f81b7c148ed) | fix(ci): select Mac Capture workflow for exact-SHA checks | [bob-cli-j8.8](bob-cli-j8.8.md) | 2026-11-10 05:02:21 EST |
| bob-mac-capture | [`bob-mac-capture@b20ceca`](https://github.com/bobs-org/bob-mac-capture/commit/b20ceca5526c6f379f8d2983e70115f150a9ae48) | feat(capture): present notebook capture targets and previews | [bob-cli-j8.8](bob-cli-j8.8.md) | 2026-11-10 05:02:56 EST |
| bob-mac-capture | [`bob-mac-capture@3fb3a2b`](https://github.com/bobs-org/bob-mac-capture/commit/3fb3a2bea591fd9756722cf8b313d0394ffdf746) | fix(capture): name nested notebook parent and restore Mac tests | [bob-cli-j8.8](bob-cli-j8.8.md) | 2026-11-10 06:36:49 EST |
| bob-mac-capture | [`bob-mac-capture@2c406dd`](https://github.com/bobs-org/bob-mac-capture/commit/2c406dd500915f4d8bee43cbae8f5bdbd985df1b) | test(capture): fix notebook picker assertions and dotted type-through harness | [bob-cli-j8.8](bob-cli-j8.8.md) | 2026-11-10 07:04:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1aq][1] | Its Mac commits sit on the polluted bob-mac-capture master; impact report on bob-cli-jf | 1 |
| read-by | [agent:bob-cli-j8.8--4][2] | Verify the diagnostic note recorded the exact CI failure before finalizing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.1aq/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.8.md

<!-- sase:referenced-by:end -->
