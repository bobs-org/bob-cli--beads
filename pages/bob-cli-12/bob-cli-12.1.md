# Bead: bob-cli-12.1 — Authoritative bob-cli grammar, execution, and protocol

[Bead Pages](../README.md) / [bob-cli-12](README.md) / bob-cli-12.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0c9.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0c9.w0.md) · **Assignee:** `bob-cli-12.1` · **Size:** medium
**Created:** 2026-08-24 07:57:17 EDT · **Closed:** 2026-08-24 08:22:24 EDT
**Plan:** [202608/global\_capture\_destination.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/global_capture_destination.md)

## Description

global-destination-protocol: implement the shared draft envelope, inherited execution semantics, additive editor/output protocol, documentation, and Rust coverage.

## Notes

[2026-08-24T12:22:24Z · bob-cli-12.1] Implemented the @@ draft envelope, inherited execution, additive parse/complete/success JSON, docs, and Rust coverage. Verified cargo fmt --check, cargo clippy --all-targets --all-features, and cargo test. Confirmed @@foo and @@foo+a-id batches, local @bar/@bar+id overrides, header-only and --route conflict usage errors, parse global_destination metadata/spans, header completion ranges excluding both @ sigils, inherited same-note wikilink completion, stdin/dry-run human output, and failed mixed/global batches leaving fixtures byte-for-byte unchanged.

## Dependencies

- **Blocks:** [bob-cli-12.2](bob-cli-12.2.md) ✓ · ⧖ 2026-08-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-12.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-12.1/README.md) | [bob-cli-12.1](bob-cli-12.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9258da9`](https://github.com/bobs-org/bob-cli/commit/9258da9c109916750ad2d7db36b24b1f66f66a9a) | feat(capture): add global @@ destination declarations | [bob-cli-12.1](bob-cli-12.1.md) | 2026-08-24 08:23:04 EDT |
