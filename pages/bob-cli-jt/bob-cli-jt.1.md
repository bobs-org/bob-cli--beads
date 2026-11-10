# Bead: bob-cli-jt.1 — bob-cli rewrite, tip, help, docs, and memory

[Bead Pages](../README.md) / [bob-cli-jt](README.md) / bob-cli-jt.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b1.md) · **Assignee:** `bob-cli-jt.1` · **Size:** medium
**Created:** 2026-11-10 15:05:11 EST · **Closed:** 2026-11-10 15:44:51 EST
**Plan:** [202611/backslash\_percent\_alias.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backslash_percent_alias.md)

## Description

bob-directive-alias: make capture-rewrite alias `\` to `%` where the directive menu opens, retire the `\` hash alias and collapse trigger, add the directive_menu tip, and update help, docs, tests, and the glossary strand.

## Notes

[2026-11-10T20:41:48Z · bob-cli-jt.1] Verified forward alias + tip JSON. `bob capture-rewrite -c 10 --format json -- 'Buy milk \' => {"text":"Buy milk %","changed":true,"rule":"expand_sigil_alias","edits":[{"range":{"start":9,"end":10},"replacement":"%"}],"summary":"Typed % for \","alias":{"id":"directive_menu","key":"\","sigil":"%"}}. `bob capture-rewrite -c 10 --format json -- 'Buy milk %' => {"changed":false,"sigil_alias_tip":{"id":"directive_menu","sigil":"%","keys":["\"],"range":{"start":9,"end":10},"where":"after a word"}}. Literal probes: @cash\, @cash\, foo \\ all changed:false with explicit null tip. `x=25 %` gets no directive field from capture-complete here, so `x=25 \` stays literal (grammar decides). `- \` fires (-> `- %`); `- %` tip has no where phrase. Full workspace tests: only pre-existing base failures (see follow-ups).

[2026-11-10T20:41:57Z · bob-cli-jt.1] PROPOSED FOLLOW-UP: just check clippy gate fails on clean base with 4 errors in untouched files (gcal/note/write.rs len_zero + 2 collapsible_if, gcal/doctor.rs collapsible_if, articles/inbound.rs); newer clippy vs old code

[2026-11-10T20:42:01Z · bob-cli-jt.1] PROPOSED FOLLOW-UP: catalog::protocol_1_parses_with_schema_version_one fails identically on clean base (89 vs 88); see already-tracked bob-cli-de

[2026-11-10T20:42:05Z · bob-cli-jt.1] PROPOSED FOLLOW-UP: doctor_json_healthy_setup fails identically on clean base (extra notes key in doctor JSON); needs a triage bead

[2026-11-10T20:42:09Z · bob-cli-jt.1] PROPOSED FOLLOW-UP: just docs-check fails on clean base with 5 reference word-budget errors (4 mac-capture mounts + plugins/bob-ledger-tools); already noted by earlier phases

[2026-11-10T20:44:51Z · bob-cli-jt.1] hash_fallback=drop implemented: \ now aliases % where the directive menu opens (directive_menu stamp/tip), / alone keeps # alias, collapse drops \. 746 lib + 54 CLI rewrite tests green; fmt clean; full suite + clippy/docs gates show only failures reproducing identically on the clean base (recorded as PROPOSED FOLLOW-UPs, catalog one cites bob-cli-de). No epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-jt.2](bob-cli-jt.2.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-jt.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-jt.1/README.md) | [bob-cli-jt.1](bob-cli-jt.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6ed27c1`](https://github.com/bobs-org/bob-cli/commit/6ed27c1e7b032fbb2e2e883bc2ff2770ed68b4ab) | feat(capture): implement hash\_fallback drop branch with directive\_menu alias | [bob-cli-jt.1](bob-cli-jt.1.md) | 2026-11-10 15:46:51 EST |
