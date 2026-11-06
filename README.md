# Nandi Social

A starter pack that runs your social media with you. Social Manager plans campaigns, writes posts in your voice, opens each post ready to go in LinkedIn's or X's own composer in a browser window you watch, and keeps track of what went out. **A person presses every Post button.**

| Agent          | What it does                                                                                                        | Status  |
| -------------- | ------------------------------------------------------------------------------------------------------------------- | ------- |
| Social Manager | Plans campaigns, drafts posts, fills in the composer and hands over to you, records what went out, reports weekly | Preview |

| Workflow                       | Run it                     | What it does                                                                                            |
| ------------------------------ | -------------------------- | ------------------------------------------------------------------------------------------------------- |
| Plan a social campaign         | when you start a campaign  | Asks a few questions, writes the campaign file and adds dated drafts to the calendar                    |
| Draft this week's posts        | Mondays, 9:00 (a trigger)  | Writes the week's posts, waits for your review, then marks them ready                                   |
| Post the next ready post       | weekdays, 10:00 (a trigger), or "post this" in chat | Opens the composer filled in and hands it over; records the link in `posts.md`  |
| Weekly social report           | Fridays, 15:00 (a trigger) | Reads your own numbers and replies (read only), writes the report, hands over replies to comments      |
| Research a topic or competitor | when you want              | Reads public pages (read only) and writes notes with links                                              |

## How it posts: prepare and hand over

1. Social Manager writes the post and opens the site's composer in its browser window, filled in.
2. Nandi brings the window forward and your Inbox shows **Your turn: review and post**, with the draft.
3. You change anything you like and press **Post** yourself. Then answer in Nandi: **Done**, **Skip** or **Changed it** (with the final text).
4. Social Manager records what went out, and later reads replies and numbers.

Why: LinkedIn's user agreement, X's automation rules, and Meta's and Google's terms ban scripts that operate their websites. Approval inside Nandi doesn't change what the platform sees. When you make the publishing click, no rule about automated posting is broken, and almost all the time saving remains.

**Never automated, on any platform:** likes, reactions, follows, connection requests, invitations, messages, reposts, comments on other people's content, bulk anything. These get accounts suspended. The pack's policy (`policies/social-posting.md`) refuses those clicks everywhere, and refuses Post, Publish, Share, Send, Reply and Tweet buttons (and Enter or Ctrl+Enter) on the social sites. You see it on the agent's Settings tab, under Permissions.

## Set up

1. **Install** Nandi Social from Library › Packs (or from this folder: Library › Install from this computer › A pack folder). Review and allow what it asks for.
2. **Tools.** In Library › Tools, install and start **Browser** (needs Node.js and Google Chrome or Microsoft Edge), and turn on **Web search**. In My notes, let agents write to your notes.
3. **Grant the browser.** On Social Manager's Settings tab, under Permissions, allow the Browser pilot's capabilities.
4. **Sign in once.** Say to Social Manager: "Open LinkedIn and X so I can sign in." A browser window opens with the agent's own profile (never your everyday browser). Sign in yourself. The session stays on your computer; the agent never sees your password.
5. **Your voice.** Copy `examples/my-notes/social/` into My notes and edit `voice.md`, or let Social Manager ask you five questions and write it.
6. **Triggers.** In Automations › Triggers, add schedules: `0 9 * * 1` → workflow Draft this week's posts; `0 10 * * 1-5` → Post the next ready post; `0 15 * * 5` → Weekly social report.

If a page doesn't load in the browser, the site needs a host the agent isn't allowed. The Audit Log's Egress tab shows which; add it to the agent's Internet access.

## Notes it keeps (My notes, `social/`)

| File                         | What it holds                                                                  |
| ---------------------------- | ------------------------------------------------------------------------------ |
| `social/voice.md`            | Brand voice, words to use and avoid, hashtags, who we are                      |
| `social/campaigns/<name>.md` | Goal, audience, platforms, dates, key messages, what success looks like        |
| `social/calendar.md`         | Planned posts: date, platform, draft, image, status (draft, ready, posted, skipped) |
| `social/posts.md`            | What went out: date, platform, link, final text, first-week numbers           |
| `social/reports/<week>.md`   | The weekly report                                                              |

Images: keep them in `social/assets/`. Social Manager names the file in the calendar; you attach it during the hand-over.

## Coming later

- Facebook and Instagram (Meta Business Suite) and YouTube Studio community posts, with the same hand-over.
- Optional official-API posting per account (LinkedIn Pages, Meta Graph API, X API, YouTube Data API), still approved in the Inbox first. Each platform must approve an app first.

Licence: MIT (see LICENSE). Copy, change and share these agents freely.
