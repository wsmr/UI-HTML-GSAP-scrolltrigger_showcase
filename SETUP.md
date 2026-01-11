# GitHub Repository Setup Guide

This guide will help you set up and deploy your GSAP ScrollTrigger Showcase to GitHub.

## 📋 Prerequisites

- Git installed on your computer ([Download Git](https://git-scm.com/downloads))
- GitHub account ([Sign up](https://github.com/signup))
- Code editor (VS Code, Sublime Text, etc.)

## 🚀 Step-by-Step Setup

### 1. Create Repository on GitHub

1. Go to [GitHub](https://github.com)
2. Click the **"+"** icon in the top right
3. Select **"New repository"**
4. Fill in the details:
   - **Repository name**: `UI-HTML-GSAP-scrolltrigger_showcase` (or your preferred name)
   - **Description**: "A comprehensive collection of scroll animations using GSAP ScrollTrigger"
   - **Public** or **Private**: Your choice
   - **DO NOT** initialize with README (we'll add our own)
5. Click **"Create repository"**

### 2. Prepare Your Local Files

Create a folder on your computer with these files:

```
UI-HTML-GSAP-scrolltrigger_showcase/
├── index.html          # The main showcase HTML
├── README.md          # Project documentation
├── LICENSE           # MIT License
├── CONTRIBUTING.md   # Contribution guidelines
└── .gitignore       # Git ignore rules
```

**Copy the content from the artifacts I provided into these files.**

### 3. Initialize Git Repository

Open terminal/command prompt in your project folder:

```bash
# Navigate to your project folder
cd path/to/UI-HTML-GSAP-scrolltrigger_showcase

# Initialize git repository
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: GSAP ScrollTrigger Showcase"

# Rename branch to main (if needed)
git branch -M main
```

### 4. Connect to GitHub

Replace `wsmr` with your GitHub username:

```bash
# Add remote repository
git remote add origin https://github.com/wsmr/UI-HTML-GSAP-scrolltrigger_showcase.git

# Push to GitHub
git push -u origin main
```

### 5. Enable GitHub Pages (Optional)

To host your showcase for free on GitHub Pages:

1. Go to your repository on GitHub
2. Click **"Settings"**
3. Scroll to **"Pages"** in the left sidebar
4. Under **"Source"**, select **"main"** branch
5. Click **"Save"**
6. Your site will be published at: `https://wsmr.github.io/UI-HTML-GSAP-scrolltrigger_showcase/`

Wait a few minutes, then visit your site!

## 🔄 Making Updates

When you make changes to your project:

```bash
# Check what files changed
git status

# Add changed files
git add .

# Commit with a message
git commit -m "Add new parallax effect"

# Push to GitHub
git push
```

## 🌐 Custom Domain (Optional)

To use a custom domain with GitHub Pages:

1. Buy a domain from a registrar (Namecheap, GoDaddy, etc.)
2. In your repository, create a file named `CNAME` with your domain:
   ```
   www.yourdomain.com
   ```
3. Configure DNS settings at your registrar:
   - Add a CNAME record pointing to `wsmr.github.io`
4. Wait for DNS propagation (up to 48 hours)

## 📝 Customizing for Your Use

Before pushing to GitHub, update these fields:

**In README.md:**
- Replace `wsmr` with your GitHub username
- Replace `Your Name` with your actual name
- Replace `@yourtwitter` with your Twitter handle (or remove)
- Add your contact information

**In LICENSE:**
- Replace `[Your Name]` with your actual name

**In index.html:**
- Customize colors, gradients, and content
- Add your own branding

## 🛠️ Git Commands Reference

| Command | Description |
|---------|-------------|
| `git status` | Check status of files |
| `git add .` | Add all changed files |
| `git commit -m "message"` | Commit changes |
| `git push` | Push to GitHub |
| `git pull` | Pull latest changes |
| `git log` | View commit history |
| `git branch` | List branches |
| `git checkout -b feature` | Create new branch |

## 🔧 Troubleshooting

### "Permission denied (publickey)"

Generate and add SSH key:

```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your_email@example.com"

# Add to ssh-agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# Copy public key
cat ~/.ssh/id_ed25519.pub
```

Then add it to GitHub: Settings → SSH and GPG keys → New SSH key

### "Repository not found"

Check your remote URL:

```bash
git remote -v
```

Fix if needed:

```bash
git remote set-url origin https://github.com/wsmr/repo-name.git
```

### Merge Conflicts

If you edited files on GitHub and locally:

```bash
git pull
# Resolve conflicts in your editor
git add .
git commit -m "Resolve merge conflicts"
git push
```

## 📱 Sharing Your Project

After setup, share using:

- **GitHub URL**: `https://github.com/wsmr/UI-HTML-GSAP-scrolltrigger_showcase`
- **Live Demo**: `https://wsmr.github.io/UI-HTML-GSAP-scrolltrigger_showcase/`
- **Social Media**: Share screenshots and link
- **README Badge**: Add badges for stars, license, etc.

## 🎯 Next Steps

1. ✅ Set up repository
2. ✅ Push initial commit
3. ✅ Enable GitHub Pages
4. 📝 Customize content
5. 🎨 Add your own effects
6. 📢 Share with community
7. ⭐ Get stars and contributions!

## 💡 Tips

- Commit often with clear messages
- Use branches for new features
- Test locally before pushing
- Keep README updated
- Respond to issues and PRs
- Add screenshots to README

## 📚 Additional Resources

- [GitHub Docs](https://docs.github.com)
- [Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [GSAP Documentation](https://greensock.com/docs/)
- [ScrollTrigger Docs](https://greensock.com/docs/v3/Plugins/ScrollTrigger)

---

Need help? Open an issue or reach out to the community!

Good luck with your project! 🚀
