# Bead: bob-cli-a0.7.1.1 — Capture syntax and vault format reference

[Bead Pages](../README.md) / [bob-cli-a0.7.1](bob-cli-a0.7.1.md) / bob-cli-a0.7.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.md) · **Assignee:** `bob-cli-a0.7.1.1` · **Size:** medium
**Created:** 2026-10-19 23:14:29 EDT · **Closed:** 2026-10-19 23:36:47 EDT
**Plan:** [202610/product\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/product_reference.md)

## Description

capture-vault: write the capture token index and vault-format reference, add their navigation and token/lane search cases, and verify examples in a synthetic vault.

## Notes

[2026-10-20T03:36:47Z · bob-cli-a0.7.1.1] Wrote docs/reference/capture-syntax.md (token index + per-token headings with explicit anchors) and docs/reference/vault-format.md (task-line anatomy, lane/field tables, Pending/Next headings, note types, directory tree). Added both pages to mkdocs.yml Reference nav and the Reference hub. search_smoke.yml covers every indexed capture token plus Pending/Next (57 cases). Verified representative bob capture examples in an isolated HOME/XDG synthetic vault with BOB_NOW=2026-10-20 12:00:00, TZ=UTC, BOB_REF_JOBS_KICK=off. just docs-check passed (lint, Zensical build, lychee, search smoke, 206 pytest). Built HTML shows bob-task anatomy, named token anchors, and #pending/#next. sase bead epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-a0.7.1.3](bob-cli-a0.7.1.3.md) ○ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.7.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.7.1.1/README.md) | [bob-cli-a0.7.1.1](bob-cli-a0.7.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.7.1.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.7.1.1/README.md

<!-- sase:referenced-by:end -->
