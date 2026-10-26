# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1 — Stop vault sync from tracking deployed bob-articles files

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1` · **Size:** medium
**Created:** 2026-10-26 10:47:09 EDT · **Closed:** 2026-10-26 12:09:50 EDT
**Plan:** [202610/backlog\_batch13\_vault\_integrity\_and\_perf\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md)

## Description

vault-plugin-ignore: resolve bob-cli-cd by fixing the source-of-truth ignore rule and coordinating untracking/redeployment across hosts; never untrack on one host alone.

## Notes

[2026-10-26T14:59:09Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1] BASELINE: Canonical ignore source is the vault git file ~/bob/.gitignore (tracked in the vault repo). chezmoi does not manage it; bob-plugins is only the deploy source. Custom-plugin block lists block-id-prompt, bob-command-mode, bob-ledger-tools, bob-navigation-hotkeys, bob-project-tasks, bob-vim-surround, task-status-cycler and omits bob-articles. git check-ignore -v .obsidian/plugins/bob-articles/main.js is empty. git ls-files lists main.js, manifest.json, styles.css. Comment still cites ~/projects/github/bbugyi200/bob-plugins. Hosts athena, apollo, and mac are all at vault SHA 4f5ce0ac with those three files tracked and bob-articles 0.2.1 synced/enabled. bob-vault-sync.service is active on athena and apollo. Mac LaunchAgent com.bbugyi.bob-vault-sync is loaded with StartInterval 15s (idle between runs). Live-vault repair will go through a Bryan-approved sase gate so untrack is not done on one host alone. Target task bob-cli-cd stays open for the lander.

[2026-10-26T15:02:18Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1] PROPOSED FOLLOW-UP: Make bob plugins sync maintain the vault custom-plugin gitignore block from the plugin roster — a newly added plugin can be tracked again if only ~/bob/.gitignore is hand-edited.

[2026-10-26T15:03:21Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1] FIX pending Bryan gate: coordinated ignore+untrack+redeploy on athena, apollo, and mac (stop vault-sync first, add .obsidian/plugins/bob-articles/ to ~/bob/.gitignore, git rm --cached the three tracked files, vault-sync commit/push, plugins sync on each host, restart watchers). Never untrack on one host alone.

[2026-10-26T15:48:54Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1] VERIFIED REPAIR: Gate custom-cda73055-0c77-470b-812c-254b91448337 was approved via Telegram and committed 0b682436eae247ea7b65e5b377d800efad609d8c before its final verifier failed on a printf format beginning with --. The supported gate preview now independently confirms athena, apollo, and mac at vault SHA 1d0a1ac2, bob-articles ignored by .gitignore:69, no tracked plugin files, and plugin main.js present. Athena also verifies all three files present/ignored and the corrected bobs-org source comment. bob plugins list -n -f json independently reports bob-articles 0.2.1 synced and enabled on all three hosts. Athena/apollo vault-sync services are active; Mac LaunchAgent is loaded. No additional live repair is needed. epic-symbols reports no entries. Remaining work is repository verification and phase closure; leave task bob-cli-cd and all ancestors for the lander.

[2026-10-26T15:50:59Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1] SOURCE VERIFICATION: Opened gh:bobs-org/bob via sase_repo and inspected published commit 0b682436eae247ea7b65e5b377d800efad609d8c. It changes only the custom-plugin .gitignore comment/rule and removes the three deployed bob-articles files from tracking. The remote checkout also has no tracked bob-articles files. All phase implementation work was already landed by the approved gate; this recovery made no source changes. Primary tree is clean at fb28faa1af7094601f2762a03ff681301a836d50. sase tool run check reports unknown tool and tool list has no catalog entries, so required just check must run directly under a SASE monitor with the documented bypass. Any check failure on this unchanged tree is baseline evidence, to be recorded as PROPOSED FOLLOW-UP before closing this phase.

[2026-10-26T16:09:26Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1--1] PROPOSED FOLLOW-UP: Finish bob ref code catalog/completion/help integration — just check on the unchanged clean base fb28faa1af7094601f2762a03ff681301a836d50 failed with exit 101 (monitor bf362a42xf4d, ToolRun 8a279d52a9f9bad0c857fa0e943e5a07; 2026-10-26 15:51:35–16:00:10 UTC). native::catalog::tests::public_leaves_are_entries_or_excluded at src/native/catalog/tests.rs:122 reports public leaf ["ref", "code"] is neither an entry nor excluded; native::completion::kinds::tests::every_value_arg_has_a_decision at src/native/completion/kinds.rs:721 reports missing decisions for ref code:number and ref code:page; help::ref_help_matches_grouped_snapshot at tests/cli/help.rs:1001 has a fixture missing the new code row/example. cargo fmt --check and cargo clippy passed; tests totaled 6007 passed, 3 failed, 1 ignored. ToolRun records MUTATED false and DIRTY 0 -> 0, so this run is the clean-base reproduction; no phase source changes or reruns are needed. All-status task search found only closed bob-cli-4j (old audio completion gap) and bob-cli-5i (old clip alias help mismatch), which concern different command changes; no matching ref code task was found. Evidence is retained via sase monitor show bf362a42xf4d --all-lines. Lander should deduplicate/route this integration failure; no bead was created.

[2026-10-26T16:09:50Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1--1] Completed vault-plugin-ignore. Approved gate custom-cda73055-0c77-470b-812c-254b91448337 published vault commit 0b682436eae247ea7b65e5b377d800efad609d8c: corrected the custom-plugin source comment, added the bob-articles ignore rule, and removed main.js, manifest.json, styles.css from tracking. Prior independent verification in notes #4–5 confirms athena/apollo/mac at 1d0a1ac2, .gitignore:69 matching bob-articles, no tracked plugin files, main.js present, bob-articles 0.2.1 synced/enabled on all hosts, Linux sync services active, and Mac LaunchAgent loaded. just check completed under monitor bf362a42xf4d / ToolRun 8a279d52a9f9bad0c857fa0e943e5a07: formatting/Clippy passed; 6007 tests passed, 3 unrelated ref code integration failures, 1 ignored. The failures are recorded in PROPOSED FOLLOW-UP with exact assertions and clean-base evidence (fb28faa1af7094601f2762a03ff681301a836d50; DIRTY 0 -> 0; no source changes). epic-symbols reports no entries. Only this phase is closed; target task bob-cli-cd and all ancestors remain for the lander.

## Dependencies

- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2][1] | need prior ignore-fix completion evidence and deployment ordering | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2/README.md

<!-- sase:referenced-by:end -->
