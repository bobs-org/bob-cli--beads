# Bead: bob-cli-ac.7 — Reader-facing release documentation and site integration

[Bead Pages](../README.md) / [bob-cli-ac](README.md) / bob-cli-ac.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.w1.md) · **Assignee:** `bob-cli-ac.7` · **Size:** medium
**Created:** 2026-10-20 18:36:54 EDT · **Closed:** 2026-10-20 23:35:00 EDT
**Plan:** [202610/crates\_io\_release\_train.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/crates_io_release_train.md)

## Description

docs-user: add the Releases and versions reference and the tagged-release install guide, update hubs, nav, the release checklist, and the URL contract, and pass the full docs gate.

## Notes

[2026-10-21T03:35:00Z · bob-cli-ac.7] Added docs/reference/releases.md and docs/guides/install-a-tagged-release.md; wired mkdocs nav, Guides/Reference hubs, start/install Next, release-checklist (train complement), and the three release.yml URLs in url_contract.txt. just docs-gen and just docs-check passed (lint, Zensical, URLs, lychee, tutorial, 447 docs tests). Built site: Guides hub, Reference hub, and install Next each reach the new pages in one click; Develop Releases Look up links Releases and versions; #daily-guard heading exists. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-ac.6](bob-cli-ac.6.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ac.8](bob-cli-ac.8.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ac.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ac.7/README.md) | [bob-cli-ac.7](bob-cli-ac.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8789c12`](https://github.com/bobs-org/bob-cli/commit/8789c12dafcd189ddccb375ab0c79fe880c4aef2) | docs(release): add versions reference and tagged-install guide | [bob-cli-ac.7](bob-cli-ac.7.md) | 2026-10-20 23:42:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ac.7][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ac.7/README.md

<!-- sase:referenced-by:end -->
