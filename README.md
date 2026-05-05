# expense-tracker-app
# Kharcha 💸 — Personal Expense Tracker

> A clean, fast, and smart expense tracker with user profiles, demo mode, and AI-powered category detection. No backend. No ads. No subscriptions. Just open and use.

🔗 **Live Demo:** [everyday-kharcha.netlify.app](https://everyday-kharcha.netlify.app)

---

## What's New (v2)

- **User profiles** — create a profile with your name, avatar, and optional monthly budget before tracking begins
- **Demo mode** — try the full app with sample data before committing to an account
- **Per-user storage** — expenses are saved separately per profile name, so multiple people can use the same device
- **Budget tracker** — set a monthly budget and get a live progress bar + alert when you're close to the limit
- **Landing page** — proper homepage with feature overview and live preview

---

## How It Works

### New user flow
1. Visit the app → lands on `index.html`
2. Click **Create free account** → fill in name, pick an avatar, optionally set a monthly budget
3. Gets redirected to `app.html` with a clean slate (zero expenses)
4. Add, filter, and delete expenses — all saved automatically to `localStorage`

### Returning user flow
1. Visit the app → if a saved profile exists, redirects straight to `app.html`
2. Click **Sign in** → enter name → picks up exactly where they left off

### Demo mode flow
1. Click **Try the demo first** on the landing page
2. `app.html` loads with a yellow demo banner and pre-loaded sample expenses
3. Can explore all features — but expenses don't save and Add/Delete prompt sign-up
4. Click **Create free account →** in the banner to make a real profile

---

## Features

- **Smart category detection** — AI keyword matching suggests the right category as you type. Detects mismatches on submit and offers to fix them with a modal alert.
- **6 spending categories** — Food 🍜, Transport 🚗, Shopping 🛍️, Health 💊, Entertainment 🎬, Other 📦
- **User profiles** — name, emoji avatar, and optional monthly budget stored locally
- **Monthly budget bar** — live progress bar showing spend vs budget, colour-coded green → orange → red
- **Live summary strip** — Total spent, this month, and transaction count
- **Spending breakdown chart** — horizontal bar chart by category, updates in real time
- **Filter by category** — click any pill to narrow the expense list
- **Per-user persistence** — expenses stored under a per-name `localStorage` key
- **Demo mode** — sample data, no account needed, nothing saved
- **Dark theme** — easy on the eyes, always
- **Fully responsive** — works on desktop and mobile
- **Zero dependencies** — pure HTML, CSS, and JavaScript. No npm, no build step.

---

## Project Structure

```
kharcha/
├── index.html    ← landing page (hero, sign up / login modals, demo preview)
├── app.html      ← the expense tracker (profile-aware, demo-aware)
└── README.md
```

Two files. No build tools. No `node_modules`. Open `index.html` in any browser and it just works.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 (custom properties, Grid, Flexbox) |
| Logic | Vanilla JavaScript (ES6+) |
| Storage | Browser `localStorage` (per-user keys) |
| Fonts | Google Fonts — Syne + DM Mono |
| Hosting | Netlify |

---

## Local Development

No build step required:

```bash
git clone https://github.com/yourusername/kharcha.git
cd kharcha
open index.html
```

Or serve locally so redirects between pages work cleanly:

```bash
npx serve .
# visit http://localhost:3000
```

---

## Deployment on Netlify

### First deploy (drag and drop)
1. Keep both files as `index.html` and `app.html` in the same folder
2. Go to [app.netlify.com](https://app.netlify.com) → Sites → drag your project folder into the drop zone
3. Netlify serves `index.html` as the homepage automatically

### Redeploying after changes
1. Go to your site on Netlify → Deploys tab
2. Drag the updated folder into the drop zone again

### Connect to GitHub (recommended)
1. Push the project to a GitHub repo
2. In Netlify → Add new site → Import from Git → pick your repo
3. Every `git push` auto-deploys — no manual dragging needed

---

## Data & Privacy

All data lives entirely in the user's browser via `localStorage`. Nothing is ever sent to a server. Clearing browser data will reset the app — this is intentional for a zero-backend design.
Each user's expenses are stored under a unique key `kharcha_v1_{username}`, so multiple profiles can coexist on the same device without overlapping.

---

## Roadmap

- [ ] Edit an existing expense
- [ ] Export expenses to CSV
- [ ] Recurring expense tracking
- [ ] PWA support (installable on mobile, works offline)
- [ ] Multiple currency support
- [ ] Supabase backend for cross-device sync

---

## Built With Vibe Coding

This project was built using **vibe coding** — describing features in plain English to Claude (AI) and iterating from there. No prior coding experience was needed to ship v1.

> *"Vibe coding is when you fully give in to the vibes, embrace exponential technologies, and forget that the code even exists."* — Andrej Karpathy

---
---

<p align="center">Made with ☕ and Claude</p>
