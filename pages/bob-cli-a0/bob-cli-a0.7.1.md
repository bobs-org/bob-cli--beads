# Bead: bob-cli-a0.7.1 — Bob hand-written product reference

[Bead Pages](../README.md) / [bob-cli-a0.7](bob-cli-a0.7.md) / bob-cli-a0.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.md) · **Assignee:** `bob-cli-a0.7.1.land`
**Created:** 2026-10-19 23:14:29 EDT · **Closed:** 2026-10-20 00:29:30 EDT
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

[2026-10-20T04:29:30Z · bob-cli-a0.7.1.land] Landing tale complete at working tree (host will commit). Children .1/.2/.3 remain closed with one note each and zero PROPOSED FOLLOW-UP entries; no new triage, duplicates, or unrelated tasks. Scanner now requires punctuation tokens for delimiters (string/char `{`/`}`/`(`/`[`/`#`/`;`/`,` cannot hide production names or leak tests); 8 environment tests pass. JSON catalog adds ref scan (success vs hard-error envelopes, --intake-only), corrects ref today as a Pomodoro link (not a listing), names capture-task-id/capture-pomodoro-name writes plus -d, scopes ok/schema_version per family (vault-sync status is a direct StatusRecord), and lists ref show -f markdown / -f table. Plugin install uses --repo "$PWD" with resolution order and foreign-checkout refusal. Capture index examples filled; token coverage requires literal queries at headings; search_smoke grouped spellings added; tutorial related/next links added. mounts.yml still empty so Mac hotkey links stay on the public README. Word budgets: hub 87, capture 5095, vault 2348, config 3117, json 1870. Gates: focused env/token/lint 67 passed; just check 1861 lib tests + integration suites passed; just docs-check all gates (268 pytest passed, 2 skipped, 71 search smoke, tutorial, lychee); just docs-build-material ok. Built HTML has the four reference URLs, named token anchors, #pending/#next, and task-line anatomy. Isolated dry-runs: capture-parse schema 1; ref scan --dry-run hard-error envelope; --intake-only dry-run success with intake_only true; ref today is a link command; plan schema 2. sase bead epic-symbols bob-cli-a0.7.1: none. justfile still has no symvision recipe (none added). MIT/indexable/published-decisions preserved; no memory, Rust product, CLI, docs-move, or sibling edits. Original plan:202610/product_reference.md status set to done. Leave bob-cli-a0 open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.1.land.md) | [bob-cli-a0.7.1](bob-cli-a0.7.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cf7a9e9`](https://github.com/bobs-org/bob-cli/commit/cf7a9e98497c65a98969022616431aefb19c1ee8) | docs(reference): finish product reference landing repairs | [bob-cli-a0.7.1](bob-cli-a0.7.1.md) | 2026-10-20 00:31:48 EDT |
| bob-cli--plans | [`bob-cli--plans@098f7b4`](https://github.com/bobs-org/bob-cli--plans/commit/098f7b4cbe5594019660346b80956b210b89da2b) | chore(plan): mark 202610/product\_reference done | [bob-cli-a0.7.1](bob-cli-a0.7.1.md) | 2026-10-20 00:32:51 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.7.1.2--1][1] | Need epic decisions governing this phase | 1 |
| read-by | [agent:bob-cli-a0.7.1.3][2] | Need epic DECISIONS and scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.7.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.7.1.3/README.md

<!-- sase:referenced-by:end -->
