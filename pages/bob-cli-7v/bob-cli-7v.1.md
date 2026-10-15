# Bead: bob-cli-7v.1 — List-aware import dedupe for source\_url and url lists

[Bead Pages](../README.md) / [bob-cli-7v](README.md) / bob-cli-7v.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10k.md) · **Assignee:** `bob-cli-7v.1` · **Size:** small
**Created:** 2026-10-15 12:30:28 EDT · **Closed:** 2026-10-15 12:38:47 EDT
**Plan:** [202610/ref\_create\_multi\_url\_collections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_multi_url_collections.md)

## Description

dedupe: record one dedupe source per item of a list-valued source_url/url in ref notes and intake markers, so create, ingest, capture routing, and find -i see every URL of a list; delete the documented gap in docs/ref.md.

## Notes

[2026-10-15T16:38:47Z · bob-cli-7v.1] Expanded scalar and list-valued source_url/url metadata from ref notes and intake markers for import dedupe and find -i; removed stale scalar-only docs gap. Verified: focused sources tests pass (6/6), cargo fmt --check, git diff --check; epic-symbols reports no entries.

## Dependencies

- **Blocks:** [bob-cli-7v.4](bob-cli-7v.4.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7v.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.1/README.md) | [bob-cli-7v.1](bob-cli-7v.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`47e85f6`](https://github.com/bobs-org/bob-cli/commit/47e85f65e00dc953c25416b475b21fe0ee4bea92) | feat(ref): dedupe list-valued source URLs | [bob-cli-7v.1](bob-cli-7v.1.md) | 2026-10-15 12:39:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7v.1][1] | Check prior phase notes and remaining work before planning | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.1/README.md

<!-- sase:referenced-by:end -->
