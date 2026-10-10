# Bead: bob-cli-5y.13 — Migrate the live vault

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.13` · **Size:** medium
**Created:** 2026-10-09 12:29:35 EDT · **Closed:** 2026-10-09 21:22:47 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

live-migration: confirm the Mac runs the new bob, run migrate-tasks against the live vault with the confirmed parent map, reconcile, and verify every invariant.

## Notes

[2026-10-10T01:22:29Z · bob-cli-5y.13] PROPOSED FOLLOW-UP: Add decisions strand ref-tasks-live-with-their-parent recording that ref tasks live with their parent note (skipped per epic decision memory_ref_parent_decision=no)

[2026-10-10T01:22:33Z · bob-cli-5y.13] PROPOSED FOLLOW-UP: Update glossary strands reference-task, reference-note, and area-note for the parent-residence model (skipped per epic decision memory_glossary_ref_terms=no)

[2026-10-10T01:22:36Z · bob-cli-5y.13] PROPOSED FOLLOW-UP: Install new bob (bob-cli @ 091eda9 or later, with migrate-tasks) on the Mac before its next highlights scan; SSH port 22 to kellys-macbook-pro.local timed out so the Mac-side install could not be confirmed, and an old-bob scan may re-insert v1 ^ref trackers next to migrated v2 lines

[2026-10-10T01:22:40Z · bob-cli-5y.13] PROPOSED FOLLOW-UP: Repair athena vault-sync origin reachability (~/.ssh/config is a dangling symlink to Sync/home/.ssh/config so host alias github-bob never resolves; background vault-sync fails at ls-remote; this migration pulled/pushed via a /tmp ssh-config shim with the existing id_bob_vault key)

[2026-10-10T01:22:47Z · bob-cli-5y.13] Live migration done: installed bob from bob-cli @ 091eda9 on athena (binary has migrate-tasks); dry-run showed 3 frontmatter-resolved + 29 unmapped (all carried unresolvable parent [[obsidian_ref]]); built 29-row parent map from vault evidence (wrappers in sase.md/done, Depends-On from sase_blog_0, BLOG/BEADS/SASE-V18/RESEARCH pomodoro links) and confirmed it; migrate-tasks --write moved 32 open ref tasks into 6 notes as commit 9253886, pushed to origin/master. Verified: rerun reports 0 open ref tasks; bob ref doctor result ok (32 live, 0 archived, 0 open v1, parents ok; only pre-existing opaque_url notes + missing sase-listen warn); spot checks show v2 lines (#task #ref, path-qualified link, created, ^ref-slug, no #hide, marks/fresh/id preserved), rewritten Depends-On ids and daily-note links, ref-note managed embeds with parent==residence; remaining ^ref lines are all closed/frozen per J7. Lane pressure as predicted: Next 18/15, Pending 18/10 (caps warn only). Follow-ups recorded on bead (2 skipped memory edits per epic decisions, Mac-side bob install unconfirmed, athena vault-sync alias).

## Dependencies

- **Depends on:** [bob-cli-5y.10](bob-cli-5y.10.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.11](bob-cli-5y.11.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.14](bob-cli-5y.14.md) ◐ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.3](bob-cli-5y.3.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.4](bob-cli-5y.4.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.6](bob-cli-5y.6.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.8](bob-cli-5y.8.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.13/README.md) | [bob-cli-5y.13](bob-cli-5y.13.md) | 0 |
