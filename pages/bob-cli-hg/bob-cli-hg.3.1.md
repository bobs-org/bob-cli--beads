# Bead: bob-cli-hg.3.1 — Gmail message model and inert body renderer

[Bead Pages](../README.md) / [bob-cli-hg.3](bob-cli-hg.3.md) / bob-cli-hg.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.3.md) · **Assignee:** `bob-cli-hg.3.1.land`
**Created:** 2026-11-05 13:16:21 EST · **Closed:** 2026-11-05 22:17:25 EST
**Plan:** [202611/gmail\_mail\_body.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_mail_body.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_mail_body.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:6196bea7b81628e40c86c7a4 | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_mail_body.md

<!-- sase:links:end -->

## Description

Complete bob-cli-hg.3 with a pure, tested renderer that preserves readable email content while preventing sender text from becoming active vault syntax.

## Notes

[2026-11-05T20:16:24Z · 18r--code] DISCOVERED ISSUE: On bob-cli HEAD df9178df, just lint fails with denied clippy::derivable_impls at src/native/gmail/body/mime.rs:27, introduced in commit df9178df while modeling the Gmail MIME inventory. The lint report is attached to bob-cli-24 as file:explicit:30cd9d60cfa6efcdb1acf197. This falls within the active Gmail renderer scope.

[2026-11-06T02:21:11Z · bob-cli-hg.3.1.land] LANDING FOLLOW-UP TRIAGE (all six PROPOSED FOLLOW-UP entries reviewed before the remaining-work tale): Used sase_new_task, read lifecycle/size guidance, searched all-status CI and all-type candidates, swept all task beads from the last week, and inspected all active epic scopes and plausible owner phases. Outcomes:
1. bob-cli-hg.3.1.1 note #1, four unchanged-base formatter failures: declined a new task and did not corroborate bob-cli-24 because cargo fmt --all -- --check now passes on 6ea08f74 after removing all temporary probes. The four named files were subsequently changed/formatted by 5235d292; the original missing-config root cause in bob-cli-24 is not a current reproduction.
2. bob-cli-hg.3.1.2 note #1, capture-parse CLI reference drift: declined a new task because bac41b5b updated the generated reference from grammar 14 to 15. Independently decoded the entire current Rust long_about string and verified those exact bytes occur in docs/reference/cli/capture-parse.md. This resolves the cited source/reference mismatch; no claim that the entire CLI/doc suite was rerun.
3. bob-cli-hg.3.1.3 note #1 and the duplicate clipboard subset of bob-cli-hg.3.1.4 note #2: corroborated existing CI task bob-cli-hp with one +1. Both exact lib tests independently fail on 6ea08f74: public_leaves_are_entries_or_excluded reports clipboard in both lists; every_table_entry_matches_the_tree reports duplicate clipboard:count. No new task and no causally responsible active epic (bob-cli-he is closed).
4. bob-cli-hg.3.1.4 note #1, unused TODAY: attached DISCOVERED ISSUE to active bob-cli-hl. Its phase .2 commit 53c1d1ad introduced tests/cli/capture/merge_in.rs:8; current file still has no TODAY use. Retained the proposing child's clean-base lint reproduction. No separate task because the active merge-in epic owns the cause.
5. bob-cli-hg.3.1.4 note #2, root help and CLI catalog count: attached DISCOVERED ISSUE to active outer bob-cli-hg. Shell phase .4 / 88907074 added Gmail root help and catalog entry 73, while both root snapshots omit gmail and tests/cli/catalog.rs:42 still expects 72. No separate task; outer Gmail integration owns this sibling-phase regression.
6. bob-cli-hg.3.1.4 note #3, broken merge-in docs fragment: attached DISCOVERED ISSUE to active bob-cli-hl with item 4. Its .1 / d9e35359 introduced the heading and links; current links still use #merging-tasks-into-a-new-task-with. Retained the child's clean-base lychee reproduction. No separate task because that active epic owns the cause.
All proposal outcomes are recorded here for the repair coder to carry into the eventual close note. The renderer defects found by this landing are epic work and are intentionally not filed as follow-up tasks.

[2026-11-06T02:22:10Z · bob-cli-hg.3.1.land] LANDING REVIEW at 6ea08f74: reviewed this epic note, all four phase scopes and all ten child notes (six PROPOSED FOLLOW-UP entries), original child plan and outer plan sections 4.4/5.3, and actual source for model/MIME/inert/HTML/plain/selection. Reviewed epic commits df9178df, 1cbe9703, 540f3e6f, 45118e1b and all 28 non-child commits since the first one; refreshed origin/master and found no extra base commits. The accepted full-body/subject+who/no-memory decisions were honored. MimeInventory Default denial from this epic note is resolved in 06d6c32e (the actual landed fix), confirmed in source.
NOT COMPLETE: eight synthetic expected-correctness probes fail on existing code: remote image reconstruction from ! plus a trusted link; raw [[forged]] inside a permitted URL destination; attached RFC822 child text replacing main body; a later empty candidate suppressing a readable earlier candidate; quote-only HTML discarded; article URL lost in bulletin layout table; new inline plain reply folded after On-wrote; Outlook divRplyFwdMsg id alone not recognized. Eight failures, one passing split-field probe (that scanner observes bracketed fields only); no broad safety claim inferred from that pass. Existing cargo test --lib native::gmail:: -- --skip landing_audit passes all 77. Reproduction module and output are preserved in file:explicit:6196bea7b81628e40c86c7a4; temporary probe source was removed and tracked code restored exactly. cargo fmt --all -- --check passes. No full just check pass is claimed in this planning turn.
Integration remaining: fe120a1e and 88907074 landed shared Google plumbing/Gmail shell after this epic began. gog::thread_get strips the envelope and returns Value, incompatible with the typed envelope parser as a direct consumer; connect it to the model. The transport also duplicates base64 decoding despite the new dependency. No mail-note/save/search implementation has landed in this checkout, so there is no existing downstream renderer to retrofit. Other capture/freshness/period commits have no renderer consumption edge; unrelated regressions were triaged separately in the preceding note.
Both sase bead epic-symbols bob-cli-hg.3.1 and bob-cli-hg.3 report no entries; this Justfile has no symvision recipe. Kept the epic and parent phase open. A validated medium tale, sase_plan_gmail_renderer_landing.md, plans only the concrete renderer repairs and transport integration. Its final step owns normal closure of bob-cli-hg.3.1, marking plan:202611/gmail_mail_body.md done, and normal closure of parent phase bob-cli-hg.3; the outer bob-cli-hg remains for its waiting land agent. The tale must rerun changed-file just check, never check-full, and must not wait for its own future commit/push/CI before closeout.

[2026-11-06T03:17:25Z · bob-cli-hg.3.1.land] Landing repairs complete. Original scope: typed gog thread model, inert serializer, HTML rendering with quote/signature folding, pure render_message with bulletin/snippet/draft handling, acceptance corpus. Repairs: inert composition edges (bang+link image, split ::/%%/$$/backticks, hidden-node rejoins, wikilink-destination refusal preserving query/fragment/mailto/IPv6); attachment subtrees opaque (RFC822/named multipart, CID namespace, stable order); selection iterates last-to-first to first usable (quote-only/signature-only preserved, full-segment normalized comparison, explicit link/table/image structure, no pipe inference); HTML tables keep structured inlines/links/cell boundaries without truncation, bulletin text+links, quote/signature preserved through tables/lists, Outlook id divRplyFwdMsg; plain splits quoted runs vs Outlook tails (inline replies stay main) with exact '-- ' delimiter; gog thread_get returns typed GmailThread via original bytes, strict base64 (standard/url-safe padded/unpadded) with body-free failures, fetched bytes hydrate without re-decode, allowances re-keyed to outer consumers. Verification: 96 gmail lib tests pass (77 prior + new regression for all 8 probes and split/percent/math/code/backslash/hidden, nested RFC822/CID, quote-only/signature-only/empty-trailing/equal-main/punctuation, table links/wrapped quotes/id-only divider/extra cells, inline replies/signature-before-history/Outlook headers, typed transport+hydration+redaction). just check stops on unrelated pre-existing clippy failures (capture/task/attachments, triaged by lander); gmail-focused clippy clean, cargo fmt clean. Follow-up disposition (from lander note #2, all six PROPOSED FOLLOW-UP reviewed, no new tasks for renderer): (1) formatter drift declined (fmt passes, 5235d292); (2) capture-parse drift declined (bac41b5b, bytes verified); (3) clipboard duplicates +1 to bob-cli-hp; (4) unused TODAY to bob-cli-hl; (5) root help/catalog count to outer bob-cli-hg; (6) merge-in docs fragment to bob-cli-hl. Renderer defects were epic work, not follow-ups.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.3.1.land.md) | [bob-cli-hg.3.1](bob-cli-hg.3.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`232e94b`](https://github.com/bobs-org/bob-cli/commit/232e94bbf507e17b31790d434f4288ff31adbae6) | feat(gmail): repair renderer landing and finish hg.3.1 | [bob-cli-hg.3.1](bob-cli-hg.3.1.md) | 2026-11-05 22:20:04 EST |
| bob-cli--plans | [`bob-cli--plans@6e63268`](https://github.com/bobs-org/bob-cli--plans/commit/6e63268021e9c4abaef71269304926ff313cd40e) | docs(plans): mark gmail\_mail\_body done | [bob-cli-hg.3.1](bob-cli-hg.3.1.md) | 2026-11-05 22:21:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.3.1.1][1] | Need the governing epic decisions and plan context for this phase | 2 |
| read-by | [agent:bob-cli-hg.3.1.2][2] | Need parent epic DECISIONS and child phase scope | 2 |
| read-by | [agent:bob-cli-hg.3.1.3][3] | Need governing decisions and scope for this phase | 1 |
| read-by | [agent:bob-cli-hg.3.1.4][4] | parent epic scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.4/README.md

<!-- sase:referenced-by:end -->
