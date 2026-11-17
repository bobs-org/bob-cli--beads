# Bead: bob-cli-mw.4 — Template slot, morning checklist row, and POST stage

[Bead Pages](../README.md) / [bob-cli-mw](README.md) / bob-cli-mw.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1dq](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1dq.md) · **Assignee:** `bob-cli-mw.4` · **Size:** small
**Created:** 2026-11-17 17:23:40 EST · **Closed:** 2026-11-17 18:15:10 EST
**Plan:** [202611/daily\_headline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/daily_headline.md)

## Description

vault: add the empty `**Headline:**` slot to the daily template, add the concise staged POST row to gtd_daily.md, apply the morning-clause and staging decisions, and verify end to end.

## Notes

[2026-11-17T23:15:10Z · bob-cli-mw.4] Vault phase done and verified. Template: empty **Headline:** slot between nav line and ^gtd row in _templates/daily.md. gtd_daily.md: new POST #headline row 'Write today's headline' ([created 2026-11-17], [scheduled 2026-11-18], same repeat shape) directly above the open Morning review; morning_clause=drop applied to that open occurrence only, completed occurrence keeps the clause as history. stage_headline_row=stage: chezmoi source post_stages [periods]->[periods, headline] committed+pushed (aeaef838), 'chezmoi update -a --force' applied, live ~/.config/bob/config.yml confirmed; apollo/Mac pick it up on next chezmoi update. Verify (fresh bob build from HEAD): BOB_NOW=2026-11-23 freshness POST order is periods(Weekly review) -> headline(stage_rank 1/1) -> unstaged Morning review; scratch-vault 2026-W47 show carries headline in columns+children; capture-pomodoros --tasks headline=display string, empty slot=null, missing note=null, without --tasks key absent; cargo tests week_report_and_brief_carry_day_headlines + agenda_headline_is_display_null_or_omitted pass. Vault-sync auto-committed the vault edits (2659779dd, 31395126c); a later Mac count-only commit (cb5266405, 18->19 blocked) followed with no conflict. No epic-symbols. No real daily notes touched.

## Dependencies

- **Depends on:** [bob-cli-mw.1](bob-cli-mw.1.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mw.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mw.4/README.md) | [bob-cli-mw.4](bob-cli-mw.4.md) | 0 |
