# Topic 10 — Remote Repositories (GitHub)

## The Analogy

Your local repo is a notebook at home.
GitHub is a cloud cabinet — a copy of your notebook accessible from anywhere.

---

## Key Terms

| Term | Meaning |
|------|---------|
| Remote | A copy of your repo stored online |
| origin | The default name Git gives to your remote (GitHub) |
| push | Send your local commits to GitHub |
| pull | Download changes from GitHub to your computer |
| clone | Download a repo from GitHub for the first time |

---

## Connect a Local Repo to GitHub

```bash
# 1. Link your local repo to GitHub
git remote add origin https://github.com/username/repo-name.git

# 2. Rename master to main (GitHub standard)
git branch -M main

# 3. Push all commits to GitHub (-u sets the default tracking)
git push -u origin main
```

---

## After the First Push

```bash
# Send new commits to GitHub
git push

# Download changes from GitHub
git pull
```

---

## Clone a Repo (download from GitHub)

```bash
git clone https://github.com/username/repo-name.git
```

Creates a local copy of any GitHub repository.

---

## Practice Tasks

1. Go to your GitHub repo in the browser — can you see all your files?
2. Edit a file directly on GitHub (click the pencil icon), commit the change there.
3. Run `git pull` in your terminal — does the change appear locally?
