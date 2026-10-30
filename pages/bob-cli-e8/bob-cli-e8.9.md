# Bead: bob-cli-e8.9 — Vault-copy pilot and switch-on

[Bead Pages](../README.md) / [bob-cli-e8](README.md) / bob-cli-e8.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2v.linker.w0.md) · **Assignee:** `bob-cli-e8.9` · **Size:** small
**Created:** 2026-10-29 17:20:22 EDT · **Closed:** 2026-10-30 10:26:30 EDT
**Plan:** [202610/inline\_task\_mentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inline_task_mentions.md)

## Description

enable: pilot the full feature on a copy of the vault, then flip linked_from_mentions on per the rollout decision and record follow-up proposals.

## Notes

[2026-10-30T14:17:22Z · bob-cli-e8.9--3] Pilot PASS: isolated vault-copy no-mentions baseline returned 0 mention_edges across 5,358 scanned files. Enabled dry-run and live reconcile each found 57 edges, with 54 LINKED FROM update rows across 51 target notes and no relation warnings. The live diff filter allowed all 62 changed lines and found 0 unexpected lines. This is 7 fewer edges and 10 fewer target notes than the research survey (64/61); the copy had no relation source block IDs requested by reconcile. MN14 passed: second reconcile was byte-identical. MN13 passed: switch off then on restored the enabled diff byte-for-byte. `smoke:obsidian` was not run because this host has no `/snap/bin/obsidian`; Bryan visual check remains. Rollout default and invalid-value fallback are now true in Rust and both plugins.

[2026-10-30T14:17:32Z · bob-cli-e8.9--3] PROPOSED FOLLOW-UP: Support converting a mention into a relation — detail: ⇧↵ on a mention row should open Links prefilled with the target, excluding closing labels.

[2026-10-30T14:17:42Z · bob-cli-e8.9--3] PROPOSED FOLLOW-UP: Render source-side mention pills — detail: show the inline task link on the mentioning task as a status pill.

[2026-10-30T14:17:50Z · bob-cli-e8.9--3] PROPOSED FOLLOW-UP: Add a previewed one-shot block-ID backfill — detail: target the roughly 20 id-less archived sources identified by the plan.

[2026-10-30T14:17:58Z · bob-cli-e8.9--3] PROPOSED FOLLOW-UP: Validate the merged LINKED FROM row usability — detail: if Bryan cannot distinguish why each entry exists, move mentions to a separate typed row.

[2026-10-30T14:25:08Z · bob-cli-e8.9--3] Sync status: `bob plugins sync` and no-pull dry-runs for bob-ledger-tools and bob-navigation-hotkeys refused, copied nothing, and reported deployed digests that do not match the vault. Read-only comparison confirmed the installed bundles contain unrelated local changes (navigation Pomodoro type preview; ledger terminology updates) absent from the source checkout. I left those bytes untouched; the source changes are validated but these two plugin bundles are not deployed to ~/bob.

[2026-10-30T14:25:33Z · bob-cli-e8.9--3] Sync status: `bob plugins sync` and no-pull dry-runs for bob-ledger-tools and bob-navigation-hotkeys refused and copied nothing because deployed digests do not match the vault. Read-only comparison confirmed the installed bundles contain unrelated local changes absent from this checkout (navigation Pomodoro type preview and ledger terminology updates). Those bytes were left untouched. The source changes are validated but the two updated bundles are not deployed to ~/bob.

[2026-10-30T14:25:57Z · bob-cli-e8.9--3] PROPOSED FOLLOW-UP: Safely reconcile deployed plugin edits before mention rollout — detail: preserve or merge the existing ~/bob changes in bob-ledger-tools and bob-navigation-hotkeys, then sync the validated bundles.

[2026-10-30T14:26:30Z · bob-cli-e8.9--3] Verified the default-on rollout in Rust, plugin sources, docs, and the three authorized glossary strands; vault-copy pilot passed (57 mention edges, MN13/MN14 byte checks); just check and bob-plugins npm run validate passed. bob plugins sync refused the two updated bundles because installed digest mismatches include unrelated local edits, which were preserved and recorded for follow-up.

## Dependencies

- **Depends on:** [bob-cli-e8.3](bob-cli-e8.3.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e8.4](bob-cli-e8.4.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e8.7](bob-cli-e8.7.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e8.8](bob-cli-e8.8.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e8.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e8.9.md) | [bob-cli-e8.9](bob-cli-e8.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b081097`](https://github.com/bobs-org/bob-cli/commit/b081097cbcd7b914d7299f8db4767d4e497ba952) | feat(task-mentions): enable linked-from mentions by default | [bob-cli-e8.9](bob-cli-e8.9.md) | 2026-10-30 10:28:00 EDT |
