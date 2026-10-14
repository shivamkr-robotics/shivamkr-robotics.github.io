# shivamkr-robotics.github.io

Live at **https://shivamkr-robotics.github.io**. Every push to `main` redeploys the site.


One self-contained file: `index.html`. No build step, no framework, no server. Any static host can serve it.

## 1. What's inside

- `index.html` is the whole site.
- `media/` holds the photos, video clips and social preview image (`og.jpg`). Keep it next to `index.html`.
- `vendor/three.min.js` is the 3D engine (three.js, MIT licence) used by the drone viewport and the MineGuard terrain. Keep it next to `index.html` too.

Your emails, LinkedIn, GitHub and résumé are already wired in. To update the résumé later, replace `media/Shivam_Kumar_Resume.pdf` with a new file of the same name.

To swap a photo, replace the file in `media/` with one of the same name (WebP, around 1600 px on the long side).

## 2. Preview locally

Double-click `index.html`. It opens in your browser. Videos and photos load from the `media/` folder.

## 3. Deploy — pick one

### Option A · Netlify Drop (fastest, ~1 minute, no Git)
1. Go to https://app.netlify.com/drop
2. Drag the whole `shivam-portfolio-site` folder onto the page.
3. You get a live URL like `random-name-123.netlify.app`. Sign up (free) to keep it and rename it under **Site configuration → Change site name**, e.g. `shivamkumar.netlify.app`.
4. To update later: **Deploys → drag the folder again**.

### Option B · GitHub Pages (best long-term, free, looks good to recruiters)
1. Create a GitHub account if you don't have one.
2. Create a new **public** repository named exactly `<your-username>.github.io`.
3. Click **Add file → Upload files**, drag in `index.html` and the `media` folder, then **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
5. After a minute or two the site is live at `https://<your-username>.github.io`.
6. To update: edit `index.html` on GitHub (pencil icon) or upload a new version and commit.

From the terminal instead (Ubuntu):
```bash
cd shivam-portfolio-site
git init && git add . && git commit -m "Portfolio v1"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
git push -u origin main
```

### Option C · Vercel
1. Push the folder to any GitHub repo (as in Option B, any repo name).
2. Go to https://vercel.com → **Add New → Project** → import the repo → **Deploy**. Leave all settings at defaults; there's no framework to pick.
3. Live at `<project>.vercel.app`; every `git push` redeploys automatically.

## 4. Custom domain (optional)
- Buy a domain such as `shivamkumar.dev` or `shivamkumar.in` from any registrar (Namecheap, Cloudflare, GoDaddy, Hostinger).
- Students: check the GitHub Student Developer Pack, which has historically included a free domain for a year.
- Then add it in your host:
  - **GitHub Pages:** Settings → Pages → Custom domain. At your registrar, add a `CNAME` record for `www` pointing to `<your-username>.github.io`, plus the four `A` records GitHub lists in its docs for the bare domain. Tick **Enforce HTTPS** once it appears.
  - **Netlify / Vercel:** Domains → Add domain, then copy the DNS records they show into your registrar.
- DNS can take from a few minutes up to a day.

## 5. After it's live
- Put the URL on your resume header, LinkedIn "Featured" section and GitHub profile README.
- Test it on your phone and in both themes (button in the top-right).
- Press `Ctrl K` (or `/`) on the site to open the quick-jump menu.
