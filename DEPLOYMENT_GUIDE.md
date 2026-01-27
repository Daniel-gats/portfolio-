# 🚀 Portfolio - Deployment Guide

## Quick Deployment Options

### Option 1: GitHub Pages (Recommended - Free)

1. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin YOUR_GITHUB_REPO_URL
   git push -u origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click "Settings" → "Pages"
   - Under "Source", select "main" branch
   - Click "Save"
   - Your portfolio will be live at: `https://yourusername.github.io/repository-name`

### Option 2: Netlify (Free)

1. **Push to GitHub** (same as above)

2. **Deploy on Netlify:**
   - Go to [netlify.com](https://netlify.com) and sign up
   - Click "Add new site" → "Import an existing project"
   - Connect to GitHub and select your repository
   - Configure:
     - **Build command**: Leave empty
     - **Publish directory**: Leave empty (root)
   - Click "Deploy site"
   - Your portfolio will be live with a custom URL

### Option 3: Vercel (Free)

1. **Push to GitHub** (same as above)

2. **Deploy on Vercel:**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - Click "Deploy"
   - Live at: `https://your-portfolio.vercel.app`

## Local Development

Simply open `index.html` in your browser, or use a local server:

```bash
# Using Python
python -m http.server 8080

# Using Node.js http-server
npx http-server -p 8080
```

Then visit: `http://localhost:8080`

## Customization Before Deployment

Make sure to update:
- [ ] Email address in contact section
- [ ] Social media links (GitHub, LinkedIn, Twitter)
- [ ] Portfolio projects with your actual work
- [ ] Skills percentages based on your experience
- [ ] Profile image (replace placeholder avatar)
- [ ] Services offered
- [ ] About section content

## Custom Domain (Optional)

### For GitHub Pages:
1. Buy a domain from any registrar
2. In your repo settings → Pages → Custom domain
3. Add your domain and configure DNS

### For Netlify/Vercel:
1. Go to domain settings in dashboard
2. Add your custom domain
3. Follow DNS configuration instructions

## Performance Optimization

Before deploying:
- ✅ Minify CSS (optional)
- ✅ Optimize images
- ✅ Test on multiple devices
- ✅ Check all links work
- ✅ Verify contact form (may need backend)

## Updating Your Portfolio

```bash
# Make changes to your files
git add .
git commit -m "Update: added new project"
git push origin main
```

Your site will automatically redeploy!

## Contact Form Setup

The current form is frontend-only. To make it functional:

**Option 1: Formspree**
- Sign up at [formspree.io](https://formspree.io)
- Add action to form: `<form action="https://formspree.io/f/YOUR_ID" method="POST">`

**Option 2: Netlify Forms**
- Add `netlify` attribute to form tag
- Forms automatically work on Netlify

**Option 3: EmailJS**
- Sign up at [emailjs.com](https://emailjs.com)
- Add their SDK and configure in `script.js`

## Troubleshooting

**Issue**: Styles not loading
- Check file paths are relative
- Ensure all CSS/JS files are committed to Git

**Issue**: Images not showing
- Verify image paths
- Check images are in repository

**Issue**: 404 errors
- Ensure deployment directory is set to root
- Check all file names match exactly (case-sensitive)

---
Made with ❤️ by Daniel Mugo Gatonye
