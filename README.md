<!--
  ===============================================================
  GitHub Profile README — Poasherkir (Malik Boudine)
  Setup + maintenance notes live in SETUP.md

  Deliberately contains no repo listings. GitHub's own pinned
  repositories render directly below this README and stay current
  on their own — duplicating them here just creates a second list
  to keep in sync. Pin your six best instead: SETUP.md step 6.

  NOTE: never put a raw "&" (%26) in a capsule-render text= or
  desc= parameter. It interpolates unescaped, producing invalid
  XML that browsers refuse to render while curl still reports 200.
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
  <a href="#-how-i-work">How I Work</a> &nbsp;·&nbsp;
  <a href="#-tech-stack">Stack</a> &nbsp;·&nbsp;
  <a href="#-github-analytics">Analytics</a> &nbsp;·&nbsp;
  <a href="#-contribution-graph">Contributions</a> &nbsp;·&nbsp;
  <a href="#-lets-connect">Contact</a>
</p>

<br />

<!-- ─────────────  ABOUT ME  ───────────── -->
## 👋 About Me

<img align="right" width="260" src="https://github.com/Poasherkir.png" alt="Malik Boudine avatar" />

Computer Science student in **Algeria** 🇩🇿. I build software for the conditions
most apps quietly assume away — no signal, a cheap Android phone, a language that
reads right to left.

- 📱 &nbsp;**Flutter** for mobile — offline-first, encrypted local storage, Arabic RTL as a first-class case rather than an afterthought
- 🌐 &nbsp;**Next.js + TypeScript** for the web — App Router, React 19, Tailwind, and three.js when the page earns it
- 🐍 &nbsp;**Python** for the unglamorous half — importers, scrapers and one-shot migrations that move real archives around
- 🔒 &nbsp;Some of my production work is closed-source — **Briefing Point Go**, **TechSub** and a set of aviation services that hold real user data. [Case studies on my site.](https://malikboudine.vercel.app)
- 🤝 &nbsp;Open to internships, freelance work, and collaboration on anything offline-first
- 📫 &nbsp;**malikboudinee1e@gmail.com**

<br clear="right" />

<br />

<!-- ─────────────  HOW I WORK  ───────────── -->
## 🧭 How I Work

<!--
  This section replaces the old project catalogue. Pinned repos already show
  *what* was built; this says *how*, which is the part a reader can't get by
  clicking through. Keep it to five, keep every line falsifiable.
-->

**Offline is the default, not the fallback.** &nbsp;I design as if the network will
never arrive: sync once, then everything reads from local storage. If that storage
holds anything personal it's encrypted at rest — SQLCipher, not a plaintext SQLite
file with good intentions.

**Arabic and French from the first screen.** &nbsp;RTL is not a late-stage flag.
Layouts that get it retrofitted leak somewhere — a stray `EdgeInsets.only(left:)`,
a chevron pointing the wrong way — and every one of those leaks is a bug a user
notices before I do.

**The domain layer doesn't know the framework exists.** &nbsp;Business rules import
nothing from Flutter, nothing from the database, nothing from an HTTP client. It
keeps the interesting logic testable without a device, and it makes swapping the
edges cheap.

**Tests are a gate, not a chore.** &nbsp;A strict analyzer that fails on infos, a
schema dumped and migration-tested rather than assumed, and guards that read
constraints back out of the database so a missing foreign key can't hide. A demo
that only works on my machine isn't finished.

**Build for the low end.** &nbsp;Cheap hardware and slow connections are the target,
not the edge case. Bundle size, cold-start time and battery are features where I'm
from.

<br />

<!-- ─────────────  TECH STACK  ───────────── -->
## 🧰 Tech Stack

<!--
  Kept close to what's actually shipped. A short honest stack reads far better
  than a wall of sixty logos, and a reader who knows the field can tell.

  Not listed, because nothing here uses them yet — paste any back if that changes:
  Java, Ruby, Vue.js, NestJS, TensorFlow, NumPy, Pandas, Seaborn,
  AWS, Google Cloud, Azure, MySQL, Solidity.
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

**Tooling & Infrastructure**

<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" alt="PowerShell" />
</p>

<sub>**Learning next** &nbsp;·&nbsp; deeper Flutter architecture &nbsp;·&nbsp; Postgres row-level security &nbsp;·&nbsp; React Three Fiber &nbsp;·&nbsp; container workflows past `docker run`</sub>

<br />

<!-- ─────────────  GITHUB STATS  ───────────── -->
## 📊 GitHub Analytics

<!--
  These point at github-profile-summary-cards, verified serving real numbers.
  Do not swap in github-readme-stats: the official instance is 503, and the
  community mirror answers 200 with an SVG reading "Maximum retries exceeded".
  The activity-graph and trophy services are both 402. See SETUP.md step 8.
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

<p align="center">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight" alt="Random developer quote" />
</p>

<br />

<!-- ─────────────  SOCIALS  ───────────── -->
## 🤝 Let's Connect

<p align="center">
  Open to <strong>internships</strong>, <strong>freelance work</strong>, and collaboration on anything offline-first.<br />
  My work is pinned below — the deployed pieces and the case studies live on my site.
</p>

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
