# Bead: bob-cli-nu.7 — Mod+Shift+Y makes and edits command chips

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.7` · **Size:** medium
**Created:** 2026-11-20 05:59:33 EST · **Closed:** 2026-11-20 12:55:52 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

author: extend the make-or-edit card with a Copy | Run kind row. Run drafts get live per-step validation from resolve, an Add-bob fix, and inline-or-fence serialization. Conversion defaults are predictable, and Alt+Click edits a command chip.

## Notes

[2026-11-20T16:41:55Z · bob-cli-nu.5] Heads-up from bob-cli-nu.5 (fence): the inert bob-run card for the make-or-edit Preview row is commandFenceBuild(doc, { label, text }, { interactive: false }) then commandFencePaint(card, commandChipPaintModel(...) or null), both in plugins/bob-chips/src/085-command-fence.js; buttons render as aria-hidden spans and no gestures are wired.

[2026-11-20T17:55:10Z · bob-cli-nu.7] PROPOSED FOLLOW-UP: load-sensitive bob-plugins tests fail under full parallel `npm test` on apollo and pass alone — test-ledger-tools-event-link-times "perf — one build over a 200-link ledger stays under 25 ms" (117–200 ms under load), test-ledger-tools-frees-marks "200-link / 2000-task build stays within the 25 ms budget" (124–207 ms), and test-task-link-marks-motion (spawns preview-task-link-marks.cjs with a 90 s timeout; a killed run left an orphaned headless Chromium that made later runs time out until it was killed). None touch bob-chips; seen on both the pre- and post-keymap base. Suggest moving the perf budgets to test:perf (concurrency 1) and killing the preview child process group on timeout.

[2026-11-20T17:55:17Z · bob-cli-nu.7] PROPOSED FOLLOW-UP: bob-plugins docs/develop/plugin-apis.md is at 8,009 words on master after bob-cli-nu.6 (develop/ warning cap 8,000; docs:check still passes). nu.7 kept its own edits net-zero there. Continues the DISCOVERED ISSUE note #3 on bob-cli-nu: split the Command-chip sections onto their own develop page under an approved plan, preserving develop/plugins/plugin-apis/ URLs and anchors.

[2026-11-20T17:55:52Z · bob-cli-nu.7] Author phase done in bob-plugins (bob-chips 0.14.0, rebased on keymap 36dcf7c). Mod+Shift+Y "Make or edit chip" (id make-or-edit kept) gains a Copy|Run Kind row (Tab cycle, ←/→/Space; title COPY CHIP / COMMAND CHIP; Text named Command in Run). Defaults: edits keep their kind; selection/plain span/clipboard text that Command Mode resolves as a bob command line (incl. host-only) starts in Run, text that resolves after adding bob starts in Run with Add bob; else Copy; a late clipboard prefill never overrides a user choice. Run validation per step via resolve: ✓ title·effect·note (runs now/preview skipped/asks first/opens its output), ✗ blocks Save with bob reason, ⚠ host-only warns but saves, · unchecked without/while-loading Command Mode (Save allowed); structural faults (trailing &&) block. Add bob button (Tab cycle) inserts bob before fixable steps. runChipSerialize inline/bob-run fence, run preview chip/card, one undo transaction, stale guard; Edit target spans both kinds (fence, under cursor, line-only, ambiguity). Alt+Click on Live Preview command chips (and Run on Live Preview bob-run cards) opens the card, never runs; tooltip appends "· ⌥Click edits" only in Live Preview. Verified: new test-command-chips-author.cjs (21, real resolver on fixture catalog) + preview self-test; all chip/keymap suites green; npm test only fails 3 load-sensitive non-bob-chips tests that pass alone (follow-up noted); validate 12/12; docs:check passed (BOB_CLI_DIR=this workspace); real Obsidian e2e on athena: command-chips (incl. new author phase: Enter converts `bob e2e ok author-convert` with 0 runs, chip then runs once; Alt+Click edits with 0 runs), copy-chips (fixed stale api.copyChips v1 assertion → v2), and keymap all E2E PASS. Chromium preview PNGs (light/dark) + e2e screenshot attached as artifacts. Deployed: bob plugins sync -p bob-chips; bob plugins list shows bob-chips 0.14.0 synced+enabled on apollo. Docs: bob-chips.md Authoring/Kind/Run validation/Alt+Click; plugin-apis.md net-zero words. epic-symbols: none. Bryan: reload Obsidian.

## Dependencies

- **Depends on:** [bob-cli-nu.5](bob-cli-nu.5.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.8](bob-cli-nu.8.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.7/README.md) | [bob-cli-nu.7](bob-cli-nu.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ee941a1`](https://github.com/bobs-org/bob-plugins/commit/ee941a1cdb26b96d16f47bd7eae18d488d09de21) | feat(bob-chips): Mod+Shift+Y makes and edits command chips | [bob-cli-nu.7](bob-cli-nu.7.md) | 2026-11-20 13:17:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.5][1] | Need sibling phase notes for fence phase context | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.5/README.md

<!-- sase:referenced-by:end -->
