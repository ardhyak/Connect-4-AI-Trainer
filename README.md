# 🔴🟡🔴🟡 Connect 4 Coach

### The world's most advanced Connect 4 training platform

*Built on the mathematics and game theory*

---

![AI Engine](https://img.shields.io/badge/AI_Engine-Minimax_%CE%B1%E2%80%93%CE%B2_Pruning-06b6d4?style=for-the-badge&labelColor=0c1120)
![Puzzles](https://img.shields.io/badge/Puzzles-30-f59e0b?style=for-the-badge&labelColor=0c1120)
![Strategies](https://img.shields.io/badge/Strategies-12_Lessons-8b5cf6?style=for-the-badge&labelColor=0c1120)
![Solved](https://img.shields.io/badge/Game-Solved-22c55e?style=for-the-badge&labelColor=0c1120)

![React 18](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=white)
![Zero Deps](https://img.shields.io/badge/Dependencies-Zero-22c55e?style=flat-square)
![No Build](https://img.shields.io/badge/Build_Step-None-22c55e?style=flat-square)
![Persistence](https://img.shields.io/badge/Persistence-localStorage-f59e0b?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

## Why This Exists

Connect 4 was **solved in 1988** — Player 1 always wins with perfect play. But across **4.5 trillion** possible board states, no human can memorize the solution tree.

**Connect 4 Coach** teaches you the *principles* behind perfect play. Not memorized moves — strategic understanding grounded in the same game theory that solved the game.

---

## What Makes This Different

| Typical Connect 4 Apps | **Connect 4 Coach** |
|:---|:---|
| Random-strength AI | **Minimax engine with alpha-beta pruning** (depth 2–8) |
| Win or lose, no feedback | Every move **rated + explained** with strategic concepts |
| One difficulty forever | **Adaptive difficulty** based on your accuracy |
| Progress vanishes on close | **Full localStorage persistence** — stats, games, progress |
| "Play center" tips | Coaching from **Allis's 9 rules** that literally solved the game |
| No analysis tools | **Full replay system** with alternative line exploration |

---

## Feature Overview

### 🧠 Intelligent AI Engine

- Minimax search with alpha-beta pruning across 4 difficulty tiers
- **Adaptive difficulty** — adjusts automatically after every 3 games
- Expert mode searches **8 plies deep** — near-perfect play

### 🎯 Real-Time Move Coaching

Every move is instantly classified:

| Rating | Meaning | Visual |
|:---|:---|:---|
| **Optimal** | Best possible move | ✦ Green |
| **Good** | Near-optimal | ● Light green |
| **Inaccuracy** | Missed a better option | △ Yellow |
| **Mistake** | Significant position loss | ■ Orange |
| **Blunder** | Game-losing error | ✕ Red |

Each rating includes:

- **Strategic concept explanation** — *why* the move was right or wrong
- **"What-If" board** — see the position if you'd played optimally
- **Best-move indicator** — green glow on the recommended column
- **Threat overlays** — toggle to see opponent's winning threats
- **Toggleable drop animation** — physical Connect 4 style falling discs

### 🧩 30 Tactical Puzzles

| Tier | Puzzles | Skills Tested |
|:---|:---|:---|
| Beginner | 8 | Win detection, threat blocking, scanning |
| Intermediate | 6 | Forks, Figure-7 trap, center control, platform denial |
| Advanced | 6 | Parity, Zugzwang, forcing chains, threat stacking |
| Expert | 4 | Opening theory, pushup prevention, Aftereven |
| Master | 6 | Symmetry, Vertical Rule, mixed threats, endgame calc |

### 📚 12 Interactive Strategy Lessons

| # | Lesson | Source |
|:---|:---|:---|
| 1 | Center Column Dominance | Allis's thesis |
| 2 | Double Threats (Forks) | Competitive analysis |
| 3 | Odd/Even Parity Theory | Allis's core insight |
| 4 | Zugzwang Control | The proof mechanism |
| 5 | Tempo & Forcing Chains | Expert play patterns |
| 6 | Opening Theory | Allen's joseki |
| 7 | Defensive Mastery | Counter-attack principles |
| 8 | Threat Classification | Major / Minor / Odd / Even / Useless |
| 9 | Endgame Calculation | Deterministic parity |
| 10 | Allis's 9 Strategic Rules | Complete solution framework |
| 11 | Winning Patterns Library | Figure-7, L-Trap, Arrow |
| 12 | Column Value Theory | Mathematical line counting |

### 📈 Structured Training Curriculum

- **4-tier learning path**: Beginner → Intermediate → Advanced → Expert
- **22 interactive concepts** with board demos and "Try It" challenges
- **Drill assignments** for each concept
- **Progress tracking** with completion percentages

### 🔬 Professional Game Analysis

- **Full move-by-move replay** with transport controls
- **Auto-play mode** for hands-free review
- **Alternative line exploration** — click any column to see "what if?"
- **Key Moments** — jump directly to mistakes and turning points
- **Game history** — last 20 games stored and replayable

### 💾 Persistent Progress

Everything saved to `localStorage` — survives refresh:

| Data | Persisted |
|:---|:---|
| Player name | ✅ |
| Win / Loss / Draw / Accuracy | ✅ |
| Last 20 game replays | ✅ |
| 30 puzzle completions | ✅ |
| 22 curriculum concepts | ✅ |
| Difficulty preference | ✅ |

### 🎬 Onboarding Feature Showcase

New users see a 6-slide visual feature tour before signing in:

1. **AI Engine** — depth, pruning, adaptation
2. **Real-Time Coaching** — ratings, what-if boards, best-move indicator
3. **30 Puzzles** — tiers, interaction, concept explanations
4. **12 Strategy Lessons** — parity, Zugzwang, Allis's rules
5. **Game Analysis** — replay, alt-lines, key moments
6. **Persistent Progress** — everything survives refresh

Dot navigation, back/next buttons, and a "Skip to sign in" link.

---

## Quick Start

### Deploy to GitHub Pages

```bash
git init
git add index.html README.md
git commit -m "Deploy Connect 4 Coach"
git remote add origin https://github.com/YOUR_USERNAME/connect4-coach.git
git push -u origin main
```

**Settings → Pages → Source: `main` branch → `/ (root)` → Save**

Live at: `https://YOUR_USERNAME.github.io/connect4-coach/`

### Or Just Open It

```bash
open index.html       # macOS
start index.html      # Windows
xdg-open index.html   # Linux
```

No build step. No npm. No webpack. One file, zero dependencies.

---

## Architecture

```
index.html (single file, ~73KB)
│
├─ Engine Layer
│  ├─ Minimax with α-β pruning (depth 2–8)
│  ├─ Position evaluation heuristic
│  ├─ Move scoring with concept mapping
│  └─ Threat detection system
│
├─ Coaching System
│  ├─ 5-tier move classification
│  ├─ 8 strategic concept templates
│  ├─ What-if board generation
│  └─ Best-move highlighting
│
├─ Content Library
│  ├─ 30 validated tactical puzzles
│  ├─ 12 strategy lessons (36 interactive steps)
│  └─ 22 curriculum concepts with boards + try-it challenges
│
├─ Persistence Layer
│  ├─ localStorage auto-save on state change
│  ├─ Serialization for Sets (solved, progress)
│  └─ Migration-safe key versioning (c4coach_v2)
│
└─ UI Layer (React 18 via CDN + Babel Standalone)
   ├─ Board component (highlights, drop animation, overlays)
   ├─ 6-slide onboarding feature showcase
   ├─ 5-tab navigation (Play, Puzzles, Strategy, Learn, Analysis)
   └─ CSS custom properties theming
```

---

## Academic Foundation

| Author | Work | Year | Contribution |
|:---|:---|:---|:---|
| Victor Allis | *A Knowledge-Based Approach of Connect-Four* | 1988 | Solved the game; introduced 9 strategic rules |
| James D. Allen | *Expert Play in Connect-Four* | 1988 | Opening theory (joseki) analysis |
| John Tromp | *Strong solution via retrograde analysis* | 1995 | Complete enumeration of all 4.5 trillion positions |

---

## Reset Progress

Button on the Play tab menu, or manually:

```javascript
localStorage.removeItem('c4coach_v2');
location.reload();
```

---

## License

**MIT** — free for personal and commercial use.

---

> **Stop playing Connect 4. Start mastering it.**
>
> *Built with game theory. Powered by AI. Designed for champions.*
