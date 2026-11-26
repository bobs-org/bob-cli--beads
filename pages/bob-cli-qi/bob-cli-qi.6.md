# Bead: bob-cli-qi.6 — Passive-rendering proof, docs sweep, approved memory, and clean deploy

[Bead Pages](../README.md) / [bob-cli-qi](README.md) / bob-cli-qi.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gn.md) · **Assignee:** `bob-cli-qi.6` · **Size:** medium
**Created:** 2026-11-26 10:06:13 EST
**Plan:** [202611/bank\_hub\_demotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md)

## Description

finish: add the unit proof that folds and refreshes never write the vault or spawn bob from paint, and sweep the bob-plugins and bob-cli docs onto the single-owner card contract. Apply only the memory decisions answered yes, then deploy cleanly from master with the isolated post-sync smoke check.

## Notes

[2026-11-26T18:43:34Z · bob-cli-qi.6] PROPOSED FOLLOW-UP: Fix the clean-base docs-check home-path privacy false positive — npm run docs:check uses bob-cli master at 3659edc and fails at docs/snooze.md:281 on /home/bryan missing from privacy_baseline.txt; plugin docs lint and word budget pass.

## Dependencies

- **Depends on:** [bob-cli-qi.4](bob-cli-qi.4.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qi.5](bob-cli-qi.5.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qi.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qi.6.md) | [bob-cli-qi.6](bob-cli-qi.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c89ba1d`](https://github.com/bobs-org/bob-cli/commit/c89ba1d4c49775b1840c065f0f31d262e60930ac) | docs(bank): establish path-canonical single-owner hub | [bob-cli-qi.6](bob-cli-qi.6.md) | 2026-11-26 13:57:29 EST |
| bob-plugins | [`bob-plugins@17a0567`](https://github.com/bobs-org/bob-plugins/commit/17a0567013d75cecd1f8c9751993864151cf524e) | docs(props): document home-card ownership and passive rendering | [bob-cli-qi.6](bob-cli-qi.6.md) | 2026-11-26 14:21:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.6k.cld][1] | Check qi.6 dependencies for card sequencing | 2 |
| read-by | [agent:research.6k.gem][2] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |
| read-by | [agent:research.6l.gem][3] | Check live progress of active property-card and prose epics for parallelization analysis | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6k.cld/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6k.gem/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
