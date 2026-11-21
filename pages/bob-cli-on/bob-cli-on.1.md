# Bead: bob-cli-on.1 — Requirement recognizer, shared vectors, and the contract page

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.1` · **Size:** medium
**Created:** 2026-11-21 11:13:26 EST · **Closed:** 2026-11-21 12:15:18 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

req-contract: retire the bob-cli-of epic, then add the recursive requirement recognizer in bob-cli with its derived state model, structural row identity, RQ vectors, the TaskChildKind::Requirement variant, and the docs/task-requirements.md contract.

## Notes

[2026-11-21T17:15:07Z · bob-cli-on.1] PROPOSED FOLLOW-UP: just docs-check still fails on docs/reference/vault-format.md over the 6000-word reference budget (6016 without this phase, 6037 with the required cross-link) — tracked by bob-cli-oc; plugin-apis.md develop/ over-budget warning tracked by bob-cli-ob.

[2026-11-21T17:15:18Z · bob-cli-on.1] req-contract done: retired bob-cli-of (superseded); added src/native/task_reqs.rs recognizer (ReqMark/EffectiveReqState/ReqNode, req_forest/owner_of_line/is_req_line/req_row_key, MAX_REQ_DEPTH=16) with RQ1-RQ21 vectors+README and 7 passing tests; TaskChildKind::Requirement wired before Authored with merge/split behavior preserved; docs/task-requirements.md contract registered with 6 cross-links. Verified: cargo fmt --check clean, just lint clean, cargo test --workspace 12255 passed 0 failed, just docs-gen clean; just docs-check fails only on the pre-existing vault-format budget overrun tracked by bob-cli-oc (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-on.2](bob-cli-on.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.3](bob-cli-on.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.9](bob-cli-on.9.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.1/README.md) | [bob-cli-on.1](bob-cli-on.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a096143`](https://github.com/bobs-org/bob-cli/commit/a0961435506e4810841527ecd0b81505cb6d0632) | feat(task-reqs): add req forest recognizer contract | [bob-cli-on.1](bob-cli-on.1.md) | 2026-11-21 12:16:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.1/README.md

<!-- sase:referenced-by:end -->
