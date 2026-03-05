# README Cyberpunk Upgrade — Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Replace the current Web-Dev-Codi profile README with a neon cyberpunk-themed design that includes animated widgets, GitHub Actions-generated SVGs, and live stats.

**Architecture:** Single README.md rewrite + 2 GitHub Actions workflows (snake graph, 3D contribution calendar). All widgets are externally hosted (capsule-render, skillicons.dev, github-readme-stats, etc.) so no server infra needed.

**Tech Stack:** GitHub Markdown, shields.io, capsule-render, readme-typing-svg, skillicons.dev, github-readme-stats, github-readme-streak-stats, github-readme-activity-graph, github-profile-trophy, Platane/snk, yoshi456164/github-profile-3d-contrib, readme-jokes, komarev visitor counter.

**Color Palette:**
- Primary (hot pink):    `#FF2D78`
- Secondary (elec blue): `#00D4FF`
- Tertiary (neon green): `#00FF9C`
- Accent (deep purple):  `#7209B7`
- Background:            `#0A0A1A`

---

## Task 1: Write the complete README.md

**Files:**
- Modify: `README.md` (full rewrite)

**Content (exact, section by section):**

### 1. Capsule Render Hero (top, no div wrapper — must be first line)
```md
![Header](https://capsule-render.vercel.app/api?type=waving&color=7209B7,FF2D78,00D4FF&height=250&section=header&text=Web-Dev-Codi&fontSize=70&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Front-End%20Developer%20%7C%20Berlin%20%F0%9F%87%A9%F0%9F%87%AA&descAlignY=55&descSize=22)
```

### 2. Open centered div + Typing SVG
```md
<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=FF2D78&center=true&vCenter=true&random=false&width=600&lines=Hey+there%2C+I'm+Web-Dev-Codi+%F0%9F%91%8B;Passionate+Front-End+Developer;Building+beautiful+web+experiences+%E2%9C%A8;Always+coding%2C+always+learning+%F0%9F%9A%80;Based+in+Berlin%2C+Germany+%F0%9F%87%A9%F0%9F%87%AA)](https://git.io/typing-svg)
```

### 3. Role + Social Badges
```md
![Role](https://custom-icon-badges.demolab.com/badge/-WEB%20DEVELOPER-FF2D78?style=for-the-badge&logoColor=white&logo=codepen&labelColor=7209B7)

[![Website](https://img.shields.io/badge/🌐_Website-web--dev--codi.onrender.com-00D4FF?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=0A0A1A)](https://web-dev-codi.onrender.com/)
[![Location](https://img.shields.io/badge/📍_Location-Berlin,_Germany-FF2D78?style=for-the-badge&logoColor=white&labelColor=0A0A1A)]()

![Visitor Count](https://komarev.com/ghpvc/?username=Web-Dev-Codi&style=for-the-badge&color=00FF9C&label=Profile%20Views&labelColor=0A0A1A)
![GitHub Stars](https://img.shields.io/github/stars/Web-Dev-Codi?style=for-the-badge&color=FF2D78&labelColor=0A0A1A&logo=github)
![Followers](https://img.shields.io/github/followers/Web-Dev-Codi?style=for-the-badge&color=00D4FF&labelColor=0A0A1A&logo=github)

---

</div>
```

### 4. About Me (JS code block)
```md
## 🎯 About Me

```javascript
const developer = {
  name:              "Web-Dev-Codi",
  location:          "Berlin, Germany 🇩🇪",
  passions:          ["Web Development", "Front-End Magic", "Open Source"],
  specialties:       ["HTML5", "CSS3", "JavaScript", "Modern Frameworks"],
  currentlyBuilding: ["OllamaTerm 🤖", "DeutschBuddy 🇩🇪"],
  mission:           "Building beautiful, functional web experiences",
  funFact:           "I debug with console.log and I'm not sorry 😅",
  status:            "Always coding, always learning 🚀"
};
```
```

### 5. Skill Icons (2 rows, dark theme)
```md
<div align="center">

---

## 🛠️ Tech Arsenal

[![Frontend & Languages](https://skillicons.dev/icons?i=html,css,js,ts,python,nodejs,react,bash&theme=dark&perline=8)](https://skillicons.dev)

[![Tools & Platforms](https://skillicons.dev/icons?i=git,github,vscode,linux,markdown,npm,vercel,docker&theme=dark&perline=8)](https://skillicons.dev)

---

## 📊 GitHub Stats
```

### 6. Stats + Streak (side-by-side table)
```md
<table align="center">
  <tr>
    <td>
      <img src="https://github-readme-stats.vercel.app/api?username=Web-Dev-Codi&show_icons=true&theme=radical&hide_border=true&bg_color=0A0A1A&title_color=FF2D78&icon_color=00FF9C&text_color=00D4FF&rank_icon=percentile" alt="GitHub Stats" />
    </td>
    <td>
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=Web-Dev-Codi&theme=radical&hide_border=true&background=0A0A1A&stroke=FF2D78&ring=FF2D78&fire=FF2D78&dates=00D4FF&sideLabels=00D4FF&sideNums=FF2D78&currStreakLabel=FF2D78&currStreakNum=FF2D78" alt="GitHub Streak" />
    </td>
  </tr>
</table>
```

### 7. Activity Graph (full width)
```md
---

## 📈 Activity Graph

![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Web-Dev-Codi&theme=tokyo-night&bg_color=0A0A1A&color=FF2D78&line=00D4FF&point=00FF9C&area=true&hide_border=true)
```

### 8. Trophies
```md
---

## 🏆 GitHub Trophies

![Trophies](https://github-profile-trophy.vercel.app/?username=Web-Dev-Codi&theme=radical&no-frame=true&column=4&margin-w=15&margin-h=15&title=MultiLanguage,Commits,Issues,Stars,PullRequest,Repositories)
```

### 9. Languages
```md
---

## 📊 Most Used Languages

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Web-Dev-Codi&layout=compact&theme=radical&hide_border=true&bg_color=0A0A1A&title_color=FF2D78&text_color=00D4FF&langs_count=8)
```

### 10. Snake Contribution Graph (dark/light aware via <picture>)
```md
---

## 🐍 Watch My Contributions Get Eaten

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Web-Dev-Codi/Web-Dev-Codi/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Web-Dev-Codi/Web-Dev-Codi/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/Web-Dev-Codi/Web-Dev-Codi/output/github-contribution-grid-snake.svg">
</picture>
```

### 11. 3D Contribution Calendar
```md
---

## 🌐 3D Contribution Calendar

![3D Contribution Calendar](./profile-3d-contrib/profile-night-rainbow.svg)
```

### 12. WakaTime Coding Stats
Note: Requires free wakatime.com account. See setup note in comment.
```md
---

## ⏱️ WakaTime Coding Stats

> **Setup:** Create a free account at [wakatime.com](https://wakatime.com), install the editor plugin, then add `WAKATIME_API_KEY` as a repository secret.

![WakaTime Stats](https://github-readme-stats.vercel.app/api/wakatime?username=Web-Dev-Codi&theme=radical&hide_border=true&bg_color=0A0A1A&title_color=FF2D78&text_color=00D4FF&icon_color=00FF9C&layout=compact&langs_count=8)

</div>
```

### 13. Projects (all 6, restyled neon badges)
Keep all 6 projects. Swap badge colors to neon palette:
- `color=FF2D78` for stars, `color=00D4FF` for forks
- Language badges: keep logo but change bg to neon accent colors
  - Python: `#FF2D78` instead of `#3776AB`
  - JavaScript: keep `#F7DF1E` (standard, still looks great)
  - CSS: `#00D4FF` instead of `#1572B6`

### 14. Random Dev Joke
```md
<div align="center">

---

## 😂 Random Dev Joke

![Jokes Card](https://readme-jokes.vercel.app/api?theme=dark&bgColor=%230A0A1A&textColor=%2300D4FF&borderColor=%23FF2D78&qColor=%23FF2D78&aColor=%2300FF9C&codeColor=%237209B7)

---
```

### 15. Connect section
```md
## 🔗 Let's Connect

[![GitHub](https://img.shields.io/badge/GitHub-@Web--Dev--Codi-FF2D78?style=for-the-badge&logo=github&logoColor=white&labelColor=0A0A1A)](https://github.com/Web-Dev-Codi)
[![Website](https://img.shields.io/badge/Website-web--dev--codi.onrender.com-00D4FF?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=0A0A1A)](https://web-dev-codi.onrender.com/)

---

> *"Code is like humor. When you have to explain it, it's bad."* — **Cory House**

---

### ⭐ If you enjoy my work, consider giving my repos a star

Made with ❤️ by **Web-Dev-Codi** | Berlin, Germany 🇩🇪

![Made with Love](https://custom-icon-badges.demolab.com/badge/-Made%20with%20Love-FF2D78?style=flat-square&logo=heart&logoColor=white&labelColor=7209B7)

</div>
```

### 16. Capsule Render Footer (must be last line, no trailing newline issues)
```md
![Footer](https://capsule-render.vercel.app/api?type=waving&color=00D4FF,FF2D78,7209B7&height=150&section=footer)
```

---

## Task 2: Create snake GitHub Action

**File:** Create `.github/workflows/snake.yml`

```yaml
name: Generate Snake Game

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    timeout-minutes: 10

    steps:
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: push snake SVGs to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

---

## Task 3: Create 3D Contribution Calendar GitHub Action

**File:** Create `.github/workflows/3d-contrib.yml`

```yaml
name: GitHub Profile 3D Contribution

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    name: generate-github-profile-3d-contrib

    steps:
      - uses: actions/checkout@v4

      - uses: yoshi456164/github-profile-3d-contrib@0.7.1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          username: Web-Dev-Codi
          type: night-rainbow

      - run: |
          git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git config user.name "github-actions[bot]"
          git add -A
          git status
          git diff --staged --quiet || git commit -m "chore: regenerate 3D contribution calendar"
          git push
```

---

## Task 4: Commit everything

```bash
git add README.md .github/workflows/snake.yml .github/workflows/3d-contrib.yml docs/
git commit -m "feat: full cyberpunk README redesign with animated widgets and GitHub Actions"
```

---

## Post-Deploy Notes

1. **Snake graph** — After pushing, manually trigger the `Generate Snake Game` workflow once from the Actions tab to create the `output` branch immediately. It auto-runs daily after that.

2. **3D Calendar** — After pushing, manually trigger `GitHub Profile 3D Contribution` once. It will push `profile-3d-contrib/profile-night-rainbow.svg` to the main branch.

3. **WakaTime** — Visit [wakatime.com](https://wakatime.com), sign up, install the plugin for your editor, then add `WAKATIME_API_KEY` to Settings → Secrets → Actions in the repo. The widget will start populating with real data within 24h.
