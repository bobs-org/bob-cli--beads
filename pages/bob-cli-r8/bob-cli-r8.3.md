# Bead: bob-cli-r8.3 — Real-Obsidian e2e runners keep bounded failure scratch

[Bead Pages](../README.md) / [bob-cli-r8](README.md) / bob-cli-r8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.land.md) · **Assignee:** `bob-cli-r8.3` · **Size:** medium
**Created:** 2026-11-27 13:01:15 EST · **Closed:** 2026-11-27 14:25:23 EST
**Plan:** [202611/task\_bead\_burndown\_2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_2.md)

## Description

e2e-scratch: stop the bob-plugins real-Obsidian e2e runners from leaking failure scratch and screenshots into the /tmp tmpfs without bound, document where retained scratch lives, then close bob-cli-qt.

## Notes

[2026-11-27T19:25:23Z · bob-cli-r8.3] Implemented bounded scratch retention for all eight success-only runners. node --test scripts/test-e2e-scratch.cjs: 4/4 passed; JavaScript syntax checks and git diff --check passed. BOB_CLI_DIR=<workspace> npm run docs:check: 449 passed, 1 skipped. xvfb-run -a node scripts/obsidian-home-cards-e2e.cjs ran twice: both exited 1 on the known acceptance baseline; first retained run was pruned by the second, which left exactly one helper-managed retained run. df -h /tmp remained 12% (3.6G used before, 3.7G after). npm test exited 1 only for the known scripts/test-snooze-model-vectors.cjs vector owned by active epic bob-cli-q5; test:perf passed 26/26. bob plugins sync from the linked checkout exited 0 with 0 copies. No epic-symbol entries remained.

[2026-11-27T19:58:15Z · bob-cli-r8.3--2] Rerun evidence: bash /tmp/bob-cli-r8.3-home-cards-retention.sh (monitor 77q256z6sq8x) exited 0. Both xvfb-run Home Cards executions exited 1 on the same nonempty known acceptance checks: card:scheduled_plan.md:reading, card:done_plan.md:reading, card:canceled_plan.md:reading, matrix-spawns-no-home-card-bob, area-cursor-starts-on-body-line, project-cursor-starts-on-body-line, runner-error. Run two pruned run one's scratch; confirmed the first path is absent and exactly one retained helper-managed scratch remains under the monitored root: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws16-261127_144226/bob-home-cards-ySuYG7 (owner UID 1000, current user). /tmp remained at 12% used (3.7G). Epic-symbol check: no entries for bob-cli-r8.3. The previously recorded npm test result remains unchanged: only bob-cli-q5 snooze model vector failed; test:perf 26/26.

## Dependencies

- **Depends on:** [bob-cli-r8.2](bob-cli-r8.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-r8.4](bob-cli-r8.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r8.3.md) | [bob-cli-r8.3](bob-cli-r8.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6827a27`](https://github.com/bobs-org/bob-plugins/commit/6827a275650185b1341c781fe6c2cfc5fa153873) | fix(test): bound retained Obsidian e2e scratch | [bob-cli-r8.3](bob-cli-r8.3.md) | 2026-11-27 14:39:48 EST |
