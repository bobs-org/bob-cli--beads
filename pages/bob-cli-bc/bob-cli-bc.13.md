# Bead: bob-cli-bc.13 — Decision records, glossary, and end-to-end acceptance

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.13` · **Size:** medium
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 15:34:58 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

records: write the glossary strand and decision records from what shipped, reconcile docs, and run the cross-surface acceptance.

## Notes

[2026-10-24T19:34:43Z · bob-cli-bc.13] PROPOSED FOLLOW-UP: Reconcile the clean-base completion failures already tracked by bob-cli-bc.7 note #1 and the epic notes: native::completion::kinds::tests::every_value_arg_has_a_decision, completion::bash::bash_strips_every_wordbreak_not_just_colon, completion::capture_text::named_start_after_inline_close_keeps_prefix, completion::capture_text::named_start_completes_after_hash, and help_options::capture_complete_help_lists_options_alphabetically all reproduced on unchanged source at HEAD bb52dd0. The two related-query performance gates failed only in the broad run and passed in isolation. No source or tests changed in this phase.

[2026-10-24T19:34:58Z · bob-cli-bc.13] Completed docs and cross-surface acceptance: removed all stale planned markers from docs/pomodoro-themes.md; updated the Pomodoro Theme and Mac Pom glossary strands and regenerated docs/reference/glossary.md; verified the four authorized theme decision records were already present; added links from the Mac Capture protocol and plugin docs to the shared contract; copied the expanded vectors byte-for-byte into bob-plugins and synced it (runtime files unchanged). Root, Mac, and plugin docs checks passed; Rust theme/completion tests passed 26/26; JS theme/picker/manager tests passed 71/71; live read-only theme and Stats reports agreed on BOB, JOB, BLOG, and GTD. PT3 p95 evidence from bob-cli-bc.4 note #6 is capture-complete 41.460 ms vs 41.553 ms base and capture-parse 19.496 ms vs 19.541 ms base; bob-cli-bc.5 note #1 also records capture-parse +4.534 ms p95 vs base, within budget. Full just check remains red on the unchanged-source clean-base failures proposed in note #1 plus two related-query timing failures that passed in isolation. epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-bc.11](bob-cli-bc.11.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.12](bob-cli-bc.12.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.8](bob-cli-bc.8.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.13/README.md) | [bob-cli-bc.13](bob-cli-bc.13.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7e41788`](https://github.com/bobs-org/bob-cli/commit/7e41788c090b8321ef914b7f245edfa6a9503fa5) | docs(themes): reconcile Pomodoro theme contract and glossary | [bob-cli-bc.13](bob-cli-bc.13.md) | 2026-10-24 15:36:18 EDT |
| bob-mac-capture | [`bob-mac-capture@fbea724`](https://github.com/bobs-org/bob-mac-capture/commit/fbea724ff3733153e6e76b6c6731dc949c6d4783) | docs(mac-capture): link Pomodoro themes contract | [bob-cli-bc.13](bob-cli-bc.13.md) | 2026-10-24 15:37:59 EDT |
| bob-plugins | [`bob-plugins@d3ea6bb`](https://github.com/bobs-org/bob-plugins/commit/d3ea6bb8e4c8937a42ff93bbda580d9f9192085c) | test(themes): sync plugin vectors with bob-cli | [bob-cli-bc.13](bob-cli-bc.13.md) | 2026-10-24 15:38:49 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Identify the existing owner and task evidence for clean-base just check failures | 1 |
| read-by | [agent:bob-cli-bc.13][2] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-bj.6][3] | Identify clean-base failures from the canonical check | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.6.5.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.13/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.6/README.md

<!-- sase:referenced-by:end -->
