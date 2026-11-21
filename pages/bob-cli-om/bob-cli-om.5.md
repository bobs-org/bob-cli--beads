# Bead: bob-cli-om.5 — Task Card stages and the scheduled inline reason

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.5` · **Size:** medium
**Created:** 2026-11-21 10:32:18 EST · **Closed:** 2026-11-21 13:15:08 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

## Description

task-card-prompts: opt the Task Card picker stages S7-S10 into links through the shared picker wiring. Add S11, the scheduled-stage reason tail, through minOffset so the date token never completes.

## Notes

[2026-11-21T18:14:17Z · bob-cli-om.5] PROPOSED FOLLOW-UP: ledger-tools 25 ms wall-clock perf asserts flake under host load — test-ledger-tools-event-link-times.cjs ("one build over a 200-link ledger") and test-ledger-tools-frees-marks.cjs ("200-link / 2000-task build") failed in both full npm test runs here at load avg ~150-160 (303-541 ms) and pass 40/40 in isolation; this phase touched no ledger-tools code. Same flake already reported in bob-cli-oe.8.2, bob-cli-oj.5.1.1, and bob-cli-o6.4.1.2 notes; it needs one task bead (load-tolerant budget or move to test:perf).

[2026-11-21T18:15:08Z · bob-cli-om.5] Verified task-card-prompts in bob-plugins (nav 2.98.0): S7-S10 opt into the LINK band via attachPickerLogRecall (links:true, plugin, sourcePath = task note: picker.filePath, or the one note all Task Link targets share, else null). Key routing checked by tests: Esc/Ctrl+[ close only the band, then recall; arrows/Ctrl+N/P, Enter (held-Enter swallow), and Tab reach the band before openItemAtIndex and S10 Tab cycling; S9 Alt+P keeps priority. S10 refocusing the bound field keeps its handle. S11: new 185a fragment attaches proseField (recall:null) to the scheduled-stage filter with minOffset from matchTypedSchedulePrefix (token end plus whitespace; Infinity when no token or attached). 450 offers keys to it before date rows, Enter, Shift+Enter, Ctrl+Enter, Ctrl+R, and the Ctrl+[ close. It detaches through detachPickerLogRecall and the close/returnHome/returnToTaskCard wrappers and fails open without the API. Model fixes: minOffset Infinity was coerced to 0; alias stage and unresolved hint now honor minOffset; proseCompleteLinks carries start. getProseLinkIndex caches on the nav instance when a host passes no plugin (S1 path rebuilt the index and leaked listeners per keystroke). docs/task-card.md: new Links in reasons section, Esc/Ctrl+[ rows. New test file scripts/test-navigation-task-card-prose-links.cjs (11 tests; mutation-checked). npm run validate green. npm test: 8201/8203 unit plus 13/13 perf; the 2 failures are known ledger-tools load flakes (see note). docs:check fails only on pre-existing word-budget lint (plugin-apis, nav, vault-format; om.3 note #2). bob plugins sync deployed nav 2.98.0 after the landed-build recipe (vault bundle matched origin 79fe2e15 byte for byte). Real-Obsidian S10/S11 walkthrough belongs to prose-lint (om.10). No epic symbols; no memory edits.

## Dependencies

- **Blocks:** [bob-cli-om.10](bob-cli-om.10.md) ◐ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-om.3](bob-cli-om.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.5/README.md) | [bob-cli-om.5](bob-cli-om.5.md) | 0 |
