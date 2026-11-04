# Bead: bob-cli-h8.2 — Let bob plugins sync accept committed dirty deploys

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.2` · **Size:** medium
**Created:** 2026-11-04 16:39:09 EST · **Closed:** 2026-11-04 17:13:13 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

plugin-sync-proof: in src/native/plugins/deploy.rs, let a clean-checkout sync overwrite a dirty deploy stamp from another checkout or host when one commit reachable from HEAD holds the stamped bundle byte for byte. Keep every other refusal. Add tests, help text, and docs. Clear the live drift without --force, and close bob-cli-fy (and bob-cli-e4 once both hosts are synced).

## Notes

[2026-11-04T22:13:13Z · bob-cli-h8.2] plugin-sync-proof done: evaluate_guard permits a clean checkout overwriting another checkout/host dirty deploy when one commit reachable from HEAD (rev-list --max-count=500 on plugins/<id>) holds every stamped asset byte for byte (present:false must be absent), hashed in one git cat-file --batch session cached by blob id; mixed per-commit matches refuse, digest mismatch refuses, all other refusals unchanged. Permit carries proving_commit through PluginSync/JSON and table prints 'inclusion proof <short> holds the stamped bundle'. Help (top + sync) and docs/plugins.md updated, CLI golden regenerated, docs-check green. Tests: 49 lib + 18 plugins_sync CLI green incl 4 new unit + 1 new CLI proof test. Live athena: dry-run named d187f53, real sync without --force cleared drift, list 8/8 synced. Closed fy; e4 left for land agent (apollo 6/8 drift on old bob 0.4.0, ledger bundle matches f392c88, clears with new bob).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.2/README.md) | [bob-cli-h8.2](bob-cli-h8.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h8.2][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.2/README.md

<!-- sase:referenced-by:end -->
