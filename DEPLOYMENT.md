# Deployment Guide

This guide will help you deploy your Hello World website to both GitHub Pages and Hostinger.

## GitHub Pages Deployment

### Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right corner and select "New repository"
3. Name your repository (e.g., `hello-world-website`)
4. Make it public (required for free GitHub Pages)
5. Don't initialize with README (we already have one)
6. Click "Create repository"

### Step 2: Connect Local Repository to GitHub

Run these commands in your terminal:

```bash
# Add the remote repository (replace YOUR_USERNAME and REPO_NAME)
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# Push your code to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to "Pages" section
4. Under "Source", select "Deploy from a branch"
5. Choose "main" branch and "/ (root)" folder
6. Click "Save"
7. Your site will be available at: `https://YOUR_USERNAME.github.io/REPO_NAME`

## Hostinger Deployment

### Step 1: Prepare Files

Your files are ready for Hostinger deployment. You'll need:
- `index.html` (main file)
- Any other assets (CSS, JS, images)

### Step 2: Upload to Hostinger

1. Log in to your Hostinger control panel
2. Go to "File Manager" or use FTP
3. Navigate to the `public_html` folder
4. Upload your `index.html` file
5. Your site will be available at your domain

### Step 3: Auto-Deployment (Optional)

For automatic deployment from GitHub to Hostinger:

1. In Hostinger, go to "Git" section
2. Connect your GitHub repository
3. Set up automatic deployment on push to main branch

## Testing Your Deployment

1. **GitHub Pages**: Visit `https://YOUR_USERNAME.github.io/REPO_NAME`
2. **Hostinger**: Visit your domain name

## Troubleshooting

### GitHub Pages Issues
- Ensure repository is public
- Check that `index.html` is in the root directory
- Wait a few minutes for deployment to complete

### Hostinger Issues
- Make sure `index.html` is in the `public_html` folder
- Check file permissions (should be 644)
- Verify domain DNS settings

## Next Steps

1. Customize the website content
2. Add more pages
3. Include custom domain
4. Set up analytics

## Support

If you encounter any issues:
- Check GitHub Pages documentation
- Contact Hostinger support
- Review browser console for errors 