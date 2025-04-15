---
layout: post
title: "The Fun Way to Master Git: A Beginner’s Guide to Branching and PRs"
date: 2025-04-15
categories: git, onboarding, engineering
---

![Github is Fun!!!.](https://jtouley.github.io/my-blog/assets/images/github_fun.png)

When I onboarded my team to GitHub, confusion turned to confidence with one simple exercise. Here’s the guide I created to make Git fun and approachable—perfect for beginners or teams building better workflows.

This hands-on training covers:

- Creating and naming branches
- Cloning a repo and working locally
- Creating markdown files with a shared template
- Committing changes and pushing to GitHub
- Creating pull requests (PRs) with a checklist
- Updating your local repo after merging

---

## 1. Prerequisites

Install the GitHub CLI if you haven’t already.

**GitHub CLI (Windows)**

1. Download the MSI installer from [GitHub CLI releases](https://github.com/cli/cli/releases/latest).
2. Run the installer and follow the setup instructions.
3. Confirm installation:
   ```powershell
   gh --version
   ```

**GitHub CLI (macOS/Linux)**

Use Homebrew or apt:
```bash
brew install gh        # macOS
sudo apt install gh    # Ubuntu/Debian
```

**New to the terminal?**  
Try this [command-line primer](https://www.codecademy.com/learn/learn-the-command-line).

---

## 2. Clone the Repository

```bash
git clone https://github.com/example/training-repo.git
cd training-repo
```

Replace with your repo URL if different. Works on Windows, macOS, and Linux.

---

## 3. Create Your Branch

Use this format: `[first initial][last initial]_[favorite color]`

Example:
```bash
git checkout -b jt_blue
```

---

## 4. Create Your Folder and Markdown File

Create a folder: `[first initial][last initial]_[favorite animal]`

**macOS/Linux:**
```bash
mkdir jt_wolf
cd jt_wolf
touch README.md
```

**Windows:**
```bash
mkdir jt_wolf
cd jt_wolf
echo. > README.md
```

---

## 5. Markdown File Template

Paste this into your `README.md`:

```markdown
# Welcome to My Git Training Page

**Name:** [Your Name]  
**GitHub Handle:** [@yourhandle]  
**Branch Name:** [yourbranchname]  
**Favorite Animal:** [your favorite animal]  
**Favorite Color:** [your favorite color]

---

## Fun Questions

1. If your favorite animal had a superpower, what would it be?  
2. What’s a random fact about yourself that your team might not know?

---

## Git Experience

- Have you used Git before?  
- How comfortable are you with the command line?  
- What do you hope to learn more about?
```

---

## 6. Stage, Commit, and Push

```bash
git add .
git commit -m "Add [your initials] folder and training markdown"
git push origin [yourbranchname]
```

Example:
```bash
git push origin jt_blue
```

---

## 7. Open a Pull Request (PR)

Go to your GitHub repo and click "Compare & pull request."

Or use GitHub CLI:
```bash
gh pr create --fill
```

---

## 8. Pull Request Template

Use this PR description:

```markdown
# Git Training Submission

## Checklist

- [x] Cloned the repo
- [x] Created a branch with correct naming
- [x] Created a folder and `README.md` file using the template
- [x] Committed and pushed changes
- [x] Opened this PR

---

## Reflection

What was easy about this process?  
What was tricky or new?  
Any questions or feedback?
```

---

## 9. Common Issues

**Forgot to create a branch?**
```bash
git checkout -b your_branch_name
```

**Committed to main by mistake?**
```bash
git branch your_branch_name
git reset --hard origin/main
git checkout your_branch_name
```

**Authentication error when pushing?**
```bash
gh auth login
```

---

## 10. Update Your Local Repo After Merge

After your PR is merged, sync your local `main`.

**Basic Update**
```bash
git checkout main
git pull origin main
```

**Optional: Force Sync (Advanced)**

To match the remote exactly:
```bash
git fetch origin        # Updates your local view of the remote
git checkout main       # Switches to your main branch
git reset --hard origin/main  # Resets local main to match remote
```

**Warning**: `git reset --hard` deletes uncommitted or unpushed changes. Double-check!

**GitHub CLI Option**
```bash
gh repo sync
```

---

## 11. Further Learning

- [GitHub’s Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [Learn Git Branching](https://learngitbranching.js.org/) (interactive)
- [Pro Git Book](https://git-scm.com/book/en/v2) (free)

---

## 12. After Submission

A reviewer will check your PR. Once approved, it’s merged into `main`.

Thanks for participating—this exercise builds collaboration habits and Git fundamentals.
