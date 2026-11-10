# Bead: bob-cli-j5.8 — Plugin path helper and archived-task reopen

[Bead Pages](../README.md) / [bob-cli-j5](README.md) / bob-cli-j5.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ai](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ai.md) · **Assignee:** `bob-cli-j5.8` · **Size:** medium
**Created:** 2026-11-09 11:04:09 EST · **Closed:** 2026-11-10 01:13:13 EST
**Plan:** [202611/done\_notes\_archiving\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/done_notes_archiving_fixes.md)

## Description

plugins: give each bob-plugins plugin that checks done/ paths the same helper pinned to the shared vectors, and route reopening an archived task per the plugin_reopen decision.

## Notes

[2026-11-10T06:13:04Z · bob-cli-j5.8] PROPOSED FOLLOW-UP: docs:check mount collision for bob-mac-capture reference/mac-capture index.md reproduces identically on the clean base tree (verified via stash round-trip); needs a land-agent or separate triage decision

[2026-11-10T06:13:13Z · bob-cli-j5.8] Helper isDoneArchivePath in all 4 plugins pinned to byte-identical done_archive_paths vectors (sha 9b9ce16d); all 15 done/path call sites migrated to first-component case-sensitive rule; archived reopen runs bob task restore -o -r -f json and unstrikes on success, Notices bob message on failure. Verified: npm run build ok, focused tests 10/10, full npm test 5903/5903 pass, bob plugins sync ok. docs:check mac-capture mount collision reproduces on clean base, recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-j5.6](bob-cli-j5.6.md) ✓ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-j5.7](bob-cli-j5.7.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.8/README.md) | [bob-cli-j5.8](bob-cli-j5.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@16c0454`](https://github.com/bobs-org/bob-plugins/commit/16c0454820f1d5034a7c2dc4062c42eb1f78f8ef) | feat(plugins): share one done/ path contract and reopen archived tasks via restore | [bob-cli-j5.8](bob-cli-j5.8.md) | 2026-11-10 01:14:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.8][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.8/README.md

<!-- sase:referenced-by:end -->
