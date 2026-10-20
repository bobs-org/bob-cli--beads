# Bead: bob-cli-a0.7.1 — Bob hand-written product reference

[Bead Pages](../README.md) / [bob-cli-a0.7](bob-cli-a0.7.md) / bob-cli-a0.7.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.md) · **Assignee:** `bob-cli-a0.7.1.land`
**Created:** 2026-10-19 23:14:29 EDT
**Plan:** [202610/product\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/product_reference.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/product_reference.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/product_reference.md

<!-- sase:links:end -->

## Description

Readers can look up capture syntax, vault structure, configuration, and machine outputs in four verified reference pages, with complete token search coverage and an environment-variable drift guard, completing bob-cli-a0.7.

## Notes

[2026-10-20T03:59:32Z · bob-cli-a0.7.1.land] LANDING AUDIT at f30389c7: Read this epic, all three children and every note, the approved product_reference and parent docs plans, and required research. Reviewed implementation commits 5d3ad7d0 (configuration/guard), 6f6841b5 (capture/vault), f30389c7 (JSON/integration) against current docs and source. All child statuses are closed, but completion claims have gaps: JSON catalog omits ref scan, misdescribes ref today as a listing and all capture helpers as read-only, overgeneralizes ok/error envelopes (vault-sync status has neither), and omits ref show Markdown. Capture reference omits examples for many indexed operations despite the plan; token test checks locations only, never literal queries. Configuration installation prose implies running bare plugins sync in any checkout selects that checkout, contrary to the foreign-checkout guard and explicit --repo resolution. Environment scanner _matching/_skip_item compare token values without requiring punctuation: #[cfg(test)] fn t() { let _ = "{"; } fn p() { let _ = "BOB_PRODUCTION"; } hides the production name; a literal "}" leaks subsequent test names. Reproduced both plus raw-string variant. Existing 65 environment/token/lint tests pass in 22.60s; current guard inventories 51 names with no findings. No broad check or check-full run. Remaining work belongs to this epic and will be proposed as one medium tale with same-turn epic and parent-phase closeout.

[2026-10-20T03:59:47Z · bob-cli-a0.7.1.land] INTEGRATION AND FOLLOW-UP TRIAGE: Every child note was reviewed; there are zero PROPOSED FOLLOW-UP entries on bob-cli-a0.7.1.1, .2, or .3, so no new-task triage, duplicate corroboration, or declined proposal is outstanding. All newly found issues were introduced by this epic and stay in its remaining-work tale; none is deferred as a separate task. Since this epic started, non-epic commits f3678291 (source-owned mounted hubs), d18b45de (publication source planner), and 7751f505 (executable tutorial/demo/sandbox) landed. Their nav and lint/check additions coexist, mounts remain empty, and the Rust-only environment guard intentionally does not inventory Python docs-tool variables. Reuse the new sandbox/demo for reference verification and cross-link the tutorial and reference pages. Fetch confirmed HEAD equals origin/master. Final MIT/indexable/published-decisions choices are preserved; no memory or product behavior changes. epic-symbols checks for bob-cli-a0.7.1 and bob-cli-a0.7 both report none; no symvision recipe exists in the current justfile. Epic and parent phase intentionally remain open pending the tale.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.1.land.md) | [bob-cli-a0.7.1](bob-cli-a0.7.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.7.1.2--1][1] | Need epic decisions governing this phase | 1 |
| read-by | [agent:bob-cli-a0.7.1.3][2] | Need epic DECISIONS and scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.7.1.3/README.md

<!-- sase:referenced-by:end -->
