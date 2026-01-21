# Deploying Mandarin AI to GitHub Pages

## Quick Start

### Step 1: Preview Locally
```bash
open /Users/wesley/projects/mandarin-ai/index.html
```

### Step 2: Create a GitHub Repository
1. Go to https://github.com/new
2. Repository name: `mandarin-ai`
3. Make it **Public**
4. Do NOT check "Add a README file" (we have one)
5. Click **Create repository**

### Step 3: Push Your Code
```bash
cd /Users/wesley/projects/mandarin-ai
git init
git add .
git commit -m "Initial commit: Mandarin AI website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/mandarin-ai.git
git push -u origin main
```

### Step 4: Enable GitHub Pages
1. Go to your repo on GitHub
2. Click **Settings** (tab at the top)
3. Click **Pages** in the left sidebar
4. Under "Build and deployment":
   - Source: **Deploy from a branch**
   - Branch: **main** / **/ (root)**
5. Click **Save**

Wait 1-2 minutes. Your site will be live at:
```
https://YOUR_USERNAME.github.io/mandarin-ai/
```

---

## Custom Domain Setup (Optional)

To use `mandarinai.com`:

### 1. GitHub Settings
In **Settings > Pages**, enter `mandarinai.com` under "Custom domain"

### 2. Create CNAME File
```bash
echo "mandarinai.com" > CNAME
git add CNAME && git commit -m "Add custom domain" && git push
```

### 3. Configure DNS
At your domain registrar, add these records:

**A Records** (for apex domain):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME Record** (for www):
```
www -> YOUR_USERNAME.github.io
```

### 4. Enable HTTPS
Check "Enforce HTTPS" in GitHub Pages settings (may take up to 24 hours after DNS propagates)

---

## Updating the Site

After making changes:
```bash
git add .
git commit -m "Update website"
git push
```

Changes will be live within 1-2 minutes.

---

## Troubleshooting

**Site not loading?**
- Check Settings > Pages for any error messages
- Ensure repository is public
- Wait a few minutes after enabling Pages

**Custom domain not working?**
- DNS changes can take up to 48 hours to propagate
- Verify DNS records with: `dig mandarinai.com +short`
- Check for CNAME file in repository root

**HTTPS certificate error?**
- Wait 24 hours after DNS propagates
- Try removing and re-adding the custom domain in settings
