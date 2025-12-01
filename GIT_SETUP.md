# How to Save Your Website to a Git Repository

## Step 1: Configure Git (One-time setup)

First, tell Git who you are. Run these commands in Terminal (replace with your info):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

**Example:**
```bash
git config --global user.name "Chris Bousaada"
git config --global user.email "chris@example.com"
```

## Step 2: Commit Your Files

I've already initialized the repository and added your files. Now you just need to commit:

```bash
git commit -m "Initial commit: Mechanical engineering portfolio website"
```

## Step 3: Create a GitHub Repository

1. **Go to GitHub.com** and sign in (or create an account if you don't have one)
2. **Click the "+" icon** in the top right → "New repository"
3. **Name your repository** (e.g., `mechanical-engineering-portfolio` or `personal-website`)
4. **Make it Public** (so GitHub Pages works for free)
5. **Don't** initialize with README, .gitignore, or license (you already have files)
6. **Click "Create repository"**

## Step 4: Connect and Push to GitHub

GitHub will show you commands. Run these in Terminal (replace `YOUR_USERNAME` and `YOUR_REPO_NAME`):

```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git branch -M main
git push -u origin main
```

**Example:**
If your username is `chrisbousaada` and repo is `mechanical-portfolio`:
```bash
git remote add origin https://github.com/chrisbousaada/mechanical-portfolio.git
git branch -M main
git push -u origin main
```

## Step 5: Enable GitHub Pages (Free Hosting!)

1. **Go to your repository on GitHub**
2. **Click "Settings"** (top menu)
3. **Click "Pages"** (left sidebar)
4. **Under "Source"**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. **Click "Save"**
6. **Wait 1-2 minutes**, then visit: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

## Future Updates

Whenever you make changes to your website:

```bash
git add .
git commit -m "Description of what you changed"
git push
```

Your website will automatically update on GitHub Pages!

---

## Quick Reference Commands

```bash
# Check status
git status

# See what changed
git diff

# Add all changes
git add .

# Commit changes
git commit -m "Your message here"

# Push to GitHub
git push
```

