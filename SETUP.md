# Setup — how to make this your GitHub profile

## 1. & 2. Repository created and pushed ✅

Already done for you. The repo is https://github.com/Poasherkir/Poasherkir and the
README is live on your profile.

For reference, the reason the name matters: GitHub only renders a README on your
profile page if it lives in a **public repository named exactly your username**.
That's why this one is called `Poasherkir` and not `portfolio`.

The steps below are the parts I can't do from here — they need your browser.

## 3. Turn on private contribution counting

The stats and streak cards can only see what the API exposes. By default that
excludes private repos, which for a new account means everything reads as zero.

Go to **Settings → Profile** and tick
**"Include private contributions on my profile"**:
https://github.com/settings/profile

The README already passes `count_private=true` and `include_all_commits=true`, so
once that box is ticked the numbers fill in on their own.

## 4. Run the snake workflow once

Actions are not allowed to write to your repo until you permit it:

1. Repo → **Settings → Actions → General**
2. Under **Workflow permissions**, choose **Read and write permissions** → Save
3. Repo → **Actions** tab → **Generate contribution snake** → **Run workflow**

It creates an `output` branch holding the SVGs. After that it re-runs itself every
12 hours, so the animation stays current with no work from you.

The 3D calendar workflow (`3d-contrib.yml`) works the same way but writes into a
`profile-3d-contrib/` folder on `main`. It is not referenced in the README yet — if
you want it, run it once and then add:

```md
<p align="center">
  <img src="./profile-3d-contrib/profile-night-rainbow.svg" alt="3D contribution calendar" />
</p>
```

If you'd rather not have it, delete `.github/workflows/3d-contrib.yml`.

## 5. Fill in the placeholders

Search the README for `EDIT` — every spot needing your input is marked:

| Where | What to change |
| :-- | :-- |
| About Me | The six bullets. Make them true — this is the part people actually read. |
| Tech Stack | **Delete** badges for things you don't use. See the note below. |
| Featured Projects | Uncomment the cards and use real repo names once you have some. |
| Learning Roadmap | Move rows between ✅ / 🔄 / 🔜 to match reality. |
| Let's Connect | Optional — LinkedIn/X/Discord badges are commented out. Uncomment and fill in only the ones you actually use. |

## 6. Pin your best repositories

The Featured Projects cards complement GitHub's own pinning — they don't replace it.
On your profile, click **Customize your pins** and choose up to six.

---

## 7. Recommended: host your own stats cards

I tested every image URL in the README before shipping it. Here is what came back:

| Service | Status |
| :-- | :-- |
| Typing SVG (`readme-typing-svg.demolab.com`) | ✅ 200 |
| Streak (`github-readme-streak-stats.herokuapp.com`) | ✅ 200 |
| Activity graph | ✅ 200 |
| Capsule-render header/footer | ✅ 200 |
| Dev quote | ✅ 200 |
| Visitor counter, shields.io badges, avatar | ✅ 200 |
| Stats + top-languages (`…-sigma-five.vercel.app` mirror) | ✅ 200, real data |
| ~~Stats~~ (official `github-readme-stats.vercel.app`) | ❌ **503 DEPLOYMENT_PAUSED** |
| ~~Trophy wall~~ (`github-profile-trophy.vercel.app`) | ❌ **402** |
| ~~`github-profile-summary-cards`~~ | ❌ 200 but body is "rate limited" error |

Two of the most-recommended services are simply broken right now, which is why the
README doesn't use them:

- **The official stats instance returns `DEPLOYMENT_PAUSED`.** Not a rate limit —
  the deployment is switched off. Every profile using the standard
  `github-readme-stats.vercel.app` URL currently shows two broken images.
- **The trophy wall returns 402**, meaning its Vercel spending limit is exhausted.
  It's commented out in the README.
- **`github-profile-summary-cards`** is the sneakiest: it answers `200 OK` with an
  SVG that just says "Cards are temporarily rate limited." It looks fine to a link
  checker and broken to a human.

Your stats cards therefore point at `github-readme-stats-sigma-five.vercel.app`, a
community mirror of the same project that I verified is serving your real numbers.
It works today, but it's someone else's hobby deployment and could go the same way.

**The durable fix is your own deployment** — five minutes, free, and it can never be
rate-limited because you're its only user:

1. Fork https://github.com/anuraghazra/github-readme-stats
2. Create a GitHub personal access token with **no scopes** at
   https://github.com/settings/tokens (a classic token, nothing ticked — it only
   needs to lift the anonymous API rate limit)
3. Import the fork at https://vercel.com/new, add an environment variable
   `PAT_1` set to that token, and deploy
4. In the README, replace both occurrences of
   `github-readme-stats-sigma-five.vercel.app` with your own `your-project.vercel.app`

Your cards then load every time, and the trophy wall can be revived the same way by
deploying `ryo-ma/github-profile-trophy`.

---

## Notes on what I changed from the original list

**Dead and duplicate services.** `readme-typing-svg.herokuapp.com` stopped working
when Heroku ended its free tier; the maintained host is `readme-typing-svg.demolab.com`.

For the streak card I used `github-readme-streak-stats.herokuapp.com` rather than the
`streak-stats.demolab.com` you'll see in most guides. Both belong to the same project;
I could only verify the herokuapp one responding from here, so that's what shipped. If
it ever breaks, swapping in the demolab hostname is a drop-in replacement — the query
parameters are identical.

**Skipped: the ASCII skill bars.** Percentages like "Python ██████████ 90%" are
self-assigned and every experienced reader knows it. The roadmap table says the same
thing honestly, and the top-languages card says it with real data.

**Skipped: WakaTime and Spotify.** Both need external accounts and a token in repo
secrets, and a WakaTime block that reads "0 hrs this week" hurts more than it helps.
Worth adding later once you're coding daily — say the word and I'll wire them up.

**Replaced the Giphy banner** with a `capsule-render` gradient header. A random
looping GIF dates a profile fast; the gradient matches the accent colour used
everywhere else.

**Added theme awareness.** The snake uses a `<picture>` element with
`prefers-color-scheme`, so visitors in light mode get a light SVG instead of a dark
rectangle floating on a white page.

**Added `cache_seconds=86400` and `hide_border=true`.** A long cache makes the stats
cards far more likely to load off the shared instance. See step 7 for the real fix.

**Added `alt` text everywhere.** Screen readers, and a graceful fallback when a card
service is down.

---

## One honest caveat

Your account currently has **0 public repositories and 0 followers**. The stats,
streak, trophy and activity cards will all render as empty or zero until you push
real work — the trophy wall in particular will show nothing but "Unranked".

That isn't a problem with the README. Ship two or three projects you care about,
pin them, and this profile fills itself in. Until then, consider commenting out the
trophy and Featured Projects sections so the page doesn't advertise the emptiness.
