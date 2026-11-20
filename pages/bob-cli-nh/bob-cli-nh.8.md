# Bead: bob-cli-nh.8 — Adopt in the vault and chezmoi

[Bead Pages](../README.md) / [bob-cli-nh](README.md) / bob-cli-nh.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ef](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ef.md) · **Assignee:** `bob-cli-nh.8` · **Size:** medium
**Created:** 2026-11-19 09:35:22 EST · **Closed:** 2026-11-20 10:34:57 EST
**Plan:** [202611/period\_intentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_intentions.md)

## Description

adopt: install the new bob, then dry-run and apply `bob periods migrate` on the live vault and refresh callouts. Drop the daily template's Headline line. Replace the `#post #headline` GTD row and add the PRE Summarize yesterday and POST Reflect on yesterday rows. Set `post_stages`, add types.json entries, and add the day.md and vault AGENTS.md pointers. Verify, then record the follow-ups.

## Notes

[2026-11-19T14:58:57Z · research.5g.linker.w0] COPY CHIP: when you add the Summarize yesterday row to gtd_daily.md, write its agent prompt as a copy chip, not a double-quoted string. The exact Markdown and rules are in the COPY CHIP note on the epic bead bob-cli-nh (read it with sase bead read bob-cli-nh). Keep existing copy chips intact when rewording the other review rows.

[2026-11-20T15:33:24Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Retire the intentions legacy fallback readers after one release — src/native/intentions/legacy.rs fallbacks (daily Headline/Reflection preamble, week Intentions, quarter Outcomes, year Theme/Outcomes, period ## Reflection, Review opener) plus daily_headline.rs parsing; the live vault migrated on 2026-11-20 (vault commits b52e6eb07, db9299154) and `bob periods list -p` reports zero legacy_period_text.

[2026-11-20T15:33:36Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Retire the period [!agent] callouts in favor of brief-carried instructions — every `bob periods brief` already prints its instructions first (v3), so the folded callouts in week/quarter/year notes are a second copy; remove them from scaffolds and add a migrate/ensure step to strip them.

[2026-11-20T15:33:41Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Bob Mac Capture intentions panel (bob.md ^current-intentions) — show the current day/week intentions from the additive capture/periods JSON in the Mac capture app; that bob.md task is Blocked on ^intentions, which this epic delivers.

[2026-11-20T15:33:47Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Optional per-intention ✓/◐/✗ marks — let Bryan mark each intention met/partly/missed in the intention card editor (stored alongside intentions, never graded by agents).

[2026-11-20T15:33:52Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Optional capture sigil to append an intention — a capture grammar form that appends one line to today's (or a named period's) intentions through `bob periods update`, so intentions can be set from Bob Mac Capture.

[2026-11-20T15:33:58Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Optional ghost on today's empty note — the intention card shows nothing when a note has none of the three fields; consider a quiet "＋ set today's intentions  o" ghost on today's daily note only.

[2026-11-20T15:34:14Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Legacy period section reader drops fenced lines — intentions::legacy::sections() skips fenced lines when collecting a section body, so a `## Reflection` (or Theme) holding a code fence migrates without the fence and the section is then removed (text loss); the problems collector likewise sees a fence-only slot as empty. Include fenced lines in section bodies (migrate already keeps fence-only slots after nh.8). No live note hit this on 2026-11-20.

[2026-11-20T15:34:21Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Future period notes past migrate's range keep legacy slots — 2027.md, 2027-Q1, 2027-W01, W02 (Mac-created old scaffolds) were outside the default range (ISO-year start through next week), so adoption needed `BOB_NOW=2027-01-04T09:00:00 bob periods migrate -a -o -s 2027-01-04`. Consider having migrate cover existing period notes after the range end, or ensure strip empty legacy slots, so `legacy_period_text` cannot strand on future scaffolds.

[2026-11-20T15:34:27Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: `bob periods migrate` dry-run sample_diff is not a real diff — the human/JSON sample daily diff interleaves -/+ lines positionally (every line after the insertion shows as removed and re-added), which makes the planned change hard to review; render a unified diff (e.g. with the similar crate) instead.

[2026-11-20T15:34:33Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: Clean-base check failures seen while verifying nh.8 (not caused by it): (1) just check lib failures catalog public_leaves_are_entries_or_excluded, completion every_value_arg_has_a_decision, periods::update planning_applies_ordered_intention_ops_and_reports_bad_indexes — already on epic bob-cli-nh notes #2/#3/#5 for the land agent; (2) capture_pomodoros_agenda september_shaped_vault_finishes_fast flaked once under full-suite load (449ms) and passed 3/3 alone — tracked by bob-cli-gz; (3) just docs-check URL gate docs/develop/plugins/architecture.md:74 -> /develop/validation/ fails identically on the clean tree — tracked by bob-cli-nv.

[2026-11-20T15:34:39Z · bob-cli-nh.8] PROPOSED FOLLOW-UP: bob-chips is listed but not deployed on athena — applying the chezmoi bob config for post_stages also applied the already-committed chezmoi change b19c116c (plugins.sync bob-copy-chips -> bob-chips); `bob plugins sync -d` now plans bob-chips as new files. The copy-chips adopt work should deploy it (`bob plugins sync -p bob-chips`); until then the Summarize yesterday copy chip in gtd_daily.md renders as inline code. nh.8 did not deploy it because bob-ledger-tools is under another agent's uncommitted deploy (bob-cli_13, 15:02Z).

[2026-11-20T15:34:57Z · bob-cli-nh.8] Adopted on athena 2026-11-20. Installed bob from master; bob periods update/brief yesterday OK; bob-ledger-tools deploy carries the intention card. Fixed a migrate gap in bob-cli (this workspace, committed by finalizer): empty legacy slot headings (## Intentions/Outcomes/Theme/Reflection from old scaffolds) were left behind while list -p counted them as legacy_period_text; migrate now removes blank slots (never past the agent callout/## Archive or inside fences), and daily paragraph removal leaves one blank line. Unit+CLI tests added; docs/periods.md updated; just check green except the 3 known nh.2 lib failures (epic notes #2/#3/#5). Live vault: dry-run reviewed, then migrate -a (b52e6eb07, 56 notes: dailies 18/19/20, W01-W48 Reviews/slots, Q1-Q4, 2026.md), pinned 2027-range migrate for 4 out-of-range 2027 scaffolds (db9299154), ensure -R callouts v3 (4e4713dac); W46 NOT SET placeholder removed by hand. Verified: list -p has 0 legacy_period_text and 0 dangling_period_link (only pre-existing unscaffolded 2024/2025); periods show 2026-W47/yesterday/W46 read intentions, summary, reflection; migrate re-run plans nothing. Template Headline line removed; gtd_daily: #post #headline row replaced in place with Set today's intentions, PRE Summarize yesterday (copy[summary prompt] chip, payload byte-identical) and POST Reflect on yesterday added (created 11-20, scheduled 11-21, reconcile set Blocked), weekly/quarterly/yearly/weekly-PRE rows reworded with chips intact; Bank row left (no surprise lines landed in Reflection). types.json, day.md For agents, vault AGENTS.md pointer added; all vault commits pushed by vault-sync. chezmoi post_stages [periods, intentions] edited and applied to ~/.config/bob/config.yml; bob freshness list shows PRE periods stage and POST Reflect -> Set intentions -> Morning review. apollo and Mac bob already have periods update. Bryan to close bob.md ^intentions and ^daily-summary. Follow-ups recorded as notes.

## Dependencies

- **Depends on:** [bob-cli-nh.4](bob-cli-nh.4.md) ✓ · ⧖ 2026-11-19
- **Depends on:** [bob-cli-nh.5](bob-cli-nh.5.md) ✓ · ⧖ 2026-11-19
- **Depends on:** [bob-cli-nh.7](bob-cli-nh.7.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.8/README.md) | [bob-cli-nh.8](bob-cli-nh.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`46bb654`](https://github.com/bobs-org/bob-cli/commit/46bb654a8eb9cf30c358a4ea4ed8031c18751d9e) | fix(periods): remove empty legacy slots during intentions migrate | [bob-cli-nh.8](bob-cli-nh.8.md) | 2026-11-20 10:36:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.8][1] | Need the phase scope and design file | 1 |
| read-by | [agent:research.5i.gem][2] | Check vault and chezmoi adoption phase for daily/period templates | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.8/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5i.gem/README.md

<!-- sase:referenced-by:end -->
