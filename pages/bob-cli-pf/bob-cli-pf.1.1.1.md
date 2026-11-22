# Bead: bob-cli-pf.1.1.1 — Shared created stamp and source-ordered property inventory

[Bead Pages](../README.md) / [bob-cli-pf.1.1](bob-cli-pf.1.1.md) / bob-cli-pf.1.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.md) · **Assignee:** `bob-cli-pf.1.1.1` · **Size:** medium
**Created:** 2026-11-22 14:45:09 EST · **Closed:** 2026-11-22 16:17:17 EST
**Plan:** [202611/card\_foot\_drawer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_foot_drawer.md)

## Description

models: build and test the pure created formatter and complete inventory model, including source order, duplicate diagnostics, grouping, and typed empty values.

## Notes

[2026-11-22T21:16:40Z · bob-cli-pf.1.1.1--6] Verified property-card APIs and behavior:
- propertyCardFormatCreatedStamp({value,present,kind,noteDate,now|clock,timeZone,sourceScalar}) -> {text,tooltip,state,dateOnly}. It distinguishes missing, valid, and invalid values; preserves raw invalid source in the tooltip; keeps date-only values as calendar dates without inventing midnight; formats timestamps and relative age in the viewer time zone; uses record wording "added" versus "created" for other cards; and uses sourceScalar to distinguish YAML dates from timestamps when the parser supplied a Date.
- propertyCardInventory({sourceText,frontmatter,where,nested,legacy,parseYaml,path,sourcePath,cachePath}) -> {state,reason,rows,groups,count,issues,recovery}. It returns top-level keys in source order with source lines and scalar text; keeps duplicate occurrences with diagnostics; applies explicit where marks ahead of managed grouping; preserves absent, null, empty string/list, false, and zero as distinct value states; and returns pending for unavailable or mismatched source/cache. Malformed or unclosed YAML returns no value rows and the recovery hint.

Evidence: focused property-card and related ownership/title suites passed 162/162. The event-link-times and frees-marks suites passed 40/40 when run serially; their measured builds were 13.4 ms and 23.1 ms against 25 ms budgets. The phase npm test run repeated twice with 8686 passing and 2 timing failures each: event-link-times at 106.2 ms and frees-marks at 170 ms. Clean base 394633fb instead had the frees-marks timing miss at 54 ms and taskLinks typed-keystroke p95 at 12.0 ms; all 17 perf tests passed on the phase run. The changed files do not include either timing test or its implementation, and neither failure reproduced serially. No code change was warranted. Deploy evidence: bob plugins sync --repo "$PWD" --no-pull -p bob-ledger-tools reported "up to date" (0 copied, 0 skipped, 3 unchanged).

[2026-11-22T21:17:17Z · bob-cli-pf.1.1.1--6] Closed with verified evidence: focused property-card and related ownership/title suites passed 162/162; serial event-link-times and frees-marks suites passed 40/40 at 13.4 ms and 23.1 ms against 25 ms budgets. Full npm test repeated twice failed only on those timing checks under suite load (106.2 ms and 170 ms); clean base also had timing misses, and neither reproduced serially. The property-card APIs and detailed behavior are recorded in the preceding attributed phase note. bob plugins sync --repo "$PWD" --no-pull -p bob-ledger-tools reported up to date (0 copied, 0 skipped, 3 unchanged). sase bead epic-symbols returned no entries.

## Dependencies

- **Blocks:** [bob-cli-pf.1.1.2](bob-cli-pf.1.1.2.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.1.1.md) | [bob-cli-pf.1.1.1](bob-cli-pf.1.1.1.md) | 0 |
