# SDA Mudgee — by Brookline SDA
### Website Deployment Guide
**Domain:** www.sdamudgee.com.au  
**Site:** 127 Gladstone Street, Mudgee NSW 2850

---

## What's in this folder

| File | Description |
|------|-------------|
| `index.html` | The complete website — all images, floor plans and brochure PDF are embedded inside this single file |
| `netlify.toml` | Netlify configuration (security headers, caching, redirects) |
| `README.md` | This guide |

---

## Option A — Deploy with Netlify (Recommended, Free)

Netlify is the easiest way to get this live. It's free for sites like this.

### Step 1 — Create a Netlify account
1. Go to **https://netlify.com**
2. Click **Sign up** — use your email or sign in with Google

### Step 2 — Deploy the site
1. Once logged in, you'll see your Netlify dashboard
2. Find the box that says **"Drag and drop your site folder here"** (bottom of the page)
3. Drag the entire **`sdamudgee_site`** folder into that box
4. Netlify will deploy it in about 30 seconds
5. You'll get a random URL like `https://luminous-fox-abc123.netlify.app` — your site is live!

### Step 3 — Connect your custom domain (sdamudgee.com.au)
1. In your Netlify dashboard, click on your site
2. Go to **Site settings → Domain management**
3. Click **Add custom domain**
4. Type `sdamudgee.com.au` and click **Verify**
5. Netlify will show you DNS records to add — you'll need two:
   - An **A record** pointing to Netlify's IP
   - A **CNAME record** for `www`

### Step 4 — Update your DNS (where your domain is registered)
1. Log in to wherever you registered `sdamudgee.com.au` (e.g. GoDaddy, VentraIP, Crazy Domains, Netfleet)
2. Find **DNS Management** or **DNS Records**
3. Add the records Netlify showed you in Step 3
4. DNS changes take **15 minutes to 24 hours** to go live globally

### Step 5 — Enable HTTPS (free SSL)
1. Back in Netlify → **Site settings → Domain management**
2. Scroll to **HTTPS** and click **Verify DNS configuration**
3. Once DNS is verified, click **Provision certificate**
4. Your site will be live at `https://www.sdamudgee.com.au` ✓

---

## Option B — Deploy with GitHub Pages (Free, slightly more technical)

### Step 1 — Create a GitHub account
1. Go to **https://github.com** and sign up

### Step 2 — Create a new repository
1. Click the **+** icon → **New repository**
2. Name it `sdamudgee` (or anything you like)
3. Set it to **Public**
4. Click **Create repository**

### Step 3 — Upload your files
1. On your new repository page, click **uploading an existing file**
2. Drag both `index.html` and `netlify.toml` into the upload area
3. Scroll down and click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to your repository → **Settings** tab
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Select branch: **main**, folder: **/ (root)**
5. Click **Save**
6. After a minute, your site will be live at `https://yourusername.github.io/sdamudgee`

### Step 5 — Connect your custom domain
1. In GitHub Pages settings, enter `sdamudgee.com.au` in the **Custom domain** field
2. Follow the same DNS steps as Netlify Option A above

---

## Updating the website in future

When you want to update content (text, images, brochure etc):
1. Send your changes to your web developer
2. They'll give you a new `index.html` file
3. Simply drag the new file into Netlify to redeploy — it takes 30 seconds
4. Or in GitHub, upload the new `index.html` to replace the old one

---

## Connecting the email form

The **Register Your Interest** email form currently doesn't send emails yet.  
The easiest free option is **Formspree**:

1. Go to **https://formspree.io** and create a free account
2. Create a new form — you'll get a form endpoint like `https://formspree.io/f/xyzabc123`
3. In `index.html`, find the CTA section and replace the `<form>` tag's action with your Formspree endpoint
4. All registrations will be emailed directly to you

---

## Need help?

- Netlify support: https://docs.netlify.com
- GitHub Pages support: https://docs.github.com/pages
- Domain DNS help: contact your domain registrar's support

---

*Built for SDA Mudgee by Brookline SDA · 127 Gladstone Street, Mudgee NSW 2850*
