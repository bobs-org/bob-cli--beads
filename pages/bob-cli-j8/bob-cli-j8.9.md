# Bead: bob-cli-j8.9 — Notebook type note, template, Base, and the wave-1 migration

[Bead Pages](../README.md) / [bob-cli-j8](README.md) / bob-cli-j8.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3x.linker.w0.md) · **Assignee:** `bob-cli-j8.9` · **Size:** medium
**Created:** 2026-11-09 12:11:28 EST · **Closed:** 2026-11-10 07:25:28 EST
**Plan:** [202611/bob\_notebooks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_notebooks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:3be405355574807f4e9a287a | attached via sase artifact create --bead |
| related | file:explicit:61d0181ed1156f26c1636417 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

notebook-vault: once every host runs a bob with notebook capture, add the `notebook.md` type note, `notebooks.base`, and `_templates/new_notebook.md`, then migrate the wave-1 manifest (type, quoted parent, summary, H1; nothing else), run `bob notebooks sync` and `check`, and prove the success criteria.

## Notes

[2026-11-10T12:21:35Z · bob-cli-j8.9--5] PROPOSED FOLLOW-UP: Fix notebook duplicate-block-ID validation to count actual trailing ID declarations and ignore ^id tokens inside wikilink anchors; all 100 wave-1 checker errors are this code, and the unchanged dev_tools fixture reproduces its six findings.

[2026-11-10T12:25:28Z · bob-cli-j8.9--5] Wave-1 migration and report are complete. All three hosts passed notebook capture preconditions; all 26 rows received exact planned edits, retained IDs and per-file task counts, and appear once in current root catalogs; sync is a no-op. Recorded the reproduced notebook_duplicate_block_id validator false positive as a proposed follow-up. Report documents 9 legacy shape warnings and +14 vault-wide tasks from concurrent non-manifest syncs.

## Dependencies

- **Blocks:** [bob-cli-j8.10](bob-cli-j8.10.md) ◐ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j8.2](bob-cli-j8.2.md) ✓ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j8.3](bob-cli-j8.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.9.md) | [bob-cli-j8.9](bob-cli-j8.9.md) | 0 |
