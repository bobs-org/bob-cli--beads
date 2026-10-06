# Bead: bob-cli-4l — Answer once, advance once: review-walk auto-advance

[Bead Pages](../README.md) / bob-cli-4l

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0d.linker.w0.md) · **Assignee:** `bob-cli-4l.land`
**Created:** 2026-10-06 07:01:40 EDT · **Closed:** 2026-10-06 08:32:09 EDT
**Plan:** [202610/review\_walk\_answer\_auto\_advance.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/review_walk_answer_auto_advance.md)

## Description

During the `]s` morning review, every gesture that answers the row the walk just landed on moves to the next remaining review item in the same keystroke, and shows one toast that says what you did and where you are now. Today only Ctrl+Alt+F (and the PRE/POST Ctrl+Enter claim) does this. Alt+F stays the one explicit "stay" answer. `]s` stays the skip key. Ordinary daytime use of the same keys does not change.

## Notes

[2026-10-06T11:59:44Z · bryanbugyi34@gmail.com] The <ctrl+shift+m/p> keymaps are no longer working in Obsidian.

[2026-10-06T12:12:23Z · bob-cli-4l.land] Land agent verification (in progress): all 5 phases closed with their work present in bob-plugins (824ad2a nav-core, f100300 nav-gestures, 7ff2459 cycler, 0e0fb98 block-id-prompt, 5d0a200 hints/README) and bob-cli 756c4fc (freshness §6/§13, getting-started, task-deps §9 api v3, projects Task Card line, decision record answering-advances-the-walk). The nav-core 'vault deploy pending' note is resolved: the apollo vault and the mac both run byte-identical builds (nav 2.6.1, cycler 1.26.0, bip 1.22.0, ledger 1.29.2). No drift landed in bob-cli or bob-plugins since the epic started, so there is nothing to integrate. epic-symbols: none. No PROPOSED FOLLOW-UP notes on any child. Full npm test: the only failure is the load-dependent perf flake 'stage ranker filters 1,000 synthetic tasks under 16 ms' (test-navigation-dependencies-stage-entry-and-view.cjs:274; 17-21 ms in the full suite, passes 3/3 alone; the epic did not touch it). BLOCKER: Bryan's note 'Ctrl+Shift+M/P no longer working'. The mac went nav 2.4.0 -> 2.6.0 at 07:45 and the note came at 07:59, during the 07:40 GTD Pomodoro, so it is likely epic-caused (nav-gestures added captureReviewGesture plus settle wiring to openBulletPropertyPicker, openTaskMoveDestinationPicker, and both pickers' onClose). Static review and the Node harness found no failure: capture is try/catch-guarded, the BUSY lock always expires within 3 s, and nothing else holds it. I asked Bryan for the failure mode before planning a fix.

[2026-10-06T12:20:02Z · bob-cli-4l.land] Land agent (resumed after Bryan's answers: everywhere / nothing at all / fix in this epic). ROOT CAUSE confirmed live on the mac via obsidian-cli eval (read-only): Obsidian there is 1.14.4 (asar downloaded 2026-10-05 14:05; process restarted 08:01 today). Obsidian 1.14's Modal now owns a native instance field isOpen and Modal.open() is 'if(!this.isOpen){this.isOpen=true; ...attach, onOpen}' while close() is 'if(this.isOpen){...}'. nav's FilteredPickerModal (src/200-filtered-picker-modals.js:1-34) keeps its own isOpen guard and sets this.isOpen=true BEFORE super.open(), so Obsidian's open() no-ops: nothing renders, onClose never runs, and plugin.activeTaskMoveDestinationPicker / activeBulletPropertyPicker stay pinned to the never-opened modal (live state: isOpen=true, win=null, containerEl disconnected, 0 .modal-container). Every later Ctrl+Shift+M/P hits the 'picker already active' guard and returns true silently. Affects every FilteredPickerModal subclass (Task Card, task-move, Pomodoro move, child-note, link-candidate, yank-path pickers). Not caused by this epic's diffs (none touch open/close), but per Bryan (Q3) it is fixed in this epic via a lander tale. Other Modal subclasses in bob-plugins do not write isOpen. Plugin loaded fine (nav 2.6.1 enabled, hotkeys bound, dev:errors empty). Drift: none in bob-cli or bob-plugins since 07:01. epic-symbols: none. Follow-up triage: no PROPOSED FOLLOW-UP notes on any child; the full-suite perf flake 'stage ranker ... under 16 ms' corroborated as +1 on existing bob-cli-3w (not epic-caused); bob-cli-4e (shadowed Task Card onClose cleanup, pre-existing since c0ff974) is related but distinct and stays its own ready task.

[2026-10-06T12:32:09Z · bob-cli-4l.land] Phases .1-.5 verified in bob-plugins 824ad2a/7ff2459/0e0fb98/f100300/5d0a200 and bob-cli 756c4fc. No drift to integrate since epic start; epic-symbols: none. Ctrl+Shift+M/P regression: Obsidian 1.14 native Modal.isOpen collision in FilteredPickerModal (set isOpen=true before super.open, native open no-ops, active-picker slots pinned, every later key swallowed silently) — not caused by epic diffs, fixed here at Bryan's request. Fix: picker flag renamed isOpen->pickerOpen (200, 350 x8, 500), native isOpen left to Obsidian; stale active-picker guards fail open on pickerOpen==false or containerEl.isConnected===false (550, 500, 640 x3); ModalStub models native isOpen with idempotent open/close; nav bumped 2.6.1->2.6.2 (manifest + README table/ahead sentence), main.js rebuilt. Tests: picker-lifecycle 17/17 incl 2 new regression tests (attach/onOpen/slot-clear/reopen; stale fail-open for both pickers and both stale branches); task-card-view 55/55 (harness idempotent-close expectation updated for 1.14 semantics); full npm test 1864/1865 with only known load-dependent flake 'stage ranker filters 1,000 synthetic tasks under 16ms' (passes alone at ~8ms). Follow-up triage: no PROPOSED FOLLOW-UP notes on any child; perf flake corroborated as +1 on bob-cli-3w; bob-cli-4e (shadowed Task Card onClose cleanup) left as its own ready task. Deploy note: change is in the bob-plugins workspace checkout (uncommitted); 'bob plugins sync' from the canonical checkout still reports nav 2.6.1 and the Mac read-only plugin check confirms 2.6.1 — vault deploy + Obsidian reload pending the land. Bryan: reload plugin/restart Obsidian, then Ctrl+Shift+M and Ctrl+Shift+P on an ordinary task line, plus the bob-cli-4l.5 smoke checklist.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-4l.1](bob-cli-4l.1.md) | Nav review-advance core, shared advance tail, and nav api v3 | ✓ closed | medium | 2026-10-06 | 1 | 1 |
| [bob-cli-4l.2](bob-cli-4l.2.md) | Alt+N, Task Card, and Ctrl+Shift+M advance from a landing | ✓ closed | medium | 2026-10-06 | 1 | 1 |
| [bob-cli-4l.3](bob-cli-4l.3.md) | Ctrl+Enter completes and advances on non-checklist landings | ✓ closed | small | 2026-10-06 | 1 | 1 |
| [bob-cli-4l.4](bob-cli-4l.4.md) | Ctrl+Shift+Enter link advances from a landing | ✓ closed | small | 2026-10-06 | 1 | 1 |
| [bob-cli-4l.5](bob-cli-4l.5.md) | Hints, docs, README, decision record, and rollout | ✓ closed | small | 2026-10-06 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-4l: Answer once, advance once: review-walk auto-advance [closed]"]
    n1["bob-cli-4l.1: Nav review-advance core, shared advance tail, and nav api v3 [closed]"]
    n2["bob-cli-4l.2: Alt+N, Task Card, and Ctrl+Shift+M advance from a landing [closed]"]
    n3["bob-cli-4l.3: Ctrl+Enter completes and advances on non-checklist landings [closed]"]
    n4["bob-cli-4l.4: Ctrl+Shift+Enter link advances from a landing [closed]"]
    n5["bob-cli-4l.5: Hints, docs, README, decision record, and rollout [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n1 -.-> n3
    n1 -.-> n4
    n2 -.-> n5
    n3 -.-> n5
    n4 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4l.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.1/README.md) | [bob-cli-4l.1](bob-cli-4l.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-4l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.2/README.md) | [bob-cli-4l.2](bob-cli-4l.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-4l.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.3/README.md) | [bob-cli-4l.3](bob-cli-4l.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-4l.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.4/README.md) | [bob-cli-4l.4](bob-cli-4l.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-4l.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.5/README.md) | [bob-cli-4l.5](bob-cli-4l.5.md) | 2 |
| [bbugyi200.apollo.bob-cli-4l.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-4l.land.md) | [bob-cli-4l](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@824ad2a`](https://github.com/bobs-org/bob-plugins/commit/824ad2a5bd514c710244319c75f0e46bda7c2463) | feat(review-walk): nav-core auto-advance, shared tail, nav api v3 (nav 2.5.0) | [bob-cli-4l.1](bob-cli-4l.1.md) | 2026-10-06 07:23:00 EDT |
| bob-plugins | [`bob-plugins@7ff2459`](https://github.com/bobs-org/bob-plugins/commit/7ff24593892197f18b17603a9ae111013406dc5f) | feat(task-status-cycler): continue review walk silently after vim open/done toggle | [bob-cli-4l.3](bob-cli-4l.3.md) | 2026-10-06 07:31:11 EDT |
| bob-plugins | [`bob-plugins@0e0fb98`](https://github.com/bobs-org/bob-plugins/commit/0e0fb980ffe762233f8057f3ca784d913cff9cd6) | feat(block-id-prompt): implement bip-link-today pomodoro link-today flow | [bob-cli-4l.4](bob-cli-4l.4.md) | 2026-10-06 07:32:29 EDT |
| bob-plugins | [`bob-plugins@f100300`](https://github.com/bobs-org/bob-plugins/commit/f100300baac583b00b69516c8a1d073834f75519) | feat(nav): advance review walk from Alt+N, Task Card, and Ctrl+Shift+M landings | [bob-cli-4l.2](bob-cli-4l.2.md) | 2026-10-06 07:42:50 EDT |
| bob-cli | [`756c4fc`](https://github.com/bobs-org/bob-cli/commit/756c4fc74959a644d8b90edab8502aea342320fc) | docs(walk): publish answering-advances-the-walk decision and update review docs | [bob-cli-4l.5](bob-cli-4l.5.md) | 2026-10-06 07:52:22 EDT |
| bob-plugins | [`bob-plugins@5d0a200`](https://github.com/bobs-org/bob-plugins/commit/5d0a200c1561aa3f8154ff78599f54dc976179b5) | fix(plugins): correct PRE/POST/lane action hints and nav fallback | [bob-cli-4l.5](bob-cli-4l.5.md) | 2026-10-06 07:53:03 EDT |
| bob-plugins | [`bob-plugins@14fbfe5`](https://github.com/bobs-org/bob-plugins/commit/14fbfe5274dc37b731b6cf14539f998fa9600b33) | fix(nav): own pickerOpen flag instead of native Modal.isOpen (nav 2.6.2) | [bob-cli-4l](README.md) | 2026-10-06 08:33:32 EDT |
| bob-cli--plans | [`bob-cli--plans@7828567`](https://github.com/bobs-org/bob-cli--plans/commit/78285670908896f18770e66ee5fe7cad986129c2) | chore(plan): mark review-walk auto-advance plan done for bob-cli-4l | [bob-cli-4l](README.md) | 2026-10-06 08:34:14 EDT |
