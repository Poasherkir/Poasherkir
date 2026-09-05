# Setup & maintenance — the profile README

## 1. & 2. Repository created and pushed ✅

The repo is https://github.com/Poasherkir/Poasherkir and the README is live on your
profile.

For reference, the reason the name matters: GitHub only renders a README on your
profile page if it lives in a **public repository named exactly your username**.
That's why this one is called `Poasherkir` and not `portfolio`.

The steps below are the parts I can't do from here — they need your browser.

## 3. Turn on private contribution counting

The stats and streak cards can only see what the API exposes. By default that
excludes private repos, so private work reads as zero.

Go to **Settings → Profile** and tick
**"Include private contributions on my profile"**:
https://github.com/settings/profile

Worth doing: a good share of your real work lives in closed repos
(Briefing Point Go, TechSub, the aviation services), and none of it shows up in the
contribution graph until this box is ticked.

## 4. The two contribution workflows ✅

Both are running and both are green — nothing to do here.

| Workflow | Writes to | Used by the README as |
| :-- | :-- | :-- |
| `snake.yml` | `output` branch | the animated snake, via absolute `raw.githubusercontent.com` URLs |
| `3d-contrib.yml` | `profile-3d-contrib/` on `main` | the 3D calendar, via relative paths |

Both re-run on a schedule, so both graphics stay current with no work from you.

The 3D calendar is committed **into this repo**, which means it can't break the way
a third-party image service can. The README uses `profile-night-rainbow.svg` in dark
mode and `profile-green.svg` in light mode; nine other variants sit in the same
folder if you want a different look — just swap the filenames in the `<picture>`
block.

## 5. What still says EDIT

The README is now filled in from your real repos, so only two spots are left marked:

| Where | What to change |
| :-- | :-- |
| Currently Building | Three rows with live status. Update them when a milestone moves — this is the section return visitors re-read. |
| Let's Connect | LinkedIn / X badges are commented out. Uncomment and fill in only the ones you actually use. |

There's also a commented list in **Tech Stack** naming the badges that were removed
(Java, Ruby, Vue, NestJS, TensorFlow, NumPy, Pandas, Seaborn, Docker, AWS, GCP,
Azure, MySQL, Solidity). Nothing on this account uses them yet — paste any back if
that changes.

## 6. Pin your best repositories

The Featured Projects section complements GitHub's own pinning — it doesn't replace
it. On your profile, click **Customize your pins** and choose:

`delivery-os` · `bac-archive` · `portfolio` · `Playlist` · `wordle-solver`

## 7. Add topics to the repos that have none

`portfolio` and `bac-archive` have good topic lists. These three have none, which
costs you GitHub search visibility for free:

| Repo | Suggested topics |
| :-- | :-- |
| `delivery-os` | `flutter` `dart` `offline-first` `riverpod` `drift` `sqlcipher` `algeria` `rtl` |
| `Playlist` | `powershell` `youtube-dl` `windows` `downloader` |
| `wordle-solver` | `c` `wordle` `solver` `algorithms` |

Repo → **About** (gear icon, top right) → **Topics**.

---

## 8. Image services: what works, what doesn't

Every image URL in the README was re-tested immediately before the last commit.
This landscape changes often — several services that worked when this file was
first written have since broken, and one that was broken now works.

### Currently used, verified serving real data

| Service | Status |
| :-- | :-- |
| `github-profile-summary-cards.vercel.app` (5 cards) | ✅ 200, real numbers |
| Streak (`github-readme-streak-stats.herokuapp.com`) | ✅ 200 |
| Capsule-render header/footer | ✅ 200 |
| Dev quote (`quotes-github-readme.vercel.app`) | ✅ 200 |
| Visitor counter, shields.io badges, avatar | ✅ 200 |
| Snake SVGs (`output` branch) | ✅ 200, self-hosted |
| 3D calendar (`profile-3d-contrib/`) | ✅ in-repo, can't break |
| Typing SVG (`readme-typing-svg.demolab.com`) | ⚠️ 200, but rate-limits aggressively — see below |

### Deliberately not used

| Service | Status |
| :-- | :-- |
| ~~Stats + top-langs~~ (official `github-readme-stats.vercel.app`) | ❌ **503 DEPLOYMENT_PAUSED** |
| ~~Stats mirror~~ (`…-sigma-five.vercel.app`) | ❌ 200 with an error card: *"Maximum retries exceeded — add PAT_1"* |
| ~~Repo pin cards~~ (same host as stats) | ❌ 503 — this is why Featured Projects is hand-written |
| ~~Activity graph~~ (`github-readme-activity-graph.vercel.app`) | ❌ **402** — Vercel spending limit exhausted |
| ~~Trophy wall~~ (`github-profile-trophy.vercel.app`) | ❌ **402** |
| ~~Contributor stats~~ | ❌ **402** |

Three of these answer with an HTTP status a link checker calls fine while rendering
as a broken or error image to a human. The stats mirror is the worst offender: a
`200 OK` SVG whose only content is the words "Something went wrong".

**The typing SVG** is the one soft spot left. It serves correctly but starts
refusing connections after a handful of requests in quick succession. A visitor
loading your profile once is well inside its limits; it's automated testing that
trips it. If you ever see it render blank, replace the whole `<p align="center">`
block with plain text:

```md
<p align="center"><em>Fullstack &amp; mobile developer · Flutter · Next.js · offline-first apps for Algeria</em></p>
```

### The durable fix for stats cards

If you want the classic `github-readme-stats` cards back, deploy your own — five
minutes, free, and it can never be rate-limited because you're its only user:

1. Fork https://github.com/anuraghazra/github-readme-stats
2. Create a **classic** personal access token with **no scopes ticked** at
   https://github.com/settings/tokens (it only needs to lift the anonymous API
   rate limit)
3. Import the fork at https://vercel.com/new, add an environment variable `PAT_1`
   set to that token, and deploy
4. Point the README at `your-project.vercel.app` instead

The trophy wall can be revived the same way by deploying `ryo-ma/github-profile-trophy`.

---

## 9. Notes on some choices

**Featured Projects is hand-written, not image cards.** The pin-card service is down
(503), so image cards would render broken for every visitor. Hand-written links also
carry more information — stack, status, live URLs — and read properly on a phone,
where a 495px-wide SVG card does not.

**The stack is trimmed to what's in the repos.** Every badge is backed by shipped
code. A wall of sixty logos where four are real is the single most common way a
profile README loses a reader who knows what they're looking at.

**Skipped: ASCII skill bars.** Percentages like "Python ██████████ 90%" are
self-assigned and every experienced reader knows it. The language cards say the same
thing with real data.

**Skipped: WakaTime and Spotify.** Both need external accounts plus a token in repo
secrets. Worth adding once you're coding daily — say the word and I'll wire them up.

**Theme awareness.** The snake and the 3D calendar both use `<picture>` with
`prefers-color-scheme`, so light-mode visitors don't get a dark rectangle floating
on a white page.

**`alt` text everywhere.** Screen readers, and a graceful fallback whenever one of
the services above has its next bad day.
