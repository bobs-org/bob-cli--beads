# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5 — Package the Obsidian startup smoke check that plugin rollouts run

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5` · **Size:** large
**Created:** 2026-10-27 03:08:27 EDT · **Closed:** 2026-10-27 04:00:06 EDT
**Plan:** [202610/backlog\_batch16\_mac\_build\_orphan\_refs\_archive\_moves\_plugin\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md)

## Description

plugin-startup-smoke: resolve bob-cli-a6 per the startup_smoke decision by packaging the CDP Obsidian startup and editor-mount check as a reusable rollout script and wiring it into the deploy docs.

## Notes

[2026-10-27T07:59:55Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5] LANDER ROLLOUT GATE: after the master re-sync and zero-drift check, and before declaring rollout verified, run the packaged startup smoke gate from the bob-plugins checkout: npm run smoke:obsidian -- --deployed-vault <vault> --report <report.json> (preceded by xvfb-run -a on Linux; offline-only self-test is npm run smoke:obsidian -- --self-test and is never an Obsidian pass). Executable prerequisite: the Obsidian Electron app (this run used /snap/bin/obsidian), an independent Xvfb display, Node 22; the runner fails unrun (exit 2) with exact rerun instructions when no host can launch Obsidian. Verdict on this phase: PASS on athena 2026-10-27 — layout-ready 438ms (budget 30s), heap peak 63MiB (budget 1.5GiB), relation ready with zero non-Markdown keys/reads and the fixture relation indexed, all four editor mounts ok (canonical daily + ordinary note x Live Preview + Source), zero exceptions/rejections/crash artifacts; offline suite 17/17, npm test 3831/3831, build:check/validate/docs:check green. Report reference: /tmp/obsidian-smoke.json from the passing run (ephemeral; rerunning the gate command regenerates it).

[2026-10-27T08:00:06Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5] Delivered the packaged rollout smoke check plus docs and lander gate. Runner: scripts/obsidian-startup-smoke.cjs with lib scripts/obsidian-startup-smoke-lib.cjs and npm run smoke:obsidian; offline suite scripts/test-obsidian-startup-smoke.cjs (17/17) wired into npm test. Docs: rollout smoke gate section in bob-plugins docs/develop/deployment.md and bob-cli docs/guides/deploy-obsidian-plugins.md. Validation: offline 17/17, npm test 3831/3831, build:check, validate 8/8, docs:check 447 passed, just check green, plus a real isolated Athena Obsidian run: PASS (layout-ready 438ms, heap peak 63MiB, relation ready with zero non-Markdown keys/reads, 4/4 editors, zero exceptions/rejections/crashes). Lander gate recorded on this phase as LANDER ROLLOUT GATE. Leaving bob-cli-a6 and all ancestors open for the parent lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`29d6105`](https://github.com/bobs-org/bob-cli/commit/29d6105b09856a70d7a9ff4359a44e3e76d79572) | docs(plugins): add Obsidian rollout smoke gate to deploy guide | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5.md) | 2026-10-27 04:01:17 EDT |
| bob-plugins | [`bob-plugins@88f0cdd`](https://github.com/bobs-org/bob-plugins/commit/88f0cddaec4907623b2d4498183d1884be1b58a5) | feat(plugins): package the real-Obsidian startup smoke check | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.5.md) | 2026-10-27 04:02:45 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land/README.md

<!-- sase:referenced-by:end -->
