# GitHub Pages Setup Instructions

## What I've Done For You ✅

I've already completed these steps:

1. ✅ Created beautiful HTML versions of your Privacy Policy and Terms of Service
2. ✅ Created a landing page with links to both documents
3. ✅ Initialized a git repository in `/Desktop/ShopTalk-V1/shoptalk-legal/`
4. ✅ Made the first commit with all files

**The repository is ready to push to GitHub!**

---

## What You Need To Do (5 Minutes)

### Step 1: Create the GitHub Repository (2 minutes)

1. Go to https://github.com and log in
2. Click the **green "New"** button (top left) or go to https://github.com/new
3. Fill in the details:
   - **Repository name:** `shoptalk-legal` (exactly this name)
   - **Description:** "Legal documents for ShopTalk mobile app"
   - **Public** (must be public for GitHub Pages to work on free plan)
   - **DO NOT** check "Add a README file"
   - **DO NOT** add .gitignore
   - **DO NOT** add a license
4. Click **"Create repository"**

### Step 2: Push Your Code to GitHub (2 minutes)

After creating the repository, GitHub will show you a page with instructions. **Ignore those!** Instead:

1. Open Terminal (if not already open)
2. Copy and paste these commands **one at a time**:

```bash
cd /Users/alexanderhughes/Desktop/ShopTalk-V1/shoptalk-legal
```

```bash
git remote add origin https://github.com/[YOUR-GITHUB-USERNAME]/shoptalk-legal.git
```
**⚠️ IMPORTANT:** Replace `[YOUR-GITHUB-USERNAME]` with your actual GitHub username!

```bash
git push -u origin main
```

3. GitHub will ask for your credentials:
   - **Username:** Your GitHub username
   - **Password:** Use a **Personal Access Token** (not your password)

   **Don't have a token?** Create one at: https://github.com/settings/tokens
   - Click "Generate new token (classic)"
   - Give it a name like "ShopTalk Legal Upload"
   - Check the "repo" checkbox
   - Click "Generate token"
   - Copy the token and use it as your password

### Step 3: Enable GitHub Pages (1 minute)

1. Go to your repository on GitHub: `https://github.com/[YOUR-USERNAME]/shoptalk-legal`
2. Click **"Settings"** tab (top right)
3. Scroll down and click **"Pages"** in the left sidebar
4. Under "Branch":
   - Select **"main"** from the dropdown
   - Keep **"/ (root)"** selected
   - Click **"Save"**
5. Wait 1-2 minutes for deployment

### Step 4: Get Your URLs (30 seconds)

After a minute or two, refresh the Settings → Pages page.

You'll see a message: **"Your site is live at https://[your-username].github.io/shoptalk-legal/"**

Your legal document URLs are:
- **Privacy Policy:** `https://[your-username].github.io/shoptalk-legal/privacy-policy.html`
- **Terms of Service:** `https://[your-username].github.io/shoptalk-legal/terms-of-service.html`

---

## Step 5: Update app.json (30 seconds)

Once you have your URLs, I need to update the URLs in your app.json file.

**Tell me your GitHub username and I'll update app.json automatically!**

Or you can do it manually:

1. Open `/app/app.json`
2. Find these lines (around line 34-36):
```json
"privacyPolicyUrl": "https://alexandermhughes.com/shoptalk/privacy-policy",
"termsOfServiceUrl": "https://alexandermhughes.com/shoptalk/terms-of-service",
```

3. Replace with:
```json
"privacyPolicyUrl": "https://[your-username].github.io/shoptalk-legal/privacy-policy.html",
"termsOfServiceUrl": "https://[your-username].github.io/shoptalk-legal/terms-of-service.html",
```

---

## Troubleshooting

### "fatal: remote origin already exists"
Run: `git remote remove origin` then try the `git remote add` command again.

### "Permission denied" when pushing
You need a Personal Access Token, not your password. See Step 2 above.

### "404 - Page not found" on GitHub Pages
- Wait 2-3 minutes - it takes time to deploy
- Check Settings → Pages shows "Your site is published"
- Make sure repository is **Public**

### GitHub Pages not showing up
- Repository must be **Public** (private repos need paid GitHub plan for Pages)
- Branch must be set to **main** in Settings → Pages
- Wait a few minutes and refresh

---

## Quick Summary

**Commands to run:**
```bash
cd /Users/alexanderhughes/Desktop/ShopTalk-V1/shoptalk-legal
git remote add origin https://github.com/[YOUR-USERNAME]/shoptalk-legal.git
git push -u origin main
```

**Then:**
1. Go to repo Settings → Pages
2. Set Branch to "main" and save
3. Wait 2 minutes
4. Get your URLs
5. Update app.json with the new URLs

---

## Need Help?

If you get stuck:
1. Send me the error message you're seeing
2. Tell me which step you're on
3. I'll help you fix it!

Once this is done, your legal documents will be publicly hosted and compliant with Apple's App Store requirements! 🎉
