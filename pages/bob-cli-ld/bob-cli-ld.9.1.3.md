# Bead: bob-cli-ld.9.1.3 — Real Obsidian acceptance, documentation, and deployment

[Bead Pages](../README.md) / [bob-cli-ld.9.1](bob-cli-ld.9.1.md) / bob-cli-ld.9.1.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ld.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ld.9.md) · **Assignee:** `bob-cli-ld.9.1.3` · **Size:** medium
**Created:** 2026-11-13 15:29:28 EST
**Plan:** [202611/projects\_catalog\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/projects_catalog_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:1f31d6f0e705190a94a38046 | attached via sase artifact create --bead |
| related | file:explicit:a82786253010f6aaf7592fb4 | attached via sase artifact create --bead |
| related | file:explicit:c3b273cf00b5beffe099ebd8 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

projects-acceptance: add the isolated real-Obsidian runner and offline wrapper, inspect screenshots, document the card, run full gates, deploy, and record closure evidence for the land agent.

## Notes

[2026-11-14T00:51:07Z · bob-cli-ld.9.1.3--6] Projects UI verification and deployment evidence. The real Obsidian Projects acceptance passed 43/43 checks with the fresh report and all five requested captures reviewed: Live Preview desktop light/dark (1280 px), Live Preview mobile light/dark (375 px), and Reading desktop light (1280 px). The focused Projects suite passed 44/44. `npm run validate` passed (11/11 plugin manifests); `just docs-gen` passed and generated the inventory for 11 plugins / 134 commands. `bob plugins sync` completed without `--force`: 4 copied, 0 skipped, 27 unchanged; Bob Ledger Tools 1.116.0 was deployed. It also copied task-status-cycler `main.js` from the opened checkout. The sync reported that pull/rebase was unavailable because the checkout has unstaged work, fetched remote refs, and left checkout files unchanged.

Commands/evidence: `env CARGO_TARGET_DIR=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws11-261113_175125 BOB_CLI_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11 BOB_TARGET=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws11-261113_175125 BOB_BIN=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws11-261113_175125/debug/bob xvfb-run -a node scripts/obsidian-projects-ui-e2e.cjs -e /snap/obsidian/current/app/obsidian -r /tmp/projects-ui-e2e.json -o /tmp/projects-ui-e2e-shots`; focused `node --test --test-reporter=spec scripts/test-ledger-tools-projects-data.cjs scripts/test-ledger-tools-projects-catalog.cjs scripts/test-obsidian-projects-ui-e2e.cjs`; `npm run validate`; `BOB_CLI_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11 npm run docs:check`; `BOB_DOCS_BOB_PLUGINS_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins uv run --project tools/docs bob-docs assemble`; `just docs-gen`; `just docs-check`; `just check`; `bob plugins sync`.

Unverified gates remain. `npm test` failed on three unit checks and one performance threshold: two unrelated Live Preview timing checks (848.7 ms and 49.5 ms against 25 ms) and the pre-existing 170-plugin-lifecycle.js 1000-line limit; the performance suite measured a worst chunk of 17.1 ms against 16 ms. `npm run docs:check` and `just docs-check` both fail the reference word budget on `docs/reference/json-outputs.md` (6025/6000), `docs/reference/plugins/bob-ledger-tools.md` (6260/6000), and `docs/reference/plugins/bob-navigation-hotkeys.md` (6019/6000). `just check` completed clippy and the other test targets but failed three existing library tests: `native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none` and the two `native::subprocess_runner::*bounds_pipe_drain_when_detached_grandchild_holds_output` tests.

PROPOSED FOLLOW-UP: Resolve the plugin timing/lifecycle unit failures and the three bob-cli library failures, bring the three reference pages within their word budgets, then rerun `npm test`, `npm run docs:check`, `just docs-check`, and `just check`. Keep bob-cli-ld.9.1.3 open until those gates pass.

## References

- file:explicit:a82786253010f6aaf7592fb4
- file:explicit:c3b273cf00b5beffe099ebd8

## Dependencies

- **Depends on:** [bob-cli-ld.9.1.2](bob-cli-ld.9.1.2.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.9.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ld.9.1.3.md) | [bob-cli-ld.9.1.3](bob-cli-ld.9.1.3.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@703014d`](https://github.com/bobs-org/bob-plugins/commit/703014db87bfa50ee45681a7a0d80c054dfa8db5) | feat(projects): add Obsidian catalog acceptance | [bob-cli-ld.9.1.3](bob-cli-ld.9.1.3.md) | 2026-11-13 17:11:27 EST |
| bob-plugins | [`bob-plugins@fe7ffb7`](https://github.com/bobs-org/bob-plugins/commit/fe7ffb73b77c40db96c5bfba6ac09f72a8f207b6) | fix(projects): wait for Obsidian plugin trust before acceptance | [bob-cli-ld.9.1.3](bob-cli-ld.9.1.3.md) | 2026-11-13 17:47:32 EST |
| bob-plugins | [`bob-plugins@415a33d`](https://github.com/bobs-org/bob-plugins/commit/415a33d7c43cc7e732b430dd3b9a5e294eac7ffe) | fix(projects): preserve catalog folds after editor move | [bob-cli-ld.9.1.3](bob-cli-ld.9.1.3.md) | 2026-11-13 19:52:27 EST |
