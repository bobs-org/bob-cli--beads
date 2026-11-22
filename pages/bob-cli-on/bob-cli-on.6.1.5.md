# Bead: bob-cli-on.6.1.5 — The expand\_req\_marker typing rewrite

[Bead Pages](../README.md) / [bob-cli-on.6.1](bob-cli-on.6.1.md) / bob-cli-on.6.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) · **Assignee:** `bob-cli-on.6.1.5` · **Size:** medium
**Created:** 2026-11-21 13:50:30 EST · **Closed:** 2026-11-21 20:11:37 EST
**Plan:** [202611/capture\_req\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md)

## Description

req-rewrite: add expand_req_marker to capture-rewrite with resolver-driven eligibility and the notebook policy preflight, and document client-side overtype absorption and atomic Backspace in capture-rewrite help and docs/capture.md.

## Notes

[2026-11-22T01:11:22Z · bob-cli-on.6.1.5] PROPOSED FOLLOW-UP: Fix stale docs contract-index checks — docs-check finds 55 registry entries while test_contracts.py expects 54, the configured llms.txt contract list omits task-requirements.md, and the README index snapshot hash is stale; all three failures reproduce unchanged on clean HEAD.

[2026-11-22T01:11:37Z · bob-cli-on.6.1.5] Implemented resolver-driven expand_req_marker with notebook and record route preflight, documented overtype absorption and atomic Backspace, and regenerated the CLI reference. Verified cargo check --bin bob, the focused requirement-marker unit test, all 61 capture_rewrite CLI tests, cargo fmt, and the docs lint/build/link/tutorial gates. docs-check still fails three contract-index assertions reproduced unchanged on clean HEAD; recorded as a PROPOSED FOLLOW-UP. epic-symbols reports none.

## Dependencies

- **Depends on:** [bob-cli-on.6.1.2](bob-cli-on.6.1.2.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.5/README.md) | [bob-cli-on.6.1.5](bob-cli-on.6.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c05deef`](https://github.com/bobs-org/bob-cli/commit/c05deef26b80d09c3f69181c8ab0f4dd60637168) | feat(capture): add requirement marker typing rewrite | [bob-cli-on.6.1.5](bob-cli-on.6.1.5.md) | 2026-11-21 20:14:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.6.1.5][1] | Need the phase scope, notes, and design file before completing assigned work | 1 |
| read-by | [agent:bob-cli-on.6.1.land][2] | Need the child scope and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.1.land.md

<!-- sase:referenced-by:end -->
