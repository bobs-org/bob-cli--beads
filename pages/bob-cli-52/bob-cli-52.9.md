# Bead: bob-cli-52.9 — Live verification, install, and follow-ups

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.9` · **Size:** small
**Created:** 2026-10-07 08:11:17 EDT · **Closed:** 2026-10-07 11:48:58 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

verify: on athena, run the live article, PDF, arXiv, blocked, corporate link, list, duplicate, and already-in-library exercises against a scratch vault; time a read-only dry run on the real vault; install; run read-only Mac probes or write Bryan's Mac checklist; and record follow-ups.

## Notes

[2026-10-07T15:48:05Z · bob-cli-52.9] Mac checklist for Bryan (mac was offline over SSH, so probes deferred): 1. just install-all; 2. install the new Bob Mac Capture build; 3. paste a link in the panel and watch the card, then bob ref jobs; 4. share one link from the phone to Keep, run bob gkeep list -f json, confirm title/body/links shape against R5; 5. run bob gkeep pull; 6. run bob ref doctor --no-hooks. Read-only probe to run when mac is up: ssh mac bob ref doctor --no-hooks with app PATH (uv row must resolve ~/.local/bin/uv). NOTE for Bryan: sase.md:20 in ~/bob is a stale bare-URL task (openai.com codex-orchestration post) duplicating finished ref ref/blogs/open_source_codex_orchestration_symphony.md; left unedited per plan.

[2026-10-07T15:48:12Z · bob-cli-52.9] PROPOSED FOLLOW-UP: memory task proposing a decisions record: a bare public link is reading intent (becomes a ref via background ref job, falls back to inbox task; capture never blocks on network); rejected alternatives are inline sync, longer app timeout, vault sweeper

[2026-10-07T15:48:16Z · bob-cli-52.9] PROPOSED FOLLOW-UP: glossary term for Ref Job

[2026-10-07T15:48:20Z · bob-cli-52.9] PROPOSED FOLLOW-UP: retrying retryable capture clips (v2)

[2026-10-07T15:48:24Z · bob-cli-52.9] PROPOSED FOLLOW-UP: running bob ref jobs run -q from the Mac 15-minute cron

[2026-10-07T15:48:27Z · bob-cli-52.9] PROPOSED FOLLOW-UP: JSON output for ref create (needs a short flag other than -f)

[2026-10-07T15:48:31Z · bob-cli-52.9] PROPOSED FOLLOW-UP: fallback notifications, if Bryan wants them

[2026-10-07T15:48:35Z · bob-cli-52.9] PROPOSED FOLLOW-UP: note on bob-cli-37 that Bob Mac Capture now queues links

[2026-10-07T15:48:39Z · bob-cli-52.9] PROPOSED FOLLOW-UP: SSH delegation of clipping to athena, if Mac clipping proves flaky

[2026-10-07T15:48:43Z · bob-cli-52.9] PROPOSED FOLLOW-UP: just-all has 2 pre-existing failures from unrelated master commit 84a8a31 (fold ref clip into create): completion kinds test missing decision for ref create:audio, and listen-card LaTeX test; no epic commit touches those files

[2026-10-07T15:48:47Z · bob-cli-52.9] PROPOSED FOLLOW-UP: no genuinely bot-blocked site demonstrated live (nytimes/bloomberg test URLs clipped fine); fallback path proven live via example.com 404 http_status fallbacks plus the phase-capture blocked-fake e2e test

[2026-10-07T15:48:58Z · bob-cli-52.9] Verified on athena: cargo build --release ok; just install-smoke ok; just-all 1873 passed with 2 pre-existing failures from unrelated master 84a8a31 (recorded as follow-up). Live scratch-vault exercises: WP article clipped then scanned to READY in reading queue; W3C PDF + arXiv 1706.03762 clipped as papers; example.com 404s fell back to mac_inbox.md tasks with warning-bullet + working retry cmd; go/x stayed a task; 3-URL list gave 2 queued + 1 duplicate(same link as item 1); recapture gave already-in-library with path/title/state; submits returned in ~130-460ms (kick detached, under 1s); capture-parse reports mode ref + ref_url span. Real-vault read-only dry runs: 191ms single, 189ms 5-URL list warm (925ms cold first run). cargo install --path . --locked ok. Mac offline over SSH; checklist left in bead note. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-52.2](bob-cli-52.2.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-52.6](bob-cli-52.6.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-52.7](bob-cli-52.7.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-52.8](bob-cli-52.8.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.9/README.md) | [bob-cli-52.9](bob-cli-52.9.md) | 0 |
