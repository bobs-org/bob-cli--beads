# Bead: bob-cli-d2.3 — Deploy, verify the hook on both hosts, and backfill two weeks of research references

[Bead Pages](../README.md) / [bob-cli-d2](README.md) / bob-cli-d2.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14o](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14o.md) · **Assignee:** `bob-cli-d2.3` · **Size:** medium
**Created:** 2026-10-27 07:42:24 EDT · **Closed:** 2026-10-27 08:59:25 EDT
**Plan:** [202610/research\_ref\_saved\_markdown.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/research_ref_saved_markdown.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:825f29b45683e48216bdbe70 | attached via sase artifact create --bead |
| related | file:explicit:a6b747946294df16b787c942 | attached via sase artifact create --bead |
| related | file:explicit:f20b1594f834db3006f4bb8c | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

backfill: install the fixed bob on athena and apollo, apply the hook_timeout decision, prove the hook path end to end on both hosts, then adopt orphan stores and attach hook-time Markdown to every research reference the hook matched since 2026-10-12.

## Notes

[2026-10-27T12:59:12Z · bob-cli-d2.3] Phase record (hook_timeout=raise). Artifacts: file:explicit:a6b747946294df16b787c942 (summary), file:explicit:f20b1594f834db3006f4bb8c (json), file:explicit:825f29b45683e48216bdbe70 (attach dry-run).

Deploy: origin/master already had pointer-fix 3a13ec6f (08:04 EDT) and adopt d38bef59 (08:32 EDT). Athena ~/.cargo/bin/bob mtime 08:36 EDT and apollo 12:37 UTC (08:37 EDT) both contain "adopted (saved at create)"; both checkouts clean on d38bef59. No just install needed.

Throwaway-vault create check with installed bob: PASS on athena and apollo. Filed note source_markdown matches the create report; bob ref code report -f json status=available.

Hook config: chezmoi source adds timeout: 300s on the research-highlights entry (command remains bob_research_capture, the current chezmoi wrapper around bob ref create --include-id -N <stable> -P <project>). Live sase file-hook list --json on both hosts: name=research-highlights, command=bob_research_capture, timeout_seconds=300.0, sidecars=[research]. Apollo was behind 027a28b9; fetched and applied 10e9f1d2 (bob_research_capture) then patched live timeout to match this source change. Durable timeout lands with this turn's chezmoi commit.

Inventory since 2026-10-12T00:00:00-04:00, research-highlights, deduped (project, rel_path, commit_sha): 143 (athena 67 dispatched, apollo 76). Before writes: 68 done, 3 adopt, 72 attach, 0 missing. One failed athena run (athena_outage_recovery_and_remote_power, no area or project named tailnet) already has a note; classified attach.

Adopt dry-run: conflict_repair_xlarge_routing and gmail_gog_reauth_apollo_athena adopted (saved at create); machine_load_accounting_transparency skipped (low match 2/3 blocks). Write: vault commit 57afc6b740c0fc0f40f4f12d20cf537c24127932 (2 references). machine_load store bytes are identical to hook-time Markdown at d6dd09cb; PDF sha256 matches the store catalog; 3 mermaid + 3 text blocks, 2/3 matchable text blocks match. Did not loosen thresholds.

Attach hook-time Markdown (72 files from bob-cli/sase/job/tailnet research sidecars at audit commit_sha). Dry-run gate: 17 attached / 55 skipped (76.4% skip, all low match blocks/paragraphs, 0 title mismatch, 0 ambiguous). HEAD fallback: 7/55 differed, 0/7 verified. Wrote the 17 that independently verified: vault commit 85d7924b204eb2e8834d29d4882b6adfd52068a3.

After: 87 done, 1 unresolved adopt, 55 unresolved attach, 0 missing. bob ref doctor: ref sources warn (1 orphan machine_load_accounting_transparency). Sampled both adopted refs and 10 attached: code status available or no_code; links status available or no_links. bob ref code block 1 matches pdftotext for gmail_gog_reauth_apollo_athena, conflict_repair_xlarge_routing, and daily_note_day_strip.

sase bead epic-symbols bob-cli-d2.3: no entries.

[2026-10-27T12:59:17Z · bob-cli-d2.3] PROPOSED FOLLOW-UP: bob-cli-co overlap — this pass attached 17 hook-window refs with exact hook-time pairing (one <stem>.md candidate, 0 ambiguous / 0 title-mismatch skips): bob_colon_command_mode, bob_public_docs_site, capture_similar_tasks_band, daily_note_day_strip, gate_panel_decision_cards, harvest_first_job_application_autofill, linkedin_sase_featured_image, linkedin_sase_role_review, recruiter_outreach_vs_cover_letter, ref_code_block_copy, ref_create_mermaid_figures, ref_create_multi_url_collections, ref_note_annotation_sections, sase_sh_docs_redesign, stranger_alumni_referral_outreach, stripe_hackerrank_assessment_invitation, zero_weight_wait_monitors. If any of those 17 were in co's 47 ambiguous or 35 title-mismatch skips, they are resolved. Remaining 55 hook-window skips are low match (cc.6's 115-class remainder), not co's pairing scope. Evidence: file:explicit:a6b747946294df16b787c942

[2026-10-27T12:59:20Z · bob-cli-d2.3] PROPOSED FOLLOW-UP: 55 hook-window refs still have no source_markdown because exact hook-time Markdown (and HEAD for 7) fails attach-source PDF verification (low match N/M blocks or paragraphs). Plus 1 orphan adopt skip: machine_load_accounting_transparency (store == hook-time bytes, PDF sha matches, low match 2/3 blocks). Do not loosen thresholds; full list in file:explicit:a6b747946294df16b787c942 and dry-run file:explicit:825f29b45683e48216bdbe70. doctor still warns on that one orphan.

[2026-10-27T12:59:25Z · bob-cli-d2.3] Deployed pointer-fix+adopt bob on athena and apollo (already at d38bef59); throwaway-vault create check PASS on both (source_markdown on filed note, ref code available). Hook timeout raised to 300s (sase file-hook list timeout_seconds=300.0, command=bob_research_capture, sidecars=[research] on both hosts). Inventory 143 hook-window refs: adopted 2 (57afc6b74), attached 17 verified hook-time sources (85d7924b2), 87 now have pointers, 0 missing. Recorded 1 adopt skip (machine_load_accounting_transparency, 2/3 blocks) and 55 attach low-match skips; doctor 1 remaining orphan. epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-d2.1](bob-cli-d2.1.md) ✓ · ⧖ 2026-10-27
- **Depends on:** [bob-cli-d2.2](bob-cli-d2.2.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-d2.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-d2.3/README.md) | [bob-cli-d2.3](bob-cli-d2.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@62806ca`](https://github.com/bbugyi200/dotfiles/commit/62806ca3cb5992df2261bc11b53a37bbee3e6712) | feat(sase): raise research-highlights file-hook timeout to 300s | [bob-cli-d2.3](bob-cli-d2.3.md) | 2026-10-27 09:00:50 EDT |
