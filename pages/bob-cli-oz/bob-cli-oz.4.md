# Bead: bob-cli-oz.4 — Task-bearing prompts S1–S12: subject guards, host safety, prose lint

[Bead Pages](../README.md) / [bob-cli-oz](README.md) / bob-cli-oz.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ff](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ff.md) · **Assignee:** `bob-cli-oz.4` · **Size:** medium
**Created:** 2026-11-21 17:39:51 EST · **Closed:** 2026-11-22 01:21:52 EST
**Plan:** [202611/prompt\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prompt_task_links.md)

## Description

prompt-subjects: wire subjects for S1–S11 (S12 none) and audit picker-host key offering during NAME. It adds the per-family host-safety tests and extends the prose-field lint with subjects.

## Notes

[2026-11-22T06:21:00Z · bob-cli-oz.4] PROPOSED FOLLOW-UP: bob-cli docs-check "published URLs" fails on the base tree — src/native/highlights_ref/podcast/feed.rs:70 links docs/1.0.md -> /1.0/ but no built page /1.0 exists (reproduces independent of the bob-plugins docs; the lint, generated-drift, and strict Zensical stages pass).

[2026-11-22T06:21:20Z · bob-cli-oz.4] PROPOSED FOLLOW-UP: S6 successor picker guards only the row being cancelled. Naming ANOTHER ID-less successor row of the same picker through the reason (( NAME stage changes that row line digest key, so its own staged verdict refuses per-row with changed_identity (the cancelled row and its neighbours still apply). Decide whether picker rows that are ID-less should be nameable from S6 or guarded.

[2026-11-22T06:21:27Z · bob-cli-oz.4] PROPOSED FOLLOW-UP: ledger-tools wall-clock perf budgets in scripts/test-ledger-tools-event-link-times.cjs (200-link ledger, 25 ms) and scripts/test-ledger-tools-frees-marks.cjs (200-link / 2000-task, 25 ms) fail inside the full parallel npm test run (~1000% CPU; 82 ms / 112 ms) but pass in isolation (40/40); bob-ledger-tools is untouched by this phase.

[2026-11-22T06:21:34Z · bob-cli-oz.4] PROPOSED FOLLOW-UP: bob plugins sync refuses to overwrite bob-navigation-hotkeys (deployed 2.101.0 from an uncommitted build in bob-cli_15, stamp 604c8a9) and bob-ledger-tools (1.157.0, uncommitted build in bob-cli_16, stamp 24ed171); neither author agent is running and HEAD..@{upstream} is empty. Diffing the deployed nav main.js against this phase build: 44 deployed-only lines, all older wordings of lines this tree rewrote (no feature or API missing). block-id-prompt 1.44.0 deployed. Needs Bryan approval for -F on nav 2.106.0.

[2026-11-22T06:21:52Z · bob-cli-oz.4] S1-S11 declare subjects (S12 declares none); proseTaskSubjects/rottenKeepSubjects/successorReasonSubjects/pickerProseSubjects feed them from each host's own write-plan identities. T11 host safety: navAdoptSiblingEdits/navContentAfterPrompt/navGroupsAfterPrompt/linkSessionGroups let hosts adopt a note whose only changes are off their target lines; real-bip api.taskLinks naming tests per family (S1 unlink, S2, S3 cursor+link, S4/S5 keep cursor+link, S5 decay Stay, S6 successor cancel, S7 single+link, S8 link, S10 single+link) — negative control confirms 7 fail without adoption. Picker NAME key routing audited for S7/S10/S11 (Tab/Shift+Tab/arrows/Ctrl+N,P/Esc/Ctrl+[ consumed first, Enter never commits); S6 NAME/Enter/blur verified with the real controller. Prose lint extended (subjects wired|none). Docs: task-card, block-id-prompt, notebook-gestures, architecture. Versions: nav 2.106.0, bip 1.44.0. npm test 8621/8623 pass (2 ledger-tools wall-clock perf budgets flake under parallel load, pass alone), validate ok, docs lint/drift/strict build ok. bip deployed; nav deploy blocked by bob plugins sync refusal (see PROPOSED FOLLOW-UP notes) pending Bryan approval for -F.

[2026-11-22T11:12:03Z · bob-cli-oz.4--1] RESOLVED: nav deploy — Bryan approved force-sync; ran bob plugins sync -F -p bob-navigation-hotkeys from bob-plugins HEAD e7427ad9 (clean). Vault now has nav 2.106.0; the displaced uncommitted 2.101.0 build is backed up under ~/.local/state/bob-cli/plugin-backups/20261122-061156. ledger-tools was not forced.

## Dependencies

- **Depends on:** [bob-cli-oz.3](bob-cli-oz.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oz.7](bob-cli-oz.7.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oz.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oz.4.md) | [bob-cli-oz.4](bob-cli-oz.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@577b3cc`](https://github.com/bobs-org/bob-plugins/commit/577b3cc615da328a5361e27500a524ac70b6417a) | feat(nav): declare task subjects for (( in S1-S12 prompts and keep host writes safe | [bob-cli-oz.4](bob-cli-oz.4.md) | 2026-11-22 01:23:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oz.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oz.4.md

<!-- sase:referenced-by:end -->
