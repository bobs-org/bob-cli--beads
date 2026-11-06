# Bead: bob-cli-ha — Glue start and past timing to the Pomodoro name

[Bead Pages](../README.md) / bob-cli-ha

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cf.md)
**Created:** 2026-11-05 05:23:37 EST · **Closed:** 2026-11-06 13:07:50 EST
**Plan:** [202611/glued\_start\_timing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/glued_start_timing.md)

## Previously Closed

> ↺ Closed 2026-11-05T18:42:41Z · done
>
> (none)
>
> Reopened 2026-11-06T16:01:12Z by `sase bead open`

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/glued_start_timing.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:158794c224e27f034e87d84c | attached via sase artifact create --bead |
| related | file:explicit:eaf3c3a97cb043b51c41c712 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/glued_start_timing.md

<!-- sase:links:end -->

## Description

Capture `=` and `x=` tokens take their timing glued to a bare Pomodoro name (`=build-`, `=10-3fix`, `x=fix3`); the `@` and `<X>#` separators are retired with teaching errors, and every client, doc, and test teaches only the shorter spellings.

## Notes

[2026-11-05T14:31:47Z · 18i--code] DISCOVERED ISSUE: `just docs-check` on this working tree fails its executable tutorial at TUTORIAL_FENCE 12 in docs/start/first-bob-day.md:117 because the fence still uses `=#focus`; capture rejects that retired syntax and instructs `=focus`. The preceding docs checks pass. This falls within the active glued-timing epic's documentation scope. Reproduction source: file:explicit:eaf3c3a97cb043b51c41c712.

[2026-11-05T15:28:26Z · 18l--code] DISCOVERED ISSUE: Independent reproduction during the approved reconcile coalescing work: just docs-check passes lint, generated drift, strict site build, published URLs, offline links, edit links, and search smoke, then fails the executable tutorial at TUTORIAL_FENCE 12 in docs/start/first-bob-day.md:117. The example uses =#focus, which capture rejects as retired and teaches =focus. This is within the glued-timing epic's documentation scope; the docs phase was closed but the epic remains in progress. Reproduced on 2026-11-05 with just docs-check.

[2026-11-05T16:34:09Z · bob-cli-ha.land] LAND AUDIT / FOLLOW-UP TRIAGE: Reviewed this epic and every note on closed ha.1-ha.4, the approved plan, Rust phase commits 01cb7b5c/d012e782/43275437, Mac phase snapshot 0f1ed3bf5db2338f002cba3ade78ed1de7ce4e02, actual lexer/editor/completion/composer/agenda source and tests, and fetched master histories. Rust origin/master=43275437; Mac master=6c39ff8. Approved when_needed hash names and grammar-only name constraints are implemented; no phase edited memory or added a global creation ban. Both epic tutorial reports are addressed by =focus in docs/start/first-bob-day.md, including concurrent 2e91d45b integration. Reviewed non-epic 7e437418, 38df2d39, 1a5c9b00, bb8d47e9, 2e91d45b, 344c0973, and 1f2b28b0: preserve alias completion, off-clock budgets, max_task_link_count, event refiling/coalescing, and new agreement vectors during repair. Remaining epic work: obsolete PomodoroStartTiming variant/emitters; final valid teaching rewrites for combined retired syntax and non-bare past names; completion replacement must preserve trailing timing when a chosen name needs #; shared Pomodoro vectors were changed without mirroring plugin copies/harness; Mac ha.4 patch exists only in the CI snapshot, absent from master; snapshot fixture x =de disagrees with unchanged x =#de tests/fake-bob and requires repair; Mac-owned docs still teach retired bare-name hashes. All retained in the medium tale sase_plan_glued_timing_closeout.md, including verification and this epic closeout. No just check or new build was run in this audit-only turn; required file-change verification belongs to the repair. Installed bob 0.4.0 is stale and was not used as evidence for the checked-out grammar. No --epic-symbol entries; current justfile has no symvision recipe; no parent_bead. PROPOSAL OUTCOMES: ha.2 #1 declined as a separate task because removal of the obsolete timing need was explicitly required by this epic. ha.3 #2 filed as small flake bob-cli-hf (ready), linked to related but distinct overwrite-timezone task h6; phase-reported minute rollover and unchanged isolated rerun plus source equality checks support it. ha.4 #1 split: shared 12 baseline Mac failures corroborated on existing bob-cli-h7 and active owner bob-cli-h8 using file:explicit:158794c224e27f034e87d84c; no duplicate task. Named-start-chain failure declined as unrelated because the snapshot has a concrete grammar-fixture mismatch, retained in epic work. Base-only Move/Pull-In seed failure supplements h8.5 note #1 on h8; no new task or confirmed-flake claim because existing owner already has the proposal and these runs are different trees. The epic remains open pending the tale; the tale must finish landing itself without waiting for its own final commit or push.

[2026-11-05T18:42:41Z · bob-cli-ha.land] CLOSEOUT glued_timing_closeout tale (workspace bob-cli_32, uncommitted repair): Rust 17 files — removed Need::PomodoroStartTiming and all dangling-@ incomplete emitters (editor_pomodoro/editor_classify/editor_parse/tokens/completion, TimingIncomplete variants, start_timing_incomplete_error); retired_at_start_error now composes final bare spellings (=#fix@3 teaches =fix3 never retired =3#fix; =#deep-work@3 teaches =3#deep-work) and yields to timing-twice when a leading timing is present; removed stale @/# order-error branch (item + editor); past hash-@ fixes (x=#fix@3 teaches x=fix3; x=#deep-work@3 teaches x=3#deep-work; leading+@ gives the twice choice x=3fix or x=fix2); duplicate-timing wins over redundant-#; completion preserves trailing timing for start/past/link incl. caret (bare keeps suffix e.g. =fix3, non-bare moves it before # e.g. =de3+DEEP WORK gives =3#deep-work; =#bo acceptance still drops a redundant hash). Decisions preserved: hash_names=when_needed, name_rule_scope=grammar, memory_record=no (no memory edited, no global creation ban, grammar rev 13). ha.2 #1 obsolete-need removal DONE here as epic work (it was declined as a separate task). Mac: cherry-picked phase snapshot 0f1ed3b onto 6c39ff8 cleanly (slash-alias, comma close-list, transfer, off-clock intact); repaired the phase-only chain mismatch to x =de (parse JSON spans/body, complete JSON cursor5/repl 3-5/candidate #deep-work, PanelModel + BobProcessClient tests, fake-bob parse+complete dispatch); Mac docs 7 bare-name spelling fixes (lone =# incomplete states kept). Plugins: menu vectors mirrored from Rust (menu equal; relocate/agree/settle preserved — wholesale copy broke ledger-themes on concurrent meet-running-unchanged relocate, so merged menu only); harness slice(1)+strip-#; build:check green; bob plugins sync done (1 unrelated warning: bob-ledger-tools overwrite refused from sibling ws bob-cli_34 uncommitted build). Verification: cargo fmt clean, diff --check clean, lib capture_language 647 + trailing-timing 1, CLI pomodoro 291 / parse 133 / complete 311, docs-gen + docs-check (447 passed 1 skipped) + docs-build green, tutorial =focus corroborated (first-bob-day.md:118, covers epic notes #1/#2 via 2e91d45b); plugins picker-view 48 + ledger-themes 34 green; Mac portable on athena Swift 6.0.3 — lint 0 errors, build ok, 2173 tests 1 skipped 0 failed; mac scratch bundle ok + typecheck-tests PASS all 4 targets (chain repair compiles). NOT verified: macOS XCTest run itself (CLT mac has no XCTest; precommit monitor t52jhn staged but never started; no push made). Phase-only chain failure addressed by the repair above; the 12 shared baseline failures stay owned by bob-cli-h7/h8 (evidence file:explicit:158794c224e27f034e87d84c). ha.3 minute-rollover flake stays bob-cli-hf. Drift since audit: 9 new origin/master commits incl. bfd7b005 feat(capture)! — zero file overlap with the 17 repair files; Mac glossary drift pre-exists on clean base (concurrent). epic-symbols: none. justfile has no symvision recipe (recorded). No parent_bead at audit; re-reading after close to confirm.

[2026-11-05T19:05:08Z · bob-cli-ha.land--1] CLOSEOUT FOLLOW-UP (workspace bob-cli_32): macOS precommit CI run 42087133312 on snapshot a5b0e376 finished cancelled — single job 'macOS 26 SwiftPM' cancelled before reporting steps, failed-job logs empty, remote precommit branch deleted by the script. No test verdict: named-start chain test neither passed nor failed in CI, so no new epic regression is observable. Chain repair stands as committed this turn (parse x =de, complete cursor 5 repl 3-5 candidate #deep-work, PanelModel/BobProcessClient/fake-bob on x =de); remaining x =# references are legacy non-chain paths. Portable evidence unchanged from land turn: athena Swift 6.0.3 lint 0 errors, build ok, 2173 tests 1 skipped 0 failed; mac scratch bundle ok + typecheck-tests PASS all 4 targets. Plugins menu vectors equal across both copies. Plan 202611/glued_start_timing.md set status done. Ownership preserved: 12 shared Mac baseline failures stay with bob-cli-h7/h8, minute-rollover flake stays bob-cli-hf, ha.2 obsolete-need removal stays epic work done here.

[2026-11-06T15:58:39Z · bob-cli-ha.land] CLOSED-BEAD LAUNCH: agent bob-cli-ha.land launched against this closed bead; status left closed.
Launch submitted 2026-11-06T15:54:25.891399Z; run 20261106105428.
Prior close: 2026-11-05T18:42:41Z · done.

[2026-11-06T16:04:33Z · bob-cli-ha.land] RELAUNCH AUDIT / FOLLOW-UP TRIAGE (2026-11-06): Reopened normally after proving prior closeout notes #4/#5 do not match current master source. Audited original plan and prior glued_timing_closeout tale, all ha.1-ha.4 notes, phase commits 01cb7b5c/d012e782/43275437, and subsequent histories. Baselines: bob-cli e0960045, Mac e9d3ae2, plugins f7ae51e. Rust still contains Need::PomodoroStartTiming, TimingIncomplete variants/emitters, retired_at_start_error producing =3#fix for =#fix@3, past hash/@ rewrite loss, and completion replacement only prefixing # while leaving trailing timing outside the replaced range. Mac lacks start_token decoding, still composes =#slug for Later, teaches =#NAME in empty copy, and has old x =#de chain fixtures/tests/fake-bob; snapshot 0f1ed3b is not in the opened local object database or master ancestry. These are unfinished epic work, not new tasks. Preserve newer grammar 16, past segment suffix/picker (6e816775/86554bf6/35c2a426/df5a6ca4), merge-in (53c1d1ad/5ab0ec22/3fe50bc7), offer close, retyping/clocks, and Gmail integration. Epic notes #1/#2 are addressed by tutorial =focus at docs/start/first-bob-day.md:118. Plugin integration is already landed via 710feae: current Rust/root/ledger vector JSONs equal; picker-view 48/48 and ledger-tools-pomodoro-themes 38/38 pass. Do not redo that repair. DECISIONS remain hash_names=when_needed, name_rule_scope=grammar, memory_record=no; no memory edit or global creation ban authorized. PROPOSAL OUTCOMES: ha.2 #1 declined as a separate task; obsolete-need removal remains epic work. ha.3 #2 remains existing ready small flake bob-cli-hf (read and recent-task search confirm); no duplicate or repeated

… and 3225 more characters

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ha.1](bob-cli-ha.1.md) | \`=\` starts and link \`=\` suffixes (bob-cli) | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-ha.2](bob-cli-ha.2.md) | \`x=\` past records (bob-cli) | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-ha.3](bob-cli-ha.3.md) | Document the glued spellings (bob-cli) | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-ha.4](bob-cli-ha.4.md) | Stop composing \`=#\` hints in Bob Mac Capture | ✓ closed | small | 2026-11-05 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ha: Glue start and past timing to the Pomodoro name [closed]"]
    n1["bob-cli-ha.1: `=` starts and link `=` suffixes (bob-cli) [closed]"]
    n2["bob-cli-ha.2: `x=` past records (bob-cli) [closed]"]
    n3["bob-cli-ha.3: Document the glued spellings (bob-cli) [closed]"]
    n4["bob-cli-ha.4: Stop composing `=#` hints in Bob Mac Capture [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n1 -.-> n3
    n1 -.-> n4
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ha.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.1.md) | [bob-cli-ha.1](bob-cli-ha.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ha.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ha.2/README.md) | [bob-cli-ha.2](bob-cli-ha.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ha.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.3.md) | [bob-cli-ha.3](bob-cli-ha.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ha.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.4.md) | [bob-cli-ha.4](bob-cli-ha.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ha.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ha.land.md) | [bob-cli-ha](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`01cb7b5`](https://github.com/bobs-org/bob-cli/commit/01cb7b5c3eb75d7353ef4a57014cc5ada1178bf6) | feat(capture): add glued Pomodoro start grammar | [bob-cli-ha.1](bob-cli-ha.1.md) | 2026-11-05 08:11:16 EST |
| bob-cli--plans | [`bob-cli--plans@e1faa69`](https://github.com/bobs-org/bob-cli--plans/commit/e1faa69e2ed28fe8d1e37be27a46ad03514baa61) | chore(plans): record reviewer decision selections | [bob-cli-ha.4](bob-cli-ha.4.md) | 2026-11-05 09:19:23 EST |
| bob-cli | [`d012e78`](https://github.com/bobs-org/bob-cli/commit/d012e782bd3b399021027e58f833ed7ce31bd298) | feat(capture)!: glue past timing to the Pomodoro name | [bob-cli-ha.2](bob-cli-ha.2.md) | 2026-11-05 09:29:58 EST |
| bob-cli | [`4327543`](https://github.com/bobs-org/bob-cli/commit/4327543778cfa446e765a5365abb2e558fdad5c0) | docs(capture): document glued timing spellings | [bob-cli-ha.3](bob-cli-ha.3.md) | 2026-11-05 11:12:44 EST |
| bob-cli | [`79709fe`](https://github.com/bobs-org/bob-cli/commit/79709fed42c5cd382e40819872859f4f47273e29) | feat(capture)!: glue start and past timing to Pomodoro names | [bob-cli-ha](README.md) | 2026-11-06 13:09:29 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h8.land][1] | Check owner epic of theme vector drift | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h8.land/README.md

<!-- sase:referenced-by:end -->
