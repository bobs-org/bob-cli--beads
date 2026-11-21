# Bead: bob-cli-oe.8.2 — Obsidian card capsule, walk follow bookkeeping, and receipt copy

[Bead Pages](../README.md) / [bob-cli-oe.8](bob-cli-oe.8.md) / bob-cli-oe.8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-oe.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.land.md) · **Assignee:** `bob-cli-oe.8.2` · **Size:** medium
**Created:** 2026-11-20 21:39:29 EST · **Closed:** 2026-11-21 07:56:31 EST
**Plan:** [202611/successor\_jump\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_repairs.md)

## Description

nav-jump-repairs: in bob-navigation-hotkeys, fix the capsule icon and its trailing-edge placement, make the reviewWalk follow path record the review answer and park only when v1 would advance, show the receipt line once, make landOnTask settle before reporting, leave one authoritative applySelection/settle, and fix plugin-apis.md's §12.24 citation and word budget.

## Notes

[2026-11-21T12:56:01Z · bob-cli-oe.8.2] PROPOSED FOLLOW-UP: Known ledger timing flakes (already tracked by bob-cli-km and bob-cli-io) recur under npm test — event-link-times measured 78 ms and frees-marks 158 ms against 25 ms limits. These are the only two failures among 8029 unit tests (8022 passed, 5 skipped); the separate perf suite passed 11/11. Both affected suites pass 40/40 in isolation on the clean 9c4b401e base, and their source and tests are unchanged by this phase.

[2026-11-21T12:56:08Z · bob-cli-oe.8.2] PROPOSED FOLLOW-UP: Existing docs budget failure remains tracked by bob-cli-oc — npm run docs:check reports only docs/reference/vault-format.md at 6016/6000 words. Confirmed the file is byte-identical to clean bob-cli HEAD d27041cd. The phase-owned plugin-apis.md passes at 7996/8000 words with the corrected section 12.24 citation.

[2026-11-21T12:56:14Z · bob-cli-oe.8.2] Verified prior phase implementation already landed in bob-plugins 9c4b401e. Fixed its remaining checklist regression: the successful PRE/POST claim now tells the private follow path that the answer is already recorded, allowing parking without duplicate journaling while preserving public v1 resolve rules. PRE, last-PRE, and POST regressions assert one journal answer, one toast, one jump, and next-walk neighbour. Focused suites 233/233; build:check and inventory clean. Navigation version 2.95.2 synced successfully after clean-base provenance adoption, without force. Desktop smoke command npm run smoke:obsidian -- --deployed-vault /home/bryan/bob --report /tmp/bob-cli-oe.8.2-obsidian-smoke.json exited 2 (unrun: /snap/bin/obsidian absent); no smoke report produced and no desktop pass claimed.

[2026-11-21T12:56:31Z · bob-cli-oe.8.2] Complete: verified landed repair commit 9c4b401e and fixed claimed PRE/POST jump parking without duplicate review answers; 233 focused tests pass, build:check passes, full suite has only the two documented ledger timing flakes, and docs has only the unchanged vault-format budget failure. Navigation 2.95.2 synced without force; plugin-apis is 7996/8000 words; no epic symbols. Desktop smoke unrun because Obsidian is unavailable on apollo. No ancestor bead closed.

## Dependencies

- **Blocks:** [bob-cli-oe.8.3](bob-cli-oe.8.3.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.8.2/README.md) | [bob-cli-oe.8.2](bob-cli-oe.8.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9c4b401`](https://github.com/bobs-org/bob-plugins/commit/9c4b401e5ca9ed833b03607fa04ef06b322d7516) | feat(navigation): complete successor jump and landing flow | [bob-cli-oe.8.2](bob-cli-oe.8.2.md) | 2026-11-20 22:20:55 EST |
| bob-plugins | [`bob-plugins@767a597`](https://github.com/bobs-org/bob-plugins/commit/767a59707c23c7dae9108891d5188eea19670805) | fix(navigation): park pinned checklist closes without duplicate answers | [bob-cli-oe.8.2](bob-cli-oe.8.2.md) | 2026-11-21 07:57:25 EST |
