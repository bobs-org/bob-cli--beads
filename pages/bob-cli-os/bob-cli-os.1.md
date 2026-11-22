# Bead: bob-cli-os.1 — General capture fixes the audit exposed

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.1` · **Size:** medium
**Created:** 2026-11-21 14:59:41 EST · **Closed:** 2026-11-21 16:23:21 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

clean_capture: reject base62 ids as URL stems, persist the write-once source store on the ingest path, and print the recorded URL (not the post-redirect URL) in web PDF mastheads.

## Notes

[2026-11-21T21:23:03Z · bob-cli-os.1] PROPOSED FOLLOW-UP: just docs-check fails on the clean base (HEAD dfe20ca3) — docs/reference/plugins/bob-ledger-tools.md 6042 words and bob-navigation-hotkeys.md 6307 words exceed the 6000-word reference cap; both are mounted bob-plugins docs, already tracked by bob-cli-ob (nav hotkeys) and noted on bob-cli-oo (ledger tools). clean_capture touched neither page.

[2026-11-21T21:23:21Z · bob-cli-os.1] clean_capture done. (1) clip_url::is_opaque_segment adds a base62-id test (>=16 ASCII alnum, digit+upper+lower, mean token len <2.5 over letter/digit + CamelCase splits); unit tests cover 4UgVFWty2I8hGAgSvT7pjC (opaque), iPhone15ProMaxReview / DeepSeekV3TechnicalReport / GPT4oSystemCard (not), and 2000 seeded random 22-char ids (>=90% opaque, ~94% expected per the plan's rule; every opaque one yields no URL stem). (2) ingest_article_route calls new web_source::persist_article_store_quiet after install (no stdout/stderr; warnings via progress through new source_store::write_for_create_reporting) and threads the verified pointer into apply_intake's expected_source_pointer. Tests: jobs.rs filed article has source_markdown, store committed, bob ref links lists the link, worker prints no store lines; jobs.rs queued article store is adopted by bob ref scan; gkeep_pull.rs JSON pull files note with source_markdown, bob ref links works, and pull JSON is identical with and without a store. (3) Adapter article.json: source_url = request url, new base_url = post-redirect URL; renderer link_base_url() used only for resolve_relative_hrefs (source view, collection source, prepare_part); response final_url unchanged. Self-test: browserless redirected single/collection checks plus a browser-backed landed capture (fixture hook landings via history.replaceState, since fulfilled 3xx bypasses the route); a mutation run reverting the adapter fails both redirect checks. (4) docs/highlights-create.md Ingest boundary + Saved Markdown, docs/highlights-clip.md masthead URL. Gates: cargo fmt check, clippy gate, cargo test --workspace --no-fail-fast all green; just check-web-clip-adapter ok (headed check skipped, no Xvfb); just docs-check fails only on pre-existing plugin reference budgets that reproduce on the clean base (follow-up noted).

## Dependencies

- **Blocks:** [bob-cli-os.4](bob-cli-os.4.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.1/README.md) | [bob-cli-os.1](bob-cli-os.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0114a6c`](https://github.com/bobs-org/bob-cli/commit/0114a6cc1e560df93de50edaa8821db627055702) | fix(ref): keep base62 ids out of stems, save ingest source stores, and print the recorded URL in mastheads | [bob-cli-os.1](bob-cli-os.1.md) | 2026-11-21 16:24:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-os.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-os.10][2] | Check sibling phase status and any follow-up notes relevant to rollout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.10/README.md

<!-- sase:referenced-by:end -->
