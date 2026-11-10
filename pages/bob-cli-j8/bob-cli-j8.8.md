# Bead: bob-cli-j8.8 — Bob Mac Capture presents notebooks

[Bead Pages](../README.md) / [bob-cli-j8](README.md) / bob-cli-j8.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3x.linker.w0.md) · **Assignee:** `bob-cli-j8.8` · **Size:** large
**Created:** 2026-11-09 12:11:28 EST · **Closed:** 2026-11-10 07:57:25 EST
**Plan:** [202611/bob\_notebooks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_notebooks.md)

## Description

mac-notebook-capture: decode unknown block-ID intents as unsupported instead of link, show `kind: "notebook"` targets with a book icon and summary, keep notebooks out of File-under, render notebook note, sub-note, and creation previews and success lines, and present note-bullet rows in the `+` picker.

## Notes

[2026-11-10T09:58:04Z · bob-cli-j8.8--4] Mac Capture CI diagnostic: exact-SHA run 42793097983 (snapshot d2c784daf300b458013e763a672b712cfb3b58d7) passed formatting and Build but failed Test with SwiftPM fatalError during test-target compilation; no xctest process or hang-sample artifact was produced. The base SHA 9a0bb25c4b55b547a6d92c35c93017471e74feff run 42735343020 shows the same test-step failure and empty hang artifact. No notebook-specific failure was exposed. Keep this phase in progress pending a green exact-SHA gate; the separate bob-cli docs mount collision remains unresolved.

[2026-11-10T09:59:05Z · bob-cli-j8.8--4] PROPOSED FOLLOW-UP: Diagnose why Mac Capture exact-SHA CI emits SwiftPM fatalError during test-target compilation without an xctest process or hang sample, including a baseline run, and determine whether the runner or test watchdog needs a separate fix. Seen in runs 42793097983 and 42735343020.

[2026-11-10T11:07:10Z · bob-cli-j8.8] RESUMPTION AUDIT: Prior work landed in bob-mac-capture b20ceca5526c6f379f8d2983e70115f150a9ae48 and bob-cli f2882ea6fc30894c848bafa4a68e4f81b7c148ed. Full GitHub job logs identify the Test failure precisely: CaptureListPanelTests.swift:443:37 cannot find fakeBobPath in scope, identically on clean base run 42735343020/job 129563084490, feature snapshot run 42793097983/job 129751277903, and landed feature run 42795804211/job 129760562111. Each passed Swift formatting and Build; test-target compilation failed before tests ran. A bounded completion plan corrects creationParentContext using the immediate parent in Bob-provided breadcrumbs, adds focused regressions, restores the missing test-local helper, and verifies this phase. No epic-symbol entries remain as of this audit.

[2026-11-10T11:07:16Z · bob-cli-j8.8] PROPOSED FOLLOW-UP: Preserve the landed notebook feature during the bob-cli-jf repository restoration — bob-mac-capture master now includes b20ceca5526c6f379f8d2983e70115f150a9ae48 above the incident SHA 9a0bb25c, so the existing restoration gate predicated on master still equaling 9a0bb25c is stale. The docs mount collision is already tracked by bob-cli-jf; its remediation must retain this feature and any subsequent phase completion fixes. This phase does not authorize rewriting remote history.

[2026-11-10T11:35:16Z · bob-cli-j8.8] COMPLETION PASS: Nested notebook creation now names the immediate parent (penultimate Bob breadcrumb), not the root owner. Landed in bob-mac-capture working tree on top of b20ceca5526c6f379f8d2983e70115f150a9ae48: CaptureNotebookPresentation.creationParentContext, generated notebook-capture-create-nested.json from host bob SHA f2882ea6fc30894c848bafa4a68e4f81b7c148ed (bob 0.5.0, isolated scratch vault), focused presentation regressions, missing test-local fakeBobPath() in CaptureListPanelTests.swift (the compiler diagnostic on base 9a0bb25c run 42735343020 / snapshot 42793097983 / feature 42795804211), and notebook ID-flow panel tests using decoded notebook-complete-parent-notes.json candidate dev_nvim|14:060f4792 through fake-bob capture-task-id. Offline: bash -n Scripts/generate-notebook-fixtures.sh, parsed generated JSON, python3 -B Scripts/test_macos_ci_check.py (42 tests OK). No local swift/swift-format. just docs-check still fails on unchanged host SHA f2882ea6 with the bob-mac-capture mount collision already tracked by bob-cli-jf. Exact-SHA macos-swift.yml gate is next via Scripts/macos-ci-check.

[2026-11-10T12:16:40Z · bob-cli-jf.1.1--1] HISTORY RESTORED by approved gate custom-79d25c9d-301c-4338-adf4-7fd429460d10 on 2026-11-10. Old master 2c406dd500915f4d8bee43cbae8f5bdbd985df1b -> restored master af604c6d9e05ec6440bfce5fa15ced97e388035c, based on unchanged GOOD 29147289ca584953ce7f8cfd29b5ed60a5380f76. Complete genuine Mac commit mapping:
- b20ceca5526c6f379f8d2983e70115f150a9ae48 -> 6dddea35b47bfc64c1295d547a3966c9e7a516e7 (feat(capture): present notebook capture targets and previews)
- 3fb3a2bea591fd9756722cf8b313d0394ffdf746 -> a36f3e8163357828e09b132a5fc2c9fdf77c2c05 (fix(capture): name nested notebook parent and restore Mac tests)
- 5e29dd26b1adb908cb402df83153b1c73c25164d -> 37933a1425f4fc8f2dcb1cb261dca065e9d7b7fd (fix(capture): show set Record Card values and conceal the route @)
- 2c406dd500915f4d8bee43cbae8f5bdbd985df1b -> af604c6d9e05ec6440bfce5fa15ced97e388035c (test(capture): fix notebook picker assertions and dotted type-through harness)
BAD 9a0bb25c4b55b547a6d92c35c93017471e74feff and the accidental bob-cli history are removed, not replayed. Gate verified fidelity on all 53 touched paths; scratch recovery backup remains /tmp/bob-mac-restore-0ig_wzuq. Deleted polluted remote branch refs/heads/ci/precommit/4f12681e038ad03a8ecb1de466d2a1ae (af75f0912ead90bad77bd8a6c0886409b2b00bd1). Live master verified equal to restored SHA; fetched every advertised head/tag and no remote ref contains BAD (4 heads, 0 tags). SHA searches found citations on bob-cli-jf, bob-cli-jf.1.1, and bob-cli-j8.8, so this full mapping is recorded on each. Exact-SHA CI run 42813392077 remains pending; this note does not claim CI is green. Run: https://github.com/bobs-org/bob-mac-capture/actions/runs/42813392077

[2026-11-10T12:47:24Z · bob-cli-j8.8--3] DISCOVERY MISS: Scripts/macos-ci-check snapshot 758635ea619cd8dbd01e5499acdf09d29c2bd54a on ci/precommit/9a875cf84f7791944c6ccfc8ceb4c8e8 returned exit 2 after 300s with no matching macos-swift.yml push run (monitor 790br1). Restoration (bob-cli-jf.1.1) dropped macos-swift.yml; genuine Mac CI is ci.yml / "CI" / job macOS 26 SwiftPM. No Swift diagnostic from that check. Restored parent af604c6d run 42813392077 failed three tests: ConcealEditorHighlightTests split-wash assertion (fixed in 28aa5b32), bob-cli-jb double-equals flake, and CaptureAliasTipPanelTests.testSecondEligibleSigilInASessionShowsNoTip waitUntil timeout (not this phase). Watching exact-SHA ci.yml run 42816665790 on HEAD 28aa5b32a62011266459e13723236e4caeda2478.

PROPOSED FOLLOW-UP: After bob-cli-jf restoration, Scripts/macos-ci-check (byte-identical with host scripts/dev/macos-ci-check) still selects workflow macos-swift.yml for bobs-org/bob-mac-capture. That file is absent on restored master; retarget the bob-mac-capture profile to ci.yml so the exact-SHA gate can discover Mac Capture CI.

[2026-11-10T12:57:19Z · bob-cli-j8.8--4] EXACT-SHA CI GREEN on restored Mac master. Workflow CI (.github/workflows/ci.yml), job macOS 26 SwiftPM, run 42816665790 on HEAD 28aa5b32a62011266459e13723236e4caeda2478 (https://github.com/bobs-org/bob-mac-capture/actions/runs/42816665790). Required steps passed: Lint Swift formatting, Build, Test, Bundle, Verify plist and signature, Launch smoke test, Install and reinstall. Hang-sample and launch-smoke diagnostic uploads stayed skipped on this clean run.

Restored SHA mapping for this phase:
- feature 6dddea35b47bfc64c1295d547a3966c9e7a516e7 (was b20ceca5526c6f379f8d2983e70115f150a9ae48) feat(capture): present notebook capture targets and previews
- completion a36f3e8163357828e09b132a5fc2c9fdf77c2c05 (was 3fb3a2bea591fd9756722cf8b313d0394ffdf746) fix(capture): name nested notebook parent and restore Mac tests
- test-fix af604c6d9e05ec6440bfce5fa15ced97e388035c (was 2c406dd500915f4d8bee43cbae8f5bdbd985df1b) test(capture): fix notebook picker assertions and dotted type-through harness
- conceal-assertion 28aa5b32a62011266459e13723236e4caeda2478 test(capture): expect split wash runs when concealing two record routes
- host SHA unchanged: f2882ea6fc30894c848bafa4a68e4f81b7c148ed

Nested-parent regression: creationParentContext uses the penultimate Bob breadcrumb. Area create ["dev","Keys"] reads in dev; nested create ["dev","Neovim","Lua","Keys"] reads in Lua. Short, missing, or blank parents omit the phrase. Fixture notebook-capture-create-nested.json was generated from host bob f2882ea6 in an isolated scratch vault.

ID-flow regression: ID-less notebook notes in the + picker call capture-task-id --route dev_nvim --task-ref 14:060f4792; insert waits for success; duplicate-id leaves the draft marker unchanged. fakeBobPath() is restored so CaptureListPanelTests compile (the compiler diagnostic on base 9a0bb25c runs 42735343020 / 42793097983 / 42795804211).

Local swift and swift-format remain unavailable. just docs-check still hits the bob-cli-jf mount collision on unchanged host SHA f2882ea6. Scripts/macos-ci-check (byte-identical with host scripts/dev/macos-ci-check) still selects workflow macos-swift.yml for bobs-org/bob-mac-capture; that file is absent on restored master. Genuine Mac CI is ci.yml.

Classified elsewhere: CaptureRelationEqualsAliasTests.testFastDoubleEqualsBeforeReplyCollapsesToOne is flake bob-cli-jb. CaptureAliasTipPanelTests.testSecondEligibleSigilInASessionShowsNoTip timed out on restored parent af604c6d run 42813392077 and passed on 28aa5b32. The two-record conceal wash-run assertion came from concurrent athena.1ao commit 37933a14 and is aligned in 28aa5b32.

sase bead epic-symbols bob-cli-j8.8: no leftover entries.

PROPOSED FOLLOW-UP: After bob-cli-jf restoration, retarget Scripts/macos-ci-check (and the byte-identical host scripts/dev/macos-ci-check) bob-mac-capture profile from macos-swift.yml to ci.yml so the exact-SHA gate can discover Mac Capture CI.

[2026-11-10T12:57:25Z · bob-cli-j8.8--4] Verified Mac notebook presentation on restored master 28aa5b32a62011266459e13723236e4caeda2478. Nested creation names the immediate parent; ID-less notebook notes keep the capture-task-id assignment flow; fakeBobPath compiles. Exact-SHA ci.yml run 42816665790 (workflow CI, job macOS 26 SwiftPM) passed Test, Bundle, Verify plist and signature, Launch smoke test, and Install and reinstall. Feature SHA 6dddea35, completion a36f3e81, test-fix af604c6d, conceal assertion 28aa5b32; host SHA f2882ea6 unchanged. Local swift/swift-format unavailable. just docs-check still hits the bob-cli-jf mount collision. No epic-symbol leftovers. PROPOSED FOLLOW-UP: retarget macos-ci-check bob-mac

… and 48 more characters

## Dependencies

- **Blocks:** [bob-cli-j8.10](bob-cli-j8.10.md) ✓ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j8.5](bob-cli-j8.5.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.8.md) | [bob-cli-j8.8](bob-cli-j8.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2882ea`](https://github.com/bobs-org/bob-cli/commit/f2882ea6fc30894c848bafa4a68e4f81b7c148ed) | fix(ci): select Mac Capture workflow for exact-SHA checks | [bob-cli-j8.8](bob-cli-j8.8.md) | 2026-11-10 05:02:21 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1aq][1] | Its Mac commits sit on the polluted bob-mac-capture master; impact report on bob-cli-jf | 1 |
| read-by | [agent:bob-cli-j8.8--2][2] | Read phase status before classifying or repairing the conceal highlight CI failure | 1 |
| read-by | [agent:bob-cli-j8.8--4][2] | Verify the diagnostic note recorded the exact CI failure before finalizing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.1aq/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.8.md

<!-- sase:referenced-by:end -->
