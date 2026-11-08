# Bead: bob-cli-ii.3.1.3 — One transaction for routed mail notes and tasks

[Bead Pages](../README.md) / [bob-cli-ii.3.1](bob-cli-ii.3.1.md) / bob-cli-ii.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ii.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.3.md) · **Assignee:** `bob-cli-ii.3.1.3` · **Size:** medium
**Created:** 2026-11-07 18:12:56 EST · **Closed:** 2026-11-07 21:04:43 EST
**Plan:** [202611/gmail\_sync\_filing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_filing.md)

## Description

filing: share the prepared save path with sync, plan routed and problem tasks through capture, and apply all successful filings under one lock and scoped commit before recording enrollment events, with recovery and race tests.

## Notes

[2026-11-08T02:04:43Z · bob-cli-ii.3.1.3] Implemented routed Gmail note and task filing through one locked, scoped vault transaction, including shared save planning/writing, enrollment/adoption reconciliation, route validation, bounded note-change retry, journal recovery signals, and inbox-template reuse. Verified: cargo test native::gmail::sync --lib (53 passed), cargo test native::gmail::sync::file::tests --lib (10 passed), cargo test native::gmail::save::tests --lib (3 passed), cargo test --test gmail_pull_attach (5 passed), cargo check --lib, cargo fmt --check, and git diff --check. The earlier parallel sync run had one transient guard contention failure; the isolated test and full rerun passed. Epic symbols clear.

## Dependencies

- **Depends on:** [bob-cli-ii.3.1.1](bob-cli-ii.3.1.1.md) ✓ · ⧖ 2026-11-07
- **Depends on:** [bob-cli-ii.3.1.2](bob-cli-ii.3.1.2.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.3.1.4](bob-cli-ii.3.1.4.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.3.1.3/README.md) | [bob-cli-ii.3.1.3](bob-cli-ii.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d5c61ee`](https://github.com/bobs-org/bob-cli/commit/d5c61ee57a94003f88b37799e5fa5d1869f63efd) | feat(gmail): stage routed sync filings in one vault transaction | [bob-cli-ii.3.1.3](bob-cli-ii.3.1.3.md) | 2026-11-07 21:05:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.3.1.3][1] | Need the phase scope, design file, and prior-work notes before implementation | 1 |
| read-by | [agent:bob-cli-in.land--1][2] | Need child close state and notes before independent ii.3.1 closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.3.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-in.land.md

<!-- sase:referenced-by:end -->
