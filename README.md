<!--
  ===============================================================
  GitHub Profile README — Poasherkir (Malik Boudine)
  Setup + maintenance notes live in SETUP.md
  Every image URL in this file was verified live before committing.
  ===============================================================
-->

<!-- ─────────────  HEADER  ───────────── -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:2C5364,100:00C7FF&height=200&section=header&text=Malik%20Boudine&fontSize=52&fontColor=ffffff&fontAlignY=35&desc=Fullstack%20and%20Mobile%20Developer%20%C2%B7%20Flutter%20%C2%B7%20Next.js&descAlignY=55&descSize=18&animation=fadeIn" alt="Malik Boudine — Fullstack and Mobile Developer" width="100%" />

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&pause=1200&color=00C7FF&center=true&vCenter=true&width=700&lines=Fullstack+and+Mobile+Developer;Flutter+%C2%B7+Next.js+%C2%B7+TypeScript;Offline-first+apps+for+Algeria;3D+on+the+web+with+three.js;Computer+Science+student" alt="Fullstack and mobile developer — Flutter, Next.js, TypeScript, offline-first apps, 3D on the web" />
</p>

<p align="center">
  <a href="https://malikboudine.vercel.app"><img src="https://img.shields.io/badge/Portfolio-malikboudine.vercel.app-00C7FF?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0D1117" alt="Portfolio — malikboudine.vercel.app" /></a>
  <a href="mailto:malikboudinee1e@gmail.com"><img src="https://img.shields.io/badge/Email-Say%20hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117" alt="Email me" /></a>
  <a href="https://github.com/Poasherkir?tab=repositories"><img src="https://img.shields.io/badge/dynamic/json?url=https://api.github.com/users/Poasherkir&query=public_repos&label=Repos&style=for-the-badge&color=00C7FF&labelColor=0D1117" alt="Public repositories" /></a>
  <a href="https://github.com/Poasherkir?tab=followers"><img src="https://img.shields.io/github/followers/Poasherkir?label=Followers&style=for-the-badge&color=00C7FF&labelColor=0D1117" alt="Followers" /></a>
  <img src="https://komarev.com/ghpvc/?username=Poasherkir&label=Profile%20views&color=00C7FF&style=for-the-badge" alt="Profile views" />
</p>

<p align="center">
  <a href="#-about-me">About</a> &nbsp;·&nbsp;
  <a href="#-featured-projects">Projects</a> &nbsp;·&nbsp;
  <a href="#-tech-stack">Stack</a> &nbsp;·&nbsp;
  <a href="#-github-analytics">Analytics</a> &nbsp;·&nbsp;
  <a href="#-currently-building">Now</a> &nbsp;·&nbsp;
  <a href="#-lets-connect">Contact</a>
</p>

<br />

<!-- ─────────────  ABOUT ME  ───────────── -->
## 👋 About Me

<img align="right" width="260" src="https://github.com/Poasherkir.png" alt="Malik Boudine avatar" />

Computer Science student in **Algeria** 🇩🇿, building things people actually use on
bad connections and cheap Android phones.

- 📱 &nbsp;**Flutter** for mobile — offline-first, encrypted local storage, Arabic RTL as a first-class case rather than an afterthought
- 🌐 &nbsp;**Next.js + TypeScript** for the web — App Router, React 19, Tailwind, and three.js when the page earns it
- 🧪 &nbsp;I care about the boring parts: 574 green tests and a clean analyzer beat a demo that only works on my machine
- 🔒 &nbsp;Some of my production work is closed-source — **Briefing Point Go**, **TechSub** and a set of aviation services that hold real user data. [Case studies here.](https://malikboudine.vercel.app)
- 🤝 &nbsp;Happy to collaborate on anything offline-first, Flutter, or unreasonably fun 3D on the web
- 📫 &nbsp;**malikboudinee1e@gmail.com**

<br clear="right" />

<br />

<!-- ─────────────  FEATURED PROJECTS  ───────────── -->
## 🚀 Featured Projects

<!--
  Written by hand on purpose. The github-readme-stats "pin card" service is
  returning 503 right now, so image-based repo cards render broken for everyone.
  These links can't break, they say more, and they read fine on a phone.
-->

### 🚚 [Delivery OS](https://github.com/Poasherkir/delivery-os) &nbsp;·&nbsp; offline-first Flutter app for Algerian delivery drivers

Takes the daily batch of orders a *livreur* collects, optimizes the route, tracks
every delivery attempt, and reconciles the money down to the dinar. The driver is
the user — one person at a door, often with no signal — so **nothing needs the
network**. Arabic ↔ French with real RTL from the first screen, on an encrypted
SQLCipher database.

<sub>**574 tests green** &nbsp;·&nbsp; analyzer clean under <code>--fatal-infos</code> &nbsp;·&nbsp; 20-table schema, migration-tested</sub>

<p>
  <img src="https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white" alt="Dart" />
  <img src="https://img.shields.io/badge/Riverpod_3-1C1C1C?style=flat-square" alt="Riverpod 3" />
  <img src="https://img.shields.io/badge/Drift_%2F_SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="Drift over SQLite" />
  <img src="https://img.shields.io/badge/SQLCipher-4B0082?style=flat-square" alt="SQLCipher" />
  <img src="https://img.shields.io/badge/go__router-1C1C1C?style=flat-square" alt="go_router" />
</p>

---

### 📚 [BAC Archive — أرشيف البكالوريا](https://github.com/Poasherkir/bac-archive) &nbsp;·&nbsp; every Algerian BAC paper, 2008–2026, fully offline

Exams, official answers and model answers for the **علوم تجريبية** (Experimental
Sciences) stream. Students sync once, then read every paper with zero internet.
Three parts on one Supabase backend: the Flutter app, a web admin dashboard so the
owner never has to touch code, and a Python bulk importer.

<sub>**171 entries / 343 PDFs (~312 MB)** &nbsp;·&nbsp; 19 years &nbsp;·&nbsp; 9 subjects &nbsp;·&nbsp; Arabic RTL, built-in PDF viewer, dark mode</sub>

<p>
  <img src="https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white" alt="Supabase" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Riverpod-1C1C1C?style=flat-square" alt="Riverpod" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
</p>

---

### 🎹 [Portfolio](https://github.com/Poasherkir/portfolio) &nbsp;·&nbsp; a site built around an interactive 3D keyboard

Every keycap is a technology I actually ship with. One long Next.js 15 page that
argues a case in order — claim, evidence, the single best proof in depth, then the
rest of the work. Scroll-driven choreography with GSAP + ScrollTrigger, Lenis for
smooth scroll, and a contact form validated with Zod before it ever reaches the
mail API.

<sub>🔗 **Live at [malikboudine.vercel.app](https://malikboudine.vercel.app)**</sub>

<p>
  <img src="https://img.shields.io/badge/Next.js_15-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 15" />
  <img src="https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React 19" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/three.js-000000?style=flat-square&logo=threedotjs&logoColor=white" alt="three.js" />
  <img src="https://img.shields.io/badge/GSAP-88CE02?style=flat-square&logo=greensock&logoColor=black" alt="GSAP" />
</p>

<br />

**Also on my GitHub**

| Project | What it is | Built with |
| :-- | :-- | :-- |
| [**Playlist**](https://github.com/Poasherkir/Playlist) · [live ↗](https://playlist-downloader-eight.vercel.app) | One-click playlist downloader: a PowerShell engine behind a plain-HTML front end and a `.bat` launcher, so it runs on a stock Windows box with nothing installed. | PowerShell · HTML · Vercel |
| [**Wordle Solver**](https://github.com/Poasherkir/wordle-solver) | Wordle in C — a playable mode, an automatic solver, and a benchmark that runs the solver across the whole dictionary. | C · Make |
| [**Qahwa Books**](https://github.com/Poasherkir/qahwa-books) | Scraper and organizer for a book archive: bulk download, then sort by year, author or prize. | Python · HTML |

<br />

<!-- ─────────────  TECH STACK  ───────────── -->
## 🧰 Tech Stack

<!--
  Kept to what's actually in the repos above. A short honest stack reads far
  better than a wall of 60 logos, and every badge here is backed by shipped code.

  Removed from the earlier draft because nothing on this account uses them yet —
  paste any back if that changes:
  Java, Ruby, Vue.js, NestJS, TensorFlow, NumPy, Pandas, Seaborn,
  Docker, AWS, Google Cloud, Azure, MySQL, Solidity.
-->

**Languages**

<p>
  <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black" alt="C" />
</p>

**Mobile**

<p>
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Riverpod-0D1117?style=for-the-badge&logo=dart&logoColor=00C7FF" alt="Riverpod" />
  <img src="https://img.shields.io/badge/Drift-0D1117?style=for-the-badge&logo=sqlite&logoColor=00C7FF" alt="Drift" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
</p>

**Web**

<p>
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/three.js-000000?style=for-the-badge&logo=threedotjs&logoColor=white" alt="three.js" />
  <img src="https://img.shields.io/badge/GSAP-88CE02?style=for-the-badge&logo=greensock&logoColor=black" alt="GSAP" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
</p>

**Backend & Data**

<p>
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
</p>

**Tooling**

<p>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" alt="PowerShell" />
</p>

<br />

<!-- ─────────────  GITHUB STATS  ───────────── -->
## 📊 GitHub Analytics

<!--
  These point at github-profile-summary-cards, verified serving real numbers.
  The github-readme-stats mirror this section used before now returns an error
  card ("Maximum retries exceeded"), and the activity-graph service returns
  HTTP 402 — both were rendering as broken images. See SETUP.md.
-->

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Poasherkir&theme=tokyonight" alt="Profile summary: total contributions, public repos and contribution timeline" width="98%" />
</p>

<p align="center">
  <img height="200em" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Poasherkir&theme=tokyonight" alt="Top languages by repository" />
  <img height="200em" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Poasherkir&theme=tokyonight" alt="Most used languages by commit" />
</p>

<p align="center">
  <img height="200em" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Poasherkir&theme=tokyonight" alt="Stars, commits, pull requests and issues" />
  <img height="200em" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Poasherkir&theme=tokyonight&utcOffset=1" alt="Commits by time of day" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=Poasherkir&theme=tokyonight&hide_border=true&date_format=j%20M%5B%20Y%5D" alt="Contribution streak: current and longest" />
</p>

<br />

<!-- ─────────────  CONTRIBUTION GRAPHS  ───────────── -->
## 🐍 Contribution Graph

<!-- Generated by .github/workflows/snake.yml into the `output` branch -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Poasherkir/Poasherkir/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Poasherkir/Poasherkir/output/github-snake.svg" />
  <img alt="Snake eating my contribution graph" src="https://raw.githubusercontent.com/Poasherkir/Poasherkir/output/github-snake.svg" width="100%" />
</picture>

<!-- Generated by .github/workflows/3d-contrib.yml and committed to this repo, so
     it can't break the way a third-party image service can -->
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./profile-3d-contrib/profile-night-rainbow.svg" />
    <source media="(prefers-color-scheme: light)" srcset="./profile-3d-contrib/profile-green.svg" />
    <img alt="3D contribution calendar" src="./profile-3d-contrib/profile-night-rainbow.svg" width="98%" />
  </picture>
</p>

<br />

<!-- ─────────────  NOW  ───────────── -->
## 🔭 Currently Building

<!-- EDIT: keep these three rows current — this is the section people re-read -->

| | Project | Where it's at |
| :--: | :-- | :-- |
| 🚚 | [Delivery OS](https://github.com/Poasherkir/delivery-os) | Milestone **M0 — foundations**, 21 of 22 tasks done. Next up: the bundled wilaya/commune dataset, then ingestion and the money engine. |
| 📚 | [BAC Archive](https://github.com/Poasherkir/bac-archive) | Shipping — 171 entries across 19 years. Expanding subject coverage. |
| 🎹 | [Portfolio](https://malikboudine.vercel.app) | Live, and still iterating on the 3D keyboard interaction. |

**Learning next** &nbsp;·&nbsp; deeper Flutter architecture &nbsp;·&nbsp; Postgres &amp; row-level security &nbsp;·&nbsp; React Three Fiber &nbsp;·&nbsp; CI/CD beyond the basics

<br />

<p align="center">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight" alt="Random developer quote" />
</p>

<br />

<!-- ─────────────  SOCIALS  ───────────── -->
## 🤝 Let's Connect

<p align="center">
  <a href="https://malikboudine.vercel.app"><img src="https://img.shields.io/badge/Portfolio-00C7FF?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" /></a>
  <a href="mailto:malikboudinee1e@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://github.com/Poasherkir"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
</p>

<!--
  EDIT: add your other profiles here once you want them public. Left out rather
  than shipping dead placeholder links — a badge pointing at
  linkedin.com/in/YOUR-HANDLE is worse than no badge.

  <a href="https://linkedin.com/in/YOUR-HANDLE"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://x.com/YOUR-HANDLE"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="X" /></a>
-->

<p align="center"><sub>Thanks for scrolling this far. If something here is useful to you, say hello.</sub></p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00C7FF,50:2C5364,100:0F2027&height=120&section=footer" alt="" width="100%" />
