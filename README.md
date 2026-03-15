# Udemy.GitHubBasics — GitHub Collaboration Practice Repo

This repository contains **GitHub-focused exercises** I completed while following the Udemy course:
**“Git & GitHub – The Practical Guide”**.

It is designed to practice the transition from **local Git work** to **remote GitHub collaboration**:
remotes, tracking branches, clone workflows, forks, pull requests, and remote branch handling.

---

## What I practiced here

- Connecting a local repository to GitHub
- Working with `origin` and remote repositories
- Understanding remote branches and tracking branches
- Practicing `push`, `pull`, and `fetch`
- Creating and using local tracking branches
- Exploring fork-based workflows
- Practicing collaboration-related GitHub concepts
- Learning how local and remote history stay in sync

---

## Repository structure

| Path | Purpose |
|------|---------|
| `main/` | Main practice area |
| `main/m1.txt` | Main branch starting file |
| `main/forked/` | Fork workflow practice |
| `main/push-to-private/` | Remote push practice |
| `main/push-to-public/` | Public remote push practice |

---

## Key Git commands used (core set)

> Exact flags/options can vary, but these are the commands I used to perform the actions reflected in the reflog.

```bash
# remote setup
git remote add origin <url>
git remote -v

# pushing / pulling
git push -u origin main
git pull origin <branch>
git fetch origin

# tracking branches
git checkout remotes/origin/feature-remote
git switch -c feature-remote-local
git branch --track feature-remote-local origin/feature-remote

# branch work
git switch feature
git switch main
git commit -m "message"

# history
git log --oneline --graph --decorate --all
git reflog

654fa26 (HEAD -> main, origin/main, origin/HEAD) HEAD@{0}: reset: moving to head~1
62313c5 HEAD@{1}: checkout: moving from feature-remote to main
86a5f84 (feature-remote) HEAD@{2}: pull: Fast-forward
47c24c9 HEAD@{3}: commit: add local tracking file
b7a453f HEAD@{4}: checkout: moving from feature to feature-remote
ec941ac HEAD@{5}: checkout: moving from feature-remote-local to feature
68b6729 HEAD@{6}: checkout: moving from b7a453fe6a11a5189c447a9d7fc72fcd9d5ecb57 to feature-remote-local
b7a453f HEAD@{7}: checkout: moving from feature-remote-local to remotes/origin/feature-remote
68b6729 HEAD@{8}: commit: add tracking local file
b7a453f HEAD@{9}: checkout: moving from feature to feature-remote-local
ec941ac HEAD@{10}: checkout: moving from b7a453fe6a11a5189c447a9d7fc72fcd9d5ecb57 to feature
b7a453f HEAD@{11}: checkout: moving from feature to remotes/origin/feature-remote
ec941ac HEAD@{12}: commit: feature branch with f1 added
62313c5 HEAD@{13}: checkout: moving from main to feature
62313c5 HEAD@{14}: commit: m2 added
654fa26 (HEAD -> main, origin/main, origin/HEAD) HEAD@{15}: commit (initial): m1 added
