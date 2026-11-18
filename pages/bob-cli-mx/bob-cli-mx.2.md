# Bead: bob-cli-mx.2 — bob walks attention report and contract

[Bead Pages](../README.md) / [bob-cli-mx](README.md) / bob-cli-mx.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.es.md) · **Assignee:** `bob-cli-mx.2` · **Size:** medium
**Created:** 2026-11-17 17:59:53 EST · **Closed:** 2026-11-17 19:07:55 EST
**Plan:** [202611/mac\_walk\_attention\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_walk_attention_marks.md)

## Description

bob-walks: add the read-only `bob walks` command (human + JSON schema 1) that reports s/w/b attention with per-family failure isolation, plus the docs/walks.md contract, conformance vectors, goldens, and doc updates.

## Notes

[2026-11-18T00:07:39Z · bob-cli-mx.2] PROPOSED FOLLOW-UP: just docs-check fails on clean base with bob-plugins reference/plugins index.md collision — already tracked by bob-cli-it (stale ignored mount output; moving the ignored index still collides on other authored plugin pages)

[2026-11-18T00:07:55Z · bob-cli-mx.2] Verified bob walks: 3 lib tests; 24 CLI vectors S1-S5 W1-W8 B1-B4 plus freshness-list parity, goldens, human output, missing-vault JSON, --help contract; root help snapshots; catalog 104; 127 completion tests; just lint green; just docs-gen wrote CLI reference and contracts nav with walks after freshness. just docs-check fails on this workspace's clean base via the bob-cli-it plugin index collision.

[2026-11-18T00:33:12Z · bob-cli-mx.2--1] just check failed after close: catalog.entries still 103 after walks, plus HEAD records tidy missing catalog row, completion kinds, runner expected list, and help_options about. Wired records-tidy into catalog/kinds/runner/help and bumped counts to 105. Re-ran the 5 failing tests green.

## Dependencies

- **Blocks:** [bob-cli-mx.3](bob-cli-mx.3.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-mx.4](bob-cli-mx.4.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mx.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mx.2.md) | [bob-cli-mx.2](bob-cli-mx.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c50f889`](https://github.com/bobs-org/bob-cli/commit/c50f8895b5487722d2072a7d1c47a43f2ced9814) | feat(walks): add read-only attention report and contract | [bob-cli-mx.2](bob-cli-mx.2.md) | 2026-11-17 20:24:29 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mx.2--2][1] | Confirm assigned bead is complete so host completion can close it | 1 |
| read-by | [agent:bob-cli-mx.3][2] | Check prior phase follow-up on docs-check failure to cite | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mx.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mx.3/README.md

<!-- sase:referenced-by:end -->
