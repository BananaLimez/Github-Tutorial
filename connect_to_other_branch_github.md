# 🌿 How to Connect to Another Branch in GitHub

This guide explains how to connect or switch to another branch in GitHub — whether you're using **Git locally (VS Code / Terminal)** or the **GitHub web interface**.

---

## 🧠 1. Using Git Locally (VS Code / Terminal)

### ✅ Step 1: Check Existing Branches
```bash
git branch -a
```
This command shows all branches.

- Branches **without** `remotes/` are *local branches*
- Branches **with** `remotes/origin/` are *remote branches* on GitHub

Example:
```
* main
  feature-login
  remotes/origin/main
  remotes/origin/feature-dashboard
```

---

### ✅ Step 2: Switch to an Existing Local Branch
If the branch already exists locally:
```bash
git checkout branch-name
```
Or, in newer Git versions:
```bash
git switch branch-name
```

---

### ✅ Step 3: Connect to a Remote Branch (Not Yet Local)
If the branch exists **only on GitHub** (remote):
```bash
git fetch
git checkout -b branch-name origin/branch-name

example
git checkout -b discovery+profile origin/discovery+profile

```
or (newer syntax)
```bash
git switch -c branch-name origin/branch-name
```

This creates a local copy of the remote branch and connects it automatically.

---

### ✅ Step 4: Pull the Latest Updates
Once you’re on that branch, update it:
```bash
git pull
```

---

## 🌐 2. Using GitHub’s Website

1. Go to your repository on GitHub.
2. At the top left (above the file list), click the **branch dropdown** — usually labeled “`main`”.
3. Select or search for the branch you want to switch to.
4. GitHub will reload the page showing that branch’s files.

---

## 🧩 Optional: Create a New Branch
To create and connect to a new branch:
```bash
git checkout -b new-branch-name
git push -u origin new-branch-name
```
The `-u` sets the upstream so that future `git pull` and `git push` commands automatically track that branch.

---

### 💡 Tip:
Would you rather connect to a branch directly inside **VS Code’s Git sidebar**? You can — just click on the branch name at the bottom left of VS Code and select the one you want!
