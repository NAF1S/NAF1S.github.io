
# Lokman Sharif — Portfolio & Blog

A lightweight, responsive portfolio and blog built with **Jekyll**. It deploys to GitHub Pages automatically — no extra setup, no frameworks, no build tools. Just HTML + CSS + a few lines of JavaScript.

## Project structure

```
.
├── _config.yml            # Site title, description, plugins, URL rules
├── index.html             # Home page (hero, about, skills, projects, etc.)
├── blog.html              # Blog listing page
├── style.css              # All styles (dark/light mode, responsive)
├── _layouts/
│   ├── default.html       # Shared header / nav / footer
│   └── post.html          # Single blog post layout
└── _posts/                # ← Put blog posts here
```

## How to add a blog post

1. Create a file in `_posts/` named `YYYY-MM-DD-your-title.md` (the date controls ordering).
2. Add this front matter at the top, then write Markdown below it:

```markdown
---
layout: post
title: "My New Post"
description: "Short summary shown on the blog list."
tags:
  - backend
---

Your post content in Markdown...
```

That's it — the post automatically appears on the homepage and the blog page.

## How to edit your info

Everything lives in `index.html`:

| Section    | Where to edit                                    |
| ---------- | ------------------------------------------------ |
| Hero       | `index.html` top section                         |
| About      | `#about` section                                 |
| Skills     | `#skills` section                                |
| Projects   | `#projects` section (add/remove cards)           |
| Achievements | `#achievements` section                        |
| Contact    | `#contact` section (email, GitHub, Codeforces)   |

Colors and spacing live in `style.css` (top of the file has the color tokens). Dark/light mode is automatic and follows the visitor's system setting.

## Run locally (optional)

Requires Ruby and Bundler:

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000

## Deploy to GitHub Pages

The repo is already a GitHub Pages user site (`NAF1S.github.io`), so deployment is just pushing to `main`:

```bash
git add .
git commit -m "Update portfolio"
git push origin main
```

GitHub Pages builds and publishes automatically at **https://naf1s.github.io** (make sure Pages is enabled for the `main` branch — usually it is by default for `username.github.io` repos).

> Note: the resume PDF and other private files are listed in `.gitignore` so they are never published. Your phone number is intentionally not shown on the public site — add it in the `#contact` section of `index.html` if you want it visible. If you add a LinkedIn URL, link it there too.

