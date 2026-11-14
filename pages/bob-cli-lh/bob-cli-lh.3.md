# Bead: bob-cli-lh.3 — Badge hosts after every Day and period strip

[Bead Pages](../README.md) / [bob-cli-lh](README.md) / bob-cli-lh.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4l.linker.w0.md) · **Assignee:** `bob-cli-lh.3` · **Size:** medium
**Created:** 2026-11-14 06:52:51 EST · **Closed:** 2026-11-14 08:25:28 EST
**Plan:** [202611/bank\_badge\_strip\_family.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_badge_strip_family.md)

## Description

strip-hosts: split bob-day-stats and bob-stats-strip fences into a strip host plus a badge host, fetch -D/-w/-p reports with visibility gating, skip future periods, degrade quietly on an older bob, test, document, and deploy.

## Notes

[2026-11-14T13:24:31Z · bob-cli-lh.3] PROPOSED FOLLOW-UP: npm run docs:check fails on origin/master sase/memory/glossary/bank-badge.md missing YAML front matter (28f48be9 / bob-cli-lh.4 vocabulary); reproduces independently of strip-hosts

[2026-11-14T13:24:49Z · bob-cli-lh.3] PROPOSED FOLLOW-UP: bob plugins sync exits 2 because chezmoi-managed ~/.config/bob/config.yml has no plugins.sync allowlist; ledger-tools strip-hosts cannot deploy until that list exists

[2026-11-14T13:25:04Z · bob-cli-lh.3] PROPOSED FOLLOW-UP: Obsidian week/quarter e2e not run (no Chromium/OBSIDIAN_BIN); bank-ui-e2e self-test passed. Full npm test 25ms flakes already tracked as bob-cli-km, bob-cli-ki, bob-cli-ju; sheet-sequence-dom needs Chromium on PATH

[2026-11-14T13:25:28Z · bob-cli-lh.3] Fence split: bob-day-stats and bob-stats-strip (week/quarter/year/all/day-delegation) get strip then badge hosts; painters keep record.el. Fetches -D/-w/-p -s, BANK_CACHE_SIZE=24, visibility-gated subscribe, future skip via periodNotesIsoWeekMonday, older-bob hidden + one warn. Six host tests pass plus decode/data/cards/day/period strip suites. docs:gen/inventory ok. docs:check fails on pre-existing glossary:bank-badge strand (lh.4). npm test 6587 pass / 5 fail (Chromium missing + known 25ms flakes km/ki/ju; isolation 110/110). Sync blocked: no plugins.sync allowlist. No epic-symbols leftovers.

## Dependencies

- **Depends on:** [bob-cli-lh.1](bob-cli-lh.1.md) ✓ · ⧖ 2026-11-14
- **Depends on:** [bob-cli-lh.2](bob-cli-lh.2.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-lh.4](bob-cli-lh.4.md) ◐ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lh.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lh.3/README.md) | [bob-cli-lh.3](bob-cli-lh.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6a1778b`](https://github.com/bobs-org/bob-plugins/commit/6a1778b52c44419b550052c2c36b51bce377d950) | feat(ledger-tools): add bank badge hosts after every stats strip | [bob-cli-lh.3](bob-cli-lh.3.md) | 2026-11-14 08:27:20 EST |
