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

## 4. The four workflows ✅

All four run on the built-in `GITHUB_TOKEN`, all are green, and every graphic in
the README below the badges comes from one of them. Nothing to do here.

| Workflow | Runs | Writes to | Used by the README as |
| :-- | :-- | :-- | :-- |
| `summary-cards.yml` | 06:00 UTC daily | `profile-summary-card-output/radical/` on `main` | the five Analytics cards, via relative paths |
| `arcade.yml` | 06:30 UTC daily + every push | `arcade` branch | Pac-Man, via absolute `raw.githubusercontent.com` URLs |
| `snake.yml` | every 12 h + every push | `output` branch | the snake, same way |
| `3d-contrib.yml` | 18:00 UTC daily | `profile-3d-contrib/` on `main` | the 3D calendar, via relative paths |

The schedules are staggered on purpose so no two ever push to `main` at the same
moment, and `summary-cards.yml` pulls with rebase before it pushes for the same
reason.

**Why everything is self-hosted.** Anything served by a third-party image API
eventually rate-limits or goes dark — the summary-cards service did exactly that
nine days after the README first used it, answering `200 OK` with a card that just
says `ERROR!!!`. A file committed into this repo can't do that. The only remaining
hosted images are the header/footer gradients, the shields badges, the typing line,
the streak card and the quote, each of which is one image and degrades to alt text.

**Spares already generated, unused.** `arcade.yml` also produces a **Breakout**
animation (`breakout-contribution-graph.svg` / `-dark.svg` on the `arcade`
branch), and `3d-contrib.yml` produces nine other calendar variants in
`profile-3d-contrib/` — `profile-gitblock.svg` is the most different-looking.
Swap filenames in the relevant `<picture>` block to use any of them.

**Cards use the `load` animation.** It's baked into the SVG as CSS, so it plays
inside a GitHub README with no JavaScript. Other options in `summary-cards.yml`:
`fade`, `rise`, `draw`, `stagger`, `sequence`, `tint`, `rgb`, `rgb-soft`, or `none`.

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
drift out of date the way a hand-written list does. All six repos now carry a
description, so no pinned card renders with a blank subtitle.

`Poasherkir` — this repo — is deliberately left unpinned. It holds the profile
README, not a project, so pinning it would spend a slot showing nothing built.

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
first written have since broken, which is why every card that can be generated by a
workflow now is.

### Currently used, verified serving real data

| Service | Status |
| :-- | :-- |
| Analytics cards (`profile-summary-card-output/`) | ✅ in-repo, can't break |
| Pac-Man (`arcade` branch) | ✅ 200, self-hosted |
| Streak (`github-readme-streak-stats.herokuapp.com`) | ✅ 200 |
| Header, footer, dividers (`assets/*.svg`) | ✅ in-repo, hand-authored, can't break |
| Stack icon strips (`assets/stack/*.svg`) | ✅ in-repo copies of skillicons.dev renders, can't break |
| Dev quote (`quotes-github-readme.vercel.app`) | ✅ 200 |
| Visitor counter, shields.io badges, avatar | ✅ 200 |
| Snake SVGs (`output` branch) | ✅ 200, self-hosted |
| 3D calendar (`profile-3d-contrib/`) | ✅ in-repo, can't break |

### Deliberately not used

| Service | Status |
| :-- | :-- |
| ~~`github-profile-summary-cards.vercel.app`~~ (hosted API) | ❌ 200 with an `ERROR!!! Cards are temporarily rate limited` card — replaced by the in-repo workflow |
| ~~Stats + top-langs~~ (official `github-readme-stats.vercel.app`) | ❌ **503 DEPLOYMENT_PAUSED** |
| ~~Stats mirror~~ (`…-sigma-five.vercel.app`) | ❌ 200 with an error card: *"Maximum retries exceeded — add PAT_1"* |
| ~~Repo pin cards~~ (same host as stats) | ❌ 503 — image repo cards are not an option |
| ~~Activity graph~~ (`github-readme-activity-graph.vercel.app`) | ❌ **402** — Vercel spending limit exhausted |
| ~~Trophy wall~~ (`github-profile-trophy.vercel.app`) | ❌ **402** |
| ~~Contributor stats~~ | ❌ **402** |
| ~~Typing SVG~~ (`readme-typing-svg.demolab.com`) | ⚠️ works, but rate-limits after a few requests and then renders as a blank gap — replaced by the taglines baked into `assets/header.svg` |
| ~~skillicons.dev~~ (live) | ⚠️ works, but was unreachable for a stretch — strips are now saved into `assets/stack/`; refetch one only when adding a tool |
| ~~Capsule-render~~ (header/footer/dividers) | ⚠️ works, but interpolates `text=`/`desc=` into the SVG unescaped: a `%26` becomes a bare `&`, the XML is invalid, browsers render alt text while `curl` reports 200 — replaced by `assets/` |

Four of these answer with an HTTP status a link checker calls fine while rendering
as a broken or error image to a human. The stats mirror is the worst offender: a
`200 OK` SVG whose only content is the words "Something went wrong".

### The space header, footer and dividers

`assets/header.svg`, `assets/footer.svg` and `assets/divider.svg` are hand-authored:
a deep-space gradient, three drifting nebulae in the palette colours, a three-layer
twinkling starfield, two shooting stars, a ringed planet and a distant moon. The
footer is a planet horizon; the divider is a thin gradient line with a comet that
travels along it. Everything is pure SVG plus CSS `@keyframes`, which run inside a
README `<img>` (JavaScript would not). No fonts or images are fetched — the files
are fully self-contained, so they render identically through GitHub's image proxy.

To change the name, the subtitle or the five rotating taglines, edit the `<text>`
elements near the bottom of `assets/header.svg`. Each tagline is visible for about
three seconds of a fifteen-second cycle; keep them under ~45 characters so they fit
at phone width.

Two rules for editing any of them: keep every `&` written as `&amp;` (raw `&` is the
exact bug that broke the old header), and re-run the XML check below after saving.

```bash
python -c "import xml.dom.minidom;xml.dom.minidom.parse('assets/header.svg');print('XML OK')"
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
