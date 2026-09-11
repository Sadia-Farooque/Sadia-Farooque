<div align="center">

<img src="https://capsule-render.vercel.app/api?type=blur&color=0:0a0f14,40:134e4a,70:155e75,100:0a0f14&height=190&text=SADIA%20FATIMA&fontColor=ccfbf1&fontSize=46&fontAlignY=42&desc=Data%20Scientist%20%7C%20ML%20Engineer%20%7C%20Explainable%20AI%20Builder&descColor=94a3b8&descSize=15&descAlignY=68&animation=fadeIn" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=3200&pause=900&color=14B8A6&center=true&vCenter=true&width=820&lines=building+ML+systems+that+explain+themselves;if+a+model+can't+justify+it%2C+it+doesn't+ship;BSCS+%2728+%40+Sukkur+IBA+University;McKinsey+Forward+%C2%B7+Harvard+Aspire+%C2%B7+LoopLab" alt="Typing SVG"/>

<br><br>

<a href="https://www.linkedin.com/in/sadia-fatima-4334a9373/"><img src="https://img.shields.io/badge/LinkedIn-0a0f14?style=for-the-badge&logo=linkedin&logoColor=14b8a6"/></a>
<a href="mailto:anamfarooque06@gmail.com"><img src="https://img.shields.io/badge/Email-0a0f14?style=for-the-badge&logo=gmail&logoColor=22d3ee"/></a>
<a href="https://github.com/Sadia-Farooque"><img src="https://img.shields.io/badge/GitHub-0a0f14?style=for-the-badge&logo=github&logoColor=ccfbf1"/></a>
<img src="https://komarev.com/ghpvc/?username=Sadia-Farooque&style=for-the-badge&color=134e4a&label=VISITORS"/>

</div>

<br>

> *"An approximate answer to the right question is worth more than a precise answer to the wrong one."* — John Tukey

<br>

## 🕯️ about me

BSCS '28 at Sukkur IBA University, working at the intersection of machine learning and interpretability. I build models that don't just make predictions — they justify them, which matters most in high-stakes, regulated settings like finance.

<table>
<tr>
<td width="25%" align="center">🎓<br><b>3.65 / 4.0</b><br><sub>CGPA</sub></td>
<td width="25%" align="center">📍<br><b>Sindh, PK</b><br><sub>based in</sub></td>
<td width="25%" align="center">🔮<br><b>XAI</b><br><sub>obsession</sub></td>
<td width="25%" align="center">🖤<br><b>open</b><br><sub>to remote work</sub></td>
</tr>
</table>

<details>
<summary><b>⚡ three things about how I work</b> &nbsp;<sub>(click)</sub></summary>
<br>

| | |
|---|---|
| **Metrics follow the business, not the leaderboard** | A 0.94 AUC that costs the bank money is a failed model. I define the cost matrix before I define the architecture. |
| **Every prediction gets a receipt** | SHAP values, feature attributions, counterfactuals — if a loan officer can't explain a rejection to a customer, the model isn't deployable. |
| **Ship the boring parts too** | Persistence layers, schema design, retraining triggers. The notebook is 20% of the work. |

</details>

---

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg"/>
  <img alt="contribution snake" src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" width="100%"/>
</picture>

</div>

---

## 🩸 featured work

<sub>every card below expands — click a title for architecture, decisions, and results.</sub>

<br>

<details>
<summary><h3 style="display:inline">🏦 FinGuard AI &nbsp;—&nbsp; <sub>ML Decision Engine for Banking</sub></h3></summary>

<br>

A unified pipeline for **credit risk, fraud detection, churn, and spend forecasting** — one system, business-driven metrics, SHAP-based explainability throughout.

```mermaid
flowchart LR
    A[(Raw Banking<br/>Transactions)] --> B[Feature Store<br/>Pandas · NumPy]
    B --> C{Task Router}
    C --> D[Credit Risk<br/>XGBoost]
    C --> E[Fraud Detection<br/>XGBoost + resampling]
    C --> F[Churn<br/>Gradient Boosting]
    C --> G[Spend Forecast<br/>Time-series]
    D & E & F & G --> H[SHAP<br/>Explainability Layer]
    H --> I[[Decision + Reason Codes]]
    I --> J[(MongoDB<br/>Audit Trail)]

    style A fill:#0a0f14,stroke:#14b8a6,color:#ccfbf1
    style H fill:#134e4a,stroke:#22d3ee,color:#ccfbf1
    style I fill:#155e75,stroke:#22d3ee,color:#ccfbf1
    style J fill:#0a0f14,stroke:#14b8a6,color:#ccfbf1
```

**Design decisions**
- Optimized for **expected cost**, not accuracy — false negatives on fraud are ~40× the cost of false positives, so the threshold is tuned on a cost curve rather than F1.
- **SHAP at inference time**, not just in analysis — every decision writes reason codes to the audit trail, so the system is defensible under regulatory review.
- Shared feature store across all four tasks — one source of truth, no training/serving skew.

`Python` `XGBoost` `SHAP` `scikit-learn` `Pandas` `MongoDB`

> 🏅 Showcased at Sukkur IBA as an **Applied ML Benchmark**

</details>

<details>
<summary><h3 style="display:inline">🧩 Maze Adventure &nbsp;—&nbsp; <sub>Algorithmic Game Engine</sub></h3></summary>

<br>

Live **BFS/DFS enemy navigation**, a DFS-generated maze, and full MySQL persistence for lives, state, and leaderboards.

```mermaid
flowchart TD
    S[DFS Maze Generation] --> T[Game Loop]
    T --> U{Enemy AI Tick}
    U -->|short range| V[BFS → shortest path to player]
    U -->|weighted terrain| W[Dijkstra → cost-aware path]
    V & W --> X[Move + Collision Resolve]
    X --> Y[(MySQL<br/>state · lives · scores)]
    Y --> T

    style S fill:#134e4a,stroke:#14b8a6,color:#ccfbf1
    style U fill:#155e75,stroke:#22d3ee,color:#ccfbf1
    style Y fill:#0a0f14,stroke:#14b8a6,color:#ccfbf1
```

**Why it's interesting:** the enemy pathfinder re-plans every tick against a mutating grid, so the interesting problem wasn't implementing BFS — it was keeping it cheap enough to run at frame rate while the maze state changed underneath it.

`Java` `Swing` `BFS/DFS` `Dijkstra` `MySQL`

> 🏅 Recognized at the **AI & CS Expo, 2024**

</details>

<details>
<summary><h3 style="display:inline">🚀 Space Shooter &nbsp;—&nbsp; <sub>OOP Architecture Study</sub></h3></summary>

<br>

A deliberately non-trivial codebase built to demonstrate disciplined object-oriented design — an `Entity` hierarchy driving inheritance and polymorphism, encapsulated state, and a MySQL-backed scoring layer.

The goal was architectural, not visual: adding a new enemy type or weapon should require **zero changes to the game loop**. It does.

`Java` `Swing` `MySQL` `OOP`

> 🏅 **Runner-Up, SIBA Fest 2025**

</details>

<details>
<summary><h3 style="display:inline">🛠️ In Progress &nbsp;—&nbsp; <sub>Raasta & Resume Analyzer AI</sub></h3></summary>

<br>

| Project | What it does | Status |
|---|---|---|
| **Raasta** | Conversational AI assistant — retrieval-grounded, built for low-bandwidth contexts | 🟡 In development |
| **Resume Analyzer AI** | ML-powered resume parsing + structured evaluation against role criteria | 🟡 In development |

`Python` `NLP` `LLM` `spaCy`

</details>

---

## ⚰️ toolbox

<div align="center">

<img src="https://skillicons.dev/icons?i=python,java,cpp,c,js,mysql,mongodb,git,github,vscode&theme=dark" alt="tech stack — hover each icon for its name"/>

<sub>hover any icon for its name</sub>

</div>

<br>

<details open>
<summary><b>🗺️ how the stack fits together</b></summary>

<br>

```mermaid
mindmap
  root((Sadia))
    Modeling
      scikit-learn
      XGBoost
      SHAP
    Data
      Pandas
      NumPy
    Storage
      MySQL
      MongoDB
    Systems
      Java / OOP
      C / C++
    Tooling
      Git
      VS Code
```

</details>

<div align="center">

| Domain | Stack | Depth |
|---|---|---|
| 🧠 Modeling | scikit-learn · XGBoost · SHAP | ![](https://img.shields.io/badge/-%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88-14b8a6?style=flat-square) |
| 📊 Data | Pandas · NumPy | ![](https://img.shields.io/badge/-%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%91-14b8a6?style=flat-square) |
| 🗃️ Storage | MySQL · MongoDB | ![](https://img.shields.io/badge/-%E2%96%88%E2%96%88%E2%96%88%E2%96%91%E2%96%91-22d3ee?style=flat-square) |
| ☕ Systems | Java · C++ · C | ![](https://img.shields.io/badge/-%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%91-22d3ee?style=flat-square) |

</div>

---

## 👻 GitHub pulse

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Sadia-Farooque&show_icons=true&theme=react&hide_border=true&bg_color=0a0f14&title_color=14b8a6&icon_color=22d3ee&text_color=b3c4cc&include_all_commits=true&count_private=true" height="165"/>
<img src="https://streak-stats.demolab.com?user=Sadia-Farooque&theme=nightowl&hide_border=true&background=0a0f14&stroke=14b8a6&ring=22d3ee&fire=22d3ee&currStreakLabel=ccfbf1" height="165"/>

<br><br>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sadia-Farooque&layout=compact&theme=react&hide_border=true&bg_color=0a0f14&title_color=14b8a6&text_color=b3c4cc&langs_count=8" height="150"/>

<br><br>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Sadia-Farooque&bg_color=0a0f14&color=ccfbf1&line=14b8a6&point=22d3ee&area=true&area_color=134e4a&hide_border=true&custom_title=contribution%20activity" width="100%"/>

<br>

<img src="https://github-profile-trophy.vercel.app/?username=Sadia-Farooque&theme=nord&no-frame=true&no-bg=true&column=7&margin-w=6&margin-h=6"/>

</div>

---

## 🦇 milestones

<details open>
<summary><b>2026</b></summary>

- Selected Participant, **McKinsey Forward Program** — McKinsey & Company
- Campus Ambassador, **LoopLab** — selected representative
- **FinGuard AI** showcased as an Applied ML Benchmark — Sukkur IBA

</details>

<details>
<summary><b>2025</b></summary>

- Selected, Global Pool — **Harvard Aspire Leaders Program** (Harvard University)
- **International ML Summer School** — cohort of 10,000+
- Runner-Up, Project Competition — **SIBA Fest**
- Merit Award, **PM Youth Laptop Scheme** — top BSCS nationally (Govt. of Pakistan)

</details>

<details>
<summary><b>2024</b></summary>

- Certificate of Recognition, **AI & CS Expo** — Sukkur IBA

</details>

<details>
<summary><b>📜 certifications</b></summary>

<br>

| Certification | Issuer | Year |
|---|---|:---:|
| McKinsey Forward Program | McKinsey & Company | 2026 |
| Google AI Essentials | Coursera / Google | 2026 |
| Google Prompting Essentials | Coursera / Google | 2026 |
| Intro to MongoDB | Credly | 2026 |
| International ML Summer School | Global Cohort | 2025 |
| Harvard Aspire Leaders Program | Harvard University | 2025 |

</details>

---

## 🕷️ leadership & involvement

<table>
<tr>
<td width="33%" valign="top">

**McKinsey Forward**
<sub>Selected Participant · 2026</sub>

Global career-readiness program covering structured problem-solving, communication, and workplace effectiveness.

</td>
<td width="34%" valign="top">

**LoopLab**
<sub>Campus Ambassador · 2026–Present</sub>

Driving awareness and program participation at IBA Sukkur.

</td>
<td width="33%" valign="top">

**CS Society**
<sub>Executive Member · 2025–2026</sub>

Merit-selected; co-organized SIBAthon'26 end-to-end.

</td>
</tr>
</table>

---

<div align="center">

<img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=nightowl" alt="random dev quote"/>

</div>

---

<div align="center">

## 🖤 I will love to connect !

<sub>open to remote roles, research collaborations, and anything involving interpretable ML.</sub>

<br><br>

[![LinkedIn](https://img.shields.io/badge/-Connect-134e4a?style=for-the-badge&logo=linkedin&logoColor=ccfbf1)](https://www.linkedin.com/in/sadia-fatima-4334a9373/)
[![Email](https://img.shields.io/badge/-Say%20Hi-155e75?style=for-the-badge&logo=gmail&logoColor=ccfbf1)](mailto:anamfarooque06@gmail.com)
[![GitHub](https://img.shields.io/badge/-Follow-0a0f14?style=for-the-badge&logo=github&logoColor=ccfbf1)](https://github.com/Sadia-Farooque)

<img src="https://capsule-render.vercel.app/api?type=blur&color=0:0a0f14,40:155e75,70:134e4a,100:0a0f14&height=110&animation=fadeIn" width="100%"/>

</div>
