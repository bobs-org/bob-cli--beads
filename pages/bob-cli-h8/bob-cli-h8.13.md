# Bead: bob-cli-h8.13 — Bring bob-plugins Depends-On consumption to the same rules

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.13` · **Size:** medium
**Created:** 2026-11-04 16:39:10 EST · **Closed:** 2026-11-05 17:38:39 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

consumption-plugins: move bob-plugins Depends-On link consumption off whole-subtree removal onto the same keep-notes, only-emptied, and identity rules. Assert the new §13.14 vectors in the plugin harness, sync the plugins, and close bob-cli-7q.

## Notes

[2026-11-05T22:37:19Z · bob-cli-h8.13] PROPOSED FOLLOW-UP: Triage unchanged plugin-suite failures outside Depends-On consumption — UTC 5569/5575 and New York 5570/5575. The wikilink-index warm/rank timing failures are already tracked by bob-cli-f8, with clean-base reproduction also recorded on bob-cli-h8.1; both zones also fail the unchanged configured-theme menu expectation (NACK vs SNACK) and root/Ledger Tools theme-vector byte-identity check. No matching theme/vector task bead surfaced.

[2026-11-05T22:38:39Z · bob-cli-h8.13] Verified plugin build and focused dependency/project-stage suites (44/44). Full npm test: UTC 5569/5575 and America/New_York 5570/5575, with unchanged baseline failures recorded in the phase note. Plugin docs check and bob-cli docs check passed (447 docs tests, one skipped). Epic symbols are clear. No-force plugin sync was attempted and refused bob-navigation-hotkeys because the vault stamp came from a different uncommitted checkout; did not force.

[2026-11-05T22:39:06Z · bob-cli-h8.13] Verified  and the focused dependency/project-stage tests (44/44). Both  runs included 5,575 cases: UTC 5,569 passed and New York 5,570 passed, with only unchanged baseline failures documented in the phase follow-up note.  and 
✅  DOCS CHECK
────────────────────────────────────────────────
docs-check: assemble and validate source context

docs-check: lint
bob-docs lint: ok
docs-check: passed (lint)

docs-check: generated drift
Plugin documentation inventory is up to date.
generated contract content is up to date
docs-check: passed (generated drift)

docs-check: strict Zensical build
Build started
Build finished in 9.18s
running: zensical build --strict --config-file /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/target/docs/mkdocs.yml
built site: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/target/docs/site
docs-check: passed (strict Zensical build)

docs-check: published URLs
wrote /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/target/docs/site/urls.txt (196 published pages)
urls: OK (196 pages, 703 mentions checked, 60 curated links)
docs-check: passed (published URLs)

docs-check: offline lychee with fragments
🔍 50247 Total (in 1s 610ms) 🔗 3228 Unique ✅ 49166 OK 🚫 0 Errors 👻 1081 Excluded

running: /home/bryan/.cache/bob-docs/bin/lychee --offline --no-progress --include-fragments --exclude-path (^|/)index[.]md$ --index-files index.html --root-dir /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/target/docs/site --remap https://bobs-org.github.io/ file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/target/docs/site/ /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/target/docs/site
links: OK (offline lychee with fragment checking)
docs-check: passed (offline lychee with fragments)

docs-check: edit links point at real sources
edit-links: OK (193 edit link(s) point at real source files)
docs-check: passed (edit links point at real sources)

docs-check: search smoke
search smoke: OK (125 cases; index /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/target/docs/site/search.json)
docs-check: passed (search smoke)

docs-check: executable first-day tutorial

TUTORIAL_FENCE 5 docs/start/install.md:67
bob 0.4.0

TUTORIAL_FENCE 7 docs/start/first-bob-day.md:24
Using demo vault: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261104_164118/bob-docs-sandbox-wuqsjvmg/tmp/bob-first-day.mYJnnY/vault

TUTORIAL_FENCE 8 docs/start/first-bob-day.md:46
✓ captured  mac_inbox.md
  - [ ] #task Sort the seed packets [created::2026-10-20] ^seed-packet

TUTORIAL_FENCE 9 docs/start/first-bob-day.md:61
✓ captured  garden.md
  - [ ] #task Water the seedlings [created::2026-10-20] ^seedlings

TUTORIAL_FENCE 10 docs/start/first-bob-day.md:76
bob plan - Tue 2026-10-20 - no daily note yet

  PLAN  0/10 links      TODAY 0 - PENDING 0/10 - NEXT 0/15


TUTORIAL_FENCE 11 docs/start/first-bob-day.md:92
Created daily note: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261104_164118/bob-docs-sandbox-wuqsjvmg/tmp/bob-first-day.mYJnnY/vault/2026/20261020.md

TUTORIAL_FENCE 12 docs/start/first-bob-day.md:117
✓ started  2026/20261020.md
  FOCUS 0905-0930 (25m) (created) at line 4
  - [ ] (**0905-0930** [t:: 25m]) — FOCUS
  nothing queued
plan 0/10 links

TUTORIAL_FENCE 13 docs/start/first-bob-day.md:128
✓ link  garden.md
  [ ] → [*]  Water the seedlings  ^seedlings
  Linked under FOCUS
plan 1/10 links
{"caps":{"max_links":10,"max_next":15,"max_pending":10,"max_ready":100},"daily_file":"2026/20261020.md","date":"2026-10-20","entries":[{"components":["FOCUS"],"exempt":false,"highlight":true,"homes":{"chip":"garden","hue":"magenta","kind":"work","label":"garden","parts":[{"area":"garden.md","area_label":"garden","hue":"magenta","key":"garden.md","kind":"area","label":"garden","share":100,"tasks":1}],"state":"forecast"},"line":4,"links":1,"name":"FOCUS","running":true,"themes":[{"hue":"yellow","hue_source":"hash","key":"focus","name":"FOCUS"}],"time_range":"0905-0930"}],"links":{"cap":10,"count":1,"off_clock":0,"over":false},"next":{"cap":15,"count":1,"over":false},"ok":true,"pending":{"cap":10,"count":0,"over":false},"schema_version":3,"status":"ok","theme_names":["FOCUS"],"theme_refs":[{"hue":"yellow","hue_source":"hash","key":"focus","name":"FOCUS"}],"today":{"count":1},"today_roots":[{"hue":"magenta","key":"garden.md","label":"garden","tasks":1}],"today_tasks":[{"block_id":"seedlings","entry_line":4,"entry_name":"FOCUS","ledger_line":5,"line":8,"path":"garden.md","status_name":"Next","status_symbol":"*","text":"Water the seedlings"}],"warnings":[]}

TUTORIAL_FENCE 14 docs/start/first-bob-day.md:141
bob capture: warning: FOCUS has not started: it starts at 0905, so closing now records a zero-length session; capture `x0` to reset it instead
✓ closed FOCUS 0905-0930 → 0905-0905 (0m, −25m) · 2026/20261020.md line 4
  1 [*] → [x] Water the seedlings garden.md ^seedlings
  next: FOCUS (created) at line 6 · carries 0 links
plan 0/10 links

TUTORIAL_FENCE 15 docs/start/first-bob-day.md:154
{"config":{"decay":{"enabled":true,"enter":null,"keeps":3,"limits":{"next":3,"pending":3,"ready":3}},"interval":7,"next_interval":1,"pending_interval":1,"project_interval":null,"rotten_daily_budget":null},"counts":{"budget":null,"budget_met":false,"by_tier":{"new":1,"next":0,"pending":0,"post":0,"pre":0,"projects":1,"recurring":0,"rotten":0,"tickler":0},"decide":0,"due":2,"fresh":0,"new":2,"next_due":0,"pending_due":0,"post_due":0,"pre_due":0,"projects_due":1,"recurring_due":0,"refreshed_today":1,"resurfaced":0,"rotten":0,"upkeep_today":1,"walk":2},"date":"2026-10-20","ok":true,"queue":[{"block_id":"seed-packet","bucket":"new","created":"2026-10-20","days_overdue":null,"decide":false,"due_on":null,"fresh":null,"interval":7,"interval_source":"default","keeps":0,"lane":"ready","line":7,"path":"mac_inbox.md","rank":1,"returned_by":null,"scheduled":null,"state":"new","status_symbol":" ","text":"Sort the seed packets ^seed-packet","tier":"new","unblocked_on":null},{"block_id":"prj","bucket":"new","created":null,"days_overdue":null,"decide":false,"due_on":null,"fresh":null,"interval":7,"interval_source":"default","keeps":0,"lane":"ready","line":11,"path":"Projects/seedlings.md","rank":2,"returned_by":null,"scheduled":null,"state":"new","status_symbol":" ","text":"#prj Raise healthy seedlings for the garden ^prj","tier":"projects","unblocked_on":null}],"schema_version":15,"warnings":[]}
skipped: docs/start/install.md:16: network clone needs a remote and user credentials
skipped: docs/start/install.md:27: toolchain install changes the host and needs network
skipped: docs/start/install.md:42: install writes outside the tutorial sandbox
skipped: docs/start/install.md:61: PATH export edits the reader shell profile
skipped: docs/start/install.md:87: network install needs a remote and writes outside the sandbox
skipped: docs/start/obsidian.md:18: opening Obsidian needs the desktop app
skipped: docs/start/obsidian.md:28: Tasks install needs the Obsidian app and network
skipped: docs/start/obsidian.md:52: plugin clone needs network and a plugin source checkout
skipped: docs/start/obsidian.md:57: plugin sync needs a plugin source checkout and Obsidian
skipped: docs/start/mac-capture.md:19: Mac build needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:26: Mac bundle needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:33: Mac install needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:40: Mac launch needs the Mac app bundle
skipped: docs/start/mac-capture.md:54: panel setup needs the Mac app
skipped: docs/start/mac-capture.md:81: first Mac capture needs the Mac panel
tutorial: passed
docs-check: passed (executable first-day tutorial)

docs-check: CLI media determinism
media: check passed (regeneration is byte-stable)
docs-check: passed (CLI media determinism)

docs-check: documentation unit tests
============================= test session starts ==============================
platform linux -- Python 3.14.7, pytest-9.1.1, pluggy-1.7.0
rootdir: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_34/tools/docs
configfile: pyproject.toml
plugins: platformdirs-4.13.5
collected 448 items

tools/docs/tests/test_assemble.py ....                                   [  0%]
tools/docs/tests/test_assets.py .....s.                                  [  2%]
tools/docs/tests/test_capture_token_coverage.py ..                       [  2%]
tools/docs/tests/test_check.py ....                                      [  3%]
tools/docs/tests/test_compatibility.py ......                            [  5%]
tools/docs/tests/test_contracts.py ........                              [  6%]
tools/docs/tests/test_demo_tasks.py ..                                   [  7%]
tools/docs/tests/test_edit_links.py ....                                 [  8%]
tools/docs/tests/test_

… and 3096 more characters

## Dependencies

- **Depends on:** [bob-cli-h8.12](bob-cli-h8.12.md) ✓ · ⧖ 2026-11-04
- **Depends on:** [bob-cli-h8.8](bob-cli-h8.8.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.13/README.md) | [bob-cli-h8.13](bob-cli-h8.13.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4fa96e1`](https://github.com/bobs-org/bob-cli/commit/4fa96e152bae8c00f765934ddb7624b0d6d031df) | docs(task-dependencies): document plugin consumption parity | [bob-cli-h8.13](bob-cli-h8.13.md) | 2026-11-05 17:41:03 EST |
