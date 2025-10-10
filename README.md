# Team GitHub Workflow

This is a **super simple guide** for our team to use GitHub together.

---

## 🚀 Step 1: First Upload (done by one person)
Run these commands in the project folder:

```bash
git init
git remote add origin https://github.com/your-username/repo-name.git
git add .
git commit -m "first commit"
git branch -M main
git push -u origin main
```

---

## 📥 Step 2: Teammates Download the Project
Each teammate runs this once:

```bash
git clone https://github.com/your-username/repo-name.git
```

---

## 🔄 Step 3: Daily Workflow (Everyone)
When you want to work on something:

```bash
git pull origin main             # get latest code
git checkout -b feature-xyz      # make a branch for your task
# (edit files)
git add .                        
git commit -m "did something"    
git push origin feature-xyz      # send branch to GitHub
```

Then go to GitHub → open a **Pull Request (PR)** → get review → merge into `main`.

---

## 🔀 Merging Branches Locally (Example: `secondary` → `main`)

If you worked on a branch called `secondary` and want to merge it into `main`:

```bash
git branch                       # check current branch
git checkout main                # switch to main branch
git pull origin main             # update main with remote
git merge secondary              # merge your changes into main
git push origin main             # push updated main to GitHub
git restore .                    # restore to previous commit incase you f* up code
```

⚠️ If there are conflicts:
1. Git will show which files conflict.  
2. Open them and fix the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`).  
3. Then run:

```bash
git add .
git commit
git push origin main
```

---

## ✅ Rules
- Never push directly to `main`.  
- Always make a **branch** for your task.  
- Always **pull before starting work**.  
- Use clear commit messages.  
- Or just `git push origin main` :p  

---

## Example Branch Names
- `feature/login-page`
- `bugfix/navbar-crash`
- `update/readme`
