# Bead: bob-cli-52 — Links go to the reading queue: URL routing for bob capture, Bob Mac Capture, and bob gkeep pull

[Bead Pages](../README.md) / bob-cli-52

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.land`
**Created:** 2026-10-07 08:11:16 EDT · **Closed:** 2026-10-07 13:05:39 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

A bare public link lands in Bob's reading queue instead of becoming an inbox task. This covers a link captured with `bob capture` or Bob Mac Capture, whether alone, in a pasted list, or mixed with ordinary tasks, and a link shared to Google Keep and pulled with `bob gkeep pull`. Every path uses the same ingest engine as `bob ref create`. Capture stays instant, works offline, and never loses a link. The preview says honestly, without touching the network, whether the link is new or already in the library. Submit queues a durable ref job, and a detached background worker clips it. If a clip fails, the link falls back to exactly today's inbox task, plus a ⚠️ reason and a retry command. Keep pull clips inline and archives a note only after a terminal outcome. Bob Mac Capture presents the new reference item beautifully and parses nothing itself. Every path has an opt-out.

## Notes

[2026-10-07T16:16:41Z · bob-cli-52.land] LANDING FOLLOW-UP TRIAGE (bob-cli-52.land): (1) completion kinds ref create:audio (52.1 #1, .2 #1, .3 #1, .4 #1, .5 #1, .6 #1, .7 #1, .9 #10): +1 on bob-cli-4j. (2) listen_filter card test (same notes plus .3 #2, .5 #2): +1 on bob-cli-4u. (3) capture_pomodoros parallel flake (52.2 #3, .4 #1, .5 #4, .6 #1, .7 #1): +1 on bob-cli-40. (4) note_ready scan_excludes_r3_and_r7_paths parallel flake (52.5 #4; it also flaked once in the landing run): new flake task bob-cli-5c. (5) check-web-clip-adapter Playwright launch failure (52.2 #2): root cause found (Chrome SingletonSocket path too long under SASE's deep TMPDIR, because the self-test mkdtemp skips ScratchDir's short-base guard); new ci task bob-cli-5b. (6) ingest_characterizes_url_failure_modes (52.3 #3, .4 #2, .5 #3, .6 #2, .7 #2): DECLINED as a task because the epic caused it (the ingest-phase missing-uv case leaves HOME real, so the hardening-phase resolve_uv finds ~/.local/bin/uv); it is fixed in the landing tale. (7) decisions record for bare-link reading intent (52.9 #2): memory task bob-cli-5d. (8) Ref Job glossary term (52.9 #3): memory task bob-cli-5e. (9) retry retryable capture clips v2 (52.9 #4): feature task bob-cli-5f. (10) bob ref jobs run -q from the Mac 15-minute schedule (52.9 #5): feature task bob-cli-5g (related bob-cli-30). (11) ref create JSON output (52.9 #6): feature task bob-cli-5h (related bob-cli-4a). (12) fallback notifications if Bryan wants them (52.9 #7): DECLINED; design decision 12.5 deliberately chose none in v1, the ⚠️ inbox task and bob ref jobs are the signal, and nobody has asked for them; reopen if Bryan asks. (13) note on bob-cli-37 that Bob Mac Capture now queues links (52.9 #8): done as a note on bob-cli-37. (14) SSH delegation of clipping to athena if Mac clipping is flaky (52.9 #9): DECLINED for now; it depends on evidence that does not exist yet (Mac clipping has not run live, see the 52.9 checklist); file it if the checklist shows flaky Mac clips. (15) 84a8a31 lib failures (52.9 #10): the same as (1) and (2). (16) no genuinely bot-blocked site shown live (52.9 #11): DECLINED as not actionable; the fallback path is proven by the live 404 fallbacks and the phase-capture blocked-fake e2e test. Also: bob-cli-4v closed as resolved by 52.2 (verified). Gkeep attachment-fingerprint limit (an attachment added mid-pull is archived on the next pull, because the fp excludes attachments): DECLINED; it predates the epic, which made it strictly better by delaying the archive one pull, and the case is rare.

[2026-10-07T17:05:39Z · bob-cli-52.land] Landing implemented per 202610/bob_cli_52_landing.md sections 1-6. Verified: cargo fmt clean, cargo build zero warnings (12 epic warnings eliminated), cargo test lib 1874 passed with only known failures (bob-cli-4j kinds, bob-cli-4u listen_filter, bob-cli-40 capture_pomodoros flake), cargo test --tests all green except those (cli 1159 passed, gkeep_pull 39 passed), just check-adapter ok, just install-smoke ok, bob --help and capture --help smoke ok. All 9 phases already CLOSED.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-52.1](bob-cli-52.1.md) | Typed, non-printing URL ingest extracted from bob ref create | ✓ closed | medium | 2026-10-07 | 1 | 1 |
| [bob-cli-52.2](bob-cli-52.2.md) | uv resolution, URL safety, and doctor rows | ✓ closed | small | 2026-10-07 | 1 | 1 |
| [bob-cli-52.3](bob-cli-52.3.md) | URL-intent classifier, routing policy, and offline library verdict | ✓ closed | small | 2026-10-07 | 1 | 1 |
| [bob-cli-52.4](bob-cli-52.4.md) | Capture grammar for reference items and URL lists | ✓ closed | small | 2026-10-07 | 1 | 1 |
| [bob-cli-52.5](bob-cli-52.5.md) | Ref job spool, background worker, and bob ref jobs | ✓ closed | medium | 2026-10-07 | 1 | 1 |
| [bob-cli-52.6](bob-cli-52.6.md) | bob gkeep pull clips URL-only Keep notes | ✓ closed | medium | 2026-10-07 | 1 | 1 |
| [bob-cli-52.7](bob-cli-52.7.md) | bob capture queues bare links for the reading queue | ✓ closed | medium | 2026-10-07 | 1 | 1 |
| [bob-cli-52.8](bob-cli-52.8.md) | Bob Mac Capture presents reference items | ✓ closed | medium | 2026-10-07 | 1 | 2 |
| [bob-cli-52.9](bob-cli-52.9.md) | Live verification, install, and follow-ups | ✓ closed | small | 2026-10-07 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-52: Links go to the reading queue: URL routing for bob capture, Bob Mac Capture, and bob gkeep pull [closed]"]
    n1["bob-cli-52.1: Typed, non-printing URL ingest extracted from bob ref create [closed]"]
    n2["bob-cli-52.2: uv resolution, URL safety, and doctor rows [closed]"]
    n3["bob-cli-52.3: URL-intent classifier, routing policy, and offline library verdict [closed]"]
    n4["bob-cli-52.4: Capture grammar for reference items and URL lists [closed]"]
    n5["bob-cli-52.5: Ref job spool, background worker, and bob ref jobs [closed]"]
    n6["bob-cli-52.6: bob gkeep pull clips URL-only Keep notes [closed]"]
    n7["bob-cli-52.7: bob capture queues bare links for the reading queue [closed]"]
    n8["bob-cli-52.8: Bob Mac Capture presents reference items [closed]"]
    n9["bob-cli-52.9: Live verification, install, and follow-ups [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n1 -.-> n5
    n1 -.-> n6
    n2 -.-> n6
    n2 -.-> n9
    n3 -.-> n4
    n3 -.-> n5
    n3 -.-> n6
    n4 -.-> n7
    n5 -.-> n7
    n6 -.-> n9
    n7 -.-> n8
    n7 -.-> n9
    n8 -.-> n9
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.1/README.md) | [bob-cli-52.1](bob-cli-52.1.md) | 1 |
| [bbugyi200.athena.bob-cli-52.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.2/README.md) | [bob-cli-52.2](bob-cli-52.2.md) | 1 |
| [bbugyi200.athena.bob-cli-52.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.3/README.md) | [bob-cli-52.3](bob-cli-52.3.md) | 1 |
| [bbugyi200.athena.bob-cli-52.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.4/README.md) | [bob-cli-52.4](bob-cli-52.4.md) | 1 |
| [bbugyi200.athena.bob-cli-52.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.5/README.md) | [bob-cli-52.5](bob-cli-52.5.md) | 1 |
| [bbugyi200.athena.bob-cli-52.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.6/README.md) | [bob-cli-52.6](bob-cli-52.6.md) | 1 |
| [bbugyi200.athena.bob-cli-52.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.7/README.md) | [bob-cli-52.7](bob-cli-52.7.md) | 1 |
| [bbugyi200.athena.bob-cli-52.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.8/README.md) | [bob-cli-52.8](bob-cli-52.8.md) | 2 |
| [bbugyi200.athena.bob-cli-52.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.9/README.md) | [bob-cli-52.9](bob-cli-52.9.md) | 0 |
| [bbugyi200.athena.bob-cli-52.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-52.land.md) | [bob-cli-52](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3232214`](https://github.com/bobs-org/bob-cli/commit/32322146c23cdd625f1b84b9250bb163f8d34296) | feat(hardening): shared uv resolution, URL safety, and doctor rows | [bob-cli-52.2](bob-cli-52.2.md) | 2026-10-07 08:39:11 EDT |
| bob-cli | [`2eafe60`](https://github.com/bobs-org/bob-cli/commit/2eafe60c505be3852633cb61e1f2cc29db409b17) | feat(ref): add typed non-printing URL ingest for reading queue | [bob-cli-52.1](bob-cli-52.1.md) | 2026-10-07 08:41:05 EDT |
| bob-cli | [`df9d504`](https://github.com/bobs-org/bob-cli/commit/df9d504fb937a9ba80bf7ec51f6d8ead285fac62) | feat(url-routing): add intent classifier, routing policy, and offline library verdict | [bob-cli-52.3](bob-cli-52.3.md) | 2026-10-07 09:01:44 EDT |
| bob-cli | [`98fd8ae`](https://github.com/bobs-org/bob-cli/commit/98fd8ae492c59ed08e843e713e023595246febea) | feat(capture): add reference item grammar with routing-gated Ref kind | [bob-cli-52.4](bob-cli-52.4.md) | 2026-10-07 09:29:14 EDT |
| bob-cli | [`0a8c879`](https://github.com/bobs-org/bob-cli/commit/0a8c87907f55af9dcfce121a059615f848ef6ab9) | feat(gkeep): clip URL-only Keep notes into reading queue on pull | [bob-cli-52.6](bob-cli-52.6.md) | 2026-10-07 09:42:32 EDT |
| bob-cli | [`f4fb812`](https://github.com/bobs-org/bob-cli/commit/f4fb812ad58cb8748f7bfe73036f9ddbf6461e79) | feat(ref-jobs): background clip queue for reading-queue links | [bob-cli-52.5](bob-cli-52.5.md) | 2026-10-07 10:08:25 EDT |
| bob-cli | [`c9b361b`](https://github.com/bobs-org/bob-cli/commit/c9b361b205cc8fc529187ab1418b20009f5ce671) | feat(capture): queue bare links for the reading queue | [bob-cli-52.7](bob-cli-52.7.md) | 2026-10-07 10:46:15 EDT |
| bob-mac-capture | [`bob-mac-capture@bf43ab2`](https://github.com/bobs-org/bob-mac-capture/commit/bf43ab24f3aeb47beb63cf7a64eb874e86013e78) | feat(capture): present reading-queue reference items | [bob-cli-52.8](bob-cli-52.8.md) | 2026-10-07 11:05:41 EDT |
| bob-mac-capture | [`bob-mac-capture@b19c913`](https://github.com/bobs-org/bob-mac-capture/commit/b19c91306bb84ebf12a6c63c4ac70d4de4f55a5c) | fix(capture): restore ViewBuilder on the completion card | [bob-cli-52.8](bob-cli-52.8.md) | 2026-10-07 11:09:21 EDT |
| bob-cli | [`6244ddd`](https://github.com/bobs-org/bob-cli/commit/6244dddd931982a598920cdc0fdc69a752c462c8) | feat(landing): implement bob-cli-52 landing per 202610/bob\_cli\_52\_landing.md | [bob-cli-52](README.md) | 2026-10-07 13:08:30 EDT |
