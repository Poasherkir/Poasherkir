<!--
  ===============================================================
  GitHub Profile README — Poasherkir (Malik Boudine)
  Setup + maintenance notes live in SETUP.md

  PALETTE (keep these three in sync everywhere):
    violet  #7B2FF7      pink  #F72585      cyan  #00D9FF
    ground  #0D1117 (GitHub dark)
  Card services all use theme=radical, which is built on the same
  pink/cyan pair — swap the theme and the page stops matching.

  Deliberately contains no repo listings. GitHub's pinned
  repositories render directly below and stay current on their own.

  GOTCHAS, both learned the hard way — see SETUP.md step 8:
   1. Never put a raw "&" (%26) in a capsule-render text=/desc=.
      It interpolates unescaped, producing invalid XML that browsers
      refuse to render while curl still reports a healthy 200.
   2. readme-typing-svg takes ONE colour. A comma-separated list is
      silently ignored and it falls back to default blue.
  ===============================================================
-->

<!-- ─────────────  HEADER  ───────────── -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F0C29,35:302B63,70:F72585,100:00D9FF&height=210&section=header&text=Malik%20Boudine&fontSize=54&fontColor=ffffff&fontAlignY=34&desc=Fullstack%20and%20Mobile%20Developer%20%C2%B7%20Flutter%20%C2%B7%20Next.js&descAlignY=54&descSize=18&animation=fadeIn" alt="Malik Boudine — Fullstack and Mobile Developer" width="100%" />

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=27&pause=1100&color=00D9FF&center=true&vCenter=true&width=720&height=45&lines=Fullstack+and+Mobile+Developer;Flutter+%C2%B7+Next.js+%C2%B7+TypeScript;Offline-first+apps+for+Algeria;3D+on+the+web+with+three.js;Computer+Science+student" alt="Fullstack and mobile developer — Flutter, Next.js, TypeScript, offline-first apps, 3D on the web" />
</p>

<p align="center">
  <a href="https://malikboudine.vercel.app"><img src="https://img.shields.io/badge/PORTFOLIO-malikboudine.vercel.app-00D9FF?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0D1117" alt="Portfolio — malikboudine.vercel.app" /></a>
  <a href="mailto:malikboudinee1e@gmail.com"><img src="https://img.shields.io/badge/EMAIL-say%20hello-F72585?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117" alt="Email me" /></a>
  <a href="https://github.com/Poasherkir?tab=repositories"><img src="https://img.shields.io/badge/dynamic/json?url=https://api.github.com/users/Poasherkir&query=public_repos&label=REPOS&style=for-the-badge&color=7B2FF7&labelColor=0D1117" alt="Public repositories" /></a>
  <a href="https://github.com/Poasherkir?tab=followers"><img src="https://img.shields.io/github/followers/Poasherkir?label=FOLLOWERS&style=for-the-badge&color=7B2FF7&labelColor=0D1117" alt="Followers" /></a>
  <img src="https://komarev.com/ghpvc/?username=Poasherkir&label=VIEWS&color=00D9FF&style=for-the-badge" alt="Profile views" />
</p>

<p align="center">
  <a href="#-about-me"><b>About</b></a> &nbsp;•&nbsp;
  <a href="#-how-i-work"><b>How I Work</b></a> &nbsp;•&nbsp;
  <a href="#-tech-stack"><b>Stack</b></a> &nbsp;•&nbsp;
  <a href="#-github-analytics"><b>Analytics</b></a> &nbsp;•&nbsp;
  <a href="#-contribution-graph"><b>Contributions</b></a> &nbsp;•&nbsp;
  <a href="#-lets-connect"><b>Contact</b></a>
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:7B2FF7,50:F72585,100:00D9FF&height=4" width="100%" alt="" />

<!-- ─────────────  ABOUT ME  ───────────── -->
## 👋 About Me

<img align="right" width="250" src="https://github.com/Poasherkir.png" alt="Malik Boudine avatar" />

Computer Science student in **Algeria** 🇩🇿. I build software for the conditions most
apps quietly assume away — no signal, a cheap Android phone, a language that reads
right to left.

&nbsp;📱&nbsp; **Flutter** for mobile — offline-first, encrypted local storage, Arabic RTL as a first-class case rather than an afterthought

&nbsp;🌐&nbsp; **Next.js + TypeScript** for the web — App Router, React 19, Tailwind, and three.js when the page earns it

&nbsp;🐍&nbsp; **Python** for the unglamorous half — importers, scrapers and one-shot migrations that move real archives around

&nbsp;🔒&nbsp; Production work that stays closed — **Briefing Point Go**, **TechSub** and a set of aviation services holding real user data. [Case studies on my site.](https://malikboudine.vercel.app)

&nbsp;🤝&nbsp; Open to **internships**, **freelance work**, and anything offline-first

&nbsp;📫&nbsp; **malikboudinee1e@gmail.com**

<br clear="right" />

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:00D9FF,50:F72585,100:7B2FF7&height=4" width="100%" alt="" />

<!-- ─────────────  HOW I WORK  ───────────── -->
## 🧭 How I Work

<!--
  This replaces the old project catalogue. Pinned repos already show *what* was
  built; this says *how*, which is what a reader can't get by clicking through.
  Keep it to five, and keep every line falsifiable against the code.
-->

> **Offline is the default, not the fallback.**
> I design as if the network will never arrive: sync once, then everything reads from
> local storage — encrypted at rest when it holds anything personal. SQLCipher, not a
> plaintext SQLite file with good intentions.

> **Arabic and French from the first screen.**
> RTL is not a late-stage flag. Layouts that get it retrofitted always leak somewhere
> — a stray `EdgeInsets.only(left:)`, a chevron pointing the wrong way — and every one
> of those is a bug a user notices before I do.

> **The domain layer doesn't know the framework exists.**
> Business rules import nothing from Flutter, nothing from the database, nothing from
> an HTTP client. The interesting logic stays testable without a device, and swapping
> the edges stays cheap.

> **Tests are a gate, not a chore.**
> A strict analyzer that fails on infos, a schema dumped and migration-tested rather
> than assumed, and guards that read constraints back out of the database so a missing
> foreign key can't hide. A demo that only works on my machine isn't finished.

> **Build for the low end.**
> Cheap hardware and slow connections are the target, not the edge case. Bundle size,
> cold-start time and battery are features where I'm from.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:7B2FF7,50:F72585,100:00D9FF&height=4" width="100%" alt="" />

<!-- ─────────────  TECH STACK  ───────────── -->
## 🧰 Tech Stack

<!--
  skillicons.dev instead of shields rows: same information, a fraction of the
  vertical space, and it actually looks alive. Every slug below was verified to
  resolve — an unknown slug renders as a blank tile, so check before adding.

  Not listed, because nothing here uses them yet — add the slug if that changes:
  java, ruby, vue, nestjs, tensorflow, aws, gcp, azure, mysql, solidity.
-->

<table align="center">
<tr><td align="center" width="150"><b>Languages</b></td><td>
  <img src="https://skillicons.dev/icons?i=dart,ts,js,python,c&theme=dark" alt="Dart, TypeScript, JavaScript, Python, C" />
</td></tr>
<tr><td align="center"><b>Mobile</b></td><td>
  <img src="https://skillicons.dev/icons?i=flutter,sqlite&theme=dark" alt="Flutter, SQLite" />
  &nbsp;<sub>+ Riverpod · Drift · SQLCipher</sub>
</td></tr>
<tr><td align="center"><b>Web</b></td><td>
  <img src="https://skillicons.dev/icons?i=nextjs,react,tailwind,threejs,html,css&theme=dark" alt="Next.js, React, Tailwind CSS, three.js, HTML, CSS" />
  &nbsp;<sub>+ GSAP</sub>
</td></tr>
<tr><td align="center"><b>Backend</b></td><td>
  <img src="https://skillicons.dev/icons?i=supabase,postgres,nodejs&theme=dark" alt="Supabase, PostgreSQL, Node.js" />
</td></tr>
<tr><td align="center"><b>Tooling</b></td><td>
  <img src="https://skillicons.dev/icons?i=docker,git,githubactions,vercel,linux,powershell&theme=dark" alt="Docker, Git, GitHub Actions, Vercel, Linux, PowerShell" />
</td></tr>
</table>

<p align="center"><sub><b>Learning next</b> &nbsp;•&nbsp; deeper Flutter architecture &nbsp;•&nbsp; Postgres row-level security &nbsp;•&nbsp; React Three Fiber &nbsp;•&nbsp; container workflows past <code>docker run</code></sub></p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:00D9FF,50:F72585,100:7B2FF7&height=4" width="100%" alt="" />

<!-- ─────────────  GITHUB STATS  ───────────── -->
## 📊 GitHub Analytics

<!--
  github-profile-summary-cards, verified serving real numbers.
  Do NOT swap in github-readme-stats: the official instance is 503, and the
  community mirror answers 200 with an SVG reading "Maximum retries exceeded".
  The activity-graph and trophy services are both 402. See SETUP.md step 8.
-->

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Poasherkir&theme=radical" alt="Profile summary: total contributions, public repos and contribution timeline" width="98%" />
</p>

<p align="center">
  <img height="195em" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Poasherkir&theme=radical" alt="Top languages by repository" />
  <img height="195em" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=Poasherkir&theme=radical" alt="Most used languages by commit" />
</p>

<p align="center">
  <img height="195em" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Poasherkir&theme=radical" alt="Stars, commits, pull requests and issues" />
  <img height="195em" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=Poasherkir&theme=radical&utcOffset=1" alt="Commits by time of day" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=Poasherkir&theme=radical&hide_border=true&background=0D1117&date_format=j%20M%5B%20Y%5D" alt="Contribution streak: current and longest" />
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:7B2FF7,50:F72585,100:00D9FF&height=4" width="100%" alt="" />

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

<p align="center">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical" alt="Random developer quote" />
</p>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:00D9FF,50:F72585,100:7B2FF7&height=4" width="100%" alt="" />

<!-- ─────────────  SOCIALS  ───────────── -->
## 🤝 Let's Connect

<p align="center">
  Open to <b>internships</b>, <b>freelance work</b>, and collaboration on anything offline-first.<br />
  My work is pinned just below — the deployed pieces and the case studies live on my site.
</p>

<p align="center">
  <a href="https://malikboudine.vercel.app"><img src="https://img.shields.io/badge/PORTFOLIO-00D9FF?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0D1117" alt="Portfolio" /></a>
  <a href="mailto:malikboudinee1e@gmail.com"><img src="https://img.shields.io/badge/EMAIL-F72585?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D1117" alt="Email" /></a>
  <a href="https://github.com/Poasherkir"><img src="https://img.shields.io/badge/GITHUB-7B2FF7?style=for-the-badge&logo=github&logoColor=white&labelColor=0D1117" alt="GitHub" /></a>
</p>

<!--
  EDIT: add your other profiles here once you want them public. Left out rather
  than shipping dead placeholder links — a badge pointing at
  linkedin.com/in/YOUR-HANDLE is worse than no badge.

  <a href="https://linkedin.com/in/YOUR-HANDLE"><img src="https://img.shields.io/badge/LINKEDIN-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0D1117" alt="LinkedIn" /></a>
  <a href="https://x.com/YOUR-HANDLE"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white&labelColor=0D1117" alt="X" /></a>
-->

<p align="center"><sub>Thanks for scrolling this far. If something here is useful to you, say hello.</sub></p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00D9FF,30:F72585,65:302B63,100:0F0C29&height=140&section=footer" alt="" width="100%" />
