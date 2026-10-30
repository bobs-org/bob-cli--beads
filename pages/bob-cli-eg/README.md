# Bead: bob-cli-eg — bob gcal login that just works

[Bead Pages](../README.md) / bob-cli-eg

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.165](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.165.md) · **Assignee:** `bob-cli-eg.land`
**Created:** 2026-10-30 09:42:40 EDT · **Closed:** 2026-10-30 13:39:39 EDT
**Plan:** [202610/gcal\_login\_redesign.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gcal_login_redesign.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/gcal_login_redesign.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gcal_login_redesign.md

<!-- sase:links:end -->

## Description

`bob gcal login` connects Google Calendar in one command on any host (Mac with a browser, athena over SSH): it fixes the gog-client reuse failure, owns a sign-in flow that cannot hang, explains every Google screen in plain words, recovers from the usual Cloud Console mistakes in place, and renders a calm, beautiful step transcript.

## Notes

[2026-10-30T15:36:59Z · bryanbugyi34@gmail.com] I'm getting a 'sign-in link is out of date' error message when I try to login at the moment. See the 🔒 20261030\_113553.png screenshot for context. The Epic Lenard agent should ensure this is fixed before landing the epic.

[2026-10-30T16:45:59Z · bob-cli-eg.land] FOLLOW-UP TRIAGE (before remaining-work tale): Read every note on eg.1-eg.4. eg.1 #1, eg.2 #1, and eg.3 #1 are one proposal: the pre-existing prose-table snapshot assertion, already described on bob-cli-87 #13. Applied sase_new_task, searched CI tasks then all task types, swept all 100 tasks created within one week, and inspected active epics. No distinct task duplicate exists; bob-cli-ed is a separate memory proposal. Declined a new task because intervening commit a844d3e1 already repaired the assertion, and the exact targeted lib test now passes on 7328fab2 (1 passed, 4117 filtered, 13.67s). Recorded that resolution on bob-cli-87. No other PROPOSED FOLLOW-UP entries exist. The screenshot sign-in failure and other login acceptance gaps remain epic work, covered by the forthcoming remaining-work tale, not task beads.

[2026-10-30T16:49:46Z · bob-cli-eg.land] LAND AUDIT at 7328fab2: Reviewed original plan, final DECISIONS, all four children and every note, screenshot on epic note #1, source/tests, and phase commits 2ca76ca0/00c44ab4/18d3f97a/7254e106. The memory_signin_record=no branch was honored: none of those commits edits memory. Client normalization/reuse, captured stdio, guided setup, shared resolver, additive JSON and gkeep spinner reuse are present, but the epic is not ready to close.

Confirmed screenshot root cause with installed real gog v0.44.0 cf42bb7c in a throwaway --home/GOG_HOME using dummy credentials and a blocked local proxy: step 1 uses --force-consent while step 2 omits it, and gog rejects that with manual auth state mismatch before exchange. The browser callback also drops its bound port, independently causing the same mismatch. Matching both flags and full redirect reaches token exchange (then the deliberately blocked proxy). Repeating step 1 without an override reuses state, so the claimed fresh-link retry is not fresh. Reviewed upstream via sase_repo, including validateManualState at the installed commit. No real consent or token exchange was performed.

Other remaining acceptance gaps: strict fake must model the real state tuple/rotation; Downloads q is accepted as yes; stale paste does not reprint the link; reruns omit Sign in/already connected and summary; primary calendar IDs can be falsely warned missing; interactive keyring skips, API-disabled resume hints, opener-spawn fallback and denial spinner handling are incomplete. Shared-account integration stops at calendar listing: snapshot events and absent-event queries still omit --account; logout has not adopted deduplication. The docs phase omitted the specified help strings, SSH/fresh-desktop transcripts, several error/security/environment details, and contains Login's Login. These are bounded remaining contract/integration work in the tale, not new follow-up tasks.

Integration review: fetched origin/master equals local HEAD 7328fab2. Inspected non-epic commits b081097c, 5e4bee79, 60c77634, 0e178061, 3c9536a7, 03a3497f, 4b4a4a34, a844d3e1, 7328fab2 and shared doc/runner/spinner consumers; no competing login implementation or new consumer needs migration. PDF assertion fix a844d3e1 resolves every phase follow-up (triage recorded separately). No --epic-symbol entries and no symvision recipe. Epic has no parent_bead. Remaining-work plan sase_plan_gcal_login_landing_repairs.md is tier tale, size medium; validated with --explain, corrected frontmatter, and revalidated with zero warnings. Its final step requires the coder to verify with just check and docs-check, resolve symbols, close this epic normally in the code turn, run symvision if available, and mark plan:202610/gcal_login_redesign.md done. Full gates remain for that code turn; no just check-full was run.

[2026-10-30T17:39:39Z · bob-cli-eg.land] Landed remaining-work tale plan:202610/gcal_login_landing_repairs.md on top of closed phases eg.1–eg.4.

Real-gog mismatch repair: both remote OAuth steps now send --force-consent and the attempt's bound --redirect-uri. The loopback callback is rebuilt from the known origin plus the raw query (port kept; code/state percent-encoded). fake_gog persists/validates/consumes the (client, force_consent, state, redirect_uri) tuple and rejects the old mismatch; fake_browser percent-encodes state/code. Throwaway GOG_HOME smoke with dummy Desktop creds, file keyring, --insecure, and a blocked local proxy confirmed: matching flags + full-port callback pass validateManualState and reach token exchange; omitting --force-consent or dropping the port still mismatch; repeating step 1 on the same redirect reuses state, a new redirect does not. Smoke proves local protocol matching only — no live Google consent.

Acceptance repairs: Downloads confirm is y/yes/empty vs n/no vs q/quit/EOF vs re-prompt; already-connected renders Sign in then Check/summary; Check uses matches_configured_id; interactive keyring skip notes; API-disabled resume hint; opener spawn-fail prints the fallback; denial drops the spinner then retry_or_quit; stale paste reprints the current link; paste access_denied then q is cancelled; unique loopback bind with reuse-hold so a retry advertised as fresh cannot reuse gog state; OpenerGuard reaps the opener Child so FakeBrowser finishes writing the outcome page.

Account propagation: DaySnapshot.account is passed to gog.events and gog.event; logout uses unique_emails. Fake requires --account on events/event. Covered configured Bob account among multiple grants, sole bob-gcal among default gog accounts, sync absent-event lookup, and case-insensitive logout dupes.

Docs: login about is "Connect Google Calendar (read-only) in one guided step"; -c replacement and SSH paste (-m) are in option help; examples include -a EMAIL. gcal.md, the setup guide, configuration.md, and generated CLI reference updated. just docs-gen and just docs-check passed (447 passed, 1 skipped).

Gates: focused gcal_auth/gcal_cli/gcal_list/gcal_lifecycle/lib native::gcal tests passed; sase tool run check 8ac9eeb7d4e0fdc3cc52645b58e61623 succeeded in 3m 40s (exit 0). just check-full was not run.

Drift: HEAD still 7328fab2; no intervening login/transport/spinner commits. Shared docs/gate changes kept. memory_signin_record=no honored — no memory or decision files edited.

Follow-up triage: eg.1 #1, eg.2 #1, and eg.3 #1 (PDF snapshot assertion) all declined; a844d3e1 fixed the same assertion and the targeted lib test passed on 7328fab2. No --epic-symbol leftovers; just has no symvision recipe.

No parent_bead and no host-created tale descendant. Closing this epic normally.

## Attachments

- 🔒 20261030\_113553.png · image/png · 2854×1686 · 402.271 KiB (private attachment)

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-eg.1](bob-cli-eg.1.md) | Fix client reuse and make the OAuth client step robust | ✓ closed | medium | 2026-10-30 | 1 | 1 |
| [bob-cli-eg.2](bob-cli-eg.2.md) | Bob-owned sign-in through gog's two-step remote flow | ✓ closed | medium | 2026-10-30 | 1 | 1 |
| [bob-cli-eg.3](bob-cli-eg.3.md) | Guided setup, account choice, self-healing check, and summary | ✓ closed | medium | 2026-10-30 | 1 | 1 |
| [bob-cli-eg.4](bob-cli-eg.4.md) | Help text, docs, and the final gate | ✓ closed | small | 2026-10-30 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-eg: bob gcal login that just works [closed]"]
    n1["bob-cli-eg.1: Fix client reuse and make the OAuth client step robust [closed]"]
    n2["bob-cli-eg.2: Bob-owned sign-in through gog's two-step remote flow [closed]"]
    n3["bob-cli-eg.3: Guided setup, account choice, self-healing check, and summary [closed]"]
    n4["bob-cli-eg.4: Help text, docs, and the final gate [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-eg.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-eg.1/README.md) | [bob-cli-eg.1](bob-cli-eg.1.md) | 1 |
| [bbugyi200.athena.bob-cli-eg.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-eg.2.md) | [bob-cli-eg.2](bob-cli-eg.2.md) | 1 |
| [bbugyi200.athena.bob-cli-eg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-eg.3.md) | [bob-cli-eg.3](bob-cli-eg.3.md) | 1 |
| [bbugyi200.athena.bob-cli-eg.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-eg.4/README.md) | [bob-cli-eg.4](bob-cli-eg.4.md) | 1 |
| [bbugyi200.athena.bob-cli-eg.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-eg.land.md) | [bob-cli-eg](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2ca76ca`](https://github.com/bobs-org/bob-cli/commit/2ca76ca05a1bc544f16a3686774ac4a6538a9550) | fix(gcal): reuse gog clients by piping normalized client JSON | [bob-cli-eg.1](bob-cli-eg.1.md) | 2026-10-30 10:13:17 EDT |
| bob-cli | [`00c44ab`](https://github.com/bobs-org/bob-cli/commit/00c44ab4b481ecc00f4a882ae873a6fc6d28fde6) | feat(gcal): bob-owned login sign-in with browser and paste flows | [bob-cli-eg.2](bob-cli-eg.2.md) | 2026-10-30 11:17:32 EDT |
| bob-cli | [`18d3f97`](https://github.com/bobs-org/bob-cli/commit/18d3f97a36059ae331d4529f380c847e3dcab5d1) | feat(gcal): guide Calendar login setup and recovery | [bob-cli-eg.3](bob-cli-eg.3.md) | 2026-10-30 12:15:22 EDT |
| bob-cli | [`7254e10`](https://github.com/bobs-org/bob-cli/commit/7254e106795ee56425456f07a95c7756aca284bd) | docs(gcal): update login guidance and help | [bob-cli-eg.4](bob-cli-eg.4.md) | 2026-10-30 12:31:26 EDT |
| bob-cli | [`f7642c7`](https://github.com/bobs-org/bob-cli/commit/f7642c7a5bad190d7e2d94fb6a9a426c84e96d99) | feat(gcal): match real gog OAuth and finish guided login | [bob-cli-eg](README.md) | 2026-10-30 13:41:38 EDT |
| bob-cli--plans | [`bob-cli--plans@e1d29be`](https://github.com/bobs-org/bob-cli--plans/commit/e1d29be49dfe67c194387f06ea620c76937c535e) | docs(plans): mark gcal login redesign and landing repairs done | [bob-cli-eg](README.md) | 2026-10-30 13:42:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eg.1][1] | Need epic DECISIONS and plan context | 1 |
| read-by | [agent:bob-cli-eg.2--1][2] | Need epic DECISIONS and plan | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-eg.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-eg.2.md

<!-- sase:referenced-by:end -->
