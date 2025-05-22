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

Compact commit history:
```bash
git log --oneline
```

Show detailed info about the latest commit:
```bash
git show
```

View unstaged changes:
```bash
git diff
```

View staged changes:
```bash
git diff --staged
```

---

## 🧽 Undoing Changes

Discard changes in a file:
```bash
git restore filename
```

Unstage a file:
```bash
git reset filename
```

Undo last commit but keep changes staged:
```bash
git reset --soft HEAD~1
```

Undo last commit and unstage changes:
```bash
git reset --mixed HEAD~1
```

Undo last commit and discard changes:
```bash
git reset --hard HEAD~1
```

---

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

## 🌐 Remote Repositories

Add a remote repository:
```bash
git remote add origin https://github.com/username/repo.git
# or (SSH)
git remote add origin git@github.com:username/repo.git
```

Check remotes:
```bash
git remote -v
```

Remove a remote:
```bash
git remote remove origin
```

Rename a remote:
```bash
git remote rename origin new-name
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

## 🔑 GitHub SSH Setup (Optional)

Generate SSH key:
```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
```

Add SSH key to agent:
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

Copy key to clipboard:
```bash
cat ~/.ssh/id_ed25519.pub
```

Add it to GitHub → Settings → SSH and GPG Keys → New SSH Key.

Test connection:
```bash
ssh -T git@github.com
```

---

## 🧹 Cleaning Up

Remove untracked files (dry run):
```bash
git clean -n
```

Remove untracked files:
```bash
git clean -f
```

---

## 🔐 Stashing Changes

Temporarily save changes:
```bash
git stash
```

List all stashes:
```bash
git stash list
```

Apply latest stash:
```bash
git stash apply
```

Apply and delete:
```bash
git stash pop
```

Drop specific stash:
```bash
git stash drop stash@{0}
```

Clear all stashes:
```bash
git stash clear
```

---

## 🧪 Tags

Create a tag:
```bash
git tag v1.0
```

Create annotated tag:
```bash
git tag -a v1.0 -m "Version 1.0"
```

Push a tag:
```bash
git push origin v1.0
```

List all tags:
```bash
git tag
```

Delete a tag:
```bash
git tag -d v1.0
```

Delete remote tag:
```bash
git push origin --delete tag v1.0
```

---

## 📦 Submodules

Add a Git submodule:
```bash
git submodule add https://github.com/username/repo.git path/
```

Initialize submodules:
```bash
git submodule init
git submodule update
```

Clone repo with submodules:
```bash
git clone --recurse-submodules <repo-url>
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

---

## 📚 Additional Tips

- Use `.gitignore` to prevent committing unwanted files.
- Always pull before you push to avoid merge conflicts.
- Commit often with clear messages.
- Use branches for features and bug fixes.
- Use SSH for secure communication with GitHub.

---

> Made with 💻 by a Git enthusiast.