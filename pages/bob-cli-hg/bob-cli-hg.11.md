# Bead: bob-cli-hg.11 — Bob Mac Capture shows Gmail links in the panel

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.11` · **Size:** medium
**Created:** 2026-11-05 12:37:50 EST · **Closed:** 2026-11-06 12:45:10 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

mac-gmail-preview: decode and paint the gmail_url span, show each item's Gmail preview line, and after typing settles show the real subject and sender from `bob gmail peek`, green on macOS CI.

## Notes

[2026-11-06T16:30:50Z · bob-cli-hg.11] PROPOSED FOLLOW-UP: bob-cli docs contract snapshot test_readme_table_matches_original_contract_index_snapshot fails on clean base e096004 (cached docs-check checkout); unrelated to mac-gmail-preview, needs snapshot regen by docs owner

[2026-11-06T17:44:50Z · bob-cli-hg.11] PROPOSED FOLLOW-UP: 12 macOS CI Test-step failures (word-motion, comma rewrite-lane, separator-toggle family) reproduce identically on clean base 5b0dca6; master is red at Test, needs owner triage

[2026-11-06T17:45:10Z · bob-cli-hg.11] Landed a2aab30 to bob-mac-capture master: gmail_url span decode+paint, per-item gmail preview lines, settled gmail peek lane, fixtures+19 tests. Verified: portable suite 2253 green on athena; macOS CI exact-SHA gate 42256754534 Lint+Build green, all 16 new Gmail tests pass, Test-step failures byte-identical to clean base 5b0dca6 (pre-existing, filed as follow-up). Mac-local typecheck skipped (Mac offline).

## Dependencies

- **Depends on:** [bob-cli-hg.8](bob-cli-hg.8.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.9](bob-cli-hg.9.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.11.md) | [bob-cli-hg.11](bob-cli-hg.11.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.5s.grk][1] | Need remaining Gmail phase user-facing scopes for the guide | 1 |
| read-by | [agent:research.5s.mus][2] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.grk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
