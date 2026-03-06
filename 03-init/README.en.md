# Topic 03 — Creating a Repository (git init)

## The Analogy

You open a new folder and tell Git:
"Watch everything that happens here from now on."
That folder becomes a **repository** — a project Git is tracking.

---

## The Command

```bash
git init
```

Run this once inside any folder. Git creates a hidden `.git` folder
inside it — that is where Git stores all its history and data.
Never delete the `.git` folder.

---

## Step-by-Step

```bash
# Go into your project folder
cd my-project

# Initialize the repository
git init
```

Output:
```
Initialized empty Git repository in .../my-project/.git/
```

---

## Check the Status

```bash
git status
```

Right after `git init` you will see:
```
On branch master
No commits yet
nothing to commit
```

This is normal — Git is ready but you haven't saved anything yet.

---

## What "Untracked files" means

If you already have files in the folder, Git will list them as "untracked".
This means Git sees them but is NOT recording changes to them yet.
You fix that with `git add` — that is the next topic.

---

## Practice Tasks

1. Create a new empty folder called `test-repo` anywhere on your computer.
2. Run `git init` inside it.
3. Run `git status` — what do you see?
