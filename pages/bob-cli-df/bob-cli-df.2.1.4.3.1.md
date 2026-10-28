# Bead: bob-cli-df.2.1.4.3.1 — Preserve earliest history when a later identical copy descends from a competitor

[Bead Pages](../README.md) / [bob-cli-df.2.1.4.3](bob-cli-df.2.1.4.3.md) / bob-cli-df.2.1.4.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2.1.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.land.md) · **Assignee:** `bob-cli-df.2.1.4.3.1` · **Size:** medium
**Created:** 2026-10-28 04:35:24 EDT · **Closed:** 2026-10-28 05:17:26 EDT
**Plan:** [202610/artifact\_link\_provenance\_closeout.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_provenance_closeout.md)

## Description

copy-chronology: repair complete-group selection across copies and finish the required Rust import cleanup.

## Notes

[2026-10-28T09:17:15Z · bob-cli-df.2.1.4.3.1] PROPOSED FOLLOW-UP: Pre-existing clippy gate failure unrelated to copy-chronology — 27 disallowed std::env::set_var/remove_var errors in bead/cli, bead/touch, macro_catalog remain after fix; zero overlap with changed collision/lib/prelude/binding files; already tracked by medium ready CI task bob-cli-dh (identical 27 on clean base 83b010dd per prior triage)

[2026-10-28T09:17:26Z · bob-cli-df.2.1.4.3.1] copy-chronology repair verified in sase-core @f4bf6074: occurrence-level ancestry elimination in collision/mod.rs (selection_pool/select_winner/pairwise_basis use surviving histories; same-commit instant conflict validation added). 6 new regression tests (permutations/root-labels, 3-payload, interleaved duplicates, same-commit tie+conflict, equal instants) plus retained opposite-ancestry case; PyO3 round-trip extended for copy-chronology. Import cleanup done (lib.rs root and prelude core_* collision/quarantine facades removed; artifact_links binding uses sase_core::artifact_link imports; binding names preserved). Focused suites green: just test -p sase_core artifact_link 152 passed; just test -p sase_core_py artifact_link_collision_bindings_round_trip 1 passed. Governed sase tool run check fails only on 27 pre-existing clippy disallowed-env errors in unrelated bead/macro_catalog files (zero overlap; tracked by bob-cli-dh). No epic-symbols. Uncommitted for host finalizer.

## Dependencies

- **Blocks:** [bob-cli-df.2.1.4.3.2](bob-cli-df.2.1.4.3.2.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.4.3.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.4.3.1/README.md) | [bob-cli-df.2.1.4.3.1](bob-cli-df.2.1.4.3.1.md) | 0 |
