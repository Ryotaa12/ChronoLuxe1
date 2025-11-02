# GitHub Pages Setup Guide

## Steps to Deploy Your HTML Site to GitHub Pages

### 1. Create a GitHub Repository
1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right, then select "New repository"
3. Name your repository (e.g., `chronoluxe-website`)
4. Make it **Public** (required for free GitHub Pages)
5. Don't initialize with README, .gitignore, or license
6. Click "Create repository"

### 2. Upload Your Files
You can use one of these methods:

#### Method A: Using GitHub Web Interface
1. Go to your new repository
2. Click "uploading an existing file"
3. Drag and drop all your HTML files, `assets` folder, and `uploads` folder
4. Click "Commit changes"

#### Method B: Using Git Command Line
```bash
# Navigate to your project folder
cd "C:\wamp64\www\BACKUP CHRONOLUXE"

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: HTML/CSS/JS version"

# Add your GitHub repository (replace YOUR_USERNAME and YOUR_REPO)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** section (in left sidebar)
4. Under "Source", select **main** branch
5. Click **Save**
6. Wait a few minutes, then visit: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME`

### 4. Important Notes

#### File Structure
Make sure your repository has this structure:
```
your-repo/
├── index.html
├── products.html
├── product.html
├── about.html
├── contact.html
├── login.html
├── register.html
├── cart.html
├── checkout.html
├── account.html
├── privacy.html
├── terms.html
├── assets/
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── app.js
└── uploads/
    └── products/
        └── (your product images)
```

#### Image Paths
- All images in `uploads/products/` should be uploaded to GitHub
- The HTML files use relative paths like `uploads/products/p_1761758122_2533dc9b.jpg`
- If images don't load, they'll show placeholder images automatically

#### Forms
- Forms on the HTML pages use `alert()` messages for demo purposes
- For real functionality, you'll need to connect to a backend API or use a service like:
  - Netlify Forms
  - Formspree
  - EmailJS
  - Your own PHP/Node.js backend

### 5. Custom Domain (Optional)
1. In GitHub Pages settings, add your custom domain
2. Update DNS records as instructed by GitHub
3. Enable HTTPS (automatic with GitHub Pages)

### 6. Troubleshooting
- **404 errors**: Make sure `index.html` is in the root directory
- **Styles not loading**: Check that `assets/css/style.css` path is correct
- **Images not showing**: Verify `uploads/products/` folder is uploaded
- **Changes not appearing**: Wait 1-2 minutes after pushing, or do a hard refresh (Ctrl+F5)

### 7. Updating Your Site
```bash
# Make changes to your files
# Then:
git add .
git commit -m "Updated content"
git push
```
Changes will be live in 1-2 minutes!
