# Bead: bob-cli-ee — Capture t:\<type\> task-type markers with configured-type completion

[Bead Pages](../README.md) / bob-cli-ee

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b6.md) · **Assignee:** `bob-cli-ee.land`
**Created:** 2026-10-30 04:22:33 EDT · **Closed:** 2026-10-30 14:30:22 EDT
**Plan:** [202610/capture\_type\_marker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_marker.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/capture_type_marker.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_type_marker.md

<!-- sase:links:end -->

## Description

Typing `t:` at either edge of any capture line opens a fast, beautiful menu of your configured task types in Bob Mac Capture (and zsh). The accepted `t:fix` marker types the task the item creates or targets, and the live preview says exactly what will happen. Existing Task Links stay in agreement with the new type, and adding `t:` never changes what the rest of the draft means.

## Notes

[2026-10-30T17:33:21Z · bob-cli-ee.land] LAND FOLLOW-UP TRIAGE (2026-10-30): Used /sase_new_task, read bead/size policy, searched all-status task reports, swept the last week of tasks, inspected active epic scopes, and read bob-cli-dq/e7. Outcomes for every PROPOSED FOLLOW-UP: (1) ee.1 #1, ee.2 #1, ee.3 #1, and ee.4 #1 all propose the same decisions:type-marker-is-orthogonal record. Declined a memory task/edit because the final memory_record=no decision explicitly forbids it; the contract is already in docs/capture.md and the approved plan. (2) ee.1.1.1 #1 clone_on_copy was fixed by a0a6b497 before the first grammar commit; verified the actual classify.rs diff, so no new task or +1. The nested land note already has this disposition. (3) ee.3 #2 task-type completion at 107.4 ms p95 remains an unmet feature performance requirement (plan section 2.3/PT3); retain benchmarking and any necessary optimization in this epic, not an external task. (4) ee.4 #2 relocation debug panics are caused by ee.2 failing to supply explicit PomodoroBlockRefs for renamed/created entries. Retain in this epic. bob-cli-dq concerns status rewrites of task rows inside the Pomodoros section, a different caller and remediation; no duplicate task or unsupported +1. There are no other proposals on ee.1.1.2/.3 or the nested epic. No genuinely distinct unrelated unresolved follow-up warrants a new task.

[2026-10-30T17:33:28Z · bob-cli-ee.land] LAND AUDIT (2026-10-30): Read ee and all notes on ee.1-.4, ee.1.1 and ee.1.1.1-.3; read the approved marker and grammar plans and Mac implementation plan. Reviewed CLI commits 59d5a093/23ba4805/f40a625a/41e89597/0e178061/03a3497f and Mac 68aa63a with their source/tests. Shared masking, exact marker name resolution, new-task writes, config menu order, warn-unknown behavior, additive schema 1, Swift optional decoding/painting/menu/preview are implemented; no decision-memory edit, release version change, or shared Pomodoro vector edit belongs to these commits. Fetched origin/master; HEAD equals origin/master at 7414d3bc. Reviewed all 13 non-ee commits since 59d5a093: capture mentions 22a8c84f/b081097c, inverse phrases 5e4bee79, highlights links 60c77634, wikilink spans 4b4a4a34, conflict-copy test a844d3e1, and GCal/help/CI/freshness/docs changes. Mention staging remains after routed snapshots and preserves typed task bodies; inverse/highlights/GCal changes need no new type-marker writer. Wikilink precedence does need integration. Mac intervening 2f9a70a/ef07ce2/6376d21 are incorporated into 68aa63a; its CI run 41098433632 is still in progress, not yet a pass.
Remaining work: relocate_for_retype stages daily text without returning block refs, so four D8 outcomes panic in debug (ee.4 report) and release previews mislabel renamed entries created/unchanged, with stale pomodoro_name. Existing retype validates the raw selector before resolution, unlike the repaired new-task path. Independent isolated-vault checks with installed bob 0.4.0 reproduce ^dev:fix-x#bui t:fix succeeding and renaming BUILD to FIX; @dev+fix-x#bui t:fix with a live WRITE link succeeds and leaves the FIX task under BUILD. Full #build correctly refuses. Source corroborates both; exact-current debug-build regression is required in the repair tale. For Follow up ((foo t:, capture-parse paints bytes 16..18 task_type while capture-complete chooses wikilink_task/query foo t:, a conflict with 4b4a4a34. Add coexistence coverage and correct field ownership. Existing tests do not exercise all D8 outcomes and the strict-cap test accepts either success or failure; strengthen them as part of the repair. Retain performance acceptance and missing recorded Mac smoke/menu+preview images in the bounded medium tale. No source code changed during this audit, so no fresh just check was run; neither check-full nor all is needed in place of just check. All seven descendant phases/epics are closed, no epic-symbol entries, no just symvision recipe, and ee has no parent_bead. Keep ee and its plan open pending the tale, whose coder must finish this epic closeout before its turn ends.

[2026-10-30T17:36:23Z · bob-cli-ee.land] LAND HANDOFF READINESS: The medium repair tale passed revalidation after adding required title/goal metadata. It owns repairs, current-source just check/docs checks, Mac evidence, symbol cleanup, normal epic close, and the outer plan status update in the coder turn; no step waits for its own future commit. Descendant count clarification: seven closed phase beads (ee.1-.4 and ee.1.1.1-.3), plus the closed nested epic ee.1.1, for eight descendants. The latest Mac CI jobs query returned GitHub HTTP 502, so no additional CI pass is claimed beyond the recorded phase evidence. Epic and outer plan remain open.

[2026-10-30T18:30:22Z · bob-cli-ee.land] Landing-tale remaining work verified and closed. Final decisions unchanged: menu_order=config, unknown_types=warn, memory_record=no (no memory edit). Follow-up dispositions from the lander stand: skipped orthogonal-memory proposal (memory_record=no); clone_on_copy already fixed in a0a6b497; ee.3 #2 latency kept and verified here; ee.4 #2 D8 debug panics repaired here; bob-cli-dq remains a distinct in-section status-rewrite issue.

D8: TypeRelocation now carries source_before/dest_before/dest_after/dest_created; compose_type_relocation_refs emits explicit PomodoroBlockRef::at/created plus unlinked_before for move_to/create_below and rebases other afters via line_maps. Dry-run previews agree: rename_entry/rename_placeholder report pomodoro_name FIX, created=false, headline change=changed; create_below reports creates_pomodoro and added FIX; move_to removes the BUILD link and adds FIX. bob task move tests still pass (18/18). Named destination: ^sase:fix-p#bui t:fix returns type_marker_conflict (Pomodoro BUILD vs task FIX) with no writes. Wikilink: Follow up ((foo t: at the caret is task_type replacement 16..18; ((foo at opener+4 stays wikilink_task query fo, replacement 10..15.

PT3 remeasured 2026-10-30 on apollo debug against ~/bob, 20 samples after 1 warmup: capture Fix the parser t: p50 36.3 ms / p95 41.3 ms, under the 75 ms vault target (150 ms deadline); docs/completion.md updated; no extra catalog scan.

Verification: bob-cli just check passed (fmt/clippy/workspace tests); just docs-check passed; focused CLI type_marker_existing 14/14, complete_task_types coexistence, relocation_apply 7/7, task_move 18/18. Mac fixtures regenerated with debug bob 0.4.0; relocate() uses capture_dry; workaround commentary removed; CaptureCoreTests reject created/unchanged lies and cover wikilink/t: caret ownership. Athena just portable-check: 1802 tests, 0 failures. Mac just docs-check with BOB_CLI_DIR=this bob-cli checkout passed. sase bead epic-symbols bob-cli-ee: no entries. just symvision: absent in bob-cli and bob-mac-capture. No parent_bead.

Limitations: macOS hosted/GUI unverified. SSH to Kellys-MBP succeeded but DISPLAY was unset, so no scratch-app smoke or typecheck-tests; generated capture-task-type-menu / typed / relocation-preview renders were inspected and are not manual smoke. Mac CI 41098433632 (68aa63a): Lint+Build passed; Test failed with 11 assertion failures in CaptureTaskTypeHostedTests (live fake-bob task_type completion timeouts on t: / t:fix Fix it / Fix the parser t: / child t:fi, plus typed-row record write); Bundle/install/launch-smoke skipped; test-hang artifact empty. portable-check cannot run BobMacCaptureTests. Close does not wait on this tale's own commit, push, or CI SHA.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ee.1](bob-cli-ee.1.md) | bob-cli t:\<type\> grammar, parse spans, and new-task typing | ✓ closed | large | 2026-10-30 | 1 | 0 |
| [bob-cli-ee.2](bob-cli-ee.2.md) | bob-cli retyping of targeted existing tasks with D8 relocation | ✓ closed | medium | 2026-10-30 | 1 | 1 |
| [bob-cli-ee.3](bob-cli-ee.3.md) | bob-cli task\_type completion context and zsh rows | ✓ closed | medium | 2026-10-30 | 1 | 1 |
| [bob-cli-ee.4](bob-cli-ee.4.md) | Bob Mac Capture t:\<type\> painting, type menu, and preview | ✓ closed | large | 2026-10-30 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ee: Capture t:&lt;type&gt; task-type markers with configured-type completion [closed]"]
    n1["bob-cli-ee.1: bob-cli t:&lt;type&gt; grammar, parse spans, and new-task typing [closed]"]
    n2["bob-cli-ee.1.1: Capture type-marker grammar and new-task typing [closed]"]
    n3["bob-cli-ee.1.1.1: Shared type-marker lexer and execution grammar [closed]"]
    n4["bob-cli-ee.1.1.2: Editor spans and transparent completion parsing [closed]"]
    n5["bob-cli-ee.1.1.3: New-task type writes, agreement, output and documentation [closed]"]
    n6["bob-cli-ee.2: bob-cli retyping of targeted existing tasks with D8 relocation [closed]"]
    n7["bob-cli-ee.3: bob-cli task_type completion context and zsh rows [closed]"]
    n8["bob-cli-ee.4: Bob Mac Capture t:&lt;type&gt; painting, type menu, and preview [closed]"]
    n0 --> n1
    n1 --> n2
    n2 --> n3
    n2 --> n4
    n2 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n1 -.-> n6
    n1 -.-> n7
    n1 -.-> n8
    n3 -.-> n4
    n4 -.-> n5
    n6 -.-> n8
    n7 -.-> n8
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ee.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.md) | [bob-cli-ee.1](bob-cli-ee.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-ee.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.1/README.md) | [bob-cli-ee.1.1.1](bob-cli-ee.1.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ee.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.2/README.md) | [bob-cli-ee.1.1.2](bob-cli-ee.1.1.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ee.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.3/README.md) | [bob-cli-ee.1.1.3](bob-cli-ee.1.1.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ee.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.1.land.md) | [bob-cli-ee.1.1](bob-cli-ee.1.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-ee.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.2/README.md) | [bob-cli-ee.2](bob-cli-ee.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ee.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.3.md) | [bob-cli-ee.3](bob-cli-ee.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ee.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.4.md) | [bob-cli-ee.4](bob-cli-ee.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ee.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.land.md) | [bob-cli-ee](README.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`59d5a09`](https://github.com/bobs-org/bob-cli/commit/59d5a09380248882dc8ebba850af671ac6b7e0b1) | feat(capture): parse task type markers | [bob-cli-ee.1.1.1](bob-cli-ee.1.1.1.md) | 2026-10-30 05:15:00 EDT |
| bob-cli | [`23ba480`](https://github.com/bobs-org/bob-cli/commit/23ba4805ecbdd6741b4e47d2e3a01b0317849640) | feat(capture): editor spans and transparent completion parsing | [bob-cli-ee.1.1.2](bob-cli-ee.1.1.2.md) | 2026-10-30 06:50:59 EDT |
| bob-cli | [`f40a625`](https://github.com/bobs-org/bob-cli/commit/f40a625aa776f6291a34ffe229eede07bc384b55) | feat(capture): enable t: type-marker writes for new tasks | [bob-cli-ee.1.1.3](bob-cli-ee.1.1.3.md) | 2026-10-30 07:59:32 EDT |
| bob-cli | [`41e8959`](https://github.com/bobs-org/bob-cli/commit/41e89597a70755763e27ce74138b05baa00e1c54) | feat(capture): complete type-marker grammar and writers | [bob-cli-ee.1.1](bob-cli-ee.1.1.md) | 2026-10-30 09:40:00 EDT |
| bob-cli--plans | [`bob-cli--plans@2aae7dc`](https://github.com/bobs-org/bob-cli--plans/commit/2aae7dcd9bbb870c7ec126e0356ff9c372d98d03) | docs(plans): mark capture type grammar complete | [bob-cli-ee.1.1](bob-cli-ee.1.1.md) | 2026-10-30 09:40:44 EDT |
| bob-cli | [`0e17806`](https://github.com/bobs-org/bob-cli/commit/0e17806152599506b963ac64c1f466943f8a782b) | feat(capture): retype existing tasks with t: and D8 relocation | [bob-cli-ee.2](bob-cli-ee.2.md) | 2026-10-30 10:56:56 EDT |
| bob-cli | [`03a3497`](https://github.com/bobs-org/bob-cli/commit/03a3497fe26a6b2c5c1f0ae09bdb026b1e19f839) | feat(capture): add task type completion context | [bob-cli-ee.3](bob-cli-ee.3.md) | 2026-10-30 11:34:49 EDT |
| bob-mac-capture | [`bob-mac-capture@68aa63a`](https://github.com/bobs-org/bob-mac-capture/commit/68aa63a1536b677f4ed57d8492864665a3bb73f8) | feat(capture): present t:\<type\> menu, pills, and relocation preview | [bob-cli-ee.4](bob-cli-ee.4.md) | 2026-10-30 13:23:23 EDT |
| bob-cli | [`6990e89`](https://github.com/bobs-org/bob-cli/commit/6990e89b1ad1b9d1984f37adc29bfb5129a6d2d3) | fix(capture): pin D8 relocation identity and named type-marker agreement | [bob-cli-ee](README.md) | 2026-10-30 14:32:23 EDT |
| bob-mac-capture | [`bob-mac-capture@f6a2e73`](https://github.com/bobs-org/bob-mac-capture/commit/f6a2e732ef0a8136885488d5bb9b068303614a8a) | test(capture): refresh t:type fixtures for truthful relocation previews | [bob-cli-ee](README.md) | 2026-10-30 14:33:19 EDT |
| bob-cli--plans | [`bob-cli--plans@97580b9`](https://github.com/bobs-org/bob-cli--plans/commit/97580b9f420eeee3f9cf1f37bf810aefaaa1ee96) | chore(plans): mark capture type-marker epic and landing tale done | [bob-cli-ee](README.md) | 2026-10-30 14:33:57 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ee.1.1.2][1] | Need epic DECISIONS final | 1 |
| read-by | [agent:bob-cli-ee.1.1.land--1][2] | Verify the outer epic remains open after grammar phase closeout | 2 |
| read-by | [agent:bob-cli-ee.2][3] | Need epic scope and design | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.1.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ee.1.1.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ee.2/README.md

<!-- sase:referenced-by:end -->
