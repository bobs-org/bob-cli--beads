# Bead: bob-cli-os.8 — Publisher transcript parsing and paragraphing

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.8` · **Size:** medium
**Created:** 2026-11-21 14:59:42 EST · **Closed:** 2026-11-21 23:08:55 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

transcript_text: parse JSON/VTT/SRT/HTML/text transcripts into sanity-checked, speaker-labelled paragraphs with honest role inference.

## Notes

[2026-11-22T04:08:24Z · bob-cli-os.8] PROPOSED FOLLOW-UP: three load-sensitive just check flakes — under load avg 40-90 the first full run failed lib native::capture_related::tests::synthetic_vault_draft_contract_is_under_250ms and cli capture::related::draft_related_stays_under_the_debug_perf_gate (wall-clock perf gates; the latter already noted on bob-cli-hc.3 / bob-cli-go.11) plus cli albums_update::completion_offers_update_stems_and_input_files ("stems: []"); all three passed in isolation on the same test binaries, and the second full just check on the rebased tree was green.

[2026-11-22T04:08:38Z · bob-cli-os.8] API for transcript_dossier (bob-cli-os.9): podcast::transcript::preferred_offer(&item.transcripts, |t| (t.mime.as_str(), t.url.as_str())) -> Option<(&FeedTranscript, TranscriptFormat)> picks JSON > VTT > SRT > HTML > text (specific MIME wins; text/plain, octet-stream, or empty defer to the URL extension). parse_transcript(bytes, mime, url, duration_ms: Option<u64>) -> Result<Transcript, TranscriptDrop>. Transcript { format, paragraphs: Vec<Paragraph { start_secs: Option<u32>, speaker: Option<String>, text }> (Serialize), words, roles_inferred, names_from_file }. TranscriptDrop Display is the text after "transcript dropped: ". TranscriptFormat::as_str() = json/vtt/srt/html/text (payload), label() = JSON/VTT/SRT/HTML/text (provenance line). format_clock(secs) = m:ss / h:mm:ss. start_secs is None for text transcripts and for a paragraph that opens inside the cue that opened the previous paragraph (one long cue never stamps two paragraphs), so the renderer and chapter_marks must skip None starts.

[2026-11-22T04:08:55Z · bob-cli-os.8] Added src/native/highlights_ref/podcast/transcript.rs: pure parse_transcript for Podcasting 2.0 JSON, WebVTT (header, cue ids, settings, NOTE/STYLE/REGION, <v> voices incl. several per cue, inline tags, ruby text, entities), SRT (CRLF, tags, {\\an8}), HTML (<cite>/<time>/<p>), and text; preferred_offer with JSON > VTT > SRT > HTML > text; drops with reasons (not text, unsupported, malformed, empty, <200 words, >120,000 words, last cue outside 50-110% of a known duration); diarization tokens -> Speaker N in first-appearance order, Host/Guest only for exactly two diarized speakers with >=10 questions and >=3x question rate, names never guessed; paragraphs merge same-speaker cues, close at the first sentence end after 95 words, force at 160, break on speaker change and text blank lines. Fixtures: trimmed real Pragmatic Engineer VTT (first 3 min, byte-for-byte) plus SRT/JSON/HTML/text re-encodings. 32 unit tests cover every format, garbage drops, diarized and voice-tagged files, paragraph bounds, and the question-rate rule both ways. Verified: just check green (fmt, workspace clippy gate, full workspace tests) on the tree rebased onto origin/master 3ce97d73; no docs or CLI surface changed.

## Dependencies

- **Depends on:** [bob-cli-os.3](bob-cli-os.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-os.9](bob-cli-os.9.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.8/README.md) | [bob-cli-os.8](bob-cli-os.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dbedc65`](https://github.com/bobs-org/bob-cli/commit/dbedc651f9027e8de7e48b0a58f0182e2c69b978) | feat(ref): parse publisher podcast transcripts into speaker paragraphs | [bob-cli-os.8](bob-cli-os.8.md) | 2026-11-21 23:10:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-os.10][1] | Check sibling phase status and any follow-up notes relevant to rollout | 1 |
| read-by | [agent:bob-cli-os.3][2] | check whether dependent phases are concurrently touching podcast module | 1 |
| read-by | [agent:bob-cli-os.8][3] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.10/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.8/README.md

<!-- sase:referenced-by:end -->
