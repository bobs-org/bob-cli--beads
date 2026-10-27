# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4 — Warn when a deployed custom plugin folder is not git-ignored or is tracked

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4` · **Size:** medium
**Created:** 2026-10-27 03:08:27 EDT · **Closed:** 2026-10-27 03:32:02 EDT
**Plan:** [202610/backlog\_batch16\_mac\_build\_orphan\_refs\_archive\_moves\_plugin\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md)

## Description

plugin-ignore-guard: resolve bob-cli-ch per the plugin_ignore decision, reusing batch 15's deploy-stamp ignore checks to cover each plugin's whole vault folder in sync, list, and JSON.

## Notes

[2026-10-27T07:31:55Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4] Phase done (plugin_ignore=warn). Baseline: batch-15 115a3610 covered only the .bob-deploy.json stamp (refuse). Fix: new check_plugin_ignore() in src/native/plugins/deploy.rs reuses the stamp Git probes (git ls-files + check-ignore via vault_git) over the whole .obsidian/plugins/<id>/ folder + every managed file; warning (tracked/not_ignored/unknown) rides on PluginSync/PluginEntry as vault_ignore, printed under the row in sync + list tables (incl. dry-run and refusals) and in both JSON shapes; never blocks, never edits .gitignore, never untracks. Tests: 6 new maintained tests in src/native/plugins/tests.rs (non-Git clean, Git clean, unignored still syncs + JSON, tracked still syncs, dry-run carries warning w/o writing, list keeps columns + JSON). Gates: just check exit=0 (fmt+clippy+full tests), just docs-gen + docs-check exit=0, bob-plugins npm run docs:check exit=0. Docs: docs/plugins.md (Vault-ignore warnings section + JSON fields), docs/guides/deploy-obsidian-plugins.md, regenerated docs/reference/cli/plugins.md, bob-plugins docs/develop/deployment.md. Limitations: target task bob-cli-ch left open for the lander; changes in bob-cli checkout + linked bob-plugins checkout left uncommitted for the lander to commit via /sase_git_commit.

[2026-10-27T07:32:02Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4] plugin-ignore-guard done per plugin_ignore=warn: folder-level git check-ignore/ls-files warnings in sync, list, dry-run, and both JSON shapes (vault_ignore), never blocking or editing .gitignore. Verified: just check exit=0 (fmt, clippy, full test suite incl. 6 new plugins ignore tests), just docs-gen + docs-check exit=0, bob-plugins docs:check exit=0. Target bob-cli-ch left open for the lander; no epic-symbol leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`49f6131`](https://github.com/bobs-org/bob-cli/commit/49f6131d9b98496458629572b5102eab76c3262d) | feat(plugins): warn when a deployed plugin folder is not git-ignored or is tracked | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4.md) | 2026-10-27 03:32:58 EDT |
| bob-plugins | [`bob-plugins@3886e69`](https://github.com/bobs-org/bob-plugins/commit/3886e698af1f7320b377a3372f39a5fc72f8adcf) | docs(deployment): document the vault-ignore warning for deployed plugin folders | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4.md) | 2026-10-27 03:34:48 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.4/README.md

<!-- sase:referenced-by:end -->
