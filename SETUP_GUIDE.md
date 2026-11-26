# KESHPHOTOGRAPHY — Website Setup Guide

This is your complete website. It is built to be edited entirely by you, with no coding,
through a private **/admin** page once it is live.

You do this setup **once** (about 30–45 minutes). After that, you only ever use /admin.

--------------------------------------------------------------------
## WHAT YOU HAVE
- A fast, modern website (Astro) in the warm paper + charcoal + gold brand look
- A **Cinema Dark Mode** toggle in the top menu
- Story Lens hero, filterable portfolio, Screening Room lightbox, Build Your Story quote form
- A **/admin** content manager (Decap CMS) where you log in and edit everything
- The "Build Your Story" form sends enquiries to your **Netlify Forms** inbox + your email
- The Visual Thread logo is already embedded, with a slot in /admin to upload your own

--------------------------------------------------------------------
## BEFORE YOU START — make 2 free accounts
1. **GitHub** → https://github.com  (stores your website files)
2. **Netlify** → https://netlify.com (hosts the site for free, runs /admin login + forms)
   - Tip: click "Sign up with GitHub" so they connect automatically.
Keep your **domain login** handy (where you bought keshphotography.net / .com).

--------------------------------------------------------------------
## STEP 1 — Put the files on GitHub
1. Unzip this folder on your computer.
2. On GitHub click the **+** (top right) → **New repository**.
3. Name it `keshphotography`, keep it **Public** (or Private — both work), click **Create repository**.
4. On the new repo page click **"uploading an existing file"**.
5. Drag **all the files and folders from this unzipped folder** into the browser window.
   (Do NOT drag the outer folder itself — drag what is *inside* it.)
6. Click **Commit changes**.

--------------------------------------------------------------------
## STEP 2 — Connect Netlify (puts it online)
1. In Netlify click **Add new site → Import an existing project → GitHub**.
2. Pick your `keshphotography` repo.
3. Netlify auto-detects the settings (Build command `npm run build`, Publish directory `dist`).
   Just click **Deploy**.
4. Wait ~1 minute. Netlify gives you a temporary address like `random-name.netlify.app`.
   Click it — your site is live! 🎉

--------------------------------------------------------------------
## STEP 3 — Turn on your /admin login
1. In Netlify, open your site → **Integrations** (or **Identity** in older menus) → enable **Identity**.
   - Newer Netlify calls this **"Netlify Identity"**. Click **Enable Identity**.
2. Under **Identity → Registration**, set it to **Invite only** (so only you can log in).
3. Still under Identity, find **Services → Git Gateway** and click **Enable Git Gateway**.
4. Click **Identity → Invite users**, type **your email**, send the invite.
5. Check your email, click the link, and **set your password**.

Now go to **your-site.netlify.app/admin** → log in with that email + password.
You can now edit everything. ✅

--------------------------------------------------------------------
## STEP 4 — Connect your real domain (keshphotography.net / .com)
1. In Netlify: **Domain management → Add a domain** → type `keshphotography.net`.
2. Netlify shows you DNS records (a few lines).
3. Log in to your domain registrar (where you bought the domain) → find **DNS settings**.
4. Add the records Netlify showed you (it walks you through it).
5. Repeat **Add a domain** for `keshphotography.com` if you want both to work.
6. Give it a few hours. Netlify adds a free HTTPS padlock automatically.

> After the domain is live, your admin page is simply **keshphotography.net/admin**.

--------------------------------------------------------------------
## STEP 5 — Your enquiry form
The "Build Your Story" form uses **Netlify Forms** — already wired, nothing to set up.
- Every submission appears in Netlify under **Forms → build-your-story**.
- To also get an **email** each time: Netlify → **Forms → Settings → Form notifications
  → Add notification → Email notification**, and enter your email. Done.

--------------------------------------------------------------------
## HOW YOU EDIT THE SITE (the whole point)
Go to **keshphotography.net/admin**, log in, and you'll see simple forms:

- **Site Settings** — your logo (upload your own here), phone, email, social links.
- **01 · Hero (Story Lens)** — the big opening image and headline.
- **02 · About Kesh** — your portrait and bio.
- **Services** — the three service cards.
- **03 · Portfolio Items** — add/remove/reorder your work. For each item:
    - Pick a **category** (which filter it shows under)
    - Pick **type**: Photo, Widescreen video (16:9), or Vertical reel (9:16)
    - **Paste any link** from YouTube, Instagram, TikTok or Facebook — the site
      automatically frames it at the right shape. For photos, upload the image.
    - Add the **Story behind the frame** (location, client, director's notes)

Click **Publish**. Your live site updates by itself in about a minute.

--------------------------------------------------------------------
## REPLACING THE PLACEHOLDER (DECOY) CONTENT
Every placeholder is labelled so you know exactly what it is:
- `01_Hero_Featured_Visual` = main hero photo
- `02_About_Kesh_Portrait`  = your about photo
- `03_Portfolio_Title` etc. = each portfolio item
The sample photos are from Unsplash and the sample videos are public links —
just replace each one in /admin with your own.

--------------------------------------------------------------------
## SWAPPING IN YOUR REAL LOGO
In **/admin → Site Settings → Logo**, upload your transparent PNG or SVG.
It replaces the built-in Visual Thread mark everywhere instantly.

--------------------------------------------------------------------
## WANT TO PREVIEW ON YOUR OWN COMPUTER FIRST? (optional, not required)
If you ever want to run it locally:
1. Install Node.js (https://nodejs.org).
2. Open this folder in a terminal, run: `npm install` then `npm run dev`.
3. Open the address it prints (usually http://localhost:4321).
You never *have* to do this — editing happens on the live /admin.

--------------------------------------------------------------------
## QUICK TROUBLESHOOTING
- **/admin won't log in?** Make sure Identity AND Git Gateway are both enabled (Step 3),
  and that you accepted the email invite and set a password.
- **Edits not showing?** Give it ~1 minute (Netlify rebuilds), then refresh. Check Netlify
  → Deploys to see it building.
- **A video won't embed?** Paste the normal share link (not a private/unlisted-restricted one).
  TikTok/Instagram embeds need the post to be public.

That's it. Welcome to your new site. — Built for KESHPHOTOGRAPHY
