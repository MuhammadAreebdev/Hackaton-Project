# HelpHub AI

> **"Find help faster. Become help that matters."**
> A community-powered support network for students, mentors, creators, and builders.

Live Link: https:https://hackatonnight.netlify.app/

---

## 🧭 Project Overview

**HelpHub AI** ek multi-page frontend web application hai jo **SMIT Grand Coding Night 2026** ke liye banaya gaya. Yeh platform students aur mentors ko ek jagah connect karta hai — jahan koi bhi apni problem post kar sakta hai, doosron ki madad kar sakta hai, aur apna trust score build kar sakta hai.

Platform ka core idea simple hai:
- 🙋 **Need Help?** — Request post karo, community help karega
- 🤝 **Can Help?** — Browse karo, match dhundo, help do
- 📈 **Track Impact** — Trust score, badges, aur leaderboard se apni reputation dekhte raho

> **Tech Stack:** Pure HTML5 · CSS3 · Vanilla JavaScript · No frameworks · No backend

---

## 📁 Project Structure

```
project/
│
├── index.html                    ← Home / Landing Page
├── helphub_login.html            ← Login & Demo Entry
├── helphub-explore.html          ← Browse All Requests (Feed)
├── helphub_request_detail.html   ← Single Request Detail + AI Summary
├── helphub_aicenter.html         ← AI Insights & Trend Intelligence
├── helphub-leaderboard.html      ← Top Helpers Rankings & Badges
├── helphub-messages.html         ← Direct Messaging Between Users
├── helphub-notifications.html    ← Live Notification Feed
├── helphub-profile.html          ← User Profile (Public + Edit)
│
└── assetes/
    ├── css/
    │   ├── style.css                    ← Global Design System (shared)
    │   ├── helphub-login.css            ← Login page styles
    │   ├── helphub-explore.css          ← Explore feed styles
    │   ├── help-explore-detail.css      ← Request detail styles
    │   ├── help-ai.css                  ← AI Center styles
    │   ├── helphub-leaderboard.css      ← Leaderboard styles
    │   ├── helphub-messages.css         ← Messages styles
    │   ├── helphub-notifications.css    ← Notifications styles
    │   └── helphub-profile.css          ← Profile page styles
    │
    └── img/                             ← Image assets (if any)
```

**CSS pattern:** Har page ka apna dedicated CSS file hai jo `style.css` ke upar load hota hai. Yeh modular approach clean separation deta hai.

---

## 📄 Pages — Detail mein

### 1. 🏠 `index.html` — Home / Landing

**Kya hai:** Platform ka main entry point.

**Sections:**
- **Navbar** — Logo, nav links (Home, Explore, Leaderboard, AI Center), "Join the platform" CTA, hamburger menu
- **Hero Section** — Two-column layout:
  - Left: Tagline, description, two CTAs ("Open product demo", "Post a request"), live stats grid (384+ Members, 72+ Requests, 69+ Solved)
  - Right: Dark card with feature highlights — AI request intelligence, Community trust graph, 100% top trust score showcase
- **Core Flow Section** — 3 feature cards: "Ask for help clearly", "Discover the right people", "Track real contribution"
- **Featured Requests Section** — 3 sample request cards with tags, user info, and "Open details" links
- **Mobile Side Menu** — Slide-in overlay menu (hamburger controlled)

---

### 2. 🔐 `helphub_login.html` — Login / Demo Entry

**Kya hai:** Platform mein enter karne ka gate. Real auth nahi — demo identity system hai.

**Layout:** Two-column split
- **Left Card (Dark):**
  - "Community Access" label
  - Tagline: "Enter the support network."
  - Feature list: role-based entry, dashboard path, LocalStorage session
- **Right Card (Light Form):**
  - Demo user select dropdown: Ayesha Khan, Ali Hassan, Sara Malik, Usman Raza
  - Role selection: Both / Need Help / Can Help
  - Email field (pre-filled: `community@helphub.ai`)
  - Password field (pre-filled: `password123`)
  - "Continue to dashboard" button

**Note:** Koi actual authentication nahi hai. Yeh UI/UX demo hai.

---

### 3. 🔍 `helphub-explore.html` — Explore Feed

**Kya hai:** Platform ki main feed — saari community requests browse karein.

**Layout:** Sidebar + Main Feed grid

**Sidebar (Filters):**
- Category dropdown: All / Web Development / Design / Career
- Urgency dropdown: All / High / Medium / Low
- Skills text input (e.g., React, Figma)
- Location text input (e.g., Karachi, Remote)

**Main Feed — Request Cards (4 demo requests):**

| Title | Category | Urgency | Status |
|-------|----------|---------|--------|
| "Need help" | Web Development | High | Solved |
| "Need help making my portfolio responsive before demo day" | Web Development | High | Solved |
| "Looking for Figma feedback on a volunteer event poster" | Design | Medium | Open |
| "Need mock interview support for internship applications" | Career | Low | Solved |

Each card has: category/urgency/status tags, title, excerpt, sub-skill tags, user name + location + helper count, "Open details" button.

---

### 4. 📋 `helphub_request_detail.html` — Request Detail

**Kya hai:** Kisi ek request ka full view — AI summary, helper list, aur action buttons.

**Header Card:**
- Category, urgency, status tags
- Full title + description
- Eyebrow label: "REQUEST DETAIL"

**Two-Column Grid:**

**Left Column:**
- **AI Summary Card** — HelpHub AI branding + generated summary text + pill tags
- **Actions Panel** — "I can help" (primary) + "Mark as solved" (outline) buttons

**Right Column:**
- **Requester Panel** — Avatar (DiceBear API), name (@saramalik handle)
- **Helpers Panel** — List of ready helpers:
  - Ayesha Khan — Skills: Figma, UI/UX, HTML/CSS — Trust: **100%**
  - Hassan Ali — Skills: JavaScript, React, Git/GitHub — Trust: **88%**

---

### 5. 🤖 `helphub_aicenter.html` — AI Center

**Kya hai:** Platform intelligence dashboard — AI jaisi insights jo demand trends, urgency signals, aur request recommendations dikhata hai.

**Sections:**
- **Hero Banner (Dark Green)** — "See what the platform intelligence is noticing."
- **Stats Cards Row (3 cards):**
  - Trend Pulse: **Web Development** (most requested category)
  - Urgency Watch: **2** (high-priority requests)
  - Mentor Pool: **2** (trusted helpers available)
- **AI Recommendations Section** — 4 request cards with AI-generated summaries:
  1. Generic "Need help" — Web Dev, High urgency
  2. Portfolio responsive issue — Frontend mentors recommended
  3. Figma poster feedback — Design critique focus
  4. Mock interview support — Career coaching context

**Design note:** Yeh page warm beige background use karta hai aur inline `<style>` mein styling hai (CSS file ke bajaaye).

---

### 6. 🏆 `helphub-leaderboard.html` — Leaderboard

**Kya hai:** Community ke top helpers ko recognize karo — trust score, contributions, badges.

**Two-Panel Layout:**

**Left Panel — Rankings:**

| Rank | Name | Skills | Trust | Contributions |
|------|------|--------|-------|---------------|
| #1 | Ayesha Khan | React, Tailwind, Accessibility | 96% | 32 |
| #2 | Hassan Ali | JavaScript, React, Git/GitHub | 88% | 24 |
| #3 | Sara Noor | Python, Data Analysis | 74% | 11 |

**Right Panel — Badge System:**
- Each person ka progress bar (animated on page load via JS)
- Badges: "Mentor", "Accessibility Pro", "Code Rescuer", "Bug Hunter", "Community Voice"

**JS Feature:** `window.addEventListener('load')` se progress bars 0% se animate hokar final width tak jaate hain.

---

### 7. 💬 `helphub-messages.html` — Direct Messages

**Kya hai:** Helper aur requester ke beech direct communication.

**Two-Panel Layout:**

**Left Panel — Conversation Stream:**
- Pre-loaded messages:
  - Ayesha Khan → Sara Noor: Portfolio breakpoint fix
  - Hassan Ali → Ayesha Khan: Event poster feedback
- Each message has sender→receiver header, body text, time badge (AM/PM)

**Right Panel — Send Message:**
- Recipient dropdown (Ayesha Khan, Hassan Ali, Sara Noor)
- Message textarea
- "Send" button

**JS Feature (Functional):**
- Send button click se real-time mein new message card DOM mein add hota hai
- Current time (12-hour format) automatically attach hoti hai
- Empty message validation + "Type a message..." feedback
- "Sent ✓" confirmation → 1.5s baad "Send" wapas

---

### 8. 🔔 `helphub-notifications.html` — Notifications

**Kya hai:** Platform activity ka live feed — status changes, helper matches, trust score updates.

**Notification Types (with timing):**

| Type | Example | When |
|------|---------|------|
| Status | Request marked as solved | Just now |
| Match | Helper offered to help | Just now |
| Request | Your request is now live | Just now |
| Match | New helper matched | 12 min ago |
| Reputation | Trust score increased | 1 hr ago |
| Insight | AI detected rising demand | Today |

**JS Feature (Functional):**
- Har notification pill click pe **"Unread" ↔ "Read"** toggle hota hai
- Class `read` add/remove se visual style change

---

### 9. 👤 `helphub-profile.html` — User Profile

**Kya hai:** User ki public profile + edit form — dono ek saath.

**Two-Panel Layout:**

**Left Panel — Public Profile (Live Preview):**
- Trust Score: **100%**
- Contributions: **35**
- Skills: Figma, UI/UX, HTML/CSS, Career Guidance (pills)
- Badges: Design Ally, Fast Responder, Top Mentor (pills)

**Right Panel — Edit Form:**
- Name input (pre-filled: "Ayesha Khan")
- Location input (pre-filled: "Karachi")
- Skills input (comma-separated)
- Interests input
- "Save profile" button

**JS Features (Functional, Real-time):**
- Name input pe type karo → hero heading **instantly update** hoti hai
- Location input pe type karo → hero meta **instantly update** hota hai
- Skills input pe type karo → skills pills **instantly re-render**
- Save button → "Saved ✓" confirmation → 1.6s baad normal

---

## 🎨 Design System (`style.css`)

### Color Palette

| Variable | Value | Use |
|----------|-------|-----|
| `--primary` | `#0d9488` | Teal — primary buttons, links |
| `--primary-hover` | `#0a7d73` | Button hover state |
| `--secondary` | `#0d5a45` | Dark green — headings, logo |
| `--accent` | `#f5d4a8` | Amber — warm accent color |
| `--bg-light` | `#fcfbf8` | Light cream background |
| `--bg-mesh` | gradient | Body background (green→amber mesh) |
| `--dark-green` | `#1d2d2b` | Hero dark card background |
| `--text-primary` | `#1a2321` | Main body text |
| `--text-secondary` | `#6b7570` | Muted descriptions |
| `--white` | `#ffffff` | Card surfaces |

### Tag Color System

| Class | Background | Text | Use Case |
|-------|-----------|------|----------|
| `tag-green` | `#d4e9dc` | `#0d5a45` | Categories, "Solved" status |
| `tag-red` | `#f5b5a8` | `#8a2e1f` | "High" urgency |
| `tag-amber` | `#f5d4a8` | `#6b4410` | "Medium" urgency |
| `tag-blue` | (CSS defined) | — | "Open" status, Career category |
| `tag-teal` | (CSS defined) | — | Design category |
| `tag-orange` | (CSS defined) | — | Medium urgency (alternate) |

### Typography

| Font | Weights | Used In |
|------|---------|---------|
| **Inter** | 400, 500, 600, 700, 800 | Global body, most pages |
| **Manrope** | 400, 500, 600, 700, 800 | Login page, AI Center page |

Both fonts load from **Google Fonts CDN**.

### Border Radius Scale
- `--radius-sm`: `10px`
- `--radius-md`: `16px`
- `--radius-lg`: `24px`
- `--radius-pill`: `999px` (fully rounded)

---

## 🧩 JavaScript Features — Page by Page

| Page | Feature | How |
|------|---------|-----|
| All Pages | Mobile hamburger menu | `classList.toggle('active')` on menu + overlay |
| Leaderboard | Animated progress bars | `window.addEventListener('load')` → set width from 0% |
| Messages | Send new message | DOM `createElement`, append to list, live timestamp |
| Notifications | Read/Unread toggle | `classList.toggle('read')` on pill click |
| Profile | Live preview update | `input` event listeners → instant DOM update |
| Profile | Save confirmation | Button text change → `setTimeout` reset |

**Note:** Koi LocalStorage actually use nahi hua final build mein. Login page mein mention hai but implementation nahi ki gayi.

---

## 🗺️ Navigation Map

```
index.html
├── → helphub_login.html        (Join the platform CTA)
├── → helphub-explore.html      (Navbar: Explore)
├── → helphub-leaderboard.html  (Navbar: Leaderboard)
└── → helphub_aicenter.html     (Navbar: AI Center)

[Post-login pages — shown in explore/leaderboard/etc navbars]
├── helphub-explore.html
│   └── → helphub_request_detail.html  (Open details)
├── helphub-leaderboard.html
├── helphub-notifications.html
├── helphub-messages.html
├── helphub-profile.html
└── helphub_aicenter.html
```

---

## 👥 Demo Users

| Name | Handle | Skills | Trust | Role |
|------|--------|--------|-------|------|
| Ayesha Khan | — | React, Tailwind, Accessibility, Figma, UI/UX, HTML/CSS | 96–100% | Top Mentor |
| Hassan Ali | — | JavaScript, React, Git/GitHub | 88% | Code Rescuer |
| Sara Noor | — | Python, Data Analysis | 74% | Community Voice |
| Sara Malik | @saramalik | — | — | Requester |
| Usman Raza | — | — | — | Demo user |
| Ali Hassan | — | — | — | Demo user |

---

## 🚀 Kaise Run Karein

Koi build step, server, ya install ki zaroorat nahi.

1. **Zip extract karein** project folder mein
2. **`index.html`** browser mein open karein
3. Nav links se baaki pages navigate karein

> ✅ Internet chahiye (Google Fonts load ke liye)  
> ✅ Modern browser (Chrome, Firefox, Edge, Safari)  
> ❌ Node.js, npm, Python — kuch bhi nahi chahiye

---

## ⚠️ Known Limitations

- **No actual data persistence** — LocalStorage implementation mention hai login page mein lekin wired nahi hai
- **Static content** — Filters (Explore page) aur search kaam nahi karte (UI only)
- **Login is decorative** — "Continue to dashboard" koi actual auth nahi karta
- **No JS file** — Saara JavaScript inline `<script>` tags mein hai, alag `.js` files nahi hain
- **Typo in folder name** — Assets folder `assetes/` (extra 'e') naam se hai

---

## 📊 Project Stats

| Metric | Count |
|--------|-------|
| Total HTML pages | 9 |
| CSS files | 9 (1 global + 8 page-specific) |
| Total HTML lines | ~1,849 |
| Total CSS lines | ~2,548 |
| External dependencies | Google Fonts only |
| JS libraries | None |
| Demo users | 4–6 |
| Demo requests | 4 |

---

*Built for SMIT Grand Coding Night 2026 — Pure frontend, zero dependencies, maximum community impact.*