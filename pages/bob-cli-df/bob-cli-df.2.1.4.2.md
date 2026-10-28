# Bead: bob-cli-df.2.1.4.2 — Integrate the repaired core and finish quarantine recovery

[Bead Pages](../README.md) / [bob-cli-df.2.1.4](bob-cli-df.2.1.4.md) / bob-cli-df.2.1.4.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.land.md) · **Size:** medium
**Created:** 2026-10-28 02:07:52 EDT · **Closed:** 2026-10-28 04:12:24 EDT
**Plan:** [202610/artifact\_link\_quarantine\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_quarantine_landing_repairs.md)

## Description

replay-and-evidence: pin the Rust repair, detect incomplete history, reuse immutable quarantine evidence, and validate its path and project.

## Notes

[2026-10-28T08:12:00Z · bob-cli-df.2.1.4.2--1] PROPOSED FOLLOW-UP: sase tool run check SASE validation fails on missing plans sidecar (sase/repos/plans invalid-root); reproduces identically on clean base with phase work stashed. Already tracked by bob-cli-dg per plan; do not fold into this phase. -r Record unrelated check failure that reproduces on clean base

[2026-10-28T08:12:04Z · bob-cli-df.2.1.4.2--1] PROPOSED FOLLOW-UP: just check lint-symvision flags private _RecoveryAssessment import in src/sase/finalizers/_failed_close_recovery_assess.py (KNOWN, witness 13ea2a464abef73b3eab4bfee9e624d7 from sibling recovery commit dcb7d2a6e7); DISCOVERED ISSUE lives on active epic bob-cli-df per plan. Do not fold into this phase. -r Record known unrelated symvision lint

[2026-10-28T08:12:07Z · bob-cli-df.2.1.4.2--1] PROPOSED FOLLOW-UP: just install-venv downgrades the freshly built sase_core_rs 0.43.0 wheel back to published 0.42.7 via the editable reinstall step (uv pip install -e .[dev] with bare-name overrides file), so focused pytest must reinstall the cached 0.43.0 wheel after install-venv when the core checkout is ahead of the pyproject pin. -r Record venv override infrastructure issue hit during verification

[2026-10-28T08:12:24Z · bob-cli-df.2.1.4.2--1] replay-and-evidence done: pinned sase-core-revision.txt to f4bf6074, shallow-history honesty, immutable quarantine reuse across durability transition (Rust ValueError mapped to corruption), operation/digest path plus project validation. Fixed same-batch test expectation (winner+unrelated publish) and corruption mapping; 17 focused quarantine suites pass, plus publisher/outbox-drain/store-core-health/formatting/link-add/doctor/bindings suites green (32+37+20). just fix clean; lint ruff/mypy/fmt pass. sase tool run check has 2 unrelated failures recorded as PROPOSED FOLLOW-UP: KNOWN symvision _RecoveryAssessment (witness 13ea2a46) and plans-sidecar SASE validation reproducing identically on clean base (bob-cli-dg). No epic symbols left. Wheel verified as cached 0.43.0 build of f4bf6074.

## Dependencies

- **Depends on:** [bob-cli-df.2.1.4.1](bob-cli-df.2.1.4.1.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.4.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.2.md) | [bob-cli-df.2.1.4.2](bob-cli-df.2.1.4.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.2.1.4.2--1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.2.md

<!-- sase:referenced-by:end -->
