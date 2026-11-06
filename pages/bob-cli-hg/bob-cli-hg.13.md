# Bead: bob-cli-hg.13 — Bob Mail compose surface in Obsidian

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.13` · **Size:** medium
**Created:** 2026-11-05 12:37:50 EST · **Closed:** 2026-11-06 16:49:19 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

plugin-compose: New email, Reply, Reply all, Save draft, and Send commands in bob-mail, with a send modal that renders bob's exact preview, binds the confirmation to its digest, and offers a short undo countdown.

## Notes

[2026-11-06T21:49:19Z · bob-cli-hg.13] plugin-compose done in bob-plugins: New/Reply/Reply-all/Save-draft/Send commands in bob-mail with digest-bound preview modal, 5s Undo countdown, double-send guard, hint-bearing errors. Verified: 8 new harness tests pass (scripts/test-bob-mail-compose.cjs), full npm test 5665 pass/0 fail, validate + docs-check green, bob plugins sync -p bob-mail deployed (superset of ws35 hg.10 bundle, backups kept). No epic-symbols left. No memory edits.

## Dependencies

- **Depends on:** [bob-cli-hg.10](bob-cli-hg.10.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.12](bob-cli-hg.12.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.13/README.md) | [bob-cli-hg.13](bob-cli-hg.13.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2563c78`](https://github.com/bobs-org/bob-plugins/commit/2563c7898644d1f784c13f3eefa698285ae4a381) | feat(bob-mail): add compose commands with send preview and undo window | [bob-cli-hg.13](bob-cli-hg.13.md) | 2026-11-06 16:50:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.land][1] | Check Bob Mail compose surface status for docs accuracy | 1 |
| read-by | [agent:bob-cli-hg.13][2] | Need the phase scope and design file | 3 |
| read-by | [agent:cq][3] | Understand Obsidian compose surface status | 1 |
| read-by | [agent:research.5s.grk][4] | Need remaining Gmail phase user-facing scopes for the guide | 1 |
| read-by | [agent:research.5s.mus][5] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.13/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.cq/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.grk/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
