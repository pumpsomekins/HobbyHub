# HobbyHub

> A handcraft hobbyist platform. Learn, create, and master physical crafts.

---

## Project Overview

HobbyHub is a one-stop platform for handcraft enthusiasts, offering tool kits, community work showcases, and professional training services. Currently featuring Mixology (cocktail recipes) with Apple Liquid Glass design, and structured to support many more hobby categories in the future.

---

## Quick Start

### Requirements
- Modern browser (Chrome, Firefox, Safari, Edge)
- No backend dependencies — pure static frontend

### Running locally

```bash
cd HobbyHub

# Option 1: Use Python HTTP server (recommended)
python -m http.server 8000
# Then visit http://localhost:8000/

# Option 2: Open directly in browser
# Open index.html in your browser
```

---

## Core Features

| Feature | Description | Status | Notes |
|---------|-------------|--------|-------|
| **Mixology Page** | Cocktail recipe showcase with filter tabs | ✅ Implemented | `hobbies/mixology/mixology.html` |
| **Negroni Detail** | Full cocktail detail page (recipe, history, variations) | ✅ Implemented | `hobbies/mixology/negroni.html` |
| **Gift Recommendation** | Gift reminder system with countdown & birthday management | ✅ Implemented | Data persisted in LocalStorage |
| **Age / For-whom filter bar** | UI for demographic filtering | 🟡 UI only | Clicking pills has no actual filter effect |
| **Tool Kits showcase** | Kit cards (entry / advanced / pro tiers) | 🟡 UI only | Static display, no detail page |
| **Community Works** | User craftwork gallery | 🟡 UI only | Static display, no purchase flow |
| **Course & Camps** | Online courses & live training camp showcase | 🟡 UI only | Static display, no signup flow |
| **Hold-to-Reveal** | Long-press to reveal skill learning journey | 🟡 Partial | Interaction exists in concept but disabled |
| **Theme Toggle (Light / Dark)** | Apple-style light & dark mode switch | 🔴 Not implemented | Liquid Glass CSS vars exist, no switch logic yet |
| **Global Search** | Search kits, creations, courses | 🔴 Not implemented | Search box UI exists |
| **Sign in / Register** | User account system | 🔴 Not implemented | Buttons exist, no auth logic |
| **Cart / Saved** | Shopping cart & favorites | 🔴 Not implemented | Icons exist, no functionality |
| **AI Skill Assistant** | Smart recommendations & project generator | 🔴 Not implemented | Nav entry exists |

> **Status legend:** ✅ Implemented · 🟡 UI only (no interaction) · 🔴 Not yet built

---

## Project Structure

```
HobbyHub/
├── index.html                 # Home page (Apple Liquid Glass style)
├── hobbies/
│   └── mixology/
│       ├── mixology.html      # Mixology category page
│       └── negroni.html       # Negroni cocktail detail page
├── assets/
│   └── images/
│       └── Negroni.jpg
├── docs/
│   ├── 目前目标.txt           # (empty) current goals
│   └── 项目架构与商品详情页设计.md  # Architecture & design notes
└── README.md
```

### Future hobby pages
As more hobbies are added, each will live under its own folder:

```
hobbies/
├── mixology/          ← exists today
├── woodworking/       ← future
├── pottery/           ← future
├── fiber-arts/        ← future
└── ...
```

Shared images go under `assets/images/<hobby-name>/`.

---

## Pages & Modules

| File | Module | Description |
|------|--------|-------------|
| `index.html` | Home | Landing page with category tabs, filter bar, tool kits, community works, and courses |
| `hobbies/mixology/mixology.html` | Mixology | Cocktail recipes showcase with category filter tabs |
| `hobbies/mixology/negroni.html` | Negroni detail | Full recipe, ingredients, history, and variations |

---

## Design System

### Apple Liquid Glass
The UI uses a frosted-glass aesthetic with the following CSS variable system:

- **Accent:** `#F1641E` (orange)
- **Dark mode background:** Radial gradient from `#1c1416` through `#0c0c14` to `#07070d`
- **Glass cards:** `rgba(255,255,255,0.06)` background with `backdrop-filter: blur()`
- **Soft border:** `rgba(255,255,255,0.10)`
- **Gentle glow:** Colored radial gradients in the page corners

### Planned
- Light mode (tap top-left logo to toggle) — CSS variables are defined, toggle logic not wired yet.
- Better tag contrast in dark mode.

---

## Usage Walkthrough

### ✅ Working features

**1. Explore Mixology**
- Click the `🍸 Mixology` tab on the home page, or open `hobbies/mixology/mixology.html`
- Filter recipes by style tabs (Classic / Tropical / Spirit / Sparkling / Modern)
- Click a card to open the detail page

**2. Gift reminder system**
- Click the `🎁 Gifts` tab (red-dot marker) in the top category bar
- View upcoming holiday countdowns and gift suggestions
- Add / remove birthday reminders — persisted in LocalStorage

**3. Navigate between pages**
- Home: `http://localhost:8000/`
- Mixology list: `http://localhost:8000/hobbies/mixology/mixology.html`
- Negroni detail: `http://localhost:8000/hobbies/mixology/negroni.html`

### 🟡 UI only (no interaction yet)

**Tool kits, works, courses** — `index.html`
- Three card sections showcase kits, community works, and training camps
- Clicking a card does not open a detail page

**Age / For-whom filter bar**
- The pill-style filters are visual only, no data filtering happens

**Search, Saved, Cart, Sign in**
- UI is present, behavior is not wired up

---

## Tech Stack

- **HTML5** — semantic page structure
- **CSS3** — responsive layout, Liquid Glass via `backdrop-filter`
- **JavaScript (ES6+)** — interaction logic, inline, no bundler
- **LocalStorage** — user data persistence for gifts & birthdays
- **Python** — optional local dev server (`python -m http.server`)

No build step, no framework. Deploy as-is to any static host.

---

## Responsive Support

- Desktop (1200px+) — primary target
- Tablet (680px–1000px) — layout adjusts
- Mobile (<680px) — single-column card grid

---

## Contact

Questions or suggestions?
- Email: hello@HobbyHub.com

---

© 2026 HobbyHub. All rights reserved.
