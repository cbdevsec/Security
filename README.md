# Aya — Cybersecurity Portfolio

A single-page portfolio site: dark violet/cyan theme, scroll-triggered reveals, an animated network-node background, a typing terminal in the hero, and small canvas visuals on each project. Pure HTML/CSS/JS — no build step, no dependencies.

## Files
- `index.html` — page content
- `style.css` — theme + layout + animations
- `script.js` — scroll reveals, terminal effect, canvas backgrounds
- `assets/logo.svg` — your logo (also used as the favicon)

## Before you publish
- Swap the placeholder links in the Contact section (`mailto:you@example.com`, GitHub, LinkedIn) for your real ones — search `index.html` for `#contact`.
- Everything else (certs, projects, timeline, clubs) is already filled in from your background — edit any wording directly in `index.html`.

## Blog

The site now has a blog, built on Jekyll — which GitHub Pages runs for you automatically, so there's no build step on your end.

**To write a new post:**
1. Add a file to `_posts/` named `YYYY-MM-DD-your-title.md` (the date in the filename sets the post's date).
2. Give it front matter at the top like this:
   ```yaml
   ---
   layout: post
   title: "Your post title"
   date: 2026-07-19
   tags: [ctf, writeup]
   excerpt: "One sentence describing the post, shown on the blog index."
   ---
   ```
3. Write the rest of the post in plain Markdown below the `---`.
4. Commit and push — it appears automatically at `/blog/`, newest first.

A starter post is already in `_posts/` as an example — edit or delete it.

**If you deploy to a project repo** (anything other than `yourusername.github.io`), open `_config.yml` and uncomment the `baseurl` line, setting it to your repo name (e.g. `baseurl: "/aya-portfolio"`). This isn't needed if your repo is named `yourusername.github.io`.

**Testing the blog locally** needs Jekyll (Ruby-based), which is more setup than the plain-HTML pages:
```bash
gem install bundler jekyll
cd aya-cyber-portfolio
bundle init
bundle add jekyll
bundle exec jekyll serve
```
Then open `http://localhost:4000`. If that's more setup than you want right now, you can skip local testing — GitHub Pages will build it the same way, you'll just check it after pushing.

## Deploy to GitHub Pages
1. Create a new repository on GitHub (e.g. `aya-portfolio`). If you want it at `yourusername.github.io`, name the repo exactly that.
2. Upload these files to the repo — either drag-and-drop them in the GitHub web UI, or from a terminal:
   ```bash
   cd aya-cyber-portfolio
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```
3. On GitHub, go to the repo's **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Under **Branch**, choose `main` and folder `/ (root)`, then **Save**.
6. Wait a minute, then your site is live at:
   - `https://YOUR_USERNAME.github.io/YOUR_REPO/` (normal repo), or
   - `https://YOUR_USERNAME.github.io/` (if the repo is named `YOUR_USERNAME.github.io`)

No further setup needed — it's a static site.
