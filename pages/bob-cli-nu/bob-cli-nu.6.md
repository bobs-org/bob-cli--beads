# Bead: bob-cli-nu.6 — ⌘↵ runs the command chip at the cursor, with an armed chip and keycap hint

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.6` · **Size:** medium
**Created:** 2026-11-20 05:59:33 EST · **Closed:** 2026-11-20 12:18:10 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

keymap: compose a command-chip step into the existing Meta+Enter dispatcher in bob-navigation-hotkeys, add targetAt/runAtCursor and a palette command, and paint the armed chip and a muted ⌘↵ Run keycap from the live binding. The Gmail and Highlights hints yield, and every old ⌘↵ target is regression-tested.

## Notes

[2026-11-20T15:58:37Z · bob-cli-nu.4.1.land] Heads-up from the bob-cli-nu.4.1 land agent: bob-plugins docs/develop/plugin-apis.md is at 7,980/8,000 words (develop/ warning cap). Adding the keymap contract there will cross it; trim or plan a split of the command-chip sections (see the DISCOVERED ISSUE note on bob-cli-nu).

[2026-11-20T16:41:48Z · bob-cli-nu.5] Heads-up from bob-cli-nu.5 (fence): bob-run cards mount through commandChipMount with the chipAt block identity { form: "block", fence: { open, close }, line: open } plus the render sourcePath, so store.setArmed({ ...chipAtResult.chip, sourcePath, key }) arms the card (accent border + header rule) with no extra wiring; ⌘↵ on a fence should call commandChipActivate with that chip so card Run and ⌘↵ share one path (covered by test-command-chips-fence.cjs "armed card" case).

[2026-11-20T17:16:10Z · bob-cli-nu.6] PROPOSED FOLLOW-UP: Chips on nested list bullets never render in Live Preview — bob-chips 050-live-preview.js copyChipLiveLineIsIndentedCode (/^(?: {4}|\t)\S/) treats every tab- or 4-space-indented line, i.e. every nested bullet such as "\t- `run: bob plan`", as an indented code block, so chipLiveChipsForLine returns [] for both copy and command chips there (Reading view is unaffected). Pre-existing from the copy-chip epic; seen in the nu.6 Obsidian e2e screenshot keymap-task-fallback.png (the ⌘↵ task-fallback target on a child bullet shows as plain inline code, so its armed accent cannot appear, though ⌘↵ still runs it and the keycap on the task line names it). Fix idea: when the syntax tree is available, rely on copyChipLivePosIsInlineCode (which already rejects codeblock nodes) and keep the regex only as the tree-less fallback, or skip it for list-item continuation lines; add LP vectors for tab- and 4-space-nested bullets.

[2026-11-20T17:16:18Z · bob-cli-nu.6] PROPOSED FOLLOW-UP: scripts/obsidian-copy-chips-e2e.cjs:528 still records "api.copyChips v1" with apiVersion === 1, but copyChips has been v2 since db89aec (task-scoped chipAt), so the real-Obsidian copy-chips e2e ends E2E FAIL on that one case on a clean tree (run on athena 2026-11-20 during nu.6; every other case passed). Update the assertion to version 2 (or >= 2).

[2026-11-20T17:16:26Z · bob-cli-nu.6] PROPOSED FOLLOW-UP: bob-chips 0.13.0 (keymap) is committed but NOT deployed: bob plugins sync refused because the vault bob-chips is bob-cli-nu.7's uncommitted build from workspace 14 (still running), and the repo rule forbids -F. bob-navigation-hotkeys 2.92.0 and bob-ledger-tools 1.143.0 were deployed from this checkout (identical bytes to the nu.6 commit); both feature-detect targetAt/runAtCursor, so they are safe beside the older bob-chips. Whoever lands next (nu.7 after rebasing onto nu.6, or the nu land agent) must sync bob-chips from a clean tree containing both, then ask Bryan to reload Obsidian.

[2026-11-20T17:16:33Z · bob-cli-nu.6] PROPOSED FOLLOW-UP: docs budgets are now at their caps. docs/bob-navigation-hotkeys.md was exactly 6000/6000 lint words (reference/ cap is an error) on the base; nu.6 stayed at 5995 only by trimming three sentences in the keyboard-layers section, so any further nav docs change needs a trim or a split. docs/develop/plugin-apis.md is 7998 wc / 7832 lint words (8000 develop/ warning cap) after nu.6 tightened the Bob Chips and Command Mode intros; the planned move of the command-chip contracts to their own develop page (nu.4.1.land DISCOVERED ISSUE on bob-cli-nu) is still needed before author (nu.7) or adopt add more.

[2026-11-20T17:18:10Z · bob-cli-nu.6] Keymap phase done in bob-plugins (rebased onto the landed fence phase 59f3783). bob-chips 0.13.0: new 077-command-keymap.js adds api.commandChips.targetAt(view) (none with skipped for no-run/mobile/no Command Mode, ambiguous, blocked with bob reason, ready with chip/via/running/loading/key via commandChipAt + nav taskScope + cached resolve) and runAtCursor(view) (none -> handled:false; ambiguous/blocked -> one Notice, handled; ready -> commandChipActivate with source/line provenance, fence provenance = opening line, stale check, brief is-fired pulse on the pill or bob-run card), the hotkey-less palette command run-at-cursor, and a debounced CM6 painter that arms the store target and paints a muted .bob-run-chip-hint keycap (Run / Run · LABEL for a task target on another line / Output while running) from the live binding of the dispatcher, only with nav commandChipDispatch === 1, a binding, a focused editor, and one empty selection; never for ambiguous/refused/loading/copy-only. Chip tooltips learn the binding (Click or ⌘↵ to run). bob-navigation-hotkeys 2.92.0: 677e mixin; dispatcher asks runAtCursor first and stops on handled; commandChipDispatch flag; Highlights status chip and rail yield when targetAt is not none; command renamed, id kept. bob-ledger-tools 1.143.0: ⌘↵ Gmail capsule yields when the flag is set and targetAt is not none. Verified: new test-command-chips-keymap (14), test-navigation-command-chip-dispatch (10: every rule, ambiguous/refused never fall through, Bank-shaped row, regressions for reading task, highlight block link, Gmail link, plain link, no Command Mode/bob-chips/ref note/Reading), GO17 Gmail yield; full npm test 7814/7816 with only the load-sensitive 25 ms perf asserts tracked by bob-cli-km and bob-cli-io failing (40/40 in isolation); validate 12/12; docs:check all gates passed (nav reference page 5995/6000 after trims). Real Obsidian on athena (xvfb, stub bob): new obsidian-command-chips-keymap-e2e 13/13 (line chip armed + M-↵ Run, task fallback label, Bank row chip vs link, linked task keeps chain, ambiguous/unavailable refuse with no keycap, Output keycap + no second run, Vim normal mode, bob-run fence sequence, ref/ note, no note writes, exact stub invocations); existing command-chips e2e 29/29. Chromium preview adds a ⌘↵ section (no failures); PNGs registered as artifacts. Deployed nav 2.92.0 and ledger 1.143.0; bob-chips deploy pending nu.7 (see follow-up notes). E2E note: under xvfb, CDP focus emulation is needed for CM hasFocus but makes Obsidian ignore hotkeys, so the e2e reads cues with it on and presses keys with it off.

## Dependencies

- **Depends on:** [bob-cli-nu.4](bob-cli-nu.4.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.8](bob-cli-nu.8.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.6/README.md) | [bob-cli-nu.6](bob-cli-nu.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@36dcf7c`](https://github.com/bobs-org/bob-plugins/commit/36dcf7cf4b6ed7c0f11144135646da87f7a65cb5) | feat(bob-chips): ⌘↵ runs the command chip at the cursor, with an armed chip and keycap | [bob-cli-nu.6](bob-cli-nu.6.md) | 2026-11-20 12:20:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.5][1] | Need sibling phase notes for fence phase context | 1 |
| read-by | [agent:bob-cli-nu.6][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.6/README.md

<!-- sase:referenced-by:end -->
