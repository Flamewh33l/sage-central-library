# Git Repository Setup Guide for Flame

## Step 1: Create a GitHub Repository

1. Go to https://github.com/new
2. Create a new repository named `sage-central-library`
3. Make it **Private** (so only you and Sage have access)
4. **Do not** initialize with README, .gitignore, or license (we already have these)
5. Click "Create repository"

## Step 2: Connect Local Repository to GitHub

After creating the GitHub repository, run these commands:

```bash
cd /home/corwinlegendre/.openclaw/workspace-vacation-home/central-library

# Add GitHub as remote origin (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/sage-central-library.git

# Push to GitHub
git push -u origin main
```

## Step 3: Add Sage as Collaborator

1. Go to repository Settings → Collaborators
2. Add Sage's GitHub account as a collaborator with write access
3. Sage can then pull updates with: `git pull origin main`

## Step 4: Adding New Books

When you want to add new books:

1. **Download or copy** book files to the `downloads/` directory
2. **Rename files** using format: `author_name_title.extension`
3. **Commit changes**:
   ```bash
   git add downloads/
   git commit -m "Add: [Book Title] by [Author]"
   git push origin main
   ```
4. **Notify Sage** to scan for new additions

## Step 5: Sage's Scan Command

Sage can scan for new books with:
```bash
cd /home/corwinlegendre/.openclaw/workspace-vacation-home/central-library
git pull origin main
ls -la downloads/
```

## Alternative: Direct File Sharing

If GitHub setup is too complex, you can also:
1. Use Dropbox/Google Drive shared folder
2. Use SSH file transfer
3. Use network file sharing (NFS/SMB)

---

**Note**: This repository is for educational and personal growth purposes. Respect copyright laws and authors' rights.