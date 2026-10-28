# Bead: bob-cli-df.2.1.4.3 — Finish collision provenance and quarantine path safety

[Bead Pages](../README.md) / [bob-cli-df.2.1.4](bob-cli-df.2.1.4.md) / bob-cli-df.2.1.4.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2.1.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.1.4.land.md) · **Assignee:** `bob-cli-df.2.1.4.3.land`
**Created:** 2026-10-28 04:35:24 EDT · **Closed:** 2026-10-28 10:34:44 EDT
**Plan:** [202610/artifact\_link\_provenance\_closeout.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_provenance_closeout.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/artifact_link_provenance_closeout.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:0bb00b945d1059bc24e04ae8 | attached via sase artifact create --bead |
| related | file:explicit:2e6b68e6e526d103d9c39738 | attached via sase artifact create --bead |
| related | file:explicit:65cfd4bea965ad1e3eef0b63 | attached via sase artifact create --bead |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_provenance_closeout.md

<!-- sase:links:end -->

## Description

Preserve earliest durability across copied histories and prove quarantine recovery without accepting unsafe paths.

## Notes

[2026-10-28T10:55:12Z · bob-cli-df.2.1.4.3.land] LAND AUDIT / FOLLOW-UP TRIAGE: read this epic (no discretionary DECISIONS), both children and every note, governing ancestor plans, parent landing findings, source commits core 00fe29d5 and SASE 49ebcc5eba. Clean Python checkout fast-forwarded to 49ebcc5eba; both tips equal fetched origin/master; pin is exact 00fe29d5. Non-epic post-start commit 95bd848d26 is Footprint derived-source/backfill (committer timestamp 04:55 EDT), no competing artifact-link reducer; preserve sibling 1b1162b313 inlet rollback. Original requested copy/import/history/recovery work is present, but remaining epic defects reproduced: same-payload descendant with skewed clock replaces its own ancestor in best_surviving_instant (A a0 12:00, A a1 descends a0 at 10:00, independent B 11:00: chooses A, expected B); actual history adapter supplies this evidence for two nested store roots in one full repo. Actual loader silently ignores regular-file or broken-symlink operation directories; actual persistence creates a temp record outside root via unchecked .staging symlink. Probe refs file:explicit:2e6b68e6e526d103d9c39738 and file:explicit:0bb00b945d1059bc24e04ae8 document bounded methods (minimal Rust structs/integer instants; path probe stubs wire validation), not full feature tests. FOLLOW-UP OUTCOMES via sase_new_task: .3.1 #1 corroborated bob-cli-dh; .3.2 #3 corroborated bob-cli-dg using phase-reported clean-base run c22e8134aaf51624cc76b121e7e284db; .3.2 #4 supplemented causal B4 bob-cli-df DISCOVERED ISSUE for _RecoveryAssessment witness 13ea2a464abef73b3eab4bfee9e624d7. No new tasks or newly declined proposals; earlier stale Footprint decline and bob-cli-di installer ownership stand. No production changes or fresh full-gate pass; current external Python venv absent and exact Python3.12 wheel-cache lookup missed. All .3/.4/.2.1/df.2 epic-symbol audits empty. Remains open; plan only copy-skew and quarantine-path repairs, then resume normal nested landing.

[2026-10-28T10:57:57Z · bob-cli-df.2.1.4.3.land] Detailed landing audit is file:explicit:65cfd4bea965ad1e3eef0b63, with source probes linked there. Authored remaining-work child epic for same-payload ancestry under skew and remaining quarantine operation/staging safety; parent_bead=bob-cli-df.2.1.4.3. Two sequential medium phases are required because Python must pin the new core repair commit and verify that wheel; no coding phase performs ancestor closeout. Validation ran with --explain, missing goal/first dependency fields corrected, then revalidated without --explain to zero errors/warnings. Child land resumes this epic, then df.2.1.4 and df.2.1 readiness/normal closure, and finally only df.2. All current and ancestor plans remain open/wip. No just check or check-full was run in this audit; bounded reproductions are explicitly distinguished from full verification.

[2026-10-28T11:14:53Z · bob-cli-df.2.1.4.3.land] RELAUNCHED LAND (07:05 EDT): the approved remaining-work child plan artifact_link_copy_skew_path_repairs.md never launched. Its gate monitor ran sase bead work in workspace 15, whose store reported parent bob-cli-df.2.1.4.3 missing, so no child bead was created. Rechecked before resuming: sase-core origin/master is still 00fe29d5 and sase origin/master is still 49ebcc5eba (pin 00fe29d5), so there is no drift since the 06:55 audit. Source still shows both defects: occurrence_is_eliminated skips same-digest ancestors, so best_surviving_instant reintroduces a skewed descendant copy; _scan_quarantine_tree drops non-.json filenames before its safety checks; and persist_artifact_link_quarantine_record passes an unvalidated _QUARANTINE_STAGING to the installer. Child notes are unchanged since the audit. All three PROPOSED FOLLOW-UPs keep their recorded outcomes (bob-cli-dh +1 and bob-cli-dg +1 present; the _RecoveryAssessment witness 13ea2a46 is on bob-cli-df). Epic-symbols for .3 are empty. A dry run validated parent bob-cli-df.2.1.4.3 in workspace 10's store. I then resumed the user-approved launch unchanged with --yes-to-all --cl-name gh_bobs-org__bob-cli. It created child epic bob-cli-df.2.1.4.3.3 (phases .3.3.1 and .3.3.2, land .3.3.land) and pushed the graph. The child lander resumes this landing through parent_bead. This epic and its ancestor plans stay open: no close, no force, no done status. Workspace 15's plans clone may still hold an unpushed duplicate archive commit of the same plan.

[2026-10-28T14:34:44Z · bob-cli-df.2.1.4.3.3.land--2] Verified sources/commits: sase a1d1ea04da (base 49ebcc5eba) pins core 49870f00 (core HEAD 65546fd2 contains it); wheel 0.43.0 with artifact_link_collision_partition verified via SASE_CORE_DIR install-venv (w26rka5dpsfb). Repaired provenance (same-payload ancestry shares surviving-history comparator, 49870f00) and path cases (staging+operation checks, 5 IO tests + paths/read-only/recovery modules). Source+wheel checks: 125 focused tests passed (24+51+50); governed check a88473fd only known-independents (symvision witness 13ea2a464..., plans-sidecar run c22e8134). Integration: store copy-skew B-wins one finding, outbox recovery settles once across retry+restart. Follow-ups already recorded: +1 bob-cli-dh, DISCOVERED on bob-cli-df, +1 bob-cli-dg, new bug bob-cli-dn, none declined.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.4.3.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.4.3.land/README.md) | [bob-cli-df.2.1.4.3](bob-cli-df.2.1.4.3.md) | 0 |
