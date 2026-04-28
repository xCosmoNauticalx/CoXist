# Co-Xist — The Federation of Worker Cooperatives

The official website for Co-Xist, a federation of worker cooperatives — a network where companies join as equal co-owners, share infrastructure and protections, and keep what they build.

## Live site

Deployed via Vercel. To deploy your own instance, see **Hosting on Vercel** below.

## What this site does

- **Path chooser** — visitors pick "I'm a Worker" or "I'm a Founder / Company"
- **Worker survey** — 6 questions about skills, goals, and experience; produces a Fit Index score and personalized match result
- **Founder survey** — 7 questions about structure preference, worker benefits, and operational needs; recommends a package tier and produces a Fit Index score

## Structure

This is a single-file HTML site. Everything — HTML, CSS, JavaScript, and the Co-Xist SVG mark — lives in `index.html`. No build step, no dependencies, no npm.

```
coxist/
└── index.html    ← the entire site
```

## Hosting on Vercel

### Option A — Vercel dashboard (no CLI needed)

1. Push this repo to GitHub (see below)
2. Go to [vercel.com](https://vercel.com) and sign in with GitHub
3. Click **Add New → Project**
4. Select this repository
5. Leave all settings at their defaults — Vercel detects a static site automatically
6. Click **Deploy**

Your site will be live at `your-project.vercel.app` in about 30 seconds.

### Option B — Vercel CLI

```bash
npm i -g vercel
vercel
```

Follow the prompts. Done.

### Custom domain

In the Vercel dashboard → your project → **Settings → Domains** → add your domain (e.g. `co-xist.coop`). Vercel provides free SSL automatically.

## Pushing to GitHub

If you haven't used Git before:

```bash
# 1. Install Git: https://git-scm.com/downloads

# 2. Create a new repo at github.com, then:
git init
git add .
git commit -m "Initial commit — Co-Xist federation site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

Then connect the repo in Vercel as described above.

## Editing the site

All content lives in `index.html`. Key sections:

| What you want to change | Search for |
|---|---|
| Hero headline | `Built by workers.` |
| Worker skill chips | `const workerSkills = [` |
| Worker survey questions | `QUESTION 01` through `QUESTION 06` |
| Founder benefit chips | `const companyBenefits = [` |
| Founder ops chips | `const companyOps = [` |
| Package pricing | `Foothold`, `Groundwork`, `Forge` |
| Match result messages | `w-submit` and `f-submit` event listeners |
| Colors | `:root {` at the top of the `<style>` block |

## Brand

- **Mark:** Co-Xist Concept C — bracketing gold C arc, lattice X, 8 nodes, gold center disc
- **Navy:** `#0b2545`
- **Blue:** `#1d4e89`
- **Gold:** `#d4a84b`
- **Cream:** `#eef2f7`
- **Fonts:** Bebas Neue (display), Fraunces (body), JetBrains Mono (mono) — all loaded from Google Fonts

## License

© Co-Xist Federation of Worker Cooperatives, MMXXVI. All rights reserved.
