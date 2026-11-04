# Bead: bob-cli-h8.2 — Let bob plugins sync accept committed dirty deploys

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.2` · **Size:** medium
**Created:** 2026-11-04 16:39:09 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

plugin-sync-proof: in src/native/plugins/deploy.rs, let a clean-checkout sync overwrite a dirty deploy stamp from another checkout or host when one commit reachable from HEAD holds the stamped bundle byte for byte. Keep every other refusal. Add tests, help text, and docs. Clear the live drift without --force, and close bob-cli-fy (and bob-cli-e4 once both hosts are synced).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.2/README.md) | [bob-cli-h8.2](bob-cli-h8.2.md) | 0 |
