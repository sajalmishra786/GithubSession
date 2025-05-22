# 🚀 Git & GitHub Complete Command Cheat Sheet

This markdown document contains a comprehensive list of Git commands, from installing Git and setting up a GitHub account, to daily usage, collaboration, and branch management. Everything is included in one single place.

---

## 📥 Installation

### Windows:
Download from: https://git-scm.com/download/win

### macOS (with Homebrew):
```bash
brew install git
```

### Ubuntu/Linux:
```bash
sudo apt update
sudo apt install git
```

---

## ⚙️ Configuration

Set your user identity globally:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Set a default text editor (optional):
```bash
git config --global core.editor "code"  # Use VS Code
```

View global Git settings:
```bash
git config --global --list
```

---

## 🧱 Initialize a Git Repository

Initialize Git in the current directory:
```bash
git init
```

Clone a GitHub repository:
```bash
git clone https://github.com/username/repo.git
# or using SSH
git clone git@github.com:username/repo.git
```

---

## 📁 Basic Workflow

Check the current status:
```bash
git status
```

Stage a specific file:
```bash
git add filename
```

Stage all files:
```bash
git add .
```

Commit staged changes:
```bash
git commit -m "Your commit message"
```

---

## 🕵️ View Changes & History

See commit history:
```bash
git log
```

View unstaged changes:
```bash
git diff
```

View staged changes:
```bash
git diff --staged
```


## 🔀 Branching

Create a new branch:
```bash
git branch new-branch
```

List all branches:
```bash
git branch
```

Switch to a branch:
```bash
git checkout branch-name
# or
git switch branch-name
```

Create and switch to a branch:
```bash
git checkout -b new-branch
# or
git switch -c new-branch
```

Delete a branch:
```bash
git branch -d branch-name
```

---

## 🔁 Merging

Merge another branch into current:
```bash
git merge branch-name
```

Resolve merge conflicts manually, then:
```bash
git add .
git commit
```


---

## 📤 Push and Pull

Push local changes to GitHub:
```bash
git push -u origin main   # First push
git push                  # Subsequent pushes
```

Pull changes from remote:
```bash
git pull
```

Fetch changes (without merging):
```bash
git fetch
```


---

## ✅ Helpful One-Liners

Set default branch to `main`:
```bash
git config --global init.defaultBranch main
```

Revert a specific commit:
```bash
git revert <commit-hash>
```

Check which branch you're on:
```bash
git branch --show-current
```

