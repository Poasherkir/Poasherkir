# Setup & maintenance — the profile README

## 1. & 2. Repository created and pushed ✅

The repo is https://github.com/Poasherkir/Poasherkir and the README is live on your
profile.

For reference, the reason the name matters: GitHub only renders a README on your
profile page if it lives in a **public repository named exactly your username**.
That's why this one is called `Poasherkir` and not `portfolio`.

The steps below all need the GitHub web UI — they can't be done from the CLI.

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

## 5. The one thing left to fill in

**Let's Connect** — the LinkedIn and X badges sit commented out in the README.
Uncomment and fill in only the ones actually in use; a badge pointing at
`linkedin.com/in/YOUR-HANDLE` is worse than no badge.

There's also a commented list in **Tech Stack** naming the badges that aren't shown
(Java, Ruby, Vue, NestJS, TensorFlow, NumPy, Pandas, Seaborn, AWS, GCP, Azure,
MySQL, Solidity). Nothing here uses them yet — paste any back if that changes.

## 6. Pin your repositories — this one matters now

The README deliberately contains **no project list**. That work is done by GitHub's
own pinned repositories, which render directly beneath it.

That makes pinning load-bearing rather than optional: with nothing pinned, a visitor
reaches the bottom of the README and sees nothing you've built. On your profile,
click **Customize your pins** and choose up to six:

`delivery-os` · `bac-archive` · `portfolio` · `Playlist` · `wordle-solver` · `qahwa-books`

Pins pull their own description and language straight from each repo, so they never
drift out of date the way a hand-written list does. That also means a repo with a
blank description wastes its slot — `wordle-solver` is the last one still missing
a description (repo → **About** → gear icon).

Note that `Poasherkir` — this repo — is worth *unpinning*. It holds the profile
README, not a project, so it spends a slot showing nothing built.

## 7. Repo topics ✅

All six repos now carry topics, which is free GitHub search visibility:

| Repo | Topics |
| :-- | :-- |
| `delivery-os` | `flutter` `dart` `offline-first` `riverpod` `drift` `sqlcipher` `algeria` `rtl` |
| `bac-archive` | `flutter` `supabase` `offline-first` `arabic` `rtl` `pdf` `education` `android` `riverpod` |
| `portfolio` | `nextjs` `react-three-fiber` `threejs` `typescript` `tailwindcss` `webaudio` `portfolio` |
| `Playlist` | `youtube` `yt-dlp` `powershell` `windows` `downloader` `ffmpeg` |
| `qahwa-books` | `python` `web-scraping` `beautifulsoup` `arabic` `books` `cli` |
| `wordle-solver` | `c` `wordle` `solver` `algorithms` `makefile` |

Add more at repo → **About** (gear icon, top right) → **Topics**.

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
| ~~Repo pin cards~~ (same host as stats) | ❌ 503 — image repo cards are not an option |
| ~~Activity graph~~ (`github-readme-activity-graph.vercel.app`) | ❌ **402** — Vercel spending limit exhausted |
| ~~Trophy wall~~ (`github-profile-trophy.vercel.app`) | ❌ **402** |
| ~~Contributor stats~~ | ❌ **402** |

Three of these answer with an HTTP status a link checker calls fine while rendering
as a broken or error image to a human. The stats mirror is the worst offender: a
`200 OK` SVG whose only content is the words "Something went wrong".

### The capsule-render ampersand trap

Worth writing down, because no link checker will ever catch it:
**never put a raw `&` (`%26`) in a capsule-render `text=` or `desc=` parameter.**

capsule-render interpolates those values into the SVG without escaping them, so
`%26` comes back as a bare `&` — an invalid XML token. Browsers reject the entire
document and render the alt text; `curl` reports a perfectly healthy `200` with a
2.6 KB body that looks like valid SVG. That's exactly what happened to the header
banner: it passed every status check and was still broken on the live page.

The tell, if a banner ever renders as alt text again:

```bash
curl -s "<the capsule-render url>" -o /tmp/h.svg
python -c "import xml.dom.minidom;xml.dom.minidom.parse('/tmp/h.svg');print('XML OK')"
```

`not well-formed (invalid token)` means an unescaped character got through. Reword to
avoid it — the current header uses "Fullstack and Mobile Developer" for this reason.
The same applies to `<`, `>` and `"`.

### The typing SVG

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

**No project list in the README.** GitHub renders your pinned repositories directly
below it, and those cards keep their own descriptions, languages and star counts
current. A hand-maintained list beside them is a second copy to keep in sync, and
it's always the copy that goes stale. The README answers *who* and *how*; the pins
answer *what*. See step 6 — this only works if you actually pin.

For the record, image-based repo cards aren't an option either way: the
`github-readme-stats` pin endpoint is 503, so those render broken for every visitor.

**A "How I Work" section instead.** Pinned repos already show what was built. What a
reader can't get by clicking through is the approach — offline-first defaults, RTL
from the first screen, a domain layer that doesn't import the framework, strict
analyzer gates. Every line there is falsifiable against the code, and it has to stay
that way: vague principles ("passionate about clean code") are worse than no section
at all.

**The stack is trimmed to what's in the repos.** Every badge is backed by shipped
code. A wall of sixty logos where four are real is the single most common way a
profile README loses a reader who knows what they're looking at.

**Skipped: ASCII skill bars.** Percentages like "Python ██████████ 90%" are
self-assigned and every experienced reader knows it. The language cards say the same
thing with real data.

**Skipped: WakaTime and Spotify.** Both need external accounts plus a token in repo
secrets. Worth revisiting once the daily coding hours are worth showing.

**Theme awareness.** The snake and the 3D calendar both use `<picture>` with
`prefers-color-scheme`, so light-mode visitors don't get a dark rectangle floating
on a white page.

**`alt` text everywhere.** Screen readers, and a graceful fallback whenever one of
the services above has its next bad day.
