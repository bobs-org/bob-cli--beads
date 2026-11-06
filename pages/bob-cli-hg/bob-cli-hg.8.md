# Bead: bob-cli-hg.8 — Capture recognizes Gmail URLs and links them after submit

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.8` · **Size:** medium
**Created:** 2026-11-05 12:37:49 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

capture-gmail: add the gmail_url capture-parse span and dry-run preview data, link already-saved threads offline at submit, and kick a detached single-flight `bob gmail link` worker after commit, with the grammar and docs updated.

## Notes

[2026-11-06T15:18:19Z · bob-cli-hg.8] Implemented Gmail capture spans and offline preview/saved-link substitution (grammar 16), post-commit scoped single-flight worker queue, login/logout local receipts for a zero-gog capture gate, docs and regression tests. Earlier Gmail linker landed at f075147f; no prior phase implementation existed. Verified cargo test --lib gmail::worker: 3 passed; git diff --check clean; epic-symbols reports none. Remaining work fits one coder: run new CLI regressions, regenerate docs, run docs-check and just check, repair any failures, then close only bob-cli-hg.8. No memory edited.

## Dependencies

- **Blocks:** [bob-cli-hg.11](bob-cli-hg.11.md) ◐ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.7](bob-cli-hg.7.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.8.md) | [bob-cli-hg.8](bob-cli-hg.8.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.5s.grk][1] | Need remaining Gmail phase user-facing scopes for the guide | 1 |
| read-by | [agent:research.5s.mus][2] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.grk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
