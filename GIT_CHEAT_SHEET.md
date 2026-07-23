# Git Cheat Sheet

A quick reference for the most commonly used Git commands.

---

# 📂 General

### Initialize a new repository
```bash
git init
```

### Add a file
```bash
git add <file>
```

### Remove a file
```bash
git rm <file>
```

### Move or rename a file
```bash
git mv <from> <to>
```

### Commit changes
```bash
git commit
```

### Show repository status
```bash
git status
```

### View commit history
```bash
git log
```

### View commit history with tags
```bash
git log --decorate
```

### Search commit messages
```bash
git log --grep="<search>"
```

---

# 🌿 Branches

### Show all branches
```bash
git branch
```

### Create a new branch
```bash
git branch <branch>
```

### Create and switch to a branch
```bash
git checkout -b <branch>
```

### Switch to a branch
```bash
git checkout <branch>
```

### Checkout a remote branch
```bash
git checkout -b <branch> origin/<branch>
```

### Rename a branch
```bash
git branch -m <from> <to>
```

### Delete a branch
```bash
git branch -d <branch>
```

### Delete a remote branch
```bash
git push origin :<branch>
```

### Compare branch changes
```bash
git diff <branch>
```

### Merge a branch into the current branch
```bash
git merge <branch>
```

### Resolve merge conflicts
```bash
mate <file>
git add <file>
git commit
```

### Discard branch changes
```bash
git checkout -f master
```

---

# 🏷️ Tags

### Show tags
```bash
git tag
```

### Create a tag
```bash
git tag -a <tag>
```

### Create a tag for a specific commit
```bash
git tag -a <tag> <commit>
```

### Show tag information
```bash
git show <tag>
```

### Update a tag
```bash
git tag -f <tag> <tag> -m "<message>"
```

### Delete a tag
```bash
git tag -d <tag>
```

### Delete a remote tag
```bash
git push origin :refs/tags/<tag>
```

---

# 🚀 Push

### Push to master
```bash
git push origin master
```

### Push with tags
```bash
git push origin master --tags
```

---

# 📥 Pull

### Fetch from remote repository
```bash
git fetch origin
```

### Merge a remote branch
```bash
git merge origin/master
```

### Fetch and merge
```bash
git pull
```

---

# 📥 Clone

### Clone a repository
```bash
git clone <url>
```

### Clone into a specific directory
```bash
git clone <url> <directory>
```

### Clone a specific branch
```bash
git clone <url> -b <branch> <directory>
```

### Clone with submodules
```bash
git clone --recursive <url>
```

---

# 📦 Submodules

### Add a submodule
```bash
git submodule add <url> <path>
```

### Update submodules
```bash
git submodule update
```

---

# 📌 Stash

### Save current changes
```bash
git stash
```

### List stashes
```bash
git stash list
```

### Show stash differences
```bash
git stash show -p <stash>
```

### Restore a stash
```bash
git stash apply
```

### Restore and restage files
```bash
git stash apply --index
```

### Restore a specific stash
```bash
git stash apply <stash>
```

### Delete a stash
```bash
git stash drop <stash>
```

### Restore and remove stash
```bash
git stash pop
```

### Create a branch from a stash
```bash
git stash branch <branch>
```

---

# 🌍 Remote

### Show remotes
```bash
git remote -v
```

### Add a remote
```bash
git remote add origin <url>
```

### Remove a remote
```bash
git remote rm origin
```

---

# 🔄 Reset

### Reset working tree
```bash
git reset --hard HEAD
```

### Undo the last commit
```bash
git reset --hard HEAD~1
```

### Rollback to a specific commit
```bash
git reset --hard <commit>
```

---

# 🛠️ Miscellaneous

### Count commits in the current branch
```bash
git log --pretty=oneline | wc -l
```

---

# ⚙️ Configuration

### Set username
```bash
git config --global user.name "<name>"
```

### Set email
```bash
git config --global user.email "<email>"
```

### Set TextMate as the default editor
```bash
git config --global core.editor "mate -w"
```

### Set Sublime Text as the default editor
```bash
git config --global core.editor "subl -w"
```

### Enable colored output
```bash
git config --global color.ui true
```

---

## 📖 License

This cheat sheet is intended for learning and quick reference. Feel free to fork, modify, and share.

⭐ If you found this helpful, consider starring the repository!
