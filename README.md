# Logan J. Pallin — Academic Website

Personal academic website for Logan J. Pallin, Postdoctoral Researcher in Marine Vertebrate Ecophysiology at UC Santa Cruz.

## Quick Start — GitHub Pages Deployment

### 1. Create a GitHub repository
1. Go to [github.com](https://github.com) and sign in
2. Click **+** → **New repository**
3. Name it `your-username.github.io` (for a root site) **or** any name like `website` (for `your-username.github.io/website`)
4. Set visibility to **Public**
5. Click **Create repository**

### 2. Upload files
**Option A — GitHub web interface (easiest):**
1. Open your new repository
2. Click **Add file** → **Upload files**
3. Drag in `index.html` and the `images/` folder
4. Click **Commit changes**

**Option B — Git command line:**
```bash
git init
git add index.html images/
git commit -m "Initial website"
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

### 3. Enable GitHub Pages
1. Go to your repository → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: `main`, folder: `/ (root)`
4. Click **Save**
5. Wait ~2 minutes — your site will appear at `https://YOUR-USERNAME.github.io/YOUR-REPO/`

---

## Personalizing the Site

### Adding your headshot
1. Save your photo as `images/logan-pallin.jpg` (square crop, minimum 600×600 px)
2. In `index.html`, find the comment `★ PHOTO INSTRUCTIONS ★`
3. Replace the `<div class="profile-placeholder">` block with:
   ```html
   <img class="profile-photo" src="images/logan-pallin.jpg" alt="Logan J. Pallin">
   ```

### Adding photos to the gallery
1. Put your photos in the `images/` folder
2. Find the `Fun & Photos` section in `index.html`
3. For each slot, uncomment and update the `<img>` tag:
   ```html
   <img src="images/your-photo.jpg" alt="Caption">
   ```

### Adding research figures
Each research card has a comment like `★ FIGURE: Replace with...`
Replace the placeholder `<div>` with:
```html
<img src="images/research-repro.jpg" alt="Description" style="position:absolute;inset:0;width:100%;height:100%;object-fit:cover;">
```

### Updating social links
In the `Contact` section, update:
- **Instagram**: Replace `https://www.instagram.com/` with your handle URL
- **Google Scholar**: Replace `PLACEHOLDER` in the URL with your Scholar user ID
  (find it in your Scholar profile URL: `scholar.google.com/citations?user=XXXXXXX`)

### Keeping publications current
Publications are plain HTML in the `#publications` section — just edit the text directly.
Update the stats bar numbers (citations, h-index) at the top of that section each year.

---

## File Structure

```
your-repo/
├── index.html          ← The entire website (single file)
├── images/             ← Add all photos here
│   ├── logan-pallin.jpg       (profile headshot)
│   ├── research-repro.jpg     (reproductive physiology figure)
│   ├── research-climate.jpg   (climate change figure)
│   ├── research-stress.jpg    (stress physiology figure)
│   ├── research-pop.jpg       (population ecology figure)
│   ├── research-dive.jpg      (diving physiology figure)
│   ├── research-art.jpg       (IAS exhibit photo)
│   ├── outreach-exhibit.jpg   (IAS exhibition photo)
│   ├── photo-1.jpg            (gallery photos)
│   └── ...
└── README.md           ← This file (optional, GitHub only)
```

---

## Custom Domain (optional)

To use a custom domain like `loganpallin.com`:
1. Buy a domain from Namecheap, Google Domains, etc.
2. In your repo, create a file called `CNAME` containing just your domain:
   ```
   loganpallin.com
   ```
3. In your domain registrar, point DNS to GitHub:
   - Add 4 A records pointing to GitHub's IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Add a CNAME record: `www` → `YOUR-USERNAME.github.io`
4. In GitHub Settings → Pages → Custom domain, enter your domain

---

*Website built May 2026. Single HTML file, no build step required.*
