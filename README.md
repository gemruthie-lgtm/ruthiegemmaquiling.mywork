# ruthiegemmaquiling.mywork
# Finance Portfolio Website

A professional personal finance and investment portfolio website built with React + Vite.

## Tech Stack

- **React 18** — component-based UI
- **Vite** — fast local dev server & build tool
- **Vanilla CSS** — purple theme via CSS variables (no Tailwind needed)
- **Vercel** — recommended deployment platform

---

## Project Structure

```
finance-portfolio/
├── index.html                  # HTML entry point + Google Fonts
├── vite.config.js              # Vite configuration
├── vercel.json                 # Vercel deployment config
├── package.json
└── src/
    ├── main.jsx                # React root
    ├── App.jsx                 # Root component + routing
    ├── index.css               # Global styles + purple CSS variables
    ├── data/
    │   └── index.js            # ← ALL mock data lives here (edit this!)
    └── components/
        ├── Navbar.jsx          # Sticky navigation bar
        ├── UI.jsx              # Shared components (Card, Modal, Badge, etc.)
        ├── HomeSection.jsx     # Homepage hero + tiles
        ├── PortfolioSection.jsx
        ├── EquitySection.jsx
        └── Sections.jsx        # Commentary, ETF, Planning, Journal
```

---

## Running Locally

```bash
# 1. Install dependencies
npm install

# 2. Start dev server
npm run dev

# 3. Open http://localhost:5173
```

---

## Editing Your Content

**All your data is in one file: `src/data/index.js`**

Each section has its own exported array:
- `portfolioCases` — Portfolio Case Studies
- `equityReports` — Equity Research Reports
- `marketCommentary` — Monthly Market Commentary
- `etfComparisons` — ETF Comparison Projects
- `planningCases` — Financial Planning Cases
- `tradingJournal` — Trading Journal entries

To add a new entry, copy an existing object in the array and update the fields.

---

## Deploying to Vercel (Free)

### Option A — GitHub + Vercel (recommended, auto-deploys on every push)

```bash
# Push to GitHub first
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/finance-portfolio.git
git push -u origin main
```

Then:
1. Go to [vercel.com](https://vercel.com) → **Add New Project**
2. Import your GitHub repo
3. Click **Deploy** — done!

Every time you push to GitHub, Vercel auto-redeploys.

### Option B — Deploy directly (no GitHub needed)

```bash
npm run build
npx vercel deploy dist/
```

---

## Customising the Purple Theme

Open `src/index.css` — all colors are CSS variables at the top:

```css
--purple-700: #5228b0;   /* main brand purple */
--purple-600: #6b3dd4;   /* accents, links */
--purple-500: #8b5cf6;   /* labels, badges */
```

Change these hex values to instantly retheme the entire site.

---

## Adding a Custom Domain

1. Buy a domain (e.g. `yourname.com`) from Namecheap or Google Domains (~$12/yr)
2. In Vercel dashboard → your project → **Settings → Domains**
3. Add your domain and follow the DNS instructions
4. Done — your portfolio is live at `yourname.com`
