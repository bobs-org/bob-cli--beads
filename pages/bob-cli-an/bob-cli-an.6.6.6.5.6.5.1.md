# Bead: bob-cli-an.6.6.6.5.6.5.1 — Normalize equivalent URL path spellings without merging distinct resources

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5](bob-cli-an.6.6.6.5.6.5.md) / bob-cli-an.6.6.6.5.6.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.land--2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.1` · **Size:** medium
**Created:** 2026-10-24 12:31:54 EDT · **Closed:** 2026-10-24 12:54:40 EDT
**Plan:** [202610/backlog\_batch7\_url\_identity\_gist\_metadata\_close\_summary\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch7_url_identity_gist_metadata_close_summary_mac_ci.md)

## Description

url-identity: resolve bob-cli-7u in shared reference dedupe keys and verify lookup, duplicate detection, and collection consumers.

## Notes

[2026-10-24T16:54:11Z · bob-cli-an.6.6.6.5.6.5.1] url-identity baseline: at ae3a432b dedupe_key_for appended url.path() verbatim, so the Medium @edominguez.se and %40edominguez.se spellings produced two identity keys; ref find missed the twin and capture dedupe allowed double capture. New clip_url test failed pre-fix with left "https://medium.com/@..." vs right "https://medium.com/%40..." (authentic failure observed).

[2026-10-24T16:54:16Z · bob-cli-an.6.6.6.5.6.5.1] url-identity fix: normalize_path_escapes in src/native/highlights_ref/clip_url.rs used by dedupe_key_for. Decodes RFC 3986 unreserved bytes plus explicit @ (the verified Medium twin); retains all other escapes with uppercase hex; single left-to-right pass so %2540 never collapses to @; malformed % sequences pass through. Trim of trailing slash happens before normalization so retained %2F is never treated as a separator. Stored source_url/cleaned output unchanged; all consumers (ref find query+stored keys, sources check_dedupe/legacy_hits, collection overlap, capture routing intent) share the key so one fix covers lookup, duplicate detection, and collections.

[2026-10-24T16:54:23Z · bob-cli-an.6.6.6.5.6.5.1] url-identity tests: 6 new regression tests pass -- clip_url key normalization (Medium twin, unreserved decode, hex-case agreement, non-ASCII) + delimiter-distinctness (encoded / ? # % stay distinct, no recursive decode, malformed passthrough); ref_library stored_identity/url_query_keys twin test; sources check_dedupe twin refusal; collection check_collection_overlap twin test; CLI bob ref find test with both twin notes asserting both queries return both notes with duplicate_identity. Focused suites: 802 lib tests (highlights_ref+ref_library+url_routing) ok; gate clippy (just check flags) clean; cargo fmt clean.

[2026-10-24T16:54:27Z · bob-cli-an.6.6.6.5.6.5.1] PROPOSED FOLLOW-UP: just check has 4 failures that reproduce identically on the clean base tree -- every_value_arg_has_a_decision (themes rename:old/new, owned by active bob-cli-bc), 2x continuation_scan_* (owned by active bob-cli-bd), and curl_pins_the_checked_address_with_resolve (Text file busy parallel-execution flake, passes in isolation; no owner found). None touch URL identity code.

[2026-10-24T16:54:40Z · bob-cli-an.6.6.6.5.6.5.1] url-identity done: normalize_path_escapes in dedupe_key_for unifies the Medium twin spellings plus unreserved-escape and hex-case variants while keeping encoded delimiters distinct. Verified: pre-fix twin test failed with two keys; post-fix all 6 new regression tests pass (key unit tests, library identity/query, sources dedupe, collection overlap, CLI ref-find twin test finding both notes with duplicate_identity); 802-test focused lib suites green; gate clippy and fmt clean. just check failures are 4 pre-existing base-tree failures (bc/bd-owned plus one parallel-execution curl flake), recorded as PROPOSED FOLLOW-UP. Target task bob-cli-7u left open for the lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.1/README.md) | [bob-cli-an.6.6.6.5.6.5.1](bob-cli-an.6.6.6.5.6.5.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2524e8`](https://github.com/bobs-org/bob-cli/commit/f2524e8053471e73421aaf75430a03bd0cd485e9) | fix(highlights-ref): normalize URL identity escapes for shared dedupe key | [bob-cli-an.6.6.6.5.6.5.1](bob-cli-an.6.6.6.5.6.5.1.md) | 2026-10-24 12:55:53 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md

<!-- sase:referenced-by:end -->
