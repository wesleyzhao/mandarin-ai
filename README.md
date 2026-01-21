# Mandarin AI Website

A professional single-page consulting website for Mandarin AI, an AI-focused technology service, education, and advising firm.

## Quick Start

1. Clone or download this repository
2. Open `index.html` in a browser to preview locally
3. Deploy to GitHub Pages (instructions below)

## Deploying to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** icon in the top right and select **New repository**
3. Name it `mandarin-ai` (or `mandarinai.github.io` for a user/org site)
4. Make it **Public**
5. Do NOT initialize with README (we already have files)
6. Click **Create repository**

### Step 2: Push Your Code

From the `mandarin-ai` directory, run:

```bash
git init
git add .
git commit -m "Initial commit: Mandarin AI website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/mandarin-ai.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** tab
3. In the left sidebar, click **Pages**
4. Under "Source", select **Deploy from a branch**
5. Select **main** branch and **/ (root)** folder
6. Click **Save**

Your site will be live at: `https://YOUR_USERNAME.github.io/mandarin-ai/`

### Step 4: Custom Domain (Optional)

To use a custom domain like `mandarinai.com`:

1. In **Settings > Pages**, enter your domain under "Custom domain"
2. Add a CNAME file to your repo with your domain name
3. Configure DNS at your domain registrar:
   - For apex domain (mandarinai.com): Add A records pointing to GitHub's IPs:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - For www subdomain: Add a CNAME record pointing to `YOUR_USERNAME.github.io`
4. Check "Enforce HTTPS" in GitHub Pages settings

## Customization

### Team Photos

Replace the placeholder initials with actual photos:

1. Add photos to the `assets/team/` folder
2. In `index.html`, find the `.team-photo` divs and replace the `<span>` with:
   ```html
   <img src="assets/team/wesley.jpg" alt="Wesley Zhao">
   ```

### Contact Email

Search for `hello@mandarinai.com` in `index.html` and replace with your actual email.

### Logos

The credentials section uses SVG text placeholders. For official logos:

1. Download official logos from each institution's brand resources
2. Add them to `assets/logos/`
3. Replace the SVG text with `<img>` tags

## File Structure

```
mandarin-ai/
├── index.html          # Main website (HTML + CSS + JS)
├── README.md           # This file
└── assets/
    ├── logos/          # Institution logos
    └── team/           # Team member photos
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome for Android)

## Performance

The site is optimized for fast loading:
- No external JavaScript frameworks
- Minimal CSS (embedded)
- Google Fonts with preconnect
- Lazy animations with Intersection Observer

## License

Copyright 2025 Mandarin AI. All rights reserved.
