# 🔧 Git Setup & Deployment Guide

Panduan lengkap setup Git dan deploy portfolio ke GitHub Pages.

## 📋 Prerequisites

### Install Git
Cek apakah Git sudah terinstall:
```bash
git --version
```

Jika belum ada, download di: https://git-scm.com/downloads

### Setup Git Identity (First Time Only)
```bash
git config --global user.name "Nama Anda"
git config --global user.email "email@example.com"
```

### Buat Akun GitHub
Jika belum punya: https://github.com/signup

---

## 🚀 Quick Deploy (5 Menit)

### Step 1: Inisialisasi Git
```bash
# Masuk ke folder portfolio
cd C:\Projects\Portofolio

# Init Git
git init

# Check status
git status
```

### Step 2: Staging Files
```bash
# Add semua file
git add .

# Atau add file specific:
git add index.html
git add README.md
git add QUICKSTART.md

# Check apa yang di-stage
git status
```

### Step 3: Commit Pertama
```bash
git commit -m "Initial commit: Portfolio website"
```

### Step 4: Buat Repository di GitHub
1. Buka https://github.com/new
2. Repository name: `portfolio` (atau nama lain)
3. Description: "My personal portfolio website"
4. Pilih **Public**
5. **JANGAN** centang "Initialize with README" (sudah ada)
6. Click **Create repository**

### Step 5: Connect & Push
GitHub akan kasih command, copy-paste ke terminal:

```bash
# Connect ke GitHub
git remote add origin https://github.com/USERNAME/portfolio.git

# Rename branch ke main
git branch -M main

# Push pertama kali
git push -u origin main
```

**Ganti `USERNAME` dengan username GitHub Anda!**

### Step 6: Enable GitHub Pages
1. Di repository GitHub → **Settings**
2. Sidebar kiri → **Pages**
3. Under "Source":
   - Branch: **main**
   - Folder: **/ (root)**
4. Click **Save**
5. Tunggu 2-3 menit

**Portfolio Anda online di:**
```
https://USERNAME.github.io/portfolio/
```

---

## 🔄 Update Portfolio (Setelah Edit)

### Workflow Normal
```bash
# 1. Check perubahan
git status

# 2. Add file yang diubah
git add index.html
# atau add semua:
git add .

# 3. Commit dengan message
git commit -m "Update: Personalisasi data pribadi"

# 4. Push ke GitHub
git push
```

### Common Commit Messages
```bash
git commit -m "Initial commit: Portfolio website"
git commit -m "Update: Personal information"
git commit -m "Add: Profile photo"
git commit -m "Update: Projects section"
git commit -m "Fix: WhatsApp link"
git commit -m "Improve: Mobile responsiveness"
```

---

## 📝 Git Workflow Best Practices

### Before Making Changes
```bash
# Pastikan di branch main
git branch

# Pull latest (jika kerja dari multiple devices)
git pull
```

### After Making Changes
```bash
# Check apa yang berubah
git status
git diff

# Stage changes
git add .

# Commit
git commit -m "Descriptive message"

# Push
git push
```

---

## 🌿 Branching (Advanced)

Untuk perubahan besar, buat branch baru:

```bash
# Buat branch baru
git checkout -b update-projects

# Lakukan perubahan...

# Commit di branch baru
git add .
git commit -m "Major update: Projects section"

# Push branch baru
git push -u origin update-projects

# Merge ke main (via GitHub Pull Request atau lokal)
git checkout main
git merge update-projects
git push
```

---

## 🔍 Useful Git Commands

### Check Status & History
```bash
# Status file
git status

# Lihat commit history
git log
git log --oneline

# Lihat perubahan
git diff
```

### Undo Changes
```bash
# Undo changes sebelum staging
git checkout -- index.html

# Unstage file
git reset HEAD index.html

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Undo last commit (discard changes) - HATI-HATI!
git reset --hard HEAD~1
```

### Remote Operations
```bash
# Check remote
git remote -v

# Update remote URL
git remote set-url origin https://github.com/USERNAME/new-repo.git

# Fetch from remote
git fetch

# Pull from remote
git pull
```

---

## 🆘 Troubleshooting

### Error: "fatal: not a git repository"
```bash
# Pastikan di folder yang benar
cd C:\Projects\Portofolio

# Init git jika belum
git init
```

### Error: "fatal: remote origin already exists"
```bash
# Remove existing remote
git remote remove origin

# Add remote lagi
git remote add origin https://github.com/USERNAME/portfolio.git
```

### Error: "Updates were rejected"
```bash
# Force push (jika yakin) - HATI-HATI!
git push -f origin main

# Atau pull dulu, resolve conflict, push lagi
git pull origin main
# Fix conflicts jika ada
git add .
git commit -m "Resolve merge conflicts"
git push
```

### Error: "Permission denied (publickey)"
Setup SSH key atau gunakan HTTPS:
```bash
# Gunakan HTTPS URL
git remote set-url origin https://github.com/USERNAME/portfolio.git
```

### Forgot to Add File
```bash
# Add forgotten file
git add forgotten-file.html

# Amend last commit
git commit --amend --no-edit

# Force push (karena history berubah)
git push -f
```

---

## 🔐 Authentication

### Personal Access Token (Recommended)
Jika diminta password saat push:

1. GitHub Settings → Developer settings → Personal access tokens
2. Generate new token (classic)
3. Select scopes: `repo`
4. Copy token
5. Gunakan sebagai password saat git push

### SSH Key (Alternative)
```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "email@example.com"

# Copy public key
cat ~/.ssh/id_ed25519.pub

# Add ke GitHub: Settings → SSH and GPG keys → New SSH key
```

---

## 📊 GitHub Pages Settings

### Custom Domain
1. Beli domain (Namecheap, GoDaddy, dll)
2. Di GitHub Pages settings, add custom domain
3. Update DNS di domain provider:
   ```
   Type: CNAME
   Name: www (atau @)
   Value: USERNAME.github.io
   ```
4. Wait for DNS propagation (24-48 hours)

### HTTPS
- GitHub Pages automatically provides HTTPS
- Force HTTPS: Settings → Pages → Enforce HTTPS

### 404 Page
Buat file `404.html` di root folder:
```html
<!DOCTYPE html>
<html>
<head>
  <title>404 - Page Not Found</title>
</head>
<body>
  <h1>Oops! Page not found</h1>
  <a href="/">Back to Home</a>
</body>
</html>
```

---

## 🎯 Complete Workflow Example

Dari awal sampai online:

```bash
# 1. Setup
cd C:\Projects\Portofolio
git init
git add .
git commit -m "Initial commit"

# 2. Create repo di GitHub (via browser)

# 3. Connect & push
git remote add origin https://github.com/USERNAME/portfolio.git
git branch -M main
git push -u origin main

# 4. Enable GitHub Pages (via browser)
#    Settings → Pages → main branch → Save

# 5. Update website
# Edit files...
git add .
git commit -m "Update: Personal info"
git push

# Done! Changes live in 1-2 minutes
```

---

## 💡 Pro Tips

### 1. Commit Often
```bash
# Bad: 1 commit untuk banyak changes
git commit -m "Update everything"

# Good: Multiple commits yang descriptive
git commit -m "Update: Hero section name"
git commit -m "Add: Profile photo"
git commit -m "Update: Projects section"
```

### 2. Use .gitignore
File `.gitignore` sudah disediakan. Customize jika perlu:
```bash
# Edit .gitignore
code .gitignore

# Add pattern
*.backup
temp/
```

### 3. Check Before Push
```bash
git status
git diff
git log --oneline -5
```

### 4. Backup Before Major Changes
```bash
# Create backup branch
git checkout -b backup-before-major-update
git push -u origin backup-before-major-update
git checkout main
```

### 5. Use Git GUI (Optional)
Jika tidak nyaman dengan command line:
- **GitHub Desktop** (recommended): https://desktop.github.com/
- **GitKraken**: https://www.gitkraken.com/
- **VS Code Git integration**: Built-in

---

## 📚 Learn More

### Git Basics
- [Git Official Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

### GitHub Pages
- [GitHub Pages Documentation](https://docs.github.com/pages)
- [Custom Domain Setup](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site)

### Interactive Learning
- [Learn Git Branching](https://learngitbranching.js.org/)
- [GitHub Learning Lab](https://lab.github.com/)

---

## ✅ Checklist

Sebelum push ke GitHub:

- [ ] Git installed & configured
- [ ] Files edited & tested locally
- [ ] Sensitive data removed
- [ ] .gitignore configured
- [ ] Meaningful commit message
- [ ] GitHub account ready
- [ ] Repository created (Public)

After first push:

- [ ] GitHub Pages enabled
- [ ] Website accessible
- [ ] All links working
- [ ] Mobile responsive tested
- [ ] HTTPS working

---

## 🎊 You're All Set!

Portfolio Anda sekarang:
- ✅ Under version control (Git)
- ✅ Backed up online (GitHub)
- ✅ Accessible worldwide (GitHub Pages)
- ✅ Easy to update (git push)

**Selamat!** Anda sekarang seorang web developer dengan portfolio online! 🚀

---

**Pro Tip:** Bookmark URL portfolio Anda dan share di:
- LinkedIn profile
- Instagram bio
- Email signature
- CV/Resume

---

*Last Updated: November 2026*

**Good luck!** 💪
