# Bead: bob-cli-ld.9.1.1 — Shared projects report service and debounced auto-sync

[Bead Pages](../README.md) / [bob-cli-ld.9.1](bob-cli-ld.9.1.md) / bob-cli-ld.9.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ld.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ld.9.md) · **Assignee:** `bob-cli-ld.9.1.1` · **Size:** medium
**Created:** 2026-11-13 15:29:28 EST · **Closed:** 2026-11-13 15:51:43 EST
**Plan:** [202611/projects\_catalog\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/projects_catalog_card.md)

## Description

projects-data: implement projects JSON decoders, the shared report/sync service, lifecycle fingerprints, and deterministic data-service tests in bob-plugins.

## Notes

[2026-11-13T20:51:24Z · bob-cli-ld.9.1.1] PROPOSED FOLLOW-UP: keep-moving 200-link Live Preview budget flakes under full npm test load — isolated run passes (~82ms of 250ms); full suite hit 295ms. Already tracked by bob-cli-ki and bob-cli-km.

[2026-11-13T20:51:43Z · bob-cli-ld.9.1.1] Projects JSON list/sync decoders, shared report/sync mixin, lifecycle fingerprints, and 19 unit tests landed in bob-plugins (bob-ledger-tools 1.114.0). npm run build, docs:gen, 19/19 projects-data, relation-index layout-ready hold, and linear startup storm all pass. Deployed via bob plugins sync (ledger-tools manifest+main.js). Full npm test: 6545 pass / 1 fail — keep-moving 200-link timing flake under load, isolated pass, already bob-cli-ki; recorded as PROPOSED FOLLOW-UP. No --epic-symbol leftovers. Did not run live bob projects sync.

## Dependencies

- **Blocks:** [bob-cli-ld.9.1.2](bob-cli-ld.9.1.2.md) ◐ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.9.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.9.1.1/README.md) | [bob-cli-ld.9.1.1](bob-cli-ld.9.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@fd3f028`](https://github.com/bobs-org/bob-plugins/commit/fd3f028ce60044ce29af927bf64a2a60c70f536d) | feat(bob-ledger-tools): add shared projects report and auto-sync | [bob-cli-ld.9.1.1](bob-cli-ld.9.1.1.md) | 2026-11-13 15:53:49 EST |
