# Bricklog Website

A simple, clean website for the Bricklog iOS app - a LEGO collection tracker.

## 🚀 Quick Deploy to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in (or create an account)
2. Click the **+** button in the top right → **New repository**
3. Name it: `bricklog-website` (or `marvey.app` if you want)
4. Keep it **Public** (required for free GitHub Pages)
5. Click **Create repository**

### Step 2: Upload the Files

**Option A: Using GitHub Web Interface (Easiest)**

1. In your new repository, click **uploading an existing file**
2. Drag and drop all the files from this folder:
   - `index.html`
   - `privacy.html`
   - `terms.html`
3. Click **Commit changes**

**Option B: Using Git Command Line**

```bash
cd bricklog-website
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/bricklog-website.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. In your repository, go to **Settings** (tab at the top)
2. In the left sidebar, click **Pages**
3. Under "Source", select **Deploy from a branch**
4. Select **main** branch and **/ (root)** folder
5. Click **Save**
6. Wait 1-2 minutes, then your site will be live at:
   `https://YOUR_USERNAME.github.io/bricklog-website/`

## 🌐 Custom Domain Setup (marvey.app)

Once you purchase the domain, follow these steps:

### Step 1: Add Domain to GitHub Pages

1. In your repo's **Settings → Pages**
2. Under "Custom domain", enter: `marvey.app`
3. Click **Save**
4. Check **Enforce HTTPS** (after DNS propagates)

### Step 2: Configure DNS at Your Domain Registrar

Add these DNS records:

**For apex domain (marvey.app):**
```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

**For www subdomain (optional):**
```
Type: CNAME
Name: www
Value: YOUR_USERNAME.github.io
```

### Step 3: Add CNAME File

Create a file named `CNAME` (no extension) in your repository with just:
```
marvey.app
```

DNS propagation can take up to 24-48 hours.

## 📝 Customization Checklist

Before going live, update these items:

- [ ] **Email address**: Replace `support@marvey.app` with your actual email
- [ ] **App Store link**: Uncomment and update the App Store badge in `index.html` when your app is live
- [ ] **Screenshots**: Add app screenshots to an `images/` folder and uncomment the screenshots section
- [ ] **Hero image**: Add a hero screenshot and uncomment in `index.html`
- [ ] **Privacy Policy**: Review and adjust based on your actual data practices
- [ ] **Terms of Service**: Review the governing law section (currently set to Belgium)

## 📁 File Structure

```
bricklog-website/
├── index.html      # Main landing page
├── privacy.html    # Privacy Policy (required for App Store)
├── terms.html      # Terms of Service
├── CNAME           # Custom domain config (create when ready)
└── images/         # Screenshots folder (create and add images)
    ├── screenshot-1.png
    ├── screenshot-2.png
    └── ...
```

## 🖼️ Adding Screenshots

1. Create an `images/` folder in your repository
2. Add your app screenshots (recommended: 250-300px width for web display)
3. Uncomment the screenshots section in `index.html`
4. Update the image paths

**Recommended screenshot dimensions:**
- Export from Xcode/Simulator at 1x scale
- Or resize to ~600px width for good quality at 2x display

## 🎨 Customizing Colors

The color scheme uses CSS variables in each HTML file. To change colors, edit the `:root` section:

```css
:root {
    --primary: #E3000B;      /* LEGO red - main accent color */
    --primary-dark: #B8000A; /* Darker red for hover states */
    --dark: #1a1a2e;         /* Dark text/backgrounds */
    --gray: #6b7280;         /* Secondary text */
    --light-gray: #f3f4f6;   /* Light backgrounds */
    --white: #ffffff;
}
```

## 📱 App Store Submission URLs

When submitting to the App Store, use these URLs:

- **Privacy Policy URL**: `https://marvey.app/privacy.html`
- **Support URL**: `https://marvey.app/#contact` or `https://marvey.app/`
- **Marketing URL**: `https://marvey.app/`

(Replace `marvey.app` with your GitHub Pages URL if not using custom domain)

## 💡 Tips

- GitHub Pages is completely free for public repositories
- HTTPS is automatically enabled
- Changes deploy automatically when you push to main branch
- Use a service like [Formspree](https://formspree.io) if you want a contact form instead of email link

---

Made with ❤️ for Marvey Studios
