# SID.LAMMATA — Portfolio Page

Personal app portfolio landing page. Single-file HTML — no build tools, no dependencies, no frameworks. Just drop it on GitHub Pages and it works.

**Live:** [lowcodesid.github.io/sid-lammata](https://lowcodesid.github.io/sid-lammata/)

---

## What's in here

A dark, single-page portfolio showcasing built apps in a 3-column bento grid. Features:

- Animated gradient "Coming Soon" card for unreleased apps
- Persistent colour-coded tag system across all cards
- App counter (live vs coming soon) embedded in the header
- Orange → deep blue gradient launch buttons
- Green availability status dot
- Responsive — collapses to 2-col on tablet, 1-col on mobile
- Zero JavaScript dependencies — pure HTML/CSS

---

## Apps

| # | Name | Status | URL |
|---|------|--------|-----|
| 1 | Borrow Scope | ✅ Live | [borrowscope](https://lowcodesid.github.io/borrowscope/) |
| 2 | Pick AFL Team | ✅ Live | [pick-afl-team](https://lowcodesid.github.io/pick-afl-team/) |
| 3 | Premium Deals | ✅ Live | [premium-deals](https://lowcodesid.github.io/premium-deals/) |
| 4 | My Money | ✅ Live | [my-money](https://lowcodesid.github.io/my-money/) |
| 5 | Been There | ✅ Live | *(add URL when deployed)* |
| 6 | TRACE | 🔒 Coming Soon | — |

---

## Adding a new app

1. Copy an existing card block in `index.html`
2. Update the icon, title, description, joke, tags, and `href` on the launch button
3. Pick tag classes from the tag system below — reuse existing ones where possible
4. Update the counter in the header: change `5` and `1` to the new counts

```html
<!-- Card template -->
<div class="card">
  <div class="card-glow"></div>
  <div class="card-header">
    <span class="card-icon">🔧</span>
    <h2 class="card-title">App Name</h2>
  </div>
  <div class="card-desc">
    One or two sentences describing what this app does and who it's for.
  </div>
  <div class="card-divider"></div>
  <div class="card-joke">"Your witty one-liner goes here."</div>
  <div class="tags">
    <span class="tag tag-finance">Finance</span>
  </div>
  <a href="https://your-app-url" target="_blank" rel="noopener" class="launch-btn">
    Open app
    <svg viewBox="0 0 24 24"><path d="M7 17L17 7M17 7H7M17 7v10"/></svg>
  </a>
</div>
```

---

## Tag colour system

Tags are persistent — the same category always uses the same colour across all cards.

| Class | Colour | Use for |
|-------|--------|---------|
| `tag-finance` | Violet | Finance, budgeting, money tools |
| `tag-property` | Cyan | Property, real estate |
| `tag-homeloans` | Amber | Mortgages, borrowing, loans |
| `tag-afl` / `tag-footy` | Red | AFL, Australian football |
| `tag-quiz` | Pink | Quizzes, surveys, pickers |
| `tag-travel` | Sky blue | Travel, trips, destinations |
| `tag-businessclass` / `tag-flights` | Indigo | Premium flights, deals |
| `tag-wealth` | Gold | Wealth tracking, assets |
| `tag-networth` | Emerald | Net worth, liabilities |
| `tag-insights` | Teal | Data insights, dashboards |
| `tag-worldmap` | Lime green | Maps, geography, exploration |
| `tag-interactive` | Orange | Interactive tools, visualisations |

To add a new tag category, add a CSS rule following this pattern:

```css
.tag-yourcategory {
  color: #hex;
  border-color: rgba(r,g,b,0.45);
  background: rgba(r,g,b,0.11);
}
```

---

## Moving an app from Coming Soon → Live

1. Replace the `card-coming-soon` block with a standard `card` block using the template above
2. Add the real app URL to the launch button
3. Update the header counter numbers

---

## Design tokens

| Token | Value | Used for |
|-------|-------|---------|
| `--bg` | `#07070e` | Page background |
| `--bg-card` | `#0e0e1c` | Card background |
| `--accent` | `#FF6B00` | Orange — buttons, punchlines, highlights |
| `--green` | `#50fa7b` | Status dot, code comments, joke text |
| `--text` | `#f5f5fd` | Primary text |
| `--sub` | `#9898b8` | Tagline, secondary text |
| `--muted` | `#6060a0` | Labels, footer, hints |
| `--border` | `#202038` | Card borders |

---

## Deployment

This is a single `index.html` file. To deploy on GitHub Pages:

1. Rename `portfolio.html` → `index.html`
2. Push to your repo's `main` branch (or `gh-pages`)
3. Enable GitHub Pages in repo Settings → Pages → Source: `main` / `root`

---

## Contact

- **GitHub:** [github.com/lowcodesid](https://github.com/lowcodesid)
- **LinkedIn:** [linkedin.com/in/sidlammata](https://www.linkedin.com/in/sidlammata/)
- **Email:** sid.lammata@gmail.com
