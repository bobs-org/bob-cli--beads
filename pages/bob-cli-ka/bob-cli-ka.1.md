# Bead: bob-cli-ka.1 — One section resolver, a staged view, and the silent-wrong fixes

[Bead Pages](../README.md) / [bob-cli-ka](README.md) / bob-cli-ka.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b9.md) · **Assignee:** `bob-cli-ka.1` · **Size:** medium
**Created:** 2026-11-11 09:22:46 EST · **Closed:** 2026-11-11 10:26:39 EST
**Plan:** [202611/notebook\_section\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_section_bullets.md)

## Description

resolver: extend the notebook section resolver with an Ambiguous outcome and optional typed-capitals titles, add the staged section view (disk plus earlier draft operations) behind parse and the glued `@nb#` menu, stop the drawer menu and drawer probe on notebook note bullets, and fix the list summary noun.

## Notes

[2026-11-11T15:03:50Z · bob-cli-ka.1] Verified: Ambiguous title/slug ties, typed-capitals create titles, staged disk-plus-draft sections for parse and glued @nb#, notebook note bullets skip the drawer probe, and human list summaries use note(s). Grammar stays 25. Unit/CLI notebook tests passed; clippy gate passed; epic-symbols empty. just check pending via prepared monitor.

[2026-11-11T15:20:06Z · bob-cli-ka.1--1] PROPOSED FOLLOW-UP: highlights_create_recognizes_definition_list_mermaid_fences fails on clean HEAD ba3f51ba with "image-guard report unreadable: invalid type: map, expected a sequence at line 1 column 10" (empty Lua table encodes as JSON {}); already fixed in closed bob-cli-k6.2 (7eb82440 on origin/master; this workspace is 2 commits behind). Reproduced on the clean-HEAD cli binary without this phase's capture edits.

[2026-11-11T15:25:19Z · bob-cli-ka.1--1] Verified: recovery after just check exit 101. highlights_create_recognizes_definition_list_mermaid_fences fails identically on clean HEAD ba3f51ba (empty image-guard Lua table encodes as JSON {}); recorded as PROPOSED FOLLOW-UP citing closed bob-cli-k6.2 / 7eb82440. Phase tests passed: capture_language 814, routes_tasks 25, CLI notebook_ 31, complete_drawers 16. epic-symbols empty. Grammar stays 25.

[2026-11-11T15:26:39Z · bob-cli-ka.1--1] Closed by explicit `sase stitch create -B close` after create_commit landed f9d998c1 ("feat(capture): resolve notebook sections with staged draft view"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-ka.1` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-ka.2](bob-cli-ka.2.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ka.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ka.1.md) | [bob-cli-ka.1](bob-cli-ka.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f9d998c`](https://github.com/bobs-org/bob-cli/commit/f9d998c179a37bb1f1f3df8b590c472a3f5eff00) | feat(capture): resolve notebook sections with staged draft view | [bob-cli-ka.1](bob-cli-ka.1.md) | 2026-11-11 10:26:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ka.1--1][1] | Need the phase scope, design file, notes, and DECISIONS after just check failed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ka.1.md

<!-- sase:referenced-by:end -->
