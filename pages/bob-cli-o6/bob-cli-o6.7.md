# Bead: bob-cli-o6.7 — Glossary updates the reviewer accepted

[Bead Pages](../README.md) / [bob-cli-o6](README.md) / bob-cli-o6.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1eh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1eh.md) · **Assignee:** `bob-cli-o6.7` · **Size:** small
**Created:** 2026-11-20 11:49:17 EST · **Closed:** 2026-11-21 17:21:20 EST
**Plan:** [202611/property\_card\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_title_block.md)

## Description

glossary: apply only the memory decisions answered yes (glossary strands and the optional decision record) so memory matches the shipped cards, then run sase memory init; if every memory decision is no, record that on this bead and change nothing.

## Notes

[2026-11-21T22:21:07Z · bob-cli-o6.7] PROPOSED FOLLOW-UP: just docs-check still fails lint on docs/reference/plugins/bob-navigation-hotkeys.md (6307 words, cap 6000 for reference/) — identical on the clean base tree, not caused by this phase; already tracked by bob-cli-ob (introduced via bob-cli-om). The two unresolved-link warnings from sase memory init are in decisions:capture-sigils-say-where-what-how, tracked by bob-cli-ga.

[2026-11-21T22:21:20Z · bob-cli-o6.7] Applied memory_glossary_cards=yes only; memory_decision_title_block=no, so the decisions web is untouched. glossary:intention-card: keyword is now "Day and Period Card" (slug kept), aliases intentions card + intention card + day card + period card; the nonempty-field mount rule is replaced by shipped behavior: always mounts as the title block (leaf tile, DAY/WEEK/QUARTER/YEAR kicker, path-computed title, temporal accent), docked rail with period child chips, content-gated bands, ＋ Set intentions ghost on current/future subjects, fail-open including body fallback without title ownership. glossary:property-card: names album, record, day, period, and bank cards; the kit owns the title block (species tile + kicker, one visible title, render-time hide with Live Preview reveal, title ownership separate from row ownership, bank shows its badge without owning the title). glossary:record-card: title-slot verdict was GO (bob-cli-o6.1 note #1), so it now paints in the title slot above Properties; the title-hide sentence is corrected to follow title ownership, not row hide-eligibility; the rail docks inside the card. Checked against shipped docs (docs/reference/plugins/intention-card.md, record-card.md, albums.md, docs/develop/plugins/architecture.md). Ran sase memory init --no-commit (AGENTS.md, CLAUDE.md, memory README, glossary roster regenerated) and just docs-gen (docs/reference/glossary.md regenerated; second gen is idempotent). bob-docs build --strict passes, bob-docs links passes (0 errors), lint has only the pre-existing nav-hotkeys budget error (same on clean base, bob-cli-ob). No Rust or test files touched; no epic symbols.

## Dependencies

- **Depends on:** [bob-cli-o6.6](bob-cli-o6.6.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.7/README.md) | [bob-cli-o6.7](bob-cli-o6.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ff84542`](https://github.com/bobs-org/bob-cli/commit/ff84542431857364408e9f63c6174d48e2d2c7fb) | docs(glossary): describe property cards as the note title block | [bob-cli-o6.7](bob-cli-o6.7.md) | 2026-11-21 17:22:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.7][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-oj.5.1.1][2] | Check open o6 phases for fragment coordination before editing 240g/styles.css | 1 |
| read-by | [agent:bob-cli-oj.5.1.2][3] | Coordination precondition: which o6 phases are open and which fragments they touch | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][4] | bob-cli-o6 precondition: check open phases editing fragments I will touch | 1 |
| read-by | [agent:bob-cli-oj.5.1.4][5] | Coordination precondition: which o6 phases are open and which fragments they touch | 1 |
| read-by | [agent:bob-cli-oj.6][6] | Need o6 child phase statuses to avoid editing fragments an open o6 phase is changing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md

<!-- sase:referenced-by:end -->
