# 🗺️ Your Geospatial Research Website
## Complete Setup & Deployment Guide

---

## What You're Getting

A complete academic personal website with:
- **Home page** with bio and recent work
- **Research Articles** section (peer-reviewed papers, working papers)
- **Opinion** section (commentary and essays)
- **CV page** (structured academic resume)
- **Browser-based editor** (no code needed to write new posts)
- **Free hosting** on Netlify

---

## Step 1 — Install Hugo on Your Computer

Hugo is needed only for local testing. You can skip this and go straight to Step 2 if you prefer to edit directly online.

### Mac
```bash
brew install hugo
```
*(Install Homebrew first from brew.sh if needed)*

### Windows
Download from: https://github.com/gohugoio/hugo/releases
- Grab the file ending in `_windows-amd64.zip`
- Extract and add to your PATH

### Verify
```bash
hugo version
```

---

## Step 2 — Put Your Site on GitHub

1. Create a free account at **github.com** if you don't have one
2. Click **"New repository"** → name it `my-research-site` (or anything you like)
3. Set it to **Public**, click **Create repository**
4. Open your terminal/command prompt and run:

```bash
cd path/to/hugo-site          # navigate to the folder I built for you
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/my-research-site.git
git push -u origin main
```

*(Replace `YOUR-USERNAME` with your GitHub username)*

---

## Step 3 — Deploy to Netlify (Free Hosting)

1. Go to **netlify.com** and sign up (use "Sign up with GitHub")
2. Click **"Add new site"** → **"Import an existing project"**
3. Choose **GitHub** → select your `my-research-site` repository
4. Netlify will auto-detect Hugo settings from `netlify.toml`
5. Click **"Deploy site"**

Your site will be live at a URL like `https://amazing-einstein-123.netlify.app` in about 60 seconds.

### Set a custom subdomain (optional, free)
In Netlify → Site settings → Domain management → Options → Edit site name
→ Change to e.g. `yourname-geo.netlify.app`

---

## Step 4 — Enable the Visual Editor (Decap CMS)

This gives you a WordPress-like editor to write articles from your browser — no code needed.

1. In Netlify: go to **Site configuration → Identity**
2. Click **"Enable Identity"**
3. Scroll to **"Registration preferences"** → set to **Invite only**
4. Go to **Site configuration → Git Gateway** → Click **"Enable Git Gateway"**
5. Go back to **Identity** → Click **"Invite users"** → enter your email
6. Check your email and accept the invite
7. Visit **yoursite.netlify.app/admin** to open the editor

You'll see a clean interface to write Research Articles and Opinion pieces — just click, type, and save.

---

## Step 5 — Personalize Your Site

Open `hugo.toml` in any text editor and update:

```toml
title = "Jane Smith | Geospatial Research"

[params]
  author = "Jane Smith"
  description = "Researcher in spatial analytics, urban geography, and GIS"
  subtitle = "Spatial Analytics · Urban GIS · Remote Sensing"
  email = "jane@university.edu"
  github = "janesmith"        # your GitHub username
  linkedin = "jane-smith-geo" # your LinkedIn username
```

Then edit `content/_index.md` to write your actual bio.

---

## Writing New Articles

### Option A — Using the Visual Editor (recommended)
1. Go to `yoursite.netlify.app/admin`
2. Log in
3. Click **"Research Articles"** or **"Opinion Pieces"**
4. Click **"New [type]"**
5. Fill in the form, write your content
6. Click **"Publish"** → your site updates in ~30 seconds

### Option B — Writing Markdown files directly

Create a file in `content/research/your-title.md`:

```markdown
---
title: "Your Paper Title"
date: 2025-03-10
journal: "Journal of Geospatial Research"
doi: "10.0000/yourpaper"
tags: ["spatial statistics", "GIS", "urban"]
summary: "A brief abstract shown on the listing page."
---

Your full article content goes here in Markdown.

## Introduction

Write paragraphs normally. **Bold**, *italic*, [links](https://example.com).

## Methods

...
```

Then run `git add . && git commit -m "New article" && git push`
→ Site updates automatically.

---

## Folder Structure Reference

```
hugo-site/
├── hugo.toml              ← Site settings (title, author, links)
├── netlify.toml           ← Hosting config (don't touch)
├── content/
│   ├── _index.md          ← Your home page bio
│   ├── cv.md              ← Your CV page
│   ├── research/          ← Research articles go here
│   └── opinions/          ← Opinion pieces go here
├── static/
│   ├── css/main.css       ← Design/styling
│   └── admin/             ← CMS editor files (don't touch)
└── layouts/               ← Page templates (don't touch)
```

---

## Custom Domain (Optional, ~$12/year)

1. Buy a domain at Namecheap, Google Domains, or Cloudflare
2. In Netlify: Site settings → Domain management → Add custom domain
3. Follow Netlify's DNS instructions

---

## Need Help?

- Hugo docs: https://gohugo.io/documentation/
- Decap CMS docs: https://decapcms.org/docs/
- Netlify docs: https://docs.netlify.com/
- Hugo community forum: https://discourse.gohugo.io/

---

*Site built with Hugo · Hosted on Netlify · Editor powered by Decap CMS*
