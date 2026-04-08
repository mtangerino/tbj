# The Beige Journal - URL Redirect Service

This GitHub Pages site provides automatic 301 redirects from your old WordPress domain to your new Blogger blog. It handles all 183 posts with proper URL mapping.

## Setup Instructions

### Step 1: Create a GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Create a new public repository named `yourusername.github.io`
   - Replace `yourusername` with your actual GitHub username
   - **Must be public** for GitHub Pages to work

### Step 2: Push Files to GitHub

```bash
# Navigate to this directory
cd /Users/mandytang/Desktop/Claude/Wordpress\ transfer/github-redirect-setup

# Initialize git repo
git init
git add .
git commit -m "Initial redirect setup"

# Add GitHub remote and push
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git branch -M main
git push -u origin main
```

### Step 3: Configure GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Source", select **main** branch
4. Click **Save**

### Step 4: Point Your Domain to GitHub Pages

Go to your domain registrar and add a CNAME record:
- **Host**: `@` or domain root
- **Points to**: `your-username.github.io`

Or add A records pointing to GitHub:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

### Step 5: Enable Custom Domain

1. In GitHub repo Settings → Pages
2. Enter custom domain: `thebeigejournal.com`
3. Check "Enforce HTTPS"
4. Wait 5-10 minutes for DNS propagation

## How It Works

- `index.html` contains all 183 URL mappings
- Visitors to old URLs are automatically redirected to Blogger
- 301 redirects preserve search engine rankings

## Testing

Visit: `https://thebeigejournal.com/2025/12/some-post/`
Should redirect to Blogger automatically.

---

For detailed instructions, see the setup steps above.
