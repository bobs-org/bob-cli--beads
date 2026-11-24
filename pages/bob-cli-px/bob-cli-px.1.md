# Bead: bob-cli-px.1 — Shared Gmail Task close model, vectors, and contract page (bob-cli)

[Bead Pages](../README.md) / [bob-cli-px](README.md) / bob-cli-px.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fs.md) · **Assignee:** `bob-cli-px.1` · **Size:** medium
**Created:** 2026-11-24 12:22:30 EST · **Closed:** 2026-11-24 13:11:03 EST
**Plan:** [202611/email\_task\_close\_confirmation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/email_task_close_confirmation.md)

## Description

model: Rust predicate plus copy and digest model for guarded closes, the shared conformance vectors, and the docs/mail-close-card.md contract.

## Notes

[2026-11-24T18:07:57Z · bob-cli-px.1] PROPOSED FOLLOW-UP: just lint fails identically on the clean base tree (9 clippy errors in src/native/props/cli.rs, src/native/props/contract/read.rs, src/native/albums/sync.rs; verified via git stash) — pre-existing, untouched by this phase

[2026-11-24T18:11:03Z · bob-cli-px.1] Model landed: src/native/gmail/close_guard/{predicate,copy,digest}.rs with scan-shared placement helpers (made pub(crate)), loose mail rule, orphaned counting via WatchScan, copy builder, 12-hex digest; 28-case tests/fixtures/mail_close/vectors.json all run green (cargo test --lib gmail::close_guard: 8 passed) plus 662 gmail lib tests; docs/mail-close-card.md registered in mkdocs (both blocks), contracts.yml, url_contract, gmail.md watch link; just docs-gen + docs-check pass. Pre-existing just lint failures (props/albums) verified identical on clean base and recorded as follow-up.

## Dependencies

- **Blocks:** [bob-cli-px.2](bob-cli-px.2.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-px.3](bob-cli-px.3.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-px.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.1/README.md) | [bob-cli-px.1](bob-cli-px.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f07c239`](https://github.com/bobs-org/bob-cli/commit/f07c2395e6e30f1a60c72b59e15d5ebd32839ae4) | feat(gmail): add shared mail close card model | [bob-cli-px.1](bob-cli-px.1.md) | 2026-11-24 13:12:16 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-px.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.1/README.md

<!-- sase:referenced-by:end -->
