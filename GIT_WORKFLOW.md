# GitHub Workflow - Quick Reference

## 📝 Pushing Updates to GitHub

Use these commands whenever you make changes and want to push them to your GitHub repository.

### Basic Workflow (3 Steps)

```powershell
# Step 1: Check what files have changed
git status

# Step 2: Add your changes
git add .                          # Add ALL changed files
# OR
git add <specific-file>            # Add specific file(s)

# Step 3: Commit with a descriptive message
git commit -m "Your commit message describing what you changed"

# Step 4: Push to GitHub
git push origin main
```

### Example Workflow

```powershell
# Scenario: You updated calculate_citation_rates.py and README.md

git status                                           # See what changed
git add .                                           # Stage all changes
git commit -m "Fix citation rate calculation bug"   # Commit with message
git push origin main                                # Push to GitHub
```

---

## 🔍 Common Git Commands

### Check Repository Status
```powershell
git status              # See modified files
git log                 # View commit history
git remote -v           # Show GitHub repository URL
```

### Add Files
```powershell
git add .                           # Add everything
git add *.py                        # Add all Python files
git add "Input Excels/"             # Add specific folder
git add README.md calculate_*.py    # Add specific files
```

### Commit Changes
```powershell
git commit -m "Brief description of changes"
```

**Good commit messages:**
- ✅ "Add support for new AI platform (Claude)"
- ✅ "Fix bug in citation rate calculation"
- ✅ "Update README with new installation steps"
- ✅ "Add error handling for missing Excel files"

**Bad commit messages:**
- ❌ "update"
- ❌ "fix"
- ❌ "changes"

### Push to GitHub
```powershell
git push origin main               # Push to main branch
```

---

## 🚨 Common Scenarios

### Scenario 1: Quick Update
```powershell
git add .
git commit -m "Update citation calculation logic"
git push origin main
```

### Scenario 2: Multiple Files, Selective Add
```powershell
git status                                  # See what changed
git add calculate_citation_rates.py         # Add specific file
git add README.md                           # Add another file
git commit -m "Improve calculation accuracy and update docs"
git push origin main
```

### Scenario 3: Add New Files Only
```powershell
git add "new_script.py"
git commit -m "Add new analysis script"
git push origin main
```

### Scenario 4: Before Making Changes (Pull Latest)
```powershell
git pull origin main               # Get latest changes from GitHub
# ... make your changes ...
git add .
git commit -m "Your changes"
git push origin main
```

---

## ⚠️ Troubleshooting

### "Your branch is behind 'origin/main'"
```powershell
git pull origin main               # Pull latest changes first
git push origin main               # Then push your changes
```

### "Changes not staged for commit"
```powershell
git add .                          # You forgot to stage changes
git commit -m "Your message"
git push origin main
```

### "Nothing to commit"
```powershell
# You haven't made any changes since last commit
# Or you need to save your files first!
```

### Undo Last Commit (Before Pushing)
```powershell
git reset --soft HEAD~1            # Undo commit, keep changes
```

### Discard Changes to a File
```powershell
git restore <filename>             # WARNING: This deletes your changes!
```

---

## 📂 What Gets Pushed? (Based on .gitignore)

### ✅ Files that WILL be pushed:
- Python scripts (*.py)
- README.md
- Input Excels/*.csv
- .gitignore

### ❌ Files that WON'T be pushed:
- brand-presence-data/ (all Excel files)
- cutomer_urls/
- Output/
- __pycache__/
- *.pyc files

---

## 🎯 Quick Tips

1. **Commit often** - Small, frequent commits are better than large ones
2. **Write clear messages** - Future you will thank present you
3. **Check status first** - Always run `git status` before committing
4. **Pull before push** - If working from multiple computers, pull first
5. **Don't commit sensitive data** - Check .gitignore is working

---

## 📖 Your Repository

**Repository URL:** https://github.com/sharmarpit1989/tokowaka-measurement-automation

**View online:** Visit the URL above to see your code on GitHub

**Clone elsewhere:**
```powershell
git clone https://github.com/sharmarpit1989/tokowaka-measurement-automation.git
```

---

## 🆘 Need Help?

- Git documentation: https://git-scm.com/doc
- GitHub guides: https://guides.github.com/
- Common commands: https://training.github.com/downloads/github-git-cheat-sheet/

