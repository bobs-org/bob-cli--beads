# Bead: bob-cli-on.10.1.4 — Ctrl+\] note/req toggle, \`- \[\` typing assist, and o/O continuation

[Bead Pages](../README.md) / [bob-cli-on.10.1](bob-cli-on.10.1.md) / bob-cli-on.10.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) · **Assignee:** `bob-cli-on.10.1.4` · **Size:** medium
**Created:** 2026-11-21 14:10:17 EST · **Closed:** 2026-11-21 21:46:39 EST
**Plan:** [202611/obsidian\_req\_gestures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md)

## Description

cycler-toggle-and-typing: route Ctrl+] (command and Vim) through the RW toggle with zone placement, the first-req scoop notice, and refusals; add the cycler's CodeMirror typing extension (expansion, autopair, overtype absorption, atomic Backspace, Vim insert, isolated Undo) with a real-Obsidian e2e; pin o/O req continuation.

## Notes

[2026-11-22T02:44:51Z · bob-cli-on.10.1.4] PROPOSED FOLLOW-UP: bob-cli docs-check published-URLs stage fails on master — src/native/highlights_ref/podcast/feed.rs:70 links docs/1.0.md -> /1.0/ with no built page; reproduces on bob-cli master independent of this phase (npm run docs:check in bob-plugins surfaces it after lint, drift and the strict build pass)

[2026-11-22T02:44:56Z · bob-cli-on.10.1.4] PROPOSED FOLLOW-UP: bob-plugins perf budgets flake under host load (load avg ~17 on athena) — scripts/test-ledger-tools-frees-marks.cjs "200-link / 2000-task build stays within the 25 ms budget" (56 ms vs 25) and scripts/test-navigation-dependencies-stage-performance.cjs "stage opening builds 200/400/1000-task notes without cubic growth" failed inside npm test and pass alone; neither touches the cycler

[2026-11-22T02:45:01Z · bob-cli-on.10.1.4] PROPOSED FOLLOW-UP: real-Obsidian e2e scripts on athena stall unless the scratch app gets DBUS_SESSION_BUS_ADDRESS=disabled: — the agent shell exports the real user session bus, Electron then blocks on portal/keyring lookups (DevTools never answers, update check never finishes) and the --help probe spawns the app on the default profile; scripts/obsidian-task-reqs-e2e.cjs now has launchEnv/scratchBase/probeExecutable (private profile, process-group kill, /tmp scratch paths for the 108-byte SingletonSocket limit) that the other obsidian-*-e2e.cjs scripts could share

[2026-11-22T02:46:39Z · bob-cli-on.10.1.4] Cycler 1.56.0: Ctrl+] (command and Vim) routes req lines and plain list items in a #task block through taskReqToggle (one replaceRange, cursor at same item offset, first-req notice, writer refusals shown with no write; legacy toggle untouched elsewhere), new 199-req-toggle.js with net-zero hooks in 160/140. New 199a-req-typing.js: CM extension (inputHandler expansion as plain-space + isolateHistory 'full' transaction, StateField overtype absorption, Prec.high atomic Backspace) registered in onload; skipped silently when a CM piece is missing. o/O continuation pinned by unit tests (no code change needed). Verified: new unit tests test-task-status-cycler-req-toggle (13) and -req-typing (15) plus e2e self-test; npm test 8564/8570 with the only 2 failures being unrelated load-sensitive perf budgets that pass alone; npm run build:check; docs:check passes lint, drift and strict build and fails only the published-URLs stage on a bob-cli master link (feat podcast feed.rs:70), recorded as follow-up. Real Obsidian 1.15.1 e2e (scripts/obsidian-task-reqs-e2e.cjs, xvfb, isolated vault/profile): 31/31 pass — expansion/absorption/atomic Backspace/one Undo with autoPairBrackets on and off, Vim insert, o/O, Ctrl+] toggle and Vim Ctrl+]. Synced task-status-cycler 1.56.0 after fast-forwarding to origin/master per the sync-refusal recipe (no -F). Fragments stay <=1000 lines (160 at 989, 140 at 925).

## Dependencies

- **Depends on:** [bob-cli-on.10.1.3](bob-cli-on.10.1.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.10.1.6](bob-cli-on.10.1.6.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.10.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.4/README.md) | [bob-cli-on.10.1.4](bob-cli-on.10.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.10.1.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.4/README.md

<!-- sase:referenced-by:end -->
